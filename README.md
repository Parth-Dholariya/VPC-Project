# About the Project
creating VPC that use for servers in production environment

To improve resiliency, the servers are deployed in two Availability Zones, by using an Auto Scaling Groups and an Application Load Balancer. For additional security, the servers are deployed in private subnets. The servers receive requests through the load balancer. The servers can connect to the internet by using NAT Gateway. To improve resiliency, the NAT Gateway deployed in both Availability Zones.

## Overview

1. The VPC has public & private subnets in twwo Availability Zones.
2. Each public subnet contains a NAT gateway and a load balancer node.
3. The servers run in the private subnets, are launched and terminated by using an Auto Scaling Groups, and receive traffic from the load balancer.
4. The servers can connect to the internet by using the NAT Gateway.

> ![VPC](https://github.com/Parth-Dholariya/VPC-Project/assets/92844674/6f68c688-b71a-40b0-b2e4-c246fa244c3c)

## Steps

1. create VPC in the AWS with following resource map in [create VPC](https://github.com/Parth-Dholariya/VPC-Project/tree/main/create%20VPC) folder.
2. create a launch template as given in [Launch Templates](https://github.com/Parth-Dholariya/VPC-Project/tree/main/Launch%20Templates) folder.
3. create Auto Scaling Groups with network in private subnet as given in [Auto scaling groups](https://github.com/Parth-Dholariya/VPC-Project/tree/main/Auto%20Scaling%20Groups) folder.
4. create an bastion host or Jump instance in public subnet to access the private subnet instance using ssh.
5. now login to any of the private subnet and run you application using "python3 -m http.server 8000" command
6. create a Application Load Balancer in public subnet with desired ports in security groups, create target group with desired ec2 instances & ports.

now access the deployment by copying the DNS name from load balancer and paste in browser.
