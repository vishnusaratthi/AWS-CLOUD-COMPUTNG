AWS – Amazon Web Services

              In AWS cloud to create a virtual server we will use a service called EC2.

EC2 – Elastic Compute Cloud
               
            which is used to create a virtual server in aws 

Features of EC2:
	Creating Virtual Servers
	AMI – Amazon Machine Image
	Instances type:
     Which is called determines the hardware resources like CPU,
RAM and Storage to our virtual server, based on the application requirements.
	Key Pair:
     A secure Key, Which is used to connect out virtual server.
There are two types of key pairs are available :
1.	Public Key.
2.	Private Key.
  Security Group :
              A virtual firewall, that determines, incoming and outgoing traffic for your virtual server.
              for a security group, to allow incoming traffic, we need to give inbound rules.
INBOUND TRAFFIC

	SSH - 22
	HTTP - 80  
	HTTPS – 443


                                                          OUTBOUND TRAFFIC


	Defaultly for a virtual server, the outgoing traffic is all traffic , 0.0.00 ->which is anyway IP V4 address

	EBS – Volumes

It is a permanent storage they are attached to our virtual server.

	The default storage size 8 GB.

        Instance store Volumes:
             
                   It is a temporary storage created default. It whole  instance when you restart the instance when you restart the delete automatically.
