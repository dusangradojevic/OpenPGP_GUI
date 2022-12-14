# OpenPGP Simulation

Authors:

Dušan Gradojević

Kosta Matijević

# 1.Introduction

Goal of this project is implementation of Swing based Java application that

demonstrates usage of PGP protocol in data sending and receiving.

PGP (_Pretty Good Privacy_) is widely used security protocol that enables authentication,

integrity and privacy of data.

Functionalities:

- Reviewing collections of private and public keys
- Import and export of key rings into .asc files
- Generating new and deleting existing key rings
- Message sending ( encryption, singning, compression and radix-64 conversion)
- Message receiving (decryption and signature verification)

# 2.GUI

## Start Menu
![image](https://user-images.githubusercontent.com/59028808/185464012-30dfd636-57fe-40d8-a4c2-9dc74223ff8a.png)
## Key Management
![image](https://user-images.githubusercontent.com/59028808/185464052-9d98e445-2be0-49fa-a4f6-73caccde9ce8.png)  
![image](https://user-images.githubusercontent.com/59028808/185464069-074e787d-eaf2-49e0-85e1-41b6771b9ff6.png)  
![image](https://user-images.githubusercontent.com/59028808/185464092-79571710-9600-43ab-ac72-80fc48ae55cb.png)  
## Message sending  
![image](https://user-images.githubusercontent.com/59028808/185464159-ac35455f-2b39-4e30-8e27-9cbfb10de290.png)
## Message receiving  
![image](https://user-images.githubusercontent.com/59028808/185464216-df8ef41d-dcfe-403c-96ea-98008842e43e.png)  
![image](https://user-images.githubusercontent.com/59028808/185464235-345c7968-e319-4495-98ab-58bde0ccd517.png)

# 3.Used Algorithms

Asymmetric: RSA for signing and encryption.

Symmetric: 3DES with EDE configuration and AES.

## Asymmetric algorithms

RSA (Rivest-Shamir-Adleman) is the best known and most widely used public key encryption algorithm. It is a block algorithm where the original data and encrypted data are integers between 0 and n-1 for some n. The message is encrypted with the receiver's public key while the receiver decrypts the message with his private key. This ensures that only the recipient can decrypt the message. The sender signs the data he sends with his private key, which provides a unique signature for the user, while the receivers use the sender's public key to verify who the message came from.

## Symmetric algorithms

The 3DES algorithm is a symmetric key algorithm used to encrypt block data. 3DES is a variation of the DES algorithm where the algorithm itself is repeated three times. This particular implementation uses a three-key EDE (Encrypt-Decrypt-Encrypt) configuration.

AES (Advanced Encryption Standard) is a block algorithm intended to replace DES in commercial applications. It uses 128 bits for the block size and 128, 192 or 256 bits for the key size. AES does not use the Feistel structure.
