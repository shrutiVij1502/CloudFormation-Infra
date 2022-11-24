# Creation of the Infrastructure setup on AWS using the Cloudformation 

## the Infra contains the custom VPC and a subnet , In which I have launched the EC2 intance 
## Custom Security group having the inbound rule of 22 and 80 ports 
## custom Route Table, with the attachment of Internet Gateway

### Step1 : Created the VPC having the name and cidr as these are the conditional arguments.

### Step2 : Create the Internet Gateway

### Step3 : Attach the Internet gateway to the VPC

### Step4 : Subnet Creation In Vpc including the AZName, VPCName and CIDR IP.

### Step5 : Created the Route Table 

### Step6 : Create the ROute for the RT to the IGW

```
0.0.0.0/0 -> IGW
secondary Route Table is for the IGW Attachment - IGW
primary is for the NAT Attachment - No IGW
```
- Note - Because whenever any person comes in, he/she will add the subnet and if the primary rt having the IGW all became public , so IGW should be in secondary Rt always, not in the default one

### Step7 : Subnet Association in he Routing table.

### Step8 : Create the EC2 Instance.

### Step9 : Create the Elastic-IP.

### Step10: Create the Security-Group with the port 80 and port 22 inbound rule.

### Step11: Association of E-IP, Security Group and Key-pair to the Instance using !Ref 


