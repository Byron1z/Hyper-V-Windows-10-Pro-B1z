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
<br />
<h2>Check requirements for Windows PCs</h2>

- Windows 10 (Pro or Enterprise), or Windows 11 (Pro or Enterprise) Only!
- 64-bit Processor with Second Level Address Translation (SLAT).
- CPU support for VM Monitor Mode Extension (VT-c on Intel CPUs).
- Minimum of 4 GB memory. 8-16 GB of RAM is the Best.
<br />

<h2>Enable Hyper-V on Windows 10 Home | Video tutorial</h2>

- ### [YouTube: Enable Hyper-V on Windows 10 Home](https://www.youtube.com/watch?v=FaytvySV04s&list=WL&index=66)
<br />

<h2>Operating Systems Used</h2>

- Windows 10 Pro (22H2)

<h2>Windows Server 2019 ISO</h2>

- ### [Download](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2019)

<h2>Windows 10 download</h2>

- ### [Free Download](https://www.microsoft.com/en-us/software-download/windows10)
<br />

<h2>High-Level Deployment and Configuration Steps</h2>

- Installing Hyper-V Manager in Windows 10 Pro.
- Creating a VM in Hyper-V.
- Installing the OS (Windows Server 2019) in the Hyper-V VM.
- Working with a Virtual Machine in Hyper-V Manager.
<br />

<h2>Deployment and Configuration Steps</h2>
<h3>Installing Hyper-V Manager in Windows 10 Pro</h3>
<h4>DESCRIPTION: In this project, you install the Hyper-V feature on a Windows 10 computer.</h4>
<h4># Note</h4>
<p>
  If you are running Windows 10 Pro in a Virtual Machine, you may need to enable virtualization features to allow nested virtualization. 
  
  - In VMware Workstation, you do this in the Processors section of the Virtual Machine Settings. 
  
  - In Oracle VirtualBox, use the System tab of the Settings window for the VM. If you are using Hyper-V, open a PowerShell window and type Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true, where <VMName> is the name of your Windows 10 virtual machine.
</p>
<br />
<h4>Begin</h4>
<p>
  
  1. Start and log on to your Windows 10 Pro computer.
  
  2. In the search box, begin typing Windows Features until you see Turn Windows Features on or off in the search results, and click on it.
     
  3. In the Windows Features window, click Hyper-V to select it. Click the plus sign to see the options under Hyper-V. Enable the management tools and the Hyper-V platform. Click OK.

  4. When prompted, click Restart now to finish the installation.

  5. When Windows restarts, log on, click in the search box, and type Hyper-V. In the search results, click Hyper-V Manager to open the Hyper-V Manager console.
</p>
<p>
  <img src="https://i.imgur.com/KvfhNt2.png" height="80%" width="90%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/yWOVxDd.png" height="80%" width="90%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/qLOjUkQ.png" height="90%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
  6. For the next Task, create a Virtual Machine and explore the settings. Leave Hyper-V Manager open if you plan to continue to the next project.
</p>
<br />
<h3>Creating a VM in Hyper-V</h3>
<h4> DESCRIPTION: You have installed the Hyper-V role on Windows 10 and are ready to create a virtual machine.</h4>
<p>
  
  1. Log on to your Windows 10 computer and open Hyper-V Manager, if necessary. If your Windows 10 computer is not selected in the left pane, click Connect to Server in the Actions pane, click Local computer, and then click OK.
  
  2. In the Actions pane, click New and then click Virtual Machine.
  
  3. Read the information in the Before You Begin window. You can create a default virtual machine simply by clicking Finish in this window, but for this activity, click Next.
  
  4. In the Name text box, type VMTest1. You can choose a location to store the virtual machine configuration, but for this activity, accept the default location of C:\ProgramData\Microsoft\Windows\Hyper-V by clicking Next.
  
  5. In the Specify Generation window, you choose whether to create a generation 1 or generation 2 virtual machine. A generation 1 VM provides backward compatibility with older Hyper-V versions but provides fewer advanced features. Click Generation 2 and click Next.
  
  6. In the Assign Memory window, type 1024 in the Startup memory text box, leave the option to use dynamic memory selected, and then click Next.
  
  7. In the Configure Networking window, do not change the default option, Not Connected. Click Next.
  
  8. In the Connect Virtual Hard Disk window, you can enter the virtual hard disk’s name, size, and location. By default, the size is 127 GB, and Hyper-V assigns the hard disk the same name as the VM, with the extension .vhdx. You can also use an existing virtual disk or attach one later. Write down the location where Hyper-V stores the virtual hard disk by default, in case you want to access the virtual disk later. Click Next to accept the default settings.
  
  9. In the Installation Options window, click Install an operating system later, if necessary. Click Next.
  
  10. Completing the New Virtual Machine Wizard window displays a summary of your virtual machine configuration. Click Finish. After the virtual machine is created, you return to Hyper-V Manager and see your new VM in the Virtual Machines pane of Hyper-V Manager 
</p>
<p>
   <img src="https://i.imgur.com/rDtl1Hf.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<br />

<h3>Installing the OS (Windows Server 2019) in the Hyper-V VM</h3>
<p>
  REQUIRED TOOLS AND EQUIPMENT: Your Windows 10 computer and a Windows Server 2019 evaluation ISO file

  Download ISO File: www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2019  
</p>
<h4>DESCRIPTION: You have created a virtual machine and are ready to install Windows Server 2019 as a guest OS using the installation DVD. You need the installation media for Windows Server 2019.</h4>
<p>

  1. Log on to your Windows 10 computer and open Hyper-V Manager, if necessary. If your Windows 10 computer is not selected in the left pane, click Connect to Server in the Actions pane, click Local computer, and then click OK.
  
  2. Click VMTest1 in the Virtual Machines pane of Hyper-V Manager. In the Actions pane, click Settings under VMTest1 to open the Settings for VMTest1 window. (See Figure 8-18.)
</p>
<p>
  <img src="https://i.imgur.com/pPBE1fd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  3. Now you need to add a virtual DVD drive. Click the SCSI Controller in the left pane. In the right pane, click DVD Drive and click Add. Click the Image file and then click Browse. Locate and then click the Windows Server 2019 ISO file. Click Open. Click OK.

  4. In Hyper-V Manager, right-click the VMTest1 virtual machine and click Connect.
  
  5. Power on VMTest1 by clicking Start. You will see a message to press any key to boot from the DVD. Be sure to click in the VM window and press the spacebar or any other key. If you are too late, just click Action and Reset in the Virtual Machine Connection console to restart the VM and try again.
  
  6. Begin the installation of Windows Server 2019 by clicking Next in the Windows Setup window.
  
  7. After Windows Server 2019 is installed, close the Virtual Machine Connection console and shut down the virtual machine by right-clicking VMTest1 and clicking Shut Down. Click Shut Down to confirm, if necessary.
</p>
<p>
  <img src="https://i.imgur.com/sZKL0UY.png" height="90%" width="100%" alt="Disk Sanitization Steps"/>
  (I had to make a new VM, "VMTest2," due to an error)
</p>

