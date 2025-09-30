<p align="center">
<img src="https://i.imgur.com/jajLI6i.png" alt="Microsoft Hyper-V Logo"/>
</p>

<h1>Installing Hyper-V VM in Windows 10 Pro</h1>
This tutorial outlines the installation of the Hyper-V Feature on your Windows 10 Pro Operating System.
<br />

<h3>Fall 2022; CTC 316: OS & Network Support assignment</h3>
<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Windows 10 Pro
- Windows Features
- Hyper-V Manager Console
- PowerShell
<br />
<h2>Check requirements for Windows PCs</h2>

- Windows 10 (Pro or Enterprise), or Windows 11 (Pro or Enterprise) Only!
- 64-bit Processor with Second Level Address Translation (SLAT).
- CPU support for VM Monitor Mode Extension (VT-c on Intel CPUs).
- Minimum of 4 GB memory. 8-16 GB of RAM is the Best.
<br />
<h2>Enable Hyper-V on Windows 10 Home; Video Tutorial</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)
<br />

<h2>Operating Systems Used</h2>

- Windows 10 Pro (21H2)
<br />
<h2>High-Level Deployment and Configuration Steps</h2>

- Installing Hyper-V Manager in Windows 10 Pro.
- Creating a VM in Hyper-V.
- Installing the OS (Windows Server 2019) in the Hyper-V VM.
- Working with a Virtual Machine in Hyper-V Manager.
<br />
<h2>Deployment and Configuration Steps</h2>
<h3>Installing Hyper-V in Windows 10 Pro</h3>
<p>
  
  1. Start and log on to your Windows 10 computer.
  
  2. In the search box, begin typing Windows Features until you see Turn Windows Features on or off in the search results, and click on it.
     
  3. In the Windows Features window, click Hyper-V to select it. Click the plus sign to see the options under Hyper-V. Enable the management tools and the Hyper-V platform. Click OK.

  4. When prompted, click Restart now to finish the installation.

  5. When Windows restarts, log on, click in the search box, and type Hyper-V. In the search results, click Hyper-V Manager to open the Hyper-V Manager console.
</p>
<p>
  <img src="https://i.imgur.com/KvfhNt2.png" height="80%" width="90%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/yWOVxDd.png" height="80%" width="90%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/Tevjoqi.png" height="90%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
  6. For the next Task, create a Virtual Machine and explore the settings. Leave Hyper-V Manager open if you plan to continue to the next project.
</p>
<br />
<h3>Creating a VM in Hyper-V</h3>
<p>
  
  DESCRIPTION: You have installed the Hyper-V role on Windows 10 and are ready to create a virtual machine.
  
  1. Log on to your Windows 10 computer and open Hyper-V Manager, if necessary. If your Windows 10 computer is not selected in the left pane, click Connect to Server in the Actions pane, click Local computer, and then click OK.
  
  2. In the Actions pane, click New and then click Virtual Machine.
  
  3. Read the information in the Before You Begin window. You can create a default virtual machine simply by clicking Finish in this window, but for this activity, click Next.
  
  4. In the Name text box, type VMTest1. You can choose a location to store the virtual machine configuration, but for this activity, accept the default location of C:\ProgramData\Microsoft\Windows\Hyper-V by clicking Next.
  
  5. In the Specify Generation window, you choose whether to create a generation 1 or generation 2 virtual machine. A generation 1 VM provides backward compatibility with older Hyper-V versions but provides fewer advanced features. Click Generation 2 and click Next.
  
  6. In the Assign Memory window, type 1024 in the Startup memory text box, leave the option to use dynamic memory selected, and then click Next.
  
  7. In the Configure Networking window, do not change the default option, Not Connected. Click Next.
  
  8. In the Connect Virtual Hard Disk window, you can enter the virtual hard disk’s name, size, and location. By default, the size is 127 GB, and Hyper-V assigns the hard disk the same name as the VM, with the extension .vhdx. You can also use an existing virtual disk or attach one later. Write down the location where Hyper-V stores the virtual hard disk by default, in case you want to access the virtual disk later. Click Next to accept the default settings.
  
  9. In the Installation Options window, click Install an operating system later, if necessary. Click Next.
  
  10. The Completing the New Virtual Machine Wizard window displays a summary of your virtual machine configuration. Click Finish. After the virtual machine is created, you return to Hyper-V Manager and see your new VM in the Virtual Machines pane of Hyper-V Manager 
</p>
<p>
  <img src="https://i.imgur.com/AJ4G9vU.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>


