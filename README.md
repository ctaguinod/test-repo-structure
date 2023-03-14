# Proposed New Repo Structure

This is a proposed repo structure that contains all resources to depploy a specific environment.

## Proposed Directory Structure

Directory | Comments | 
---       |---       |
Layers    | *Contains TF codes to deploy resources separated by different layers/directories* |
Scripts   | *Contains custom scripts* |
Modules   | *Contains custom Modules* |
Docs      | *Contains Documentations* |


## Proposed Structure for Layers Directory

Directory | Comments | 
---       |---       |
000base | *Contains base resources such as VPCs, Subnets, Internal Zones, SNS etc..* |
100data | *Contains data related resources such as RDS, Elasticache, S3 buckets, etc..* |
200compute | *Contains compute related resources such as EC2, EKS, ASG, ALB/ELB, etc..* |

## Proposed Code structure

Simplify to the ff:

- main.tf - call modules, locals, and data sources to create all resources
- variables.tf - contains declarations of variables used in main.tf
- outputs.tf - contains outputs from the resources created in main.tf
- versions.tf - contains version requirements for Terraform and providers
- terraform.tfvars - utilize tfvars to assign values to variables

## TODOS

1. Create separate repo for shared/common resources?
    - S3 buckets to store terraform state files
    - Route53 Zones
    
2. Create separate repo for all custom modules?