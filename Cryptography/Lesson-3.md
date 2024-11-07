# Cryptography 101: Lesson 3 – Hash Functions

## What is a Hash Function?

A **hash function** is a special type of cryptographic algorithm that takes an input (or "message") and returns a fixed-size string of characters, which is typically a hash value or digest. Regardless of the size of the input, the output (the hash) will always have a fixed length. Unlike encryption, hash functions are **one-way functions**, meaning that the original input cannot be recovered from the hash.

Hash functions are essential for ensuring the integrity of data, as even a small change in the input will result in a completely different hash. This property makes hash functions useful for verifying data integrity and creating digital signatures.

### Key Characteristics of Hash Functions:

1. **Deterministic**: The same input will always produce the same hash output.
2. **Fast to Compute**: Hash functions are designed to be quick to compute for any input size.
3. **Pre-image Resistance**: Given a hash, it should be computationally infeasible to find the original input.
4. **Small Change, Large Effect**: Any small change in the input drastically changes the hash output (avalanche effect).
5. **Fixed Output Size**: The hash size is always the same, regardless of the input size.
6. **Collision Resistance**: It should be computationally infeasible to find two different inputs that produce the same hash output.

### How Hash Functions Work

When you pass a piece of data (such as a message, file, or password) into a hash function, the function transforms it into a unique, fixed-size string of characters. This string is a condensed representation of the input data.

For example, a hash function might turn the message "Hello, World!" into something like `2ef7bde608ce5404e97d5f042f95f89f1c232871`.

Hash functions are designed to prevent attackers from reversing the process to retrieve the original input, making them ideal for data verification and integrity checks.

### Key Algorithms in Hashing

1. **MD5 (Message Digest Algorithm 5)**:
   - Produces a 128-bit hash value.
   - Once widely used for verifying file integrity, MD5 is now considered insecure due to vulnerabilities that allow for hash collisions (when two inputs produce the same hash).
   
2. **SHA-1 (Secure Hash Algorithm 1)**:
   - Produces a 160-bit hash value.
   - SHA-1 is more secure than MD5 but has also been deprecated due to discovered vulnerabilities.
   
3. **SHA-256 (Secure Hash Algorithm 256-bit)**:
   - Part of the SHA-2 family, SHA-256 generates a 256-bit hash value and is widely used for security-sensitive applications.
   - Commonly used in blockchain technology and cryptographic applications.

4. **SHA-3**:
   - The latest member of the Secure Hash Algorithm family, providing additional security and flexibility over SHA-2.

### Example of a Hash Function

Suppose you have the following input string:  
`"Cryptography101"`

Using the **SHA-256** algorithm, the hash output would be:  
`4d7b6a80f79f5c6375e50d1b7d019eae376469d6b7a5a4cf4b6a646148f896f2`

Now, if you slightly change the input to `"Cryptography102"`, the hash will look completely different:  
`32b2b8e6d2fe5f6f818ab0b35b13355896f27c6fa78d208d8c7b9f060f1643b9`

This dramatic change in the hash output due to a small change in the input demonstrates the **avalanche effect**.

### Applications of Hash Functions

1. **Data Integrity**:
   - Hash functions are used to ensure that data has not been altered. For example, file integrity checks compare the hash of a downloaded file with its original hash to ensure it hasn’t been corrupted.
   
2. **Password Storage**:
   - Hashes are commonly used to store passwords securely. Instead of storing plain text passwords, systems store hashed versions. When a user logs in, the system hashes their input and compares it to the stored hash.
   
3. **Digital Signatures**:
   - Hash functions are used in digital signatures to create unique identifiers for documents or transactions, ensuring data authenticity.
   
4. **Blockchain**:
   - Cryptocurrencies like Bitcoin and Ethereum use hash functions to ensure the integrity and security of blockchain data. Hashing is used to create links between blocks and validate transactions.

### Pros and Cons of Hash Functions

#### Pros:
- **One-Way Functionality**: Impossible to retrieve the original input, making it ideal for password protection.
- **Efficient Verification**: Fast and easy to verify data integrity with hash values.
- **Small Output Size**: Regardless of input size, the output is always of fixed length.

#### Cons:
- **Vulnerabilities in Older Hashes**: Algorithms like MD5 and SHA-1 have known vulnerabilities that make them unsuitable for modern cryptography.
- **No Encryption**: Hash functions cannot be used to encrypt data since they are one-way. They only verify integrity or store sensitive information in a secure way.

### Real-World Use Case Example

- **Blockchain**: In Bitcoin, the transactions within a block are hashed together to form a **Merkle Tree**. The root of the Merkle Tree is used in the process of mining new blocks, ensuring that any change in a transaction will completely alter the block's hash, making tampering detectable.

## More Resources

1. [MD5 for programming](https://www.geeksforgeeks.org/what-is-the-md5-algorithm/)
2. [MD5 in general](https://www.okta.com/identity-101/md5/)
3. [Differences between all the hash algorithms](https://codesigningstore.com/hash-algorithm-comparison)
4. [Anders Brownsworth Website](https://andersbrownworth.com/blockchain/)