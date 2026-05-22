# OluTech-Production-VPC

Production-ready AWS VPC with 4 subnets across 2 AZs, public/private tiers, and IGW.  
Built during AWS Cloud Accelerator Week 3 · Day 1 - VPC Fundamentals

## VPC Architecture Overview

<img width="800" alt="OluTech_VPC" src="https://github.com/user-attachments/assets/c488f3be-09a1-4fe9-bfab-65b02d207936" />

*Figure 1: Complete VPC architecture with public and private subnets across two Availability Zones.*

## VPC Console View

<img width="1309" alt="VPC_Console" src="https://github.com/user-attachments/assets/7ab37b1e-ded1-4ce8-9cb2-b3cc251355f2" />

*Figure 2: The custom VPC `OluTech-Production-VPC` with CIDR `10.0.0.0/16`.*

## Subnets Configuration

<img width="1309" alt="Subnet_console" src="https://github.com/user-attachments/assets/2f27ddbe-8aea-4f33-9fa7-72f48427ec7a" />

*Figure 3: Four subnets – two public, two private – correctly provisioned across `us-east-1a` and `us-east-1b`.*

## Public Subnet Settings (Auto-assign Public IP)

<img width="1319" alt="Public_Subnet_Settings" src="https://github.com/user-attachments/assets/558ddc2c-4283-4af2-bec9-e59563f9997d" />

*Figure 4: Public subnets configured to auto-assign public IPv4 addresses for internet-facing resources.*

## Key Configuration Details

| Component | Configuration |
|-----------|---------------|
| VPC CIDR | `10.0.0.0/16` |
| Availability Zones | `us-east-1a`, `us-east-1b` |
| Public Subnets | `10.0.1.0/24` (AZ-a), `10.0.2.0/24` (AZ-b) |
| Private Subnets | `10.0.10.0/24` (app tier), `10.0.20.0/24` (data tier) |
| Internet Gateway | Attached to VPC |
| NAT Gateway | Placed in public subnets (one per AZ) |
| Route Tables | Public route table with IGW route; private route tables with NAT routes |
| Auto-assign Public IP | Enabled on public subnets |

## What This Architecture Provides

- **High availability** across 2 AZs
- **Security isolation** between public and private tiers
- **Outbound internet access** for private subnets via NAT Gateway
- **Scalable foundation** for web, application, and database layers

## Skills Demonstrated

- VPC CIDR planning and subnet design
- Multi-AZ high availability architecture
- Public vs private subnet separation
- Internet Gateway and NAT Gateway configuration
- Route table management
- Infrastructure documentation

## Repository Contents

- Architecture diagrams and console screenshots
- Subnet mapping and configuration details
- (Optional) CloudFormation / Terraform templates

## Author

**Oluwatoba**  
AWS Cloud Learner | AWS Cloud Accelerator Program  
Week 3 · Day 1 – VPC Fundamentals
