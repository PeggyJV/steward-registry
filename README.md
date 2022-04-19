# steward-authorities

This is a temporary registry for recording Validator's Steward information needed by Strategy Provider clients to establish a secure connection. 

## Registration

If you are a Validator who has [generated certificates]() and [configured Steward](), please make a PR to this repository with the following changes:

1. Add a directory with your validator name in snake-case and place your `server_ca.crt` (or whatever you named it) inside:

```
my_validator_name/
    server_ca.crt
```

2. Append the following JSON object to the list inside of `steward_infos.json` with your information:

```json
{
    "steward_endpoint": "https://steward.mydomain.com:5784",
    "ca": "my_validator_name/server_ca.crt"
}
```
