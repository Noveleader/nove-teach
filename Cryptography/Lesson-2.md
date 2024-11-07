# Cryptography 101: Lesson 2 – Asymmetric Cryptography

## What is Asymmetric Cryptography?

Asymmetric cryptography, also known as **public-key cryptography**, is a cryptographic technique that uses two different but mathematically related keys for encryption and decryption. Unlike symmetric cryptography, where both parties use the same key, asymmetric cryptography involves a **public key** for encryption and a **private key** for decryption.

### Key Concepts

- **Public Key**: A key that is shared openly and can be used by anyone to encrypt a message.
- **Private Key**: A secret key that is known only to the owner and is used to decrypt messages encrypted with the public key.
- **Encryption**: The process of converting plaintext into ciphertext using the recipient's public key.
- **Decryption**: The reverse process, converting ciphertext back to plaintext using the private key.

### How Asymmetric Cryptography Works

In asymmetric encryption, the key pair consists of a public key (which anyone can access) and a private key (kept secret). The public key is used to encrypt messages, and only the corresponding private key can decrypt them. This ensures that even if someone intercepts the encrypted message, they cannot decrypt it without the private key.

#### Flow of Communication:
1. **Sender**: Uses the recipient's public key to encrypt the message.
2. **Receiver**: Uses their private key to decrypt the ciphertext and recover the plaintext.

This system ensures that only the intended recipient, who holds the private key, can decrypt the message.

### Key Algorithms in Asymmetric Cryptography

1. **RSA (Rivest-Shamir-Adleman)**:
   - One of the most widely used asymmetric encryption algorithms.
   - RSA allows secure data transmission over the internet by using large key sizes (commonly 2048 or 4096 bits).
   - Commonly used in secure email communication, digital signatures, and SSL/TLS protocols.

2. **ECC (Elliptic Curve Cryptography)**:
   - A more efficient alternative to RSA that provides the same level of security with smaller key sizes.
   - ECC is especially useful in devices with limited processing power, such as smartphones or IoT devices.

### Example of Asymmetric Encryption

Imagine Bob wants to send Alice a secure message:

1. Bob encrypts the message using Alice's **public key**.
2. Alice receives the encrypted message.
3. Alice uses her **private key** to decrypt the message and read it.

Even if a third party intercepts the encrypted message, they cannot decrypt it without Alice's private key.

### Public Key Infrastructure (PKI)

For asymmetric cryptography to work at scale, a system called **Public Key Infrastructure (PKI)** is often used. PKI manages the generation, distribution, and verification of public and private key pairs, ensuring that public keys are authentic and belong to the correct entity.

### Digital Signatures

Asymmetric cryptography is also used in digital signatures, where the sender signs a message with their **private key**, and the receiver can verify the signature using the sender's **public key**. This provides both authentication and non-repudiation, ensuring that the message truly came from the claimed sender.

### Pros and Cons of Asymmetric Cryptography

#### Pros:
- **No Need for Secure Key Distribution**: Since the public key is openly shared, there is no need to securely distribute secret keys, unlike symmetric cryptography.
- **Authentication and Digital Signatures**: Asymmetric cryptography supports digital signatures, which verify the authenticity of messages and documents.
  
#### Cons:
- **Slower than Symmetric Cryptography**: Asymmetric encryption is computationally more intensive, making it slower, especially for large amounts of data.
- **Larger Key Sizes**: It requires larger key sizes for equivalent security compared to symmetric cryptography, which increases computational overhead.

### Use Cases of Asymmetric Cryptography

1. **Secure Email**: Email encryption tools like PGP (Pretty Good Privacy) use asymmetric cryptography to secure email communication.
2. **SSL/TLS**: Used in securing web communications by encrypting data exchanged between users and websites.
3. **Digital Signatures**: Ensuring authenticity and integrity of documents and software through public-private key pairs.

## More Resources

1. [RSA](https://www.geeksforgeeks.org/rsa-algorithm-cryptography/)
2. [ECC - by cloudfare](https://blog.cloudflare.com/a-relatively-easy-to-understand-primer-on-elliptic-curve-cryptography/)
3. [More on ECC](https://www.geeksforgeeks.org/blockchain-elliptic-curve-cryptography/)
4. [PKI - Public Key Infrastructure](https://www.keyfactor.com/education-center/what-is-pki/)
5. [Digital Signatures](https://www.geeksforgeeks.org/digital-signatures-certificates/)
6. [Digital Signature - By Binance](https://academy.binance.com/en/articles/what-is-a-digital-signature)