# LDAP Configuration Guide

This guide walks through the complete process of configuring an LDAP server and client setup.

## Server Configuration

### 1. Check SLDAP Status
![SLDAP Status](./img/01.png)
*Verify the SLDAP service is running correctly*

### 2. Verify Directory Creation
![Directory Verification](./img/02.png)
*Confirm the LDAP directory structure has been created as intended*

### 3. Reconfigure SLDAP
![Dpkg Reconfigure Command](./img/03.png)
*Execute the reconfiguration command: `dpkg-reconfigure sldap`*

### 4. Configuration Wizard - Step 1
![Wizard No Option](./img/04.png)
*Select "No" at the initial prompt*

### 5. Set Domain Name
![Domain Configuration](./img/05.png)
*Enter the domain: `innovatech28.test`*

### 6. Organization Name
![Organization Name](./img/06.png)
*Set organization name: `inovatechxx` (where xx is your list number)*

### 7. Administrator Password
![Admin Password](./img/07.png)
*Set the administrator password (usuari)*

### 8. Confirmation Prompts
![Confirmation Yes](./img/08.png)
*Confirm with "Yes" for both prompts*

### 9. Verify Directory Structure
![Final Directory Check](./img/09.png)
*Confirm the directory has been properly created*

## Creating LDIF Files

### 10. Create First File
![Create LDIF File](./img/10.png)
*Create the initial LDIF configuration file*

### 11. File Modifications
![LDIF Modifications](./img/11.png)
*Add the necessary modifications to the LDIF file*

### 12. Add Elements Command
![LDAP Add Command](./img/12.png)
*Use ldapadd command to insert elements into the directory*

### 13. Add Entry
![Add Entry Data](./img/13.png)
*Add the new entry to the LDAP directory*

### 14. Search Verification
![LDAP Search](./img/14.png)
*Search the directory to verify the entry was added*

### 15. Attribute Search
![Attribute Search](./img/15.png)
*Search for specific attributes in LDAP*

### 16. Execute Search Command
![Search Command Execution](./img/16.png)
*Run the search command to retrieve data*

## LDAP Account Manager Setup

### 17. Install Account Manager
![Install Account Manager](./img/17.png)
*Install LDAP Account Manager package*

### 18. Open LAM Interface
![LAM Login](./img/18.png)
*Access LDAP Account Manager web interface and edit server profiles*

### 19. Server Profile Password
![Server Profile Password](./img/19.png)
*Enter the LAM configuration password: `lam`*

### 20. Account Type Configuration
![Account Types Settings](./img/20.png)
*Configure active account types (users/groups)*

## Creating Groups

### 21. Create Group
![Create New Group](./img/21.png)
*Create a new group in LDAP*

### 22. Save and Return
![Save Group](./img/22.png)
*Save the group configuration and return to main menu*

### 23. Tech Group
![Tech Group](./img/23.png)
*Configure the tech group*

### 24. Groups List
![Groups Listing](./img/24.png)
*View complete list of created groups*

## Creating Users

### 25. New Users Section
![New User Personal](./img/25.png)
*Navigate to "New Users" section and fill in personal credentials*

### 26. Unix Password Header
![Unix Password Header](./img/26.png)
*Near the password header, check the Unix header and save*

### 27. Unix Section Configuration
![Unix Section](./img/27.png)
*Configure and save Unix section settings*

### 28. Create Manager User
![Create Manager](./img/28.png)
*Create a manager user account*

### 29. Manager Unix Settings
![Manager Unix](./img/29.png)
*Configure Unix settings for manager account*

### 30. Set Manager Password
![Manager Password](./img/30.png)
*Set password for manager and save*

### 31. Users List
![Users Listing](./img/31.png)
*View complete list of created users*

## Client Configuration (Zorin OS)

### 32. Edit Hosts File
![Edit Hosts](./img/32.png)
*On the client (ZORIN), edit `/etc/hosts` file*

### 33. Verification Command
![Verify Connection](./img/33.png)
*Run command to verify connectivity*

### 34. Additional Command
![Additional Check](./img/34.png)
*Execute additional verification command*

### 35. Server Name Configuration
![Server Name](./img/35.png)
*Fill in the missing parts with your server name*

### 36. Further Modifications
![More Modifications](./img/36.png)
*Make additional configuration modifications*

### 37. Verification Check
![Verify Settings](./img/37.png)
*Verify all configuration settings*

### 38. Configure Client File
![Client File Config](./img/38.png)
*Configure the client configuration file*

### 39. Remove use_autho Line
![Remove Line](./img/39.png)
*Edit the file and remove the `use_autho` line*

### 40. Perfect Configuration
![Perfect Setup](./img/40.png)
*Configuration completed successfully*

### 41. Restart Service
![Restart Service](./img/41.png)
*Restart the LDAP service*

### 42. Reinitialize Service
![Reinit Service](./img/42.png)
*Reinitialize the service*

### 43. Check Clients
![Check Clients](./img/43.png)
*Verify that clients are properly connected*

## Summary

This guide covers:
- LDAP server installation and configuration
- Directory structure creation
- LDIF file management
- LDAP Account Manager setup
- Group and user creation
- Client configuration on Zorin OS
- Service verification and troubleshooting

All configuration files and commands are executed with appropriate permissions and verified at each step.
