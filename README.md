# AWS CodeArtifact Python Proxy

Proxies requests to AWS CodeArtifact Python for anonymous access

![ci](https://github.com/Polymathian/aws-codeartifact-python-proxy/workflows/ci/badge.svg)

## Usage

Best used as a Docker container with the following env vars

| Env Var                   | Value                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------|
| `CODEARTIFACT_REGION`     | AWS Region<br>e.g. `ap-southeast-2`                                                       |
| `CODEARTIFACT_ACCOUNT_ID` | AWS Account ID<br>e.g. `123456789012`                                                     |
| `CODEARTIFACT_DOMAIN`     | AWS CodeArtifact domain name<br>e.g. `mycompany`                                          |
| `CODEARTIFACT_REPOSITORY` | AWS CodeArtifact repository name<br>e.g. `pypi-store`                                     |
| `PROXY_AUTH`              | Optional<br>HTTP Basic auth credentials expected by the proxy<br>e.g. `username:password` |

You may also pass in AWS credential environment variables or make credentials available some other way.

The container exposes on port 5000, you can then use this container in your pip config/commands to pull packages from CodeArtifact.
