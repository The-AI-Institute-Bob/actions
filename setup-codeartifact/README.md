# Setup Codeartifact

This action request a temporary Codeartifact token from AWS and configure `yarn`

`codeartifact-domain` and `codeartifact-owner` inputs are required, see [inputs](#inputs) belows

## AWS Credential

This action requires configured AWS credentials to request the token !

You must:

- Configure AWS in a previous steps
- or
- Pass `aws-*` inputs for an automatic configuration

## Registry

This action set `yarn` config with the `registry-url` and the **token**

- Pass the input `registry-url` for use a custom registry
- Leave blank for using configured registry
- Pass `false` to `registry-url` for disabled `yarn` configuration

## Inputs

| name                    | description               | required |
| ----------------------- | ------------------------- | :------: |
| `codeartifact-domain`   | Codeartifact domain       |   [x]    |
| `codeartifact-owner`    | Codeartifact domain owner |   [x]    |
| `registry-url`          | Codeartifact registry url |          |
| `aws-access-key-id`     | AWS access key            |          |
| `aws-secret-access-key` | AWS secret access key     |          |
| `aws-region`            | AWS region                |          |

## Outputs

| name        | description            |
| ----------- | ---------------------- |
| `npm-token` | The Codeartifact token |
