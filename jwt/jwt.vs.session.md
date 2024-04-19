__Stateful vs Stateless Architecture:__

https://www.freecodecamp.org/news/stateful-vs-stateless-architectures-explained/ \
![image](https://github.com/VIK2395/JWT_auth/assets/50545334/d55f7e58-9704-4752-ba5e-93cacef888af)

![image](https://github.com/VIK2395/JWT_auth/assets/50545334/fa6390f6-afd2-4bce-8e3e-65fd2f7fb73d)

__Session vs JWT authentication:__\
https://www.youtube.com/watch?v=7Q17ubqLfaM \
https://www.geeksforgeeks.org/session-vs-token-based-authentication/amp/ \
https://medium.com/@tiff.sage/client-side-session-vs-server-side-session-d506f5408e8c \
https://stackoverflow.com/questions/68902836/what-is-the-difference-between-client-side-based-sessions-and-server-side-sessio

Session authentication:
- Client-side sessions (user info stored on client; signs the cookies cryptographically for security => you can see data, but not modify, like with jwt);
- Server-side sessions (user info stored on server; bad for multiple servers);

JWT authentication:

JWT is encoded, but not encrypted. This means everyone can see what is inside.\
It is digitally signed using __HMAC-SHA256 algorithm with secret__ or a public/private key pair using RSA or ECDSA.

![image](https://github.com/VIK2395/JWT_auth/assets/50545334/aff4375f-038d-43e6-98f1-ca9900cd5bf7)

Source: https://learn.microsoft.com/en-us/dotnet/api/system.security.cryptography.hmacsha256?view=net-8.0 \
![image](https://github.com/VIK2395/JWT_auth/assets/50545334/d0dae7b2-e729-4ea3-b5da-c44fc1a8428d)

https://medium.com/@chauhanshubham19765/jwt-refresh-token-61823e888bc7

Authentication flow with access token only.

![image](https://github.com/VIK2395/JWT_auth/assets/50545334/cc711603-72a4-4b6d-86da-6bd4aa9485b5)

Authentication flow with access and refresh tokens.

![image](https://github.com/VIK2395/JWT_auth/assets/50545334/d28537bd-d001-4bad-8ea2-2377e5eb1a1b)

__Typically access token stored in local storage and refresh token in cookies.__

Refresh Token Rotation => when sending refresh token, get new pair of __refresh__ and access tokens.
There are different approaches/flows how to deal with refresh tokens:

- Different secrets can be used for __refresh__ and access tokens like here https://www.geeksforgeeks.org/jwt-authentication-with-refresh-tokens/
- No saving refresh tokens in db at all like here https://www.geeksforgeeks.org/jwt-authentication-with-refresh-tokens/ (in this example, only access token are reissued)
- Store only last valid refresh token in db and remove it when refreshing(replacing with new one) like here https://www.youtube.com/watch?v=vQldMjSJ6-w
- Keep track of all related refresh tokens for Reuse Detection like here https://auth0.com/blog/refresh-tokens-what-are-they-and-when-to-use-them/
