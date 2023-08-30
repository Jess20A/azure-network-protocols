<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this overview, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />

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

- Create Virtual Machines
- Install Wireshark
- Create Inbound Security Rules
- Observe Live Network Traffic


<h2>Actions and Observations</h2>

<p>
<img width="389" alt="image" src="https://github.com/Jess20A/azure-network-protocols/assets/142112890/aeec5c75-e52e-4a55-befc-08491e87fbcd">

<img width="369" alt="image" src="https://github.com/Jess20A/azure-network-protocols/assets/142112890/ff5805e4-2dd1-4a77-bae4-908f418f321d">

To observe the network traffic two virtual machines will need to be created, one running windows 10 (VM1) and the other running linux (VM2).  



<p>
<img width="380" alt="image" src="https://github.com/Jess20A/azure-network-protocols/assets/142112890/b0c07012-8601-4ff1-a8c7-54034580f5e8">


<p>
To inspect traffic Wireshark will need to be downloaded and installed. This is a protocol analyzer that will let you see the live traffic happening on your virtual machines. We will be observing traffic from VM1 to VM2.
</p>


<p>
<img width="471" alt="image" src="https://github.com/Jess20A/azure-network-protocols/assets/142112890/1667a080-99af-482a-aa78-35bdfb7c4db0">


In Microsoft Azure by going to Network Security Groups for VM2 and then Inbound Security Rules, you can add new rules that can deny or allow certain network traffic and observe the changes. 


<img width="808" alt="image" src="https://github.com/Jess20A/azure-network-protocols/assets/142112890/138aceac-45b5-4ecf-9ffd-a56d73a921e4">


This picture shows ICMP traffic going from being blocked to being allowed to come through from VM1 to VM2. You can also open up Power Shell and by pinging VM2's Private IP Address you will see replies or timed out requests.


