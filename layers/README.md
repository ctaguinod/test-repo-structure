# Layers

Contains layers for deploying actual resources using terraform

## Proposed Directory Structure

Directory | Comments | 
---       |---       |
000base | *Contains base resources such as VPCs, Subnets, Internal Zones, SNS etc..* |
100data | *Contains data related resources such as RDS, Elasticache, S3 buckets, etc..* |
200compute | *Contains compute related such as EC2, EKS, ASG, ALB/ELB, etc..* |

## Proposed Code structure

Simplify  to the ff:

- main.tf - call modules, locals, and data sources to create all resources
- variables.tf - contains declarations of variables used in main.tf
- outputs.tf - contains outputs from the resources created in main.tf
- versions.tf - contains version requirements for Terraform and providers
- terraform.tfvars - contains assigned variables