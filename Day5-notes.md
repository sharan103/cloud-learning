
Azure Network Day-5 ( 27-02-2025 ) 09:02 AM IST
-------------------------------------------------

Public IP -- 2 types of Sku -- Basic , Standard
Static IP address, Dynamic IP Address

* Azure Virtual Machine , it by default select the Public IP as Standard --> Static

* Basic Sku ---> Static, Dynamic

Public IP address ---> service used to create a external Public IP Address

### Security Aspects of Public IP SKU's:
----------------------------------------------------
*  1.Security Aspects is always associated with the Public IP creation either it be Basic sku or Standard sku
* In AWS , by default we have virtual network vpc. for each and every region we have 1 default vpc.
* IN AZURE , there is no default network vnet.
-------------------------------------------------------------------
* 2. Azure Public IP Dynamic Assignment Vs Static Assignment
* In this session practice , i used option none in inbound port rule, if any user want to connect from his laptop to created windows machine we always open port 3389 but we are not used for this session.
* By default basic sku disabled how to enable
2 -VM
* Routing preference when create a public ip of baasic & standard.
* Zone refundant.
* When comes to security aspect of your public ip in basic we try to connect from our local laptop to this remote machine with rdp port 3389.
* When we use basic sku , by default all the ports should be open.
* here i disabled the pubic ip also it will open by default , external user can connect in basic sku.
* In standard sku by default ports are blocked if an external user try to login with rdp client it will not allowed and blocked the external user.
* In NSG you opened for port 3389 then it will open or otherwise it will blocked.
* Basic sku is less secure, nsg is not optional or disabled.
* How to create a Public IP Basic SKU , Standard SKU

* VM2 , default subnet inside we have vm2 , external user try to connect it is not allowing, now you should coonect then create NSG .
* In NSG , we have 2rules 1. inbound and outbound 2 rules set it.NSG ASSOCIATE WITH SUBNET.
* NSG IS OPTIONAL YOU REQUIRED YOU USE OR NOT YOU CAN AVOID IN BASIC SKU, THERE IS NO RULE.
* IN STANDARD SKU ,NSG IS MANDATORY , YOU NEED NSG TO OPEN ANY PORTS OR TO LOGIN , PUBLIC IP STANDARD SKU IS HIGHLY RECOMMENDED. 
* Still the connection is not established because you not set the rules of inbound and outbound.
* We know that for every vm nic card is associated with vm.for every NIC CARD we have 1public ip of standard sku is associated.
* Now external user try to connect it will check the rules of inbound and outbound rules


NExt Security Aspect of Public IP SKU - 30 mins

Pricing Public IP


Azure Public IP Address pricing 
https://azure.microsoft.com/en-us/pricing/details/ip-addresses/


How to decide on Public IP Address Assignment
--------------------------------------------------------
Static
Dynamic

Next Session -> Vnet Peering , NSG(Network Security Group)

VPN Site to site


