# Cryptography 101: Lesson 1 – Symmetric Cryptography

## What is Symmetric Cryptography?

Symmetric cryptography is one of the foundational techniques in cryptography. It involves the use of a single shared secret key for both encryption and decryption. In this method, both the sender and the receiver must possess the same key, which must be kept secure to maintain confidentiality.

### Key Concepts

- **Plaintext**: The original, readable data or message.
- **Ciphertext**: The encrypted, unreadable version of the plaintext.
- **Encryption**: The process of converting plaintext into ciphertext using a key.
- **Decryption**: The reverse process, converting ciphertext back to plaintext using the same key.

### How Symmetric Cryptography Works

In symmetric encryption, the same key is used to both scramble the message (encryption) and unscramble it (decryption). The security of the system depends entirely on how well the secret key is protected. If an adversary gains access to the key, they can decrypt the messages.

Here’s a simplified flow:
1. **Sender**: Uses a secret key to encrypt the plaintext and produce ciphertext.
2. **Receiver**: Uses the same secret key to decrypt the ciphertext and recover the plaintext.

### Key Algorithms in Symmetric Cryptography

1. **AES (Advanced Encryption Standard)**:
   - AES is the most widely used symmetric encryption algorithm today.
   - It supports key sizes of 128, 192, or 256 bits, with larger keys providing more security.
   - Commonly used in applications like securing Wi-Fi connections, file encryption, and messaging apps.

2. **DES (Data Encryption Standard)**:
   - An older symmetric encryption algorithm, now considered insecure due to its short 56-bit key size.
   - DES has been largely replaced by AES, though it was a standard in the 1970s and 1980s.

3. **Triple DES (3DES)**:
   - An improvement over DES that applies the DES algorithm three times with different keys, increasing security.
   - While more secure than DES, it is slower and less efficient than modern algorithms like AES.

### Example of Symmetric Encryption

Let’s say Alice wants to send a secret message, "HELLO," to Bob:

1. Alice uses the shared key to encrypt "HELLO" into ciphertext.
2. Alice sends the ciphertext to Bob.
3. Bob uses the same key to decrypt the ciphertext and recover the message "HELLO."

### Pros and Cons of Symmetric Cryptography

#### Pros:
- **Fast and Efficient**: Encryption and decryption processes are quick, making symmetric cryptography suitable for large amounts of data.
- **Less Computationally Intensive**: Compared to asymmetric cryptography, symmetric algorithms require fewer resources.

#### Cons:
- **Key Distribution Problem**: Both parties must securely share the same key. If the key is intercepted during transmission, the security of the entire system is compromised.
- **Scalability Issues**: As the number of participants increases, managing and securely distributing the keys becomes more complex.

### Use Cases of Symmetric Cryptography

1. **Encrypting Files and Data**: Symmetric encryption is used to protect sensitive information stored on devices.
2. **Securing Communication Channels**: It is used in protocols like SSL/TLS to encrypt data exchanged over the internet.
3. **Database Encryption**: Large amounts of data stored in databases are often protected using symmetric encryption.

## More Resources

1. [Introduction](https://www.geeksforgeeks.org/symmetric-key-cryptography/)
2. [AES](https://www.geeksforgeeks.org/advanced-encryption-standard-aes/)
3. [DES](https://www.geeksforgeeks.org/data-encryption-standard-des-set-1/)
4. [SDES](https://www.geeksforgeeks.org/simplified-data-encryption-standard-set-2/)
5. [3DES](https://www.geeksforgeeks.org/triple-des-3des/)