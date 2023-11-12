See laptop: __Network and security fundamentals__ for more info.

Session key exchange is asymmetric;\
Data encription is symmetric;

=================================================================================

1 SSL/TLS (digital) certificates:
- __Root certificates => pre-installed in OS; self-signed; contain public keys__;
- Intermediate certificates;
- Self-signed certificate;
- Certificate chain;

https://www.youtube.com/watch?v=r1nJT63BFQ0 \
https://www.youtube.com/watch?v=6wCwjIhGylY

1.1 Digital signatures in SSL/TLS:

How signarure happens in terms of public/private keys\
https://www.ibm.com/docs/en/cics-ts/5.4?topic=protection-public-key-encryption

- Information encrypted using the public key can be decrypted only with the private key.
- Information encrypted using the private key can be decrypted only with the public key.

https://www.youtube.com/watch?v=heacxYUnFHA
![image](https://github.com/VIK2395/JWT_auth/assets/50545334/2e46ba0a-ad65-4f3a-87e9-4eabaf095de5)

![image](https://github.com/VIK2395/JWT_auth/assets/50545334/d73c0e7e-1ff8-4f70-a7be-5da93cf880ac)

https://www.ibm.com/docs/en/ibm-mq/9.3?topic=tls-digital-signatures-in-ssltls
![image](https://github.com/VIK2395/JWT_auth/assets/50545334/80efaaf7-5c9e-4930-b16b-005661d13a84)

SHA(Secure Hash Algorithm)

Sender:\
hash = SHA/bcrypt func(data);\
sign = encript(hash, sign's private key);\
output => data + sign + (sign's public key);

Consumer:\
input => data + sign + (sign's public key);\
hash1 = SHA/bcrypt func(data);\
hash2 = decript(sign, sign's public key);\
hash1 == hash2;

=================================================================================

2 Handshake (proccess of exchnge "session key" between client and server):
- Session key;\
TLS 1.2 uses RSA(Rivest-Shamir-Adelman) algorithm; doesn't have Perfect forward secrecy; client generates "session key";\
TLS 1.3 uses DH(Diffie-Hellman) or enhanced ECDH(Elliptic Curve Diffie-Hellman) algorithm; has Perfect forward secrecy; client generates: private x and public g, n, g^x%n, which are sent publicly;

https://www.youtube.com/watch?v=AlE5X1NlHgg \
https://www.youtube.com/watch?v=kCkQRH5eweg

Server sends all sertificates chain(exept root one)

https://www.ssl.com/article/ssl-tls-handshake-ensuring-secure-online-interactions/
![image](https://github.com/VIK2395/JWT_auth/assets/50545334/dad3da24-e57c-4194-949b-a83c167e5228)

3 TLS 1.3 Diffie-Hellman in details:

https://www.youtube.com/watch?v=64geP_LAZ5U

4 Certification authority (intermediate certificates used) and bying a certificate:\
https://www.youtube.com/watch?v=qXLD2UHq2vk
