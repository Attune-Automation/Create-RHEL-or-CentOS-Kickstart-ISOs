## Kickstart Red Hat 8.4 from Boot ISO on ESXi (VMware)

This blueprint is for the setup and installation of a Red Hat virtual machine running on a ESXi Host.   
It uses the Boot ISO image of Red Hat which then requires connections to a repository server to install software packages.   

This has been tested with Red Hat 8.4.

## Red Hat

[Red Hat](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux)  is the world’s leading enterprise Linux platform.   It’s an open source operating system (OS).  
It’s the foundation from which you can scale existing apps—and roll out emerging technologies—across bare-metal, virtual, container, and all types of cloud environments.    

## Boot ISO
A Minimal boot ISO image that is used to boot into the installation program.   This option requires access to the BaseOS and AppStream repositories to install software packages.

## VMware ESXi
[ESXi](https://www.vmware.com/au/products/esxi-and-esx.html) robust, bare-metal hypervisor that installs directly onto your physical server.   
With direct access to and control of underlying resources, VMware ESXi effectively partitions hardware to consolidate applications and cut costs. It’s the industry leader for efficient architecture, setting the standard for reliability, performance, and support.  

## Required Files 
Download Red Hat 8.4 or newer Boot ISO file you wish to build the VM from and add the file in Step 3 `KS RH84 Deploy Boot ISO`. 

## PowerCLI
[PowerCLI](https://developer.vmware.com/powercli) is the tool millions of customers around the world use to manage and automate their VMware environments.  

## To install the PowerCLI for VMWare
`sudo yum install https://github.com/PowerShell/PowerShell/releases/download/v6.2.3/powershell-6.2.3-1.rhel.7.x86_64.rpm`    
`sudo pwsh -Command`