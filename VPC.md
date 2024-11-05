# About Virtual Private Cloud(VPC)
A Virtual Private Cloud (VPC) is a private cloud environment hosted within a public cloud infrastructure. It allows users to create a logically isolated network within a public cloud, enabling greater control over their cloud resources while benefiting from the scalability and cost-effectiveness of a public cloud.

# Importance of a VPC
A VPC is essential for enhancing security, control, and flexibility in your cloud setup. **WITHOUT IT!**   you risk exposing your data to threats and losing the ability to manage your resources effectively.

# Uses of a VPC
**1. Hosting Web Applications**

**2. Disaster Recovery**



# 
- Go to VPC and create a VPC then we 
 have to create 4 subnets , where 2     subnets are private and other two are  public .

![image](https://github.com/user-attachments/assets/da062c01-c6bc-496f-862b-41c830407fe3)


## create  gateways:- 

 1st  create INTERNET GATWAY , whic is  to be connected to your VPC which is   created earliy.
![image](https://github.com/user-attachments/assets/aa0591f2-eafb-4bc3-815e-b52313b26bb6)



•2nd we have to create VPG virtual      privaye gate, and connect to VPC .

## create route tables 

•Now we have to go to the route table   and create 2 route table , one for     IGW and another for VGW .


![image](https://github.com/user-attachments/assets/b3d55501-2d31-41b6-861d-1a89f9473eb7)


•Now we have to connect two public      subnet in myigw and on other we have   to add the private subnets .

![image](https://github.com/user-attachments/assets/cb33be64-fa79-4be5-ab18-99cad9e3687d)


## create instances

• now we have to create two instnaces    where we have to enable the public     IPv4 .

•then on both instance we have to       downlaod the web server here i have    downlaoded the apache2 server

-- after that i chech that my             instances are working or not .

![Screenshot_2024_1104_182258](https://github.com/user-attachments/assets/c913fb61-bc91-43d2-bd2a-47fdba5e508e)

## now we have to create the load         balancer

--where we have to give vpc, aviablity   zone of the ec2 instance

•then we have to create the target      group where we have to select the two  insatance we have create then we have  to go to helath check edited option    which was present below the load       balancer is create ,then edit it as    given below image


![Screenshot_2024_1104_182902](https://github.com/user-attachments/assets/0ae0ab8a-9196-486b-ad41-b9e27c901240)

•after that come to load balancer       where we have to select the target     group which we have created then make  the load balancer , it will look like  the given image below .

![Screenshot_2024_1104_183106](https://github.com/user-attachments/assets/a891ba72-6a20-4f33-89c2-cbe07cd88904)

![Screenshot_2024_1104_183126](https://github.com/user-attachments/assets/1c5a8cf9-ff8d-4565-8968-7d1c0df5920a)

*now put on any one instance write following commands in putty -*

* ```
  htop
  ```
  ```
  seq 999999999999999999999999999999999999999999999999999999999 > /dev/null &
  ```
  ```
  htop
  ```



