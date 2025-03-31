# AWS VPC Setup with Terraform

This project contains a Terraform configuration file (`vpc.tf`) to set up a basic Virtual Private Cloud (VPC) infrastructure in AWS. It includes resources such as a VPC, an Internet Gateway, a public subnet, a route table, and associations to enable public access.

# Resources Created

The `vpc.tf` file creates the following AWS resources:

1. VPC:
   - CIDR Block: `10.0.0.0/16`
   - DNS Support: Enabled
   - DNS Hostnames: Enabled

2. Internet Gateway:
   - Attached to the VPC.

3. Public Subnet:
   - CIDR Block: `10.0.1.0/24`
   - Public IP Mapping: Enabled
   - Availability Zone: `us-west-2a`

4. Route Table:
   - Associated with the VPC.
   - Contains a route to the Internet Gateway for `0.0.0.0/0`.

5. Route Table Association:
   - Associates the public subnet with the route table.

# File Overview

`vpc.tf`

This file contains the Terraform configuration for setting up the AWS VPC infrastructure. Below is a summary of its key components:

- Provider Configuration:
  Specifies the AWS region (`us-west-1`).

- VPC:
  Creates a VPC with DNS support and hostnames enabled.

- Internet Gateway:
  Creates and attaches an Internet Gateway to the VPC.

- Subnet:
  Creates a public subnet within the VPC.

- Route Table:
  Creates a route table and adds a route to the Internet Gateway.

- Route Table Association:
  Associates the route table with the public subnet.

## Prerequisites

- Terraform installed on your local machine.
- AWS CLI configured with credentials and a default region.
- An AWS account with permissions to create VPC resources.

## Result

![image](https://github.com/user-attachments/assets/83a0c296-e006-4625-973b-a3b83886c150)

