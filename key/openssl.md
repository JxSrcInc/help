## Openssl cmd

Convert keystore from PKCS12 (file with extension .p12) to PEM (file with extension .pem). Note: process will ask for phrase.
>openssl pacs12 -in _key-store.p12_ -out _key-store.pem_

Extract private key from keystore to a file which is without password/phrase
>openssl rsa -in _key-store.pem_ -out _private-key.pem_

Extract x509 certificate from keystore to a file which is without password/phrase
>openssl x509 -in _key-store.pem_ -out _cert.pem_

Extract public key from certificate. Note: use ">" not "-out".
>openssl x509 -pubkey -noout -in _cert.pem_ > _pubkey.pem_
