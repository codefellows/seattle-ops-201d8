# Setup Your Lab Environment

## Hardware

Your primary computer (that you Zoom into class with) must meet minimum hardware specifications as outlined on the course website under “Laptop Requirements.”

## Software

### Personal Computer

On the personal computer that you'll be attending class with:

- Connected your computer to a high speed internet connection, preferably using Cat6 ethernet cabling for optimal reliability.
- Install [Zoom](https://zoom.us/){:target="_blank"}. Use the Settings menu to pepare your webcam and microphone for use in class.
- Install [Slack](https://slack.com/){:target="_blank"} and ensure you are logged into the class chat. If you need an invitation, contact your instructor.
- Install [Google Chrome](https://www.google.com/chrome/index.html){:target="_blank"} for use with the Remo virtual campus.
- Install [WinRAR](https://www.rarlab.com/rar/winrar-x64-591.exe){:target="_blank"} or 7-ZIP to handle compressed archives.
- Install [Visual Studio Code](https://code.visualstudio.com/){:target="_blank"}.
- Install [WinSCP](https://winscp.net/eng/index.php){:target="_blank"} if you are a Windows user. 
  - MacOS users can use [Cyberduck](https://cyberduck.io/){:target="_blank"}. Reference [this guide](https://kb.iu.edu/d/akom){:target="_blank"} for a step-by-step walkthrough.
- If you are a macOS user, install [Microsoft Remote Desktop](https://apps.apple.com/us/app/microsoft-remote-desktop/id1295203466?mt=12){:target="_blank"} from the Apple Store. Windows users may disregard, as RDP comes preloaded.
  - Windows users will use Remote Desktop Connection, which is an RDP client that comes with Windows.




### Cyber Range on your Lab Computer

**The following instructions detail Ubuntu software setup operations performed in Ops 102. If you successfully set up your cyber range in a previous class, disregard this section.**

 The objective of Ops 102 was to introduce non-computer users to the basics of computer operations by standing up a Ubuntu Linux lab PC that will act as a dedication VirtualBox server for use during the overall Ops program moving forward. A "cyber range" like this allow you to simulate aggressive security operations while abiding by industry-accepted standards of conduct such as the [ISC2 Code of Ethics](https://isc2chapter-phoenix.org/index.php/membership/isc-2-code-of-ethics){:target="_blank"}.

On the lab kit PC that you received from Code Fellows:
- First, check that you've installed the provided solid state drive (SSD) to your lab kit PC. You'll be installing Ubuntu to the SSD for optimal perfomance.
- Connect the computer to the same network as your personal computer. Use cabled ethernet connectivity if possible; wireless connectivity introduces variables that may negatively impact performance.
- Install [Ubuntu Desktop LTS](https://ubuntu.com/download/desktop){:target="_blank"} using the bootable flash drive provided in your lab kit. Format the drive FAT32 for compatibility.
- Once Ubuntu is installed, log into the Desktop and open the Terminal.
- Now we're going to run a series of commands to stand up the required software:
  - Open [Computer Setup Instructions](https://codefellows.github.io/setup-guide/) on your lab computer and follow the link for Ops and Cybersecurity Course near the bottom of the page.
  
  - Follow the instructions in the setup guide exactly. To reduce errors, copy and paste each command into the linux terminal.

  _**Note:** copy/paste works slightly differently in Linux than it does on Windows and Mac. If you're having trouble, check out [this guide](https://linuxconfig.org/copy-and-paste-text-into-the-terminal-on-ubuntu-20-04)._

  - These instructions include installing and enabling apps and configuring system settings. If you're curious what a command does, try googling it!

When you have finished the lab setup guide, you'll have some basic software, including VirtualBox, that will be used throughout the Ops program.

#### Lab System Operations

Next up, we need to make the lab computer accessible remotely from our personal Zoom computer.

- Assign a reserved IP to the lab computer. This is done from the DHCP server your lab computer is plugged into. This is typically a home router/cable modem appliance. If you cannot assign a reserved IP to your lab computer, that's OK but you'll need to periodically check the IP of it so that you can remote in to the correct IP address.
- Test and confirm SSH connectivity from personal computer to lab computer. Practice how to shutdown and reboot the lab computer from SSH terminal.
- Test and confirm RDP connectivity from personal computer to lab computer:
  - Windows users will open Remote Desktop Connection, which is an RDP client that comes with Windows.
  - MacOS users will need to download and install [Microsoft Remote Desktop](https://apps.apple.com/us/app/microsoft-remote-desktop/id1295203466?mt=12){:target="_blank"} in order to use the RDP protocol to access Ubuntu remotely.
  > If you're seeing a black screen as your RDP session, this is probably because XRDP does not allow a user profile to be logged in on Ubuntu itself while another computer is attempting to establish a RDP connection to it. Log out of your lab computer using its keyboard and monitor, then attempt RDP again.
  > If you're still having trouble, check that the sharing switch and remote desktop switches are turned to ***ON***, instructions can be found here: [Ubuntu Turn on Sharing](https://help.ubuntu.com/stable/ubuntu-help/sharing-desktop.html){:target="_blank"}
- Download/install and test a file transfer program:
  - Windows users can use [WinSCP](https://winscp.net/eng/index.php){:target="_blank"}.
  - MacOS users can use [Cyberduck](https://cyberduck.io/){:target="_blank"} to transfer files from the personal computer to the lab computer via SFTP protocol. Reference [this guide](https://kb.iu.edu/d/akom){:target="_blank"} for a step-by-step walkthrough.


Once you can connect to the lab computer via SSH, RDP, SCP, and can create virtual machines in VirtualBox, you're all caught up.

#### Windows 10 VM

Your final task is to create a Windows 10 VM in VirtualBox on the Ubuntu PC:
- In Ubuntu, download the [Windows 10 ISO (4.79 GB)](https://codefellows.github.io/ops-201-guide/curriculum/#course-schedule) onto your lab computer and mount it on a new VM in VirtualBox.
- Create a new Virtual Machine in Virtual Box adjust various parameters to optimize performance of the VM:
  - Adjust RAM to 4 GB.
  - Adjust CPU the utilize 2 cores.
  - Allocate the maximum possible video memory.
  - Set the network adapter to bridge mode.
  - Attach the Windows 10 ISO file to the VM's virtual CD drive.
- Boot into the Windows 10 installer, install Windows 10 Pro, and configure it.
  - Do not sign in with a Microsoft account. Follow [this guide](https://www.windowscentral.com/how-set-windows-10-local-account) to set up Windows 10 with a local account instead.
    - DO NOT use a pre-existing personal account either.
  - Disable as many "features" and extras as seem reasonable for a minimalist installation.
  - When you have access to the Windows 10 desktop, this part is complete.


Once you have a Windows 10 VM deployed, you're all caught up with Ops 102 grads. If you are an Ops 102 grad, indicate in your submission doc that you have reviewed these requirements and your systems configuration meets them.

## Submission Instructions

1. Create a new blank Google Doc. Include above assignment submission text and images within this Google Doc.
1. Name the document according to your course code and assignment.
   - i.e. `seattle-ops-201d1: Reading 01` or `seattle-ops-201d1: Lab 04`.
1. Add your name & date at the top of the Google Doc.
1. Share your Google Doc so that "Anyone with the link can view".
1. Paste the link to your Google Doc in the discussion field below and share an observation from your experience in this lab including how long this lab took to complete.
