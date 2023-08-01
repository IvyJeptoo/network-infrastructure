# Infrastructure-as-Code : network-infrastructure
Using cloud formation we are creating code that builds infrastructure.

## Infrastructure Diagram
![screenshot-2021-02-16-at-5 24 30-pm](https://github.com/IvyJeptoo/network-infrastructure/assets/98116399/8b3843b3-fc3e-44b6-a87a-753d951f135a)

## Resources
The resources built will - : 
-  VPC,Subnets
-  Internet Gateway and NAT Gateway
-  Route Table

  
## Shell Script
**create.sh** - The file contains the `create-stack` command which expects three command-line arguments.
```
aws cloudformation create-stack --stack-name $1 --template-body file://$2  --parameters file://$3 --region=us-east-1
```
**update.sh** - The file contains the `update-stack` command which expects three command-line arguments.
```
aws cloudformation update-stack --stack-name $1 --template-body file://$2  --parameters file://$3 --region=us-east-1
```


