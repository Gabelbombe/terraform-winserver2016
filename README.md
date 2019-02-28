### Do this

```bash
terraform init
aws-vault exec $(YOUR_AWS_PROFILE) --assume-role-ttl=60m -- terraform plan -var 'aws_region=$(YOUR_AWS_REGION)' -var 'admin_password=$(YOUR_NOT_IDIOTIC_PASSWORD)' -var 'key_name=$(YOUR_KEY_GENERATED_FROM_AWS)'
aws-vault exec $(YOUR_AWS_PROFILE) --assume-role-ttl=60m -- terraform apply -var 'aws_region=$(YOUR_AWS_REGION)' -var 'admin_password=$(YOUR_NOT_IDIOTIC_PASSWORD)' -var 'key_name=$(YOUR_KEY_GENERATED_FROM_AWS)'--auto-approve

# profit?
```
