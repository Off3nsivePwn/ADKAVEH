# ADKAVEH
This PowerShell script is designed for various attacks and security 
assessments in an Active Directory (AD) environment. To execute this 
script, certain prerequisites and configurations are required. Below, a 
complete explanation of the requirements, capabilities, and advantages 
of this tool is provided.

 #Prerequisites for Running the Script

1. **Windows Operating System:**

This script is designed for Windows environments and requires PowerShell.

2. **PowerShell Modules:**

The script utilizes the ActiveDirectory and GroupPolicy
modules. These modules are typically pre-installed on Windows Server 
systems. However, if they are not installed, you can install them using 
the following command:
                       Install-WindowsFeature -Name RSAT-AD-PowerShell

After installation, import the modules using the following command:
                       Import-Module ActiveDirectory
                       Import-Module GroupPolicy

3. **Administrative Access:**
   - To execute this script, you need Domain Admin privileges or equivalent 
permissions, as many of the script's functions access sensitive AD 
information.

4. **Temporarily Disabling Windows Defender:**
  - Some functions of this script may be blocked by Windows Defender. Therefore,
    the script temporarily disables Windows Defender. If Windows Defender 
    is already disabled, this step is not necessary.

5. **Domain Information:**
   - To run the script, you need the domain name (DomainName), username 
     (Username), and password (Password). These details are used to connect 
      to the domain and execute commands.

   **Script Capabilities**
   This script includes various functions for assessing and attacking Active Directory. Below are the main capabilities        explained:

 **Temporarily Disabling Windows Defender:**
   To prevent the script from being blocked by Windows Defender, this function temporarily disables Defender.

**Kerberoasting Check:**
   - This function identifies user accounts with Service Principal Names (SPNs) that could be exploited in Kerberoasting attacks.
 
**ACL Misuse Check:**
This function examines Access Control Lists (ACLs) to detect unauthorized access or potential ACL misuse.

**Password Spraying Attack:**
This function simulates a Password Spraying attack. It uses a test password to attempt logins on user accounts.

**Golden Ticket Detection:**
This function reviews security event logs to detect signs of Golden Ticket attacks.

**Discovery of Inactive Accounts:**
This function identifies user accounts that have been inactive for more than 90 days.

**GPO Misuse Check:**
This function reviews Group Policy Objects (GPOs) to detect unauthorized access or potential GPO misuse.

**AdminSDHolder Misuse Check:**
This function examines AdminSDHolder to detect unauthorized access or potential misuse.

**AS-REP Roasting Check:**
This function identifies user accounts that do not require Kerberos 
Pre-Authentication and could be exploited in AS-REP Roasting attacks.

**Unconstrained Delegation Misuse Check:**
This function identifies computers with Unconstrained Delegation enabled.

**Constrained Delegation Misuse Check:**
This function identifies user accounts with Constrained Delegation enabled/


