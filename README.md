



[![Docs](https://img.shields.io/badge/docs-latest-brightgreen.svg)](http://doc.servertribe.com)
[![Discord](https://img.shields.io/discord/844971127703994369)](http://discord.servertribe.com)
[![Docs](https://img.shields.io/badge/videos-watch-brightgreen.svg)](https://www.youtube.com/@servertribe)
[![Generic badge](https://img.shields.io/badge/download-latest-brightgreen.svg)](https://www.servertribe.com/community-edition/)

# Create RHEL and CentOS Kickstart ISOs






# Attune

[Attune](https://www.servertribe.com/)
automates and orchestrates processes to streamline deployments, scaling,
migrations, and management of your systems. The Attune platform is building a
community of sharable automated and orchestrated processes.

You can leverage the publicly available orchestrated blueprints to increase
your productivity, and accelerate the delivery of your projects. You can
open-source your own work and improve existing community orchestrated projects.

## Get Started with Attune, Download NOW!

The **Attune Community Edition** can be
[downloaded](https://www.servertribe.com/comunity-edition/)
for free from our
[ServerTribe website](https://www.servertribe.com/comunity-edition/).
You can learn more about Attune through
[ServerTribe's YouTube Channel](https://www.youtube.com/@servertribe).







# Clone this Project

Clone this project into your own instance of Attune.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-clone-new-project-01.png" alt="clone a new project"/>

---

Paste the GIT repository URL into Attune and Select Clone.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-clone-new-project-02.png" alt="clone a new project"/>

---

**Now that this project is in your Attune instance you can begin creating
Jobs.**

Navigate to the Plan workspace and create a Job from a Blueprint in the
Project you cloned.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-plan-new-job-11.png" alt="plan a new job"/>

---

Configure the Parameters for the Job you created. Create the Values you're
missing in the next step.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-plan-new-job-12.png" alt="plan a new job"/>

---

Create the Values required to fill the Parameters for the Job.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-plan-new-job-13-1.png" alt="plan a new job"/>

---

Run your Job.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-run-job-01.png" alt="run your job"/>

---

**Congratulations, you’ve run a cloned project.**

If you need further assistance, please explore our help.

<img width=200 src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-get-help-01.png" alt="get help"/>




## Blueprints

This Project contains the following Blueprints.



### Create and Configure CentOS8.5 Kickstart Boot ISO


### Create and Configure RHEL8.7 Kickstart Boot ISO


### Create and Configure RHEL8.7 Kickstart DVD ISO

#### Kickstart Red Hat 8.4 from Boot ISO on ESXi (VMware)

This blueprint is for the setup and installation of a Red Hat virtual machine running on a ESXi Host.   
It uses the Boot ISO image of Red Hat which then requires connections to a repository server to install software packages.   

This has been tested with Red Hat 8.4.

#### Red Hat

[Red Hat](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux)  is the world’s leading enterprise Linux platform.   It’s an open source operating system (OS).  
It’s the foundation from which you can scale existing apps—and roll out emerging technologies—across bare-metal, virtual, container, and all types of cloud environments.    

#### Boot ISO
A Minimal boot ISO image that is used to boot into the installation program.   This option requires access to the BaseOS and AppStream repositories to install software packages.

#### VMware ESXi
[ESXi](https://www.vmware.com/au/products/esxi-and-esx.html) robust, bare-metal hypervisor that installs directly onto your physical server.   
With direct access to and control of underlying resources, VMware ESXi effectively partitions hardware to consolidate applications and cut costs. It’s the industry leader for efficient architecture, setting the standard for reliability, performance, and support.  

#### Required Files 
Download Red Hat 8.4 or newer Boot ISO file you wish to build the VM from and add the file in Step 3 `KS RH84 Deploy Boot ISO`. 

#### PowerCLI
[PowerCLI](https://developer.vmware.com/powercli) is the tool millions of customers around the world use to manage and automate their VMware environments.  

#### To install the PowerCLI for VMWare
`sudo yum install https://github.com/PowerShell/PowerShell/releases/download/v6.2.3/powershell-6.2.3-1.rhel.7.x86_64.rpm`    
`sudo pwsh -Command`




## Parameters


| Name | Type | Script Reference | Comment |
| ---- | ---- | ---------------- | ------- |
| Build Base Dir | Text | `buildbasedir` | Base directory to install Kickstart files under.    |
| Build Node | Linux/Unix Node | `buildnode` | This is the Node used to build the ISO. |
| Build Node User | Linux/Unix Credential | `buildnodeuser` | User on your Attune Build server to connect as. |
| ISO Configured Subnet | Network IPv4 Subnet | `isoconfiguredsubnet` | Subnet your host is on.   Enter the DNS servers for the subnet as part of the Parameter. |
| ISO Language | Text | `isolanguage` | Set the language you wish the new VM to use.    |
| ISO Node | Linux/Unix Node | `isonode` | The target server is a generic placeholder, usually used for the server a script will run on.
For example, the server being built if the procedure is building a server. |
| ISO root User | Linux/Unix Credential | `isorootuser` | UserID for the root user. |
| ISO TimeZone | Text | `isotimezone` | Set the timezone you wish your new VM to use. |
| RPM Mirror URL | Text | `rpmmirrorurl` | CentOS mirror examples:
http://mirror.centos.org/centos/7/os/x86_64/
http://mirror.centos.org/centos/8-stream/AppStream/x86_64/os/ |




## Files


| Name | Type | Comment |
| ---- | ---- | ------- |
| AD Root CA certificate | Version Controlled Files | This is the root CA certificate from the Windows Ad server.  Used for all SSL security procedures and SSL to the rpm servers.    

Update this if you wish to download rpms via SSL. |
| CentOS8.5 Boot ISO | Large Archives | https://archive.kernel.org/centos-vault//8.5.2111/isos/x86_64/CentOS-8.5.2111-x86_64-boot.iso |
| Kickstart from DVD Config | Version Controlled Files | Kickstart commands and options reference
https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/performing_an_advanced_rhel_8_installation/kickstart-commands-and-options-reference_installing-rhel-as-an-experienced-user

Kickstart Generator: https://access.redhat.com/labs/kickstartconfig/ |
| Kickstart from RPM Mirror Config | Version Controlled Files | Kickstart commands and options reference
https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/performing_an_advanced_rhel_8_installation/kickstart-commands-and-options-reference_installing-rhel-as-an-experienced-user

Kickstart Generator: https://access.redhat.com/labs/kickstartconfig/ |
| RHEL8.7 Boot ISO | Large Archives | Download the required Red Hat Boot ISO and attached  here. |
| RHEL8.7 DVD ISO | Large Archives | Download the required Red Hat DVD ISO and attached  here. |






# Contribute to this Project

**The collective power of a community of talented individuals working in
concert delivers not only more ideas, but quicker development and
troubleshooting when issues arise.**

If you’d like to contribute and help improve these projects, please fork our
repository, commit your changes in Attune, push you changes, and create a
pull request.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-pull-request-01.png" alt="pull request"/>

---

Please feel free to raise any issues or questions you have.

<img src="https://www.servertribe.com/wp-content/uploads/2023/02/Attune-get-help-02.png" alt="create an issue"/>


---

**Thank you**
