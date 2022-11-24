# Creation of the Infrastructure setup on AWS using the Cloudformation 

- Code is in the Repository, and the description of the code is given below

### Step1 : Created the VPC having the name and cidr as these are the conditional arguments.

### Step2 : Create the Internet Gateway

### Step3 : Attach the Internet gateway to the VPC

<img width="695" alt="image" src="https://user-images.githubusercontent.com/67600604/203746399-b8fd9112-f20f-4437-9584-4e33184359c2.png">

### Step4 : Subnet Creation In Vpc including the AZName, VPCName and CIDR IP.

### Step5 : Created the Route Table 

### Step6 : Create the ROute for the RT to the IGW

<img width="774" alt="image" src="https://user-images.githubusercontent.com/67600604/203746607-ec6f0d08-f89b-4ac7-a299-ee6d39a1c396.png">

```
0.0.0.0/0 -> IGW
secondary Route Table is for the IGW Attachment - IGW
primary is for the NAT Attachment - No IGW
```
- Note - Because whenever any person comes in, he/she will add the subnet and if the primary rt having the IGW all became public , so IGW should be in secondary Rt always, not in the default one

### Step7 : Subnet Association in he Routing table.

### Step8 : Create the EC2 Instance.

### Step9: Create the Security-Group with the port 80 and port 22 inbound rule.

<img width="682" alt="image" src="https://user-images.githubusercontent.com/67600604/203746908-e3e994cb-fa70-4343-9afd-5284f6ff1ea8.png">

### Step10 : Create the Elastic-IP and Association of E-IP, Security Group and Key-pair to the Instance using !Ref 

<img width="809" alt="image" src="https://user-images.githubusercontent.com/67600604/203746799-38780b22-d332-4fcb-95fb-91e419efe7ac.png">






