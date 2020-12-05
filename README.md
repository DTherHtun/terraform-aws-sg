# terraform-aws-sg
This is a module that makes it easy to create security groups in AWS. Built for 0.12

Example Usage:
```
module "sg" {
    source = "DTherHtun/sg/aws"
    name = var.name
    description = var.description
    vpc_id = var.vpc_id

    ingress_rules = [
        {
            protocol = "tcp"
            port = 80
            cidr_blocks = ["0.0.0.0/0"]
        }
    ]    
}

```
outputs:
the created security group accesible via: `module.sg.security_group`

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| aws | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| description | n/a | `string` | `null` | no |
| egress\_rules | A list of custom egress rules to apply | `any` | `[]` | no |
| ingress\_rules | A list of custom ingress rules to apply | `any` | `[]` | no |
| name | n/a | `string` | `null` | no |
| vpc\_id | n/a | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| security\_group | n/a |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
