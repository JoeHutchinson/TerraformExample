# Terraform Example

Simple introduction into Terraform.

### To run:
1. Install Terraform locally
2. Create variables.tf using template below or supply as arguments
3. Execute `terraform init` in same directory as example.tf
4. Execute `terraform plan`
5. Execute `terraform apply`
6. Execute `terraform output ip`
7. Wait some time and check AWS, you should be able to ping using ip above
8. Execute `terraform destroy`

### Example variables.tf
```
variable "access_key" {
  default = "<>" // if you remove this you are prompted at execution to supply
}
variable "secret_key" {
  default = "<>" // if you remove this you are prompted at execution to supply
}
variable "region" {
  default = "eu-west-2"
}

variable "amis" {
  type = "map"
  default = {
    "eu-west-1" = "ami-492e7d30"   #.NET Core with Ubuntu Server 16.04 - Version 1.0 [Ireland]
    "eu-west-2" = "ami-6db9580a"  #.NET Core with Ubuntu Server 16.04 - Version 1.0 [London]
  }
}
```