# Steward Registry

This is a temporary registry for recording Sommelier Validators' Steward information needed by Strategy Provider clients to establish a secure connection.

## Registration

If you are a Validator who has [generated certificates](https://github.com/PeggyJV/steward/blob/main/docs/04-GeneratingCertificates.md) and [configured Steward](https://github.com/PeggyJV/steward/blob/main/docs/02-StewardForValidators.md), please make a PR to this repository with the following changes:

1. Add a directory with your validator name in snake-case and place your `server_ca.crt` (or whatever you named it) inside:

```
my_validator_name/
    server_ca.crt
```

2. Append the following JSON object to the list inside of `stewards.json` with your information:

```json
{
    "ca": "my_validator_name/server_ca.crt",
    "endpoint": "https://steward.mydomain.com:5734"
}
```

