# Use your own certificate SSL

- Generate CSR online : <https://csrgenerator.com>
- Insert domain name : mydomain.com OR *.mydomain.com (wildcard)
- Use generated CSR to copy to your SSL provider
- Save private.key securely
- After that, download certificate result from SSL provider

- If no bundle crt, combine it using cat:

```shell
cat cert.crt root.crt intermediate.crt > bundle.crt
```

## Single Domain

- Create secret TLS with namespace (myapp)

```shell
> get copy of your private.key from csrgenerator.com

kubectl create secret tls mydomain-tls --cert=bundle.crt --key=private.key -n <namespace>
```

- Add your secret tls to ingress.yaml

```shell
  tls:
    - hosts:
        - "mydomain.com"
      secretName: mydomain-tls
```

## Wildcard

- Create secret TLS with namespace (myapp)

```shell
> get copy of your private.key from csrgenerator.com

kubectl create secret tls wildcard.mydomain-tls --cert=bundle.crt --key=private.key -n <namespace>
```

- Add your secret tls to ingress.yaml

```shell
  tls:
    - hosts:
        - "*.mydomain.com"
      secretName: wildcard.mydomain-tls
```
