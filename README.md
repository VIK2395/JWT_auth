__OpenID vs OAuth__

__JWT vs sessions:__\
https://www.youtube.com/watch?v=7Q17ubqLfaM \
https://stackoverflow.com/questions/68902836/what-is-the-difference-between-client-side-based-sessions-and-server-side-sessio

JWT is encoded, but not encrypted. This means everyone can see what is inside.\
It is digitally signed using secret(HMAC SHA256 algorithm) or a public/private key pair using RSA or ECDSA.

![image](https://github.com/VIK2395/JWT_auth/assets/50545334/d058ed3a-144e-46d6-81d9-95ce6583f5f2)

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
  
