# Secure Chat Simulation using Diffie-Hellman, AES and HMAC

## Course
CSE311 – Cryptography and Data Security Lab  
Mini Project  
Prepared by: Suad Alsayed

## Project Overview
This project simulates secure communication between two users (Alice and Bob) using multiple cryptographic techniques integrated into one application.

It implements:

- Diffie-Hellman key exchange for shared secret generation
- AES encryption for confidentiality
- HMAC for message integrity and authentication

An attacker simulation (Eve) is included to demonstrate tampering detection.

---

## Features
- Secure shared key generation
- Message encryption and decryption
- HMAC verification
- Tampering attack detection
- Secure chat simulation

---

## Technologies Used
Python 3

Libraries:
- os
- hashlib
- hmac
- cryptography

Install dependency:

```bash
pip install cryptography
```

---

## How to Run

```bash
python main.py
```

Or run the code in Google Colab.

---

## Program Flow
1. Alice and Bob perform Diffie-Hellman key exchange.

2. Both generate the same shared secret.

3. Shared secret derives:
- AES key
- HMAC key

4. Alice encrypts a message.

5. Bob verifies HMAC:
- If valid → decrypts the message  
- If modified → rejects the message

6. Eve tampering attack is demonstrated.

---

## Sample Output
Bob reads:

Meet me at 5 PM

Integrity check failed! Message may be tampered with.

---

## Security Goals Achieved
- Confidentiality  
- Integrity  
- Authentication

---

## Security Considerations
- Random nonces are used
- Separate keys for encryption and authentication
- HMAC is verified before decryption

Note:
Small Diffie-Hellman parameters were used for educational demonstration. Real implementations use large secure primes.

---

## Future Improvements
Possible extensions:
- GUI secure messenger
- Socket-based real-time chat
- Digital signatures
- Replay attack protection

---

## Author
Suad Alsayed  
Cybersecurity Engineering  
Abdullah Al-Salem University
