# NAT-Gateway

![internet gateway](https://user-images.githubusercontent.com/24816990/71585599-76776600-2b17-11ea-970d-23401c6c32f5.png)


## What is NAT-Gateway

### NAT stands for `Network Address Translation`
  
####  NAT is designed for IP address conservation. It enables private IP networks that use unregistered IP addresses to connect to the Internet.

Lets take one familiar example. In any residential society/commercial place, there will be entrance gate and watchman. A new person entering inside premise will not know anything about inside members like where to go etc. This watchmen also keep watch on all object coming inside and allow only authorized person.

Similar to entrance of your premise, NAT is entrance of your VPC and it should be public facing to monitor all incoming object. So, it allow only authorized access to internal private EC2 or others systems.

### Nat gateway is a higly available gateway that allows you to have your private subnet communicate to the internet without becoming public.

 `You can use a network address translation (NAT) gateway to enable instances in a private subnet to connect to the internet or other AWS services, but prevent the internet from initiating a connection with those instances`

 #### NAT gateway is used to give your private network internet connectivity but still ensuring that your resources are not accessible from the internet. So in order to allow access to internet it has to route traffic through public network which has a Internet gateway attached.

 ### Why you should use Internet Gateway?
 1. An Internet Gateway allows resources within your VPC to access the internet (think yum updates, external database connections, wget calls, OS patch, etc)
 2. It only works one way. The internet at large cannot get through your NAT to your private resources unless you explicitly allow it
 3. It is a fully-managed service — just create it and it works automatically, including fail-over.

#### Important points to note while using NAT-Gateway
- Redundant inside the availability zones
- You can only have one nat gateways inside one az 
- Preferred by the enterprise 
- Starts with a throughput of 5gps and scales currently to 45 Gbps
- No need to patch the os for your nat gateway 
- Not associated with security grouups 
- Automatically assigned a public ip address
- Remember to update your route tables 
- No need to disable source/destination checks
- You’ll need one in each AZ since they only operate in a single AZ

**Finally if you have resources in one availability zones and they share one NAT gateway, in the event that the nat gateway availability zone is down, resources in the other availability zones lose internet access. To create an availability zone-independent architecture, create a NAT gateway in each availability zone and configure routing to ensure that resources use the NAT gateway in the same availability zone.**

[Read more about AWS-Gateway here](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html)


### Create a Nat-Gateway on AWS 

![ezgif com-gif-maker](https://user-images.githubusercontent.com/24816990/71599161-fa4a4600-2b49-11ea-9eab-3f142338605e.gif)


## Contributing
 Please feel free to fork this package and contribute by submitting a pull request to enhance the functionalities.
 
 ### How can I thank you?
Why not star the github repo? I'd love the attention! Why not share the link for this repository on Twitter,Hackernews or Destructoid ? Spread the word!  or feel like sending me an e-mail temitopetola@gmail.com

Don't forget to [follow me on twitter](https://twitter.com/thecraftman_)
