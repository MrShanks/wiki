# Encryption

It's a practice used to provide confidentiality during a data transmission.

- Plain Text: Data before encryption and after decryption
- Cipher Text: Data while encrypted

Encryption should render impossible for a third party who doesn't know the encryption key, to decrypt the message and tamper it.

**Symple** Encryption: Transforms Plaintext into Cipher text
- Doesn't scale because it would need to change everytime to avoid giving insights
- Can't use a publicly available alghoritms

**Key Based** Encryption:
- Combines industry vetted algorithm with a Secret Key
- Secret Keys can be randomly generated
- Keys make the same message appear differently for each user at the end of the communication.

## Two types of encryption:

### Symmetric Encryption:
- Uses the same key for encryption and decryption

Example: shift letters using the alphabet abcdefghijklmnopqrstuvwxyz
Alghoritm changes the message text by shifting the letter on the alphabet by the amount defined `hello` becomes `khoor` with a Secret Key = 3.
Decryption algorithm is going to use the same key to decrypt the message and it will go backwards on the alphabet to get back `hello` from `khoor`

### Asymmetric Encryption:
- Uses different keys for encryption and decryption.

Keys are different and going backwards is not allowed. Therefore if we use the example above, insteda of going back you need to have a different key that tells you how many step forward you will have to go, to go back to the `h` from `k`, in this case that would 21.
What I encrypt with one key can only be decrypter with the other key. The two keys are mathematically related.
Here comes the concept of Public and Private keys

In a communication between two individuals the public key of the receiver can be used by the sender to securely send a message that only the receiver will know ho to decrypt.

Asymmetric Key Pair can be used for **Signatures** that provides **Authentication** (Only the owner of the private key related to the public key I used could have encrypted that message) and **Integrity**(If I'm able to decrypt the message with the public key of the sender, it means the message hasn't been tampered.)
___

|ALGORYTHM|PROS|CONS|IDEAL USAGE|ALGHORITMS|
|---------|----|----|-----------|----------|
|Asymmetric|Secret key is never shared|Slower, Cypher text expansion| Limited amount of Data| DSA, RSA, Diffie-Hellman, ECDSA, ECDH|
|Symmetric|Faster, Cipher text is same size as Plain Text | Secret Key must be shared prior to the communication| Bulk Data| ~~DES, RC4~~, 3DES, AES, ChaCha20 |

### Hybrid Encryption
Uses both Asymmetric and Symmetric Encryption taking the best of both worlds

SSL/TLS, IPSEC, SSH all use this concept to secure connections.


### Signatures:
- Uses the Sender's Private Key to encrypt the Hash of a data
- That provides Integrity and Authentication for what is Signed.