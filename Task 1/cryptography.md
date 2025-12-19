# Cryptography Basics

Cryptography is the science of securing information by converting it into unreadable formats. It ensures confidentiality, integrity, authentication, and non-repudiation of data.

---

## Encryption

Encryption converts plain text into cipher text to protect data from unauthorized access.

---

### Symmetric Encryption

Symmetric encryption uses the same secret key for both encryption and decryption.

**Characteristics:**
- Fast processing
- Efficient for large data
- Key distribution problem

**Examples:**
- AES
- DES (obsolete)

---

### Asymmetric Encryption

Asymmetric encryption uses two keys:
- Public Key (encryption)
- Private Key (decryption)

**Characteristics:**
- Secure key exchange
- Slower than symmetric encryption

**Examples:**
- RSA
- ECC

---

## Hashing

Hashing converts data into a fixed-length hash value. It is a one-way function and cannot be reversed.

### Properties:
- Deterministic
- Fixed length output
- Collision resistance

---

### MD5
- Produces 128-bit hash
- Fast but insecure
- Vulnerable to collisions

---

### SHA-256
- Produces 256-bit hash
- Secure and widely used
- Used in blockchain and digital signatures

---

## Digital Certificates

Digital certificates verify the identity of a website or entity.

**Issued by:** Certificate Authorities (CA)  
**Contains:** Public key, domain name, issuer details

**Used in:** HTTPS, email security

---

## SSL/TLS

SSL (Secure Sockets Layer) and TLS (Transport Layer Security) encrypt data transmitted over networks.

### SSL/TLS Functions:
- Encryption
- Authentication
- Data integrity

**Used in:**
- HTTPS
- Secure login systems
- Online transactions

---

## OpenSSL Commands

### Hashing Files
md5sum file.txt  
sha256sum file.txt  

---

### Encrypting Files
openssl enc -aes-256-cbc -in file.txt -out encrypted.txt  

---

### Decrypting Files
openssl enc -aes-256-cbc -d -in encrypted.txt -out decrypted.txt  
