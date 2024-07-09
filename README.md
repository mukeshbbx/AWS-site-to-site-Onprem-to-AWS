# AWS-site-to-site-Onprem-to-AWS
AWS site-to-site configuration on-prem to aws

Configure the AWS side

## 1. Create VPC

```bash
1.VPC only.
2.Name:
3.IPv4 CIDR:
```

## 2. Create Subnet

```bash
1.(Select the VPC created) 
2.Subnet name:
3.AZ:
4.IPv4 subnet block:
```
## 3. Create Internet gateway
```bash
1.Name:

(Select the IGW you created, Action > attach to VPC)
```


## 4. Create the Route table
```bash
1.Name:
2.VPC:

*select the route you created*
- In route
  Destination: 0.0.0.0/0
  Target: IGW you created

-In subnet associations
  Select the public subnet and save.
```

In virtual private Network

## 1.create Virtual private gateway
```bash
1.Name:

*Select and attach to VPC*
```

## 2.Create Cusrtomer gateway
```bash
1.Name:
2.Ip Address:(Public IP Add of the firewall)
```

## 3.Create Site-to-Site VPN Connection
```bash
1.Name:
2.Target gateway type: Virtual private gateway
(Select the created Virtual private gateway)
3.Customer gateway: Existing 
(Select the created customer gateway)
4.Routing option: Static
5.Static IP prefixes: (CIDR Range of On-prem) 
```

Once the configuration is done Download the configuration file.


## Extra

Edit Route
Dest: Customer CIDR Range
Target: Virtual private gateway

Edit route Propagation
Enable
