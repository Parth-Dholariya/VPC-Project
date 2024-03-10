# About the Project
creating VPC that use for servers in production environment

To improve resiliency, the servers are deployed in two Availability Zones, by using an Auto Scaling Groups and an Application Load Balancer. For additional security, the servers are deployed in private subnets. The servers receive requests through the load balancer. The servers can connect to the internet by using NAT Gateway. To improve resiliency, the NAT Gateway deployed in both Availability Zones.

## Overview

1. The VPC has public & private subnets in twwo Availability Zones.
2. Each public subnet contains a NAT gateway and a load balancer node.
3. The servers run in the private subnets, are launched and terminated by using an Auto Scaling Groups, and receive traffic from the load balancer.
4. The servers can connect to the internet by using the NAT Gateway.

> ![VPC](https://github.com/Parth-Dholariya/VPC-Project/assets/92844674/6f68c688-b71a-40b0-b2e4-c246fa244c3c)

