# terraform-aws-certificate
Generate LetsEncrypt certificates for AWS(Route 53) hosted domain using Terraform.!

1. Install [Terraform](https://learn.hashicorp.com/terraform/getting-started/install.html) v11.6
2. Create a user on AWS with the set of [permissions attached](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_manage-attach-detach.html#add-policies-console) AmazonRoute53FullAccess, AWSCertificateManagerFullAccess, Route53CreateHostedZone
3. Install and setup [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html), ensure AWS credentials are in place
4. Update DOMAIN and domain ADMINISTRATOR_EMAIL in `variables.tf`
5. Run `terraform init` to initialize the working directory, run `terraform plan` to create an execution plan and finally run `terraform apply` to generate desired output.

    ```sh
   terraform init
   terraform plan
   terraform apply
    ```
6. It will take a few minutes to create certificates. Once complete, your certificates will be stored in `certificates.tf` file.