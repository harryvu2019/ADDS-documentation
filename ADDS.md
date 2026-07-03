# ADDS-documentation

This is where I document my ADDS steps for my ADDS project

I. Environment Preparation:

II. Domain Controller Configuration:
  i) Set up Computer name and WorkGroup as **AdminComputer** and **ParkWirelessINC**
    In Local Server, click on Computer name -> Change -> Edit the Computer name as **AdminComputer**, also change the name of Workgroup to **PARKWIRELESSINC**
    Restart the computer to apply new changes
  ii) Allow Remote Desktop
    In Local server, click on Remote Desktop -> select Allow remote connections to this computer
  
III. Domain Controller Setup
  i) ADDS setup (with current setup)
    Select Manage -> Add Roles and Features Wizard -> Select Role-based or feature-based installation
    (This option is suitable wehn you want to configure a single server by adding roles, role services, and features
    Select a server from the server pool ( we can have multiple servers) 
    In Server Roles, select Active Directory Domain Services
    In Features, select features you want to try on
    In Confirmation, click okay to agree to restart the device then install
    - Configuration required for Active Directory Domain Services at the computer -
    Click on the yellow flag and select Promote the machine to the controller
    Select or Create a new domain
      Add a new forest -> type the Root Domain Name:
    In Domain Controller Options
      Leave the setting as it is to use the optimal version of Window Server
      Set the password and confirm it
      DNS option
        Normally the system doesn't have any available DNS
        Install DNS in Add't Options
          Change the NetBios domain name
    Paths
      Change the name of folders or just leave them as they are
    Do a quick review and prerequisites Check to see if the device can support as a domain controller
    Install and reboot device
    
IV. Setting Roles

a) User accounts
b) Admin accounts (IT team members)
c) Manager accounts
d) Group accounts

V. Security Setup
VI. File Server
