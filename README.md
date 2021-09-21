# Creates a S3 bucket into AWS
> NOTE: This script requires Terraform v1.0.7 and Terragrunt v0.32.3
1. To let terraform know which credentials use to connect to AWS run:
    ```
    export AWS_SHARED_CREDENTIALS_FILE=${HOME}/.aws/credentials
    ```
2. To let terraform know which profile use to AWS run:
    ```
    export AWS_PROFILE=dev
    ```
3. Run `terraform init` to initialize the therraform backend.
4. Run `terraform plan` to generate an execution plan.
5. Enter the unique name for your new S3 bucket to be created.
6. Run `terraform apply` and response `yes` in the confirmation prompt to apply the configuration to AWS.
    > NOTE: Add `-auto-approve` flag to avoid confirmation prompt
7. Run `terraform destroy` and response `yes` in the confirmation prompt to destroy the configuration to AWS.
    > NOTE: Add `-auto-approve` flag to avoid confirmation prompt
8. To use Terragrunt instead run `terragrunt plan`, `terragrunt apply` and `terragrunt destroy`.
    > NOTE: 
    > - Add `-auto-approve` flag to avoid confirmation prompt in the  same way that Terraform works.
    > - Ensure to update the `bucket_name` to a unique value over the `inputs` block in the `terragrunt.hcl` config file