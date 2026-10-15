---
title: "MyBank"
excerpt: "Python desktop banking app that protects user data and money transfers with AES, RSA, digital signatures and a certificate authority hierarchy. Cryptography course project.<br/><img src='/images/mybank/logo.jpg' alt='MyBank logo' style='width: 160px; height: auto;'>"
collection: portfolio
order: 2
---

<p><a href="https://github.com/DanieleMarche/cryptographyProject" class="btn btn--primary"><i class="fab fa-github" aria-hidden="true"></i> View on GitHub</a></p>

<img src="/images/mybank/logo.jpg" alt="MyBank logo" style="width: 200px; height: auto;">

MyBank is a desktop banking application where users can send money to each other. I built it for the **Cryptography** course during my Erasmus+ semester at Universidad Carlos III de Madrid.

The goal was to put the theory from the course into practice:

- **Password storage:** passwords are salted and hashed. Key derivation uses scrypt.
- **Data at rest:** user data is encrypted with **AES** before it is saved to PostgreSQL.
- **Transactions:** each transfer is encrypted with **RSA (OAEP)** for both parties, and digitally **signed**.
- **PKI:** a hierarchy of **certificate authorities** built with OpenSSL issues the certificates used to verify signatures through the certificate chain.
- **Biometric login:** on macOS, users can log in with Touch ID.

The code follows an MVC structure, with separate models, views and controllers. The GUI is built with CustomTkinter.

<hr>

### Technologies used

- **Language:** Python
- **Database:** PostgreSQL
- **Libraries:** pycryptodome, CustomTkinter, OpenSSL (for the CA hierarchy)
