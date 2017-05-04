## Test APN certificate with OpenSSL 

#### Sandbox

```
openssl s_client -connect gateway.sandbox.push.apple.com:2195 -cert cert.pem -key key.pem
```

#### Production
```
openssl s_client -connect gateway.push.apple.com:2195 -cert cert.pem -key key.pem
```