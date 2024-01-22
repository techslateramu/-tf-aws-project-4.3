## ``Introduction:``

In this document, we outline the requirements for establishing a secure infrastructure on AWS using Terraform. The infrastructure will encompass critical components, including AWS Key Management Service (KMS), an S3 bucket, AWS Lambda, AWS Elastic Beanstalk, DynamoDB, and Amazon Elastic Kubernetes Service (EKS). Emphasis will be placed on defining access policies for AWS KMS to manage secrets securely.

## ``Prerequisites:``

AWS-Account: Ensure that you have an active AWS account with the necessary permissions to create and manage resources.

Terraform-Installed: Make sure Terraform is installed on your local machine. You can download it from Terraforms official website.

AWS-CLI: Install and configure the AWS CLI on your machine with the necessary credentials.

## ``Description:``

- We will create a modular Terraform configuration to deploy the specified AWS resources. The structure will include separate modules for AWS KMS, S3, Lambda, Elastic Beanstalk, DynamoDB, and EKS. Appropriate access policies will be defined for KMS, and outputs from S3, Lambda, DynamoDB, and EKS will be securely stored using KMS.

- Each module will be developed independently, with their outputs integrated as necessary.

## ``Steps:``

1. Clone Repository: git clone https://github.com/techslateramu/-tf-aws-project-4.3.git

2. ```Amazon S3 Module:```

- Develop a Terraform module for Amazon S3.
- Specify parameters such as bucket name, access control policies, and relevant configurations.
- Include main.tf, variables.tf, and outputs.tf files under the module.
- In the main Terraform configuration file (main.tf), call the Amazon S3 module. 

3. ```AWS KMS Module:```

- Develop a Terraform module for AWS Key Management Service (KMS).
- Specify parameters such as the key name, key policy, and relevant settings.
- Include main.tf, variables.tf, and outputs.tf files under the module.
- In the main Terraform configuration file (main.tf), call the AWS KMS module.

4. ```AWS Lambda Module:```

- Create a Terraform module for AWS Lambda.
- Include parameters for configuring the Lambda function, such as function name, runtime, handler, etc.
- Include main.tf, variables.tf, and outputs.tf files under the module.
- In the main Terraform configuration file (main.tf), call the AWS Lambda module.

5. ```AWS Elastic Beanstalk Module:```

- Develop a Terraform module for AWS Elastic Beanstalk.
- Specify parameters for configuring the Elastic Beanstalk environment, such as environment name, platform, instance type, etc.
- Include main.tf, variables.tf, and outputs.tf files under the module.
- In the main Terraform configuration file (main.tf), call the AWS Elastic Beanstalk module.

6. ```Amazon DynamoDB Module:```

- Create a Terraform module for Amazon DynamoDB.
- Include parameters for configuring the DynamoDB table, such as table name, read and write capacity, etc.
- Include main.tf, variables.tf, and outputs.tf files under the module.
- In the main Terraform configuration file (main.tf), call the Amazon DynamoDB module.

7. ```AWS Secrets Manager Module:```

- Create a Terraform module for AWS Secrets Manager.
- Specify parameters such as secret name, secret value, and relevant configurations.
- Incorporate outputs from the Amazon DynamoDB as secrets.
- Include main.tf, variables.tf, and outputs.tf files under the module.
- In the main Terraform configuration file (main.tf), call the AWS Secrets Manager module.

8. ```Test Configuration Locally to validate configurations:```

Run :

1. 'terraform init' 
2. 'terraform Validate'
2. 'terraform plan'
3. 'terraform apply' 

9. ```Cleanup:``

Run :
- ``terraform destroy`` to clean up resources.


10. ``Documentation Update:``

- Include a README with clear instructions on executing Terraform deployment.

- Commit all Terraform configurations and related files to version control (Git) .


