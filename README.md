<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />

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

1. Use Remote Desktop to connect to your Windows 10 Virtual Machine
2. Within your Windows 10 Virtual Machine, Install Wireshark
3. Open Wireshark and filter for various network traffic
4. Retrieve the private IP address of the Ubuntu VM and attempt to ping it from within the Windows 10 VM


<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/2vjjO2p.png" height="80%" width="80%" alt=""/>
</p>
<p>
Here we will be using Remote Desktop to connect to our virtual machine. On windows, you can search for "Remote Desktop Connection" in the search bar by the Windows button. After clicking it, you will be asked for the computer's IP address and username. You can find the IP address for our virtual machine by navigating through Microsoft Azure's home page until we find Virtual MAchines, and click on the first virtual machine we created. In the "essentials" drop down, we can copy our virtual machine's public IP address to connect to it with Remote Desktop. The username and password are the same ones we used when created our virtual machine the first time. 
</p>
<br />

<p>
<img src="https://i.imgur.com/wQRH6Gh.png" height="80%" width="80%" alt=""/>
</p>
<p>
While on the Virtual Machine, open the web browser and search for the Wireshark windows download and download the installer. Once downloaded, open the file and follow the prompts for the installer setup. Next, you cna close out of the web browser and open up Wireshark. From there you can start filtering through the various network traffic.
</p>
<br />

<p>
<img src="https://i.imgur.com/yiSoCQr.png" height="80%" width="80%" alt=""/>
</p>
<p>
To ping our second virtual machine, we need to obtain its private IP address the same we get found the public IP address for our first virtual machine, using Microsoft Azure. Once we find VM 2's IP address, we can now ping it from inside of VM 1 using the command line or Windows PowerShell and watch the activity as it appears in Wireshark.
</p>
<br />
