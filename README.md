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
- [ ] EC2 (Elastic Compute Cloud)

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
cat /etc/resolv.conf

# if file is empty
# add Google nameserver
sudo vi /etc/resolv.conf

# Google IPv4 nameservers
nameserver 8.8.8.8
nameserver 8.8.4.4
```

## multi step connection (for `ssh tunneling`)
```shellsession
# config file on ~/.ssh/ directory

Host bastion
    HostName [ip address]
    User ec2-user
    IdentityFile ~/.ssh/keyPair.pem
Host web01
    HostName [ip address]
    User ec2-user
    IdentityFile ~/.ssh/keyPair.pem
    ProxyCommand ssh bastion -W %h:%p
Host web02
    HostName [ip address]
    User ec2-user
    IdentityFile ~/.ssh/keyPair.pem
    ProxyCommand ssh bastion -W %h:%p
```
