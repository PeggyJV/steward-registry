# Steward Registry

This is a temporary registry for recording Sommelier Validators' Steward information needed by Strategy Provider clients to establish a secure connection. 

## Registration

If you are a Validator who has [generated certificates]() and [configured Steward](), please make a PR to this repository with the following changes:

1. Add a directory with your validator name in snake-case and place your `server_ca.crt` (or whatever you named it) inside:

```
my_validator_name/
    server_ca.crt
```

2. Append the following JSON object to the list inside of `stewards.json` with your information:

```json
{
    "ca": "my_validator_name/server_ca.crt",
    "ca_hosted": "https://steward.mydomain.com/server_ca.crt",
    "endpoint": "https://steward.mydomain.com:5784"
}
```

### Explanation

The `ca_hosted` and `ca` fields must point to two copies of the *same file*. This provides a means of ensuring that you own the domain in question.
