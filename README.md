# Run Steps

Install Ruby in your environment
`gem install jwt`


Download the Github App private key locally

If in AWS Parameter Store
```
aws ssm get-parameters --region us-east-1 --name <path> --with-decryption --query Parameters[0].Value --output text > app-private-key.pem
```

Run script `./get-github-app-access-token.sh`
