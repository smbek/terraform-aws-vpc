# terraform-aws-vpcbatch5

```hcl
module "vpc" {
    source = "smbek/terraform-aws-vpcbatch5/aws"
    region        = "us-east-2"
    vpc_cidr      = "10.0.0.0/16"
    sub1_cidr     = "10.0.1.0/24"
    sub2_cidr     = "10.0.2.0/24"
    sub3_cidr     = "10.0.3.0/24"
    ip_on_launch   = true
    instance_type = "t2.micro"
}
```