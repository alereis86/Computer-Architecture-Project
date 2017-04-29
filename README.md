# Introduction to the Assignment 

The aim of this project was to successfully install and fully configure a virtual machine hosting a LAMP stack and to demonstrate a web application functioning on it. The three main stages can be listed as follows:
- The initial configuration of the virtual machine and installation of the operating system (Linux Ubuntu)
- Installation and testing of the Apache web server, MySQL database and php processing module.
- Installation and testing of the CMS and modification of the hosted content.
This report will cover these stages in a step-by-step manner with a special focus on the learning process involved.

# Explanation of Virtualisation and VM VirtualBox
A virtual machine is a computer environment software in which an operating system or program can be installed and run. In a more simplified way, we can say that the virtual machine functions as a "computer inside the computer".
Virtual machines are extremely useful on a daily basis as they allow the user to run other operating systems within a window, having access to all the software they need. They are used in a variety of cases, such as launching programs that are still in the development stage.
The virtual machine will allocate, during the execution of operating systems, a defined amount of RAM. It typically emulates a physical computing environment, but a “virtualization layer” that translates these requests to the hardware present on the machine will manage all the CPU, memory, hard drive, network, and other hardware resources.
Virtual machines are able to "trick" programs and operating systems because they believe they are running directly on physical hardware, not within a simulation. Therefore, they can be installed the same way they would be inside the operating system.
One reason for the emergence of virtualization is that years ago, when mainframes dominated the technology landscape and there were no personal computers, for example, there was no practical "buy, install, and use software" - this was Accompanied by libraries and other features that made it almost unique to the computer for which it was originally developed.
In this way, often an organization implementing a new system would be forced to acquire equipment just to run it, instead of simply taking advantage of existing machinery, leaving all the operation more expensive after all.
Virtualization has solved this problem: one can take advantage of an existing computer to run two or more separate systems, as each one runs within its own virtual machine. This avoids spending on new equipment and takes advantage of the possible idle resources of the computer.
Nowadays, virtualization allows, for example, a company running multiple services from a single server or even a home user testing an operating system on their computer before actually installing it. From the corporate point of view, its current use is intended for various applications, such as ERP systems, cloud computing services, simulation tools, among many others.
## VirtualBox 
Is a virtualization software developed by the company Innotek later bought by Sun Microsystems that later was bought by Oracle that, like the VMware Workstation, aims to create environments for installation of different systems. It allows the installation and use of one operating system within another, as well as their respective software, such as two or more independent computers, but physically sharing the same hardware.
VirtualBox has an extremely modular design with well-defined internal programming interfaces and a client / server design. This makes it easy to control multiple interfaces at once. For example: you can start a virtual machine on a typical virtual GUI machine and then control that machine from a command line, or possibly remotely.

# Configuration and Deployment of the Virtual Machine

The first step todeploy the virtual machine is to download Ubuntu Server, and the version used was OS 16.04.
This file is going to be use later when we had our virtual machine setup.
We need to create a Virtual machine to install our guest OS using VM (VirtualBox) .
For hosting our 32 Bit Ubuntu Linux server, we need to select the size and type of drive to use, as well as the memory you will assign to your machine. I recommend settings are the following:
 Memory Size: 2048mb
 Virtual Hard Disk: VDI, dynamically allocated, 20GB.
After we have mounted the .iso power on our virtual machine and the Ubuntu install file boot up. 
Following the onscreen instructions we setup username and accounts.  The most important thing about this step is to write down the settings we enter here as you will need them later. 
The machine should reboot when finished, prompting for the login details we entered earlier. Now we had successfully deployed our Ubuntu server.

# Explanation of what a web server is and Apache

The web server is the most important part of the infrastructure of an internet site. It is a program that uses HTTP (Hypertext Transfer Protocol) to serve the files that form web pages to users, in response to their requests, which are forwarded by the HTTP clients of their computers. Dedicated computers and equipment can be referred to as web servers as well.
In summary, the communication between the user and the server is due to the decomposition of the URL (page address) by the browser in several parts (domain name and protocol of the page). The DNS then translates the domain entered by the user into the IP address (numerical combination of the actual web site address) for the browser to determine which protocol to use (FTP, file transfer protocol, and http , Hypertext transfer protocol).
This causes the server to retrieve the requested files on the page. An example: When the user types http://www.escolalinux.com, the browser requests the file from the server and waits for the response. The server responds after checking that the address exists and finds the required files, then executes the instructions and delivers the results. When it does not find, the server displays the error message (Error 404, usually).
## APACHE
As a web server, is the best known and most used. The reasons include its excellent performance, security, cross-platform compatibility and all of its features.
Like any server of its type, Apache is responsible for providing pages and all resources that can be accessed by the user. Sending e-mails, messages, online shopping and various other functions can be performed thanks to servers like Apache. What stands out in Apache is that, despite everything, it is distributed under the GNU license, that is, it is free and can be studied and modified through its source code by anyone.

# Setup and Configuration of Apache Webserver	

We’re first going to install the Apache web server, logging  into our VM 
Entering the command below to install the Apache Web Server:
sudo apt-get install apache2 apache2-utils 
We want to change our setting so the Apache2 web server will start up at system boot. To do this enter the systemctl enable command.Type the following:
sudo systemctl enable apache2 
We also want to start the service now by entering the command: 
sudo systemctl start apache2 
After makeing sure that ou rnetwork adapter settings make our VM visible, we should be able to access the default apache homepage by typing http://localhost:80 into our browser. A webpage entitled Apache2 Ubuntu Default Page should load if it has been configured correctly. 
The next step was to Install MySQL, an open source Database programwith the following codes:
sudo apt-get install mysql-client mysql-server
Sudo mysql_secure_installation
Also we Install PHP and Modules PHP, which is an open source server-side scripting language mainly used for web development.
The commands used was:
sudo apt-get install php7.0 php7.0-mysql libapache2-mod-php7.0 php7.0-cli php7.0-cgi php7.0-gd
sudo vi /var/www/html/info.php
?php
 phpinfo(); 
?>
wq to save our file and close.

# Reflection
This project was really complex at first, since I did not understand all the steps purpose. After everything was finished, the virtualization was way more clear.
For me it would be much easier to make the changes in the virtual machine in windows mode, not code. At some point I was just following codes that I don’t know exactly what they do and why are they like this. It would be better to have a windows interface.
Another problem I had was regards the passwords. If I can emphasize something it would be to take note of what you enter in this stage. Because once you done it, you cant go back and change it, leaving the only option of having to start over again if you forget.

# Conclusion
Virtualization, whether it is for services, applications or servers, is no longer a trend to be a reality in many industries and areas, whether in or outside the technology area. In addition is no longer a trend and already a reality in the corporate world, and has been bringing countless advantages to everyone, since the economy of resources and equipment is also a green technology.


