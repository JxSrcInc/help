## Java keytool cmd

Display all entries. Option -v to display alias and other info
>keytool -list -v keystore _keystore-file_

Export certificate to file by selected alias
>keytool -export -keystore _keystore-file_ -alias _alias_ -file _file_

Import certificate to file (any one of two below) - cacerts is Java default key located at 
jre/lib/security directory
>keytool -importcert -file _import-file_ -keystore _keystore-file | cacerts_ -alias _alias_

>keytool -import trustcacerts -file _import file_ -keystore _keystore-file | cacerts_ -alias _alias_ 