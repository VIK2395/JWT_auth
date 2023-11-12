See laptop: __Network and security fundamentals__ for more info.

1 SSL/TLS certificates:
- Root certificates;
- Intermediate certificates;
- Self-signed certificate;
- Certificate chain;

https://www.youtube.com/watch?v=r1nJT63BFQ0 \
https://www.youtube.com/watch?v=6wCwjIhGylY

2 Handshake (proccess of exchnge "session key" between client and server):
- Session key;\
TLS 1.2 uses RSA(Rivest-Shamir-Adelman) algorithm; doesn't have Perfect forward secrecy; client generates "session key";\
TLS 1.3 uses Diffie-Hellman (or enhanced Elliptic Curve Diffie-Hellman) algorithm; has Perfect forward secrecy; client generates: private x and public g, n, g^x%n, which are sent publicly;

https://www.youtube.com/watch?v=AlE5X1NlHgg \
https://www.youtube.com/watch?v=kCkQRH5eweg

3 TLS 1.3 Diffie-Hellman in details:

https://www.youtube.com/watch?v=64geP_LAZ5U

4 Overall flow:

https://www.ssl.com/article/ssl-tls-handshake-ensuring-secure-online-interactions/

![image](https://github.com/VIK2395/JWT_auth/assets/50545334/dad3da24-e57c-4194-949b-a83c167e5228)
