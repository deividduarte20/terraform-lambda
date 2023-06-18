## Projeto consiste em provisionar uma função lambda com python, policy e role que permite criar invalidation na distribuição do cloudfront

### Baixe o projeto
```bash
git clone https://github.com/deividduarte20/terraform-lambda.git
```

### Inicie o terraform
```bash
terraform init
```

### Aplique a infra como código
```bash
terraform apply
```

## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.0.3 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | >= 3.74.3 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | 5.4.0 |

## Resources

| Name | Type |
|------|------|
| [aws_iam_policy.cloudfront_invalidation_policy](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_policy) | resource |
| [aws_iam_role.lambda_role](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_role) | resource |
| [aws_iam_role_policy_attachment.cloudfront_invalidation_attachment](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_role_policy_attachment) | resource |
| [aws_lambda_function.my_lambda_function](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/lambda_function) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_lambda-name"></a> [lambda-name](#input\_lambda-name) | Name of lambda | `string` | `"First-lambda-tf"` | no |
| <a name="input_policy-name"></a> [policy-name](#input\_policy-name) | Name of policy | `string` | `"PolicyCreateInvalidation"` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_arn-lambda"></a> [arn-lambda](#output\_arn-lambda) | n/a |
