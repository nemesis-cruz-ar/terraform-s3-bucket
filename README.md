# Creates a S3 bucket into AWS
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
7. Run `terraform destroy` and response `yes` in the confirmation prompt to destroy the configuration to AWS.