# RSA
RSA (Rivest–Shamir–Adleman) is one of the worlds first public key cryptography which is used widely for data transmission 
# How it Works:

# 1. Setting up RSA:
1. Choose two large, distinct primes p and q, let n = pq.
2. Select an integer e so that gcd(e, (p-1)(q-1)) = 1.
3. Solve ed ≅ 1 (mod(p-1)(q-1)) for an integer d where 1<d<(p-1)(q-1).
4. Publish the encryption key (e, n).
5. Keep secure the private decryption key (d, n).

# 2. Sending a Message:
To send a message:
1. Look up the recipient's public key (e, n).
2. Generate the integer message M so that 0 ≤ M ≤ n.
3. Compute the ciphertext as follows: M^e ≅ c(mod n), where 0 ≤ c ≤ n.
4. Send C

# 3. Receiving a Message:
To decrypt a message:
1. Use your private key (d, n)
2. Compute the messagetext R from the ciphertext C as follows: 
           C^d ≅ R (mod n)where 0 ≤ R ≤ n
3. R is the original message.
