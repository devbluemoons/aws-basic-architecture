# aws-basic-architecture
account / access  / networking / computing / load balancer / database / storage / domain / monitoring / cost  

## Account

## IAM (Identity and Access Management)
- [x] root user
- [x] user
- [x] group
- [ ] role

## Networking
- [ ] VPC (Virtual Private Cloud)
- [ ] subnet
  - [ ] public subnet
  - [ ] private subnet
- [ ] routing table
- [ ] internet gateway
- [ ] NAT (Network Address Translation)
  - [ ] NAT gateway
- [ ] security group 
  - [ ] in-bound rule
  - [ ] out-bound rule
- [ ] NACL (Network Access Control List)
  - [ ] in-bound rule
  - [ ] out-bound rule
- [ ] ELB (Elastic Load Balancing)
  - [ ] Load Balancer
  - [ ] Target groups
  - [ ] ALB (Application Load Balancer) : for web-site 
  - [ ] NLB (Network Load Balancer) : for game, chatting
  - [ ] CLB (Classic Load Balancer)

## Computing

## RDS
- [ ] database engine
- [ ] parameter group
- [ ] option group
- [ ] subnet group

## Storage
- S3 (Simple Storage Service)
  - [ ] bucket
  - [ ] role

## check point
- linux nameserver
```shellsession
cat /etc/resolvconf

# there is anything
# add Google nameserver
sudo vi /etc/resolvconf

# Google IPv4 nameservers
nameserver 8.8.8.8
nameserver 8.8.4.4
```

