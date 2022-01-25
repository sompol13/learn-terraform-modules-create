## Build and Use a Local Module
In this tutorial, you will create a module to manage AWS S3 buckets used to host static websites.

### Install the local module
Whenever you add a new module to a configuration, Terraform must install the module before it can be used. Both the `terraform get` and `terraform init` commands will install and update modules.
- `terraform init`
- `terraform apply`
- After running `terraform apply`, your bucket will be created.

### Upload files to the bucket (HTML)
- `aws s3 cp modules/aws-s3-static-website-bucket/www/ s3://$(terraform output -raw website_bucket_name)/ --recursive`
- Visit `https://sompol-bucket-20220125.s3-ap-southeast-1.amazonaws.com/index.html`


### Reference
https://learn.hashicorp.com/tutorials/terraform/module-create?in=terraform/modules