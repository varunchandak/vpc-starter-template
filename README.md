Original Repo: [HERE](https://github.com/1Strategy/vpc-starter-template/)

---

This CloudFormation template will create 3 VPCs in `us-east-1, `ap-south-1` and `ap-southeast-1` with
- 2 Public Subnet
- 2 Private Subnet
- 1 NAT Gateway
- 1 Internet Gateway

in each region.

## IP Ranges

| Location   | IP CIDR       |
|------------|---------------|
| us-east-1     | 10.99.0.0/16   |
| ap-south-1    | 10.100.0.0/16  |
| ap-southeat-1 | 10.101.0.0/16 |


If you'd like to deploy this stack via the command line, you'll need the AWS CLI.

### Validate/Lint Stack

```shell
aws cloudformation validate-template --template-body file://network.yaml
```

### Deploy Stack

Run this command in the AWS CLI:

```shell
aws cloudformation deploy --template-file network.yaml --stack-name main-vpc
```

### Update Stack

Updates to the stack can also be done using the deploy command above.

## License

Licensed under the Apache License, Version 2.0.
