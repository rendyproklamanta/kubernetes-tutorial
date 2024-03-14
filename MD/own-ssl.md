## Use your own certificate SSL
- Generate CSR online : https://csrgenerator.com/
- Use generated CSR to copy to your SSL provider
- Save private.key securely
- After that, download certificate result from SSL provider
- If no bundle crt, combine it using cat:
```
cat cert.crt root.crt intermediate.crt > bundle.crt
```
- Create secret TLS with namespace (my-app)
```
> get copy of your private.key from csrgenerator.com

kubectl create secret tls wildcard.mydomain-tls --cert=bundle.crt --key=private.key -n myapp
```

- Add your secret tls to ingress.yaml
``` 
  tls:
    - hosts:
        - "*.mydomain.com"
      secretName: wildcard.mydomain-tls
```