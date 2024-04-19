# terraform-aws-vpcbatch5

## Create main.tf file and input following

```hcl
module "vpc" {
    source = "smbek/vpcbatch5/aws"
    region        = "us-east-2"
    vpc_cidr      = "10.0.0.0/16"
    sub1_cidr     = "10.0.1.0/24"
    sub2_cidr     = "10.0.2.0/24"
    sub3_cidr     = "10.0.3.0/24"
    ip_on_launch   = true
    instance_type = "t2.micro"
    subnet1_name  = "Hello1"
    subnet2_name  = "Hello2"
    subnet3_name  = "Hello3"
    ports = [ 22, 80, 81 ]
}
```

## Create apache.sh file and input a script. Eg.
```hcl
#!bin/bash

sudo apt update 
sudo apt install apache2 -y
sudo systemctl start apache2
sudo systemctl enable apache2

```

