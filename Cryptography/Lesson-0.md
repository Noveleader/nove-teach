# Cryptography 101: Lesson 0 – Introduction to Cryptography

## What is Cryptography?

Cryptography is the practice and study of techniques for securing communication and protecting information. At its heart, cryptography is about creating systems that allow information to be transferred securely, even in the presence of malicious third parties, known as adversaries. This means that unauthorized parties cannot read, alter, or forge messages.

### Key Goals of Cryptography:

1. **Confidentiality**: Ensuring that only authorized individuals can access the information.
2. **Integrity**: Verifying that the message has not been altered.
3. **Authentication**: Confirming the identity of the sender or receiver.
4. **Non-repudiation**: Ensuring that the sender cannot deny having sent the message.

These principles are critical for modern applications such as online banking, private messaging, e-commerce, and secure data storage.

## How Does Cryptography Work?

Cryptography works by transforming readable data (known as plaintext) into an unreadable form (known as ciphertext) using a process called encryption. This makes it so that only someone with the correct key can reverse the process (decryption) and recover the original information.

### Types of Cryptography:

1. **Symmetric Cryptography**: Both the sender and receiver use the same secret key to encrypt and decrypt the message. This method is fast and efficient but requires secure key sharing.

   - **Example**: AES (Advanced Encryption Standard)

2. **Asymmetric Cryptography**: Also known as public-key cryptography, it involves two keys: a public key (which can be shared with everyone) and a private key (which must remain secret). The public key encrypts the data, and only the private key can decrypt it.

   - **Example**: RSA (Rivest-Shamir-Adleman)

3. **Hash Functions**: These are one-way cryptographic algorithms that take input data and produce a fixed-size string of characters. Hashing is used for integrity checks and digital signatures, ensuring data hasn’t been tampered with.
   - **Example**: MD5, SHA-256

### Real-World Applications of Cryptography:

- **Secure Communications**: Encryption is used in messaging apps like WhatsApp and Signal.
- **Digital Signatures**: Used in digital contracts, ensuring authenticity and integrity.
- **Blockchain Technology**: Cryptography underpins the security of cryptocurrencies like Bitcoin and Ethereum.

## More Resources:

1. [GFG](https://www.geeksforgeeks.org/cryptography-introduction/)
2. [Tech Target Article](https://www.techtarget.com/searchsecurity/definition/cryptography)
3. [Medium Article](https://medium.com/edureka/what-is-cryptography-c94dae2d5974)
