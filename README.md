# NAT-Gateway

## What is NAT-Gateway
  ### NAT stands for `Network Address Translation`
  ####  NAT is designed for IP address conservation. It enables private IP networks that use unregistered IP addresses to connect to the Internet.

Lets take one familiar example. In any residential society/commercial place, there will be entrance gate and watchman. A new person entering inside premise will not know anything about inside members like where to go etc. This watchmen also keep watch on all object coming inside and allow only authorized person.

Similar to entrance of your premise, NAT is entrance of your VPC and it should be public facing to monitor all incoming object. So, it allow only authorized access to internal private EC2 or others systems.

### Nat gateway is a higly available gateway that allows you to have your privte subnet communicate to the internet without becoming public.``

 `You can use a network address translation (NAT) gateway to enable instances in a private subnet to connect to the internet or other AWS services, but prevent the internet from initiating a connection with those instances`

 #### NAT gateway is used to give your private network internet connectivity but still ensuring that your resources are not accessible from the internet. So in order to allow access to internet it has to route traffic through public network which has a Internet gateway attached.

 ### Why you should use Internet Gateway?
 1.An Internet Gateway allows resources within your VPC to access the internet (think yum updates, external database connections, wget calls, OS patch, etc). 

