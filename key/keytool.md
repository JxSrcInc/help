## Java keytool cmd

Display all entries. Option -v to display alias and other info
>keytool -list -v keystore _keystore-file_

Export certificate to file by selected alias
>keytool -export -keystore _keystore-file_ -alias _alias_ -file _file_

Import certificate to file (any one of two below) - cacerts is Java default key located at
jre/lib/security directory
>keytool -importcert -file _import-file_ -keystore _keystore-file | cacerts_ -alias _alias_

>keytool -import trustcacerts -file _import file_ -keystore _keystore-file | cacerts_ -alias _alias_

Convert keystore from type jks to pkcs12. (See openssl cmd for convert keystore from type pkcs12 to pem) - Note: between [ and ] are optional
>keytool -importkeystore -srckeystore _src-key-store.jks_ -destkeystore _dest-key-store.p12_ [-srcalias _src-alias_] -srcstoretype jks -deststoretype pkcs12

Extract X509 certificate. Note: option -rfc specifies the certificate format is X509
> keytool -exportcert -rfc -keystore _key-store.jks_ -alias _alias_ -file _cert.pem_
