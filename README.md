### Do this

```bash
terraform init
aws-vault exec $(YOUR_AWS_PROFILE) --assume-role-ttl=60m -- "/usr/local/bin/terraform" "plan"
aws-vault exec $(YOUR_AWS_PROFILE) --assume-role-ttl=60m -- "/usr/local/bin/terraform" "apply" "--auto-approve"

# profit?
```
