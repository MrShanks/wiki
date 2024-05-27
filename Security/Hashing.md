# Hashing
Hashing is a practice used in many different applications such as:

- Password storage --> User and Passwords are stored in a scrambled represantation making it more difficult to retrieve the original for an attacker
- Digital signatures and data integrity --> A bit of data added to the message to ensure the message hasn't changed since the sending.
- File management --> Hashes are used as index to identify files and get rid of duplicates.

Hashes should be: 
- Divide the input into data Block
- Avalanche effect, meaning each block is fed to the next one for the calculation
- PseudoRandom 
- Not trivial to calculate
- The output must have the same fixed length 
- Same input leads to the same output
- Irreversible
