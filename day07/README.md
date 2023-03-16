### AWS SECURITY GROUP

A security group acts as a virtual firewall for EC2 instances to control incoming and outgoing traffic.
- INBOUND rules control the incoming traffic
- OUTBOUND rules control the outgoing traffic.

NOTE: 
- If we don't specify a security group, Amazon EC2 uses the default security group. We can add and remove rules in it.
- We can add multiple security group in one instance as well as One security group can be added multiple instance.


### AWS Elastic IPs

It is essential to host a website in cloud.
An Elastic IP address is static; it does not change over time. An Elastic IP address is for use in a specific Region only, and cannot be moved to a different Region.



Problem Statement
> After restart my AWS Instance public ip changed
>

Solve:
> Step One:
> 
> Go to EC2 > Netwrok & Security > Elastic IPs > Allocate Elastic IP address > Allocate
>
> Step Two:
> 
> Select the allocated ip > Actions > Associate Elastic IP address > Instance: _select instance_ > Associate.

NOTE: `If you don't use the Allocated Elastic IP with Instance then remove it. Otherwish you will be charged $`

To Remove the Elastic IP address
> Got to  EC2 > Netwrok & Security > Elastic IPs > _Select Allocated IP_ > Actions > Release Elastic IP address
