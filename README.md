# sctp-wk15-2.15-secret
![License](https://img.shields.io/badge/license-MIT-blue.svg)  
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)  

# sctp-wk14-2.14-serverless

## Table of Contents
- [What is needed to authorize your EC2 to retrieve secrets from the AWS Secret Manager?](#1)
- [Derive the IAM policy (i.e. JSON)? Using the secret name prod/cart-service/credentials, derive a sensible ARN as the specific resource for access](#2)

<a id="1"></a>
### What is needed to authorize your EC2 to retrieve secrets from the AWS Secret Manager?
```
The Ec2 needs a role with custom policy that has permission secretsmanager:GetSecretValue to retrieve secrets from AWS secret manager
```
<a id="2"></a>
### Derive the IAM policy (i.e. JSON)? Using the secret name prod/cart-service/credentials, derive a sensible ARN as the specific resource for access?
```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": "secretsmanager:GetSecretValue",
            "Resource": "arn:aws:secretsmanager:us-east-1:255945442255:secret: prod/cart-service/credentials -54W77G"
        }
    ]
}
```


