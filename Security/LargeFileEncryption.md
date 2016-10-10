## Large File Encryption

### Encrrption


```shell
openssl smime -encrypt -binary -aes-256-cbc -in plain-file.zip -out encrypted-file.zip.enc -outform DER your-ssl-certificate.pem
```

### Decryption


```shell
openssl smime -decrypt -binary -in encrypted-file.zip.enc -inform DER -out plain-file.zip -inkey private.key 
```

you can add `-passin pass:your_password` if you set password for private key