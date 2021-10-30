# SSL localhost (MacOS)
1. Generate key
```
keytool \
 -keystore  [name].jks  -alias [alias] -deststoretype pkcs12 \
 -genkeypair -keyalg RSA -validity [in-days:36500] \
 -dname "CN=127.0.0.1" \
 -ext "SAN=IP:127.0.0.1"
```
2. Add Spring config
```
server:
  ssl:
    key-store: classpath:[path]/[name].jks
    key-store-password: ${KEYSTORE_PWD}
    key-store-type: pkcs12
    key-alias: [alias]
    key-password: ${KEY_PWD}
  port: 8443
```
3. Run service
3. Copy cert to local
3. Add to Keychain
3. Restart browser
