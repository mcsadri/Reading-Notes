# Cryptography

## Reading

### [Encryption, Decryption & Hacking](https://www.khanacademy.org/computing/computers-and-internet/xcae6f4a7ff015e7d:online-data-security/xcae6f4a7ff015e7d:data-encryption-techniques/a/encryption-decryption-and-code-cracking)

- the Caesar Cipher, invented by Julius Caesar more than two thousand years ago
- Three main techniques:
  - frequency analysis
    - Human languages tend to use some letters more than others.
  - known plaintext
    - the original unencrypted message is plaintext
  - brute force
    - attempt all possible solutions
- Key aspects of data encryption:
  - Encryption: scrambling the data according to a secret key (in this case, the alphabet shift).
  - Decryption: recovering the original data from scrambled data by using the secret key.
  - Code cracking: uncovering the original data without knowing the secret, by using a variety of clever techniques.
- When considering a possible encryption technique, think about all those aspects:
  - how easy is it to encrypt?
  - how easy is it to decrypt?
  - how easy is it for a nefarious individual to crack the code? (most important)

### [Ceasar Cipher](https://en.wikipedia.org/wiki/Caesar_cipher)

## Videos

### [Cryptography Crash Course](https://www.youtube.com/watch?v=jhXCTbFnK8o)

## Additional Resources

### [Introduction to Cryptography](https://thebestvpn.com/cryptography/)

- Types of cryptography:
  - hashing
  - symmetric cryptography
  - asymmetric cyptography
  - key exchange algorithms
- Types of cryptographic functions:
  - authentication
  - nonrepudiation
  - confidentiality
  - integrity

### [How Computers Generate Random Numbers](https://www.howtogeek.com/183051/htg-explains-how-computers-generate-random-numbers/)

---

## Reading Questions

- What is the basic principle behind the Caesar Cipher, and how was it used historically?
  - a single-alphabet substituion cipher used by Julius Ceaser to communicate with allies
  - uses a alphabet shift to modify the plaintext message to an encoded state

- What are the key differences between symmetric and asymmetric encryption? How is asymmetric used in secure communication today?

  | Symmetric Key Encryption | Asymmetric Key Encryption |
  |---|---|
  | It only requires a single key for both encryption and decryption. | It requires two keys, a public key and a private key, one to encrypt and the other one to decrypt. |
  | The size of cipher text is the same or smaller than the original plain text. | The size of cipher text is the same or larger than the original plain text. |
  | The encryption process is very fast. | The encryption process is slow. |
  | It is used when a large amount of data is required to transfer. | It is used to transfer small amounts of data. |
  | It only provides confidentiality. | It provides confidentiality, authenticity, and non-repudiation. |
  | The length of key used is 128 or 256 bits | The  length of key used is 2048 or higher |
  | In symmetric key encryption, resource utilization is low as compared to asymmetric key encryption. | In asymmetric key encryption, resource utilization is high. |
  | It is efficient as it is used for handling large amount of data. | It is comparatively less efficient as it can handle a small amount of data. |
  | Security is less as only one key is used for both encryption and decryption purpose. | It is more secure as two keys are used here- one for encryption and the other for decryption. |
  | The Mathematical Representation is as follows- P = D (K, E(P)) where K –> encryption and decryption key P –> plain text D –> Decryption  E(P) –> Encryption of plain text | The Mathematical Representation is as follows- P = D(Kd, E (Ke,P)) where Ke –> encryption key Kd –> decryption key D –> Decryption E(Ke, P) –> Encryption of plain text using encryption key Ke . P –> plain text |
  | Examples: 3DES, AES, DES and RC4 | Examples: Diffie-Hellman, ECC, El Gamal, DSA and RSA |

  [Difference Between Symmetric and Asymmetric Key Encryption](https://www.geeksforgeeks.org/difference-between-symmetric-and-asymmetric-key-encryption/)

- How do computers generate random numbers, and what are the differences between true random number generation (TRNG) and pseudo-random number generation (PRNG)? Discuss their use cases in cryptography.
  - Computers can generate truly random numbers by observing some outside data, like mouse movements or fan noise, which is not predictable, and creating data from it. This is known as entropy.
  - Other times, they generate “pseudorandom” numbers by using an algorithm so the results appear random, even though they aren’t.
  - Cryptography requires numbers that attackers can’t guess. There's a need to generate these numbers in a very unpredictable way so attackers can’t guess them. These random numbers are essential for secure encryption.

- What’s the difference between encryption and decryption? Explain with an analogy.
  - Drink more Ovaltine
