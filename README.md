# aws-capstone
This GitHub repository was made to help me host my AWS Capstone 2023 Capstone project. It will provide a complete breakdown of the steps that I took to get my project to function.


## Task 1 - Planning
The first step that was done was carefully planning out the services that were needed for this project. I set out to make this project be highly availiable, load balanced, have low latency, and most importantly be cost optimized. I budgeted my self $100 to see if I can pull off building a POC infastructure. To make sure I stayed within my budget, I used [Lucidchart](https://www.lucidchart.com/pages/) to help me create a visual representation of my project. Once I figured out what services I was going to use, I headed over to [Amazons Pricing Calculator](https://calculator.aws/#/) to help me guage the total pricing for all the services I have selected. 

During the development of my Lucidchart visual, I mapped out the users and how everything would interconnect within eachother. The way that I wanted to map it out would be starting off with the VPC gateway so my EC2 instances can have inbound and outbound access. Then, I would have my EC2 instances setup with an elastic load balancer which would help my project be highly available without having any loss in performance. This entire infastructure, would be wrapped around in Amazons VPC. (Lucidchart visual explains this concept better.)

~~insert image of your lucidchart (inital infastructure) **TO BE INSERTED LATER**~~
~~insert image of your pricing calculator **TO BE INSERTED LATER**~~
~~insert image of your lucidchart (final modified infastructure) **TO BE INSERTED LATER**~~

## Task 2 - Starting the base for the Cloud Infastructure
Once I got to finished the planning phase, I went into the AWS Cloud Platform and started to create my VPC. For the way that I chose to build out my infastrcuture, I wanted to create 2 availibility zones that would help me later on create a load balancer to help me even the traffic, during peak times. During the setup proccess of my VPC I started out creating the 2 availability zones with both a private and public subnet in each AZ. For the private and public subnets, I had the public subnets use a IPV4 range of 10.0.0.0/24, whilst the private subnets used a 10.0.1.0/24 IPV4 CIDR block. Once I got the VPCs' setup, the next step was to setup the temporary EC2 Instance that would host the application this entire project is about. 

~~insert image of setting up the temporary vpc~~



## Task 3 - Implementing The Load Balancer
Once I have confirmed that the VPC and the temporary EC2 instance are functional, 
