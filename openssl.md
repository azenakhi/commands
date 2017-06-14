
## OpenSSL - Extract P12
```
#!/bin/bash
CN=$1
p12=${CN}-1.0.p12
openssl pkcs12 -clcerts -nokeys -in ${p12} -out ${CN}.crt -passin pass:****
openssl pkcs12 -in ${p12} -out ${CN}.key -nodes -passin pass:****
cp ${CN}.key ${CN}.key.new
openssl rsa -in ${CN}.key.new -out ${CN}.key
rm -rf ${CN}.key.new
```
