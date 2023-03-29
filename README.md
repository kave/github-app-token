# Run Steps

Install Ruby in your environment
`gem install jwt`


Download the Github App private key locally

If in AWS Parameter Store
```
aws ssm get-parameters --region us-east-1 --name <path> --with-decryption --query Parameters[0].Value --output text > app-private-key.pem
```
If in Azure Keyvault
```
az keyvault secret download --vault-name ${AZ_KEYVAULT_NAME} --name ${AZ_ATLANTIS_PRIVATE_KEY_SECRET_NAME} --file > app-private-key.pem
```

Run script `./get-github-app-access-token.sh`
