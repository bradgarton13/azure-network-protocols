# azure-network-protocols
<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Using the Microsoft Azure Portal, create two virtual machines in the same virtual network.
- Using Remote Desktop connect to Virtual Machine 1 and download/ install Wireshark.
- Initiate communication between Virtual machine 1 and 2, and then analyze their traffic wit Wireshark.


<h2>Actions and Observations</h2>

<p>

![image](https://github.com/bradgarton13/azure-network-protocols/assets/166873905/56fb7f13-b704-4146-bc64-a211d6a48fc5)

  
</p>
<p>
After launching any web browser and navigating to the Microsoft Azure Portal I created a resource group known as RGNetworkLab. Inside this resource group I created two virtual machines, one being a Window's 10 machine(VM1) and the other a Linux based machine(VM2).
  During creation I made sure to put both of these machine inside the same virtual network;"VM1-vnet".
</p>
<br />

<p>

![image](https://github.com/bradgarton13/azure-network-protocols/assets/166873905/e33dbd43-14ef-497d-865f-51e5bb2df751)


</p>
<p>
As displayed above, I used VM1 to communicate with VM2 in a few different ways. First I sent a normal and continuous ping command to VM2's private IP address on the virtual network. After that, I initiated a ssh connection with a user on VM2 and executed a few linux commands on the linux command line. One of the commands being pwd( print working directory) which displays the current working directory. I then exited the ssh connection with the exit command and verified I was back in the VM1 command line by executing the ipconfig command.
</p>
<br />


![image](https://github.com/bradgarton13/azure-network-protocols/assets/166873905/2d5740b7-1e91-4ed3-b136-991679fec89c)



</p>
<p>
Displayed above, I have installed and launched Wireshark to analyze some traffic on VM1. By using certain specifiers like dhcp, ssh, and dns in Wireshark's search bar, I'm able to filter for specific traffic. In the example above, I've filtered specifically for traffic from the SSH protocol that came from the ssh connection we initiated earlier with VM1 and VM2
</p>
<br />
