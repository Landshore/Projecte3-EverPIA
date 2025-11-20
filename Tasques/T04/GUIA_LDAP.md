# LDAP Configuration Guide

This guide walks through the complete process of configuring an LDAP server and client setup.

## Server Configuration

### 1. Check SLDAP Status
![SLDAP Status](./img/01.png)
*Verify the SLDAP service is running correctly*

### 2. Verify Directory Creation
![Directory Verification](Projecte3-EverPIA/Tasques/T04/img/02_directory_check.png)
*Confirm the LDAP directory structure has been created as intended*

### 3. Reconfigure SLDAP
![Dpkg Reconfigure Command](Projecte3-EverPIA/Tasques/T04/img/03_dpkg_reconfigure.png)
*Execute the reconfiguration command: `dpkg-reconfigure sldap`*

### 4. Configuration Wizard - Step 1
![Wizard No Option](Projecte3-EverPIA/Tasques/T04/img/04_wizard_no.png)
*Select "No" at the initial prompt*

### 5. Set Domain Name
![Domain Configuration](Projecte3-EverPIA/Tasques/T04/img/05_domain_innovatech28.png)
*Enter the domain: `innovatech28.test`*

### 6. Organization Name
![Organization Name](Projecte3-EverPIA/Tasques/T04/img/06_organization_name.png)
*Set organization name: `inovatechxx` (where xx is your list number)*

### 7. Administrator Password
![Admin Password](Projecte3-EverPIA/Tasques/T04/img/07_admin_password.png)
*Set the administrator password (usuari)*

### 8. Confirmation Prompts
![Confirmation Yes](Projecte3-EverPIA/Tasques/T04/img/08_confirm_yes.png)
*Confirm with "Yes" for both prompts*

### 9. Verify Directory Structure
![Final Directory Check](Projecte3-EverPIA/Tasques/T04/img/09_directory_verified.png)
*Confirm the directory has been properly created*

## Creating LDIF Files

### 10. Create First File
![Create LDIF File](Projecte3-EverPIA/Tasques/T04/img/10_create_file.png)
*Create the initial LDIF configuration file*

### 11. File Modifications
![LDIF Modifications](Projecte3-EverPIA/Tasques/T04/img/11_file_modifications.png)
*Add the necessary modifications to the LDIF file*

### 12. Add Elements Command
![LDAP Add Command](Projecte3-EverPIA/Tasques/T04/img/12_ldapadd_command.png)
*Use ldapadd command to insert elements into the directory*

### 13. Add Entry
![Add Entry Data](Projecte3-EverPIA/Tasques/T04/img/13_add_entry.png)
*Add the new entry to the LDAP directory*

### 14. Search Verification
![LDAP Search](Projecte3-EverPIA/Tasques/T04/img/14_ldapsearch_verify.png)
*Search the directory to verify the entry was added*

### 15. Attribute Search
![Attribute Search](Projecte3-EverPIA/Tasques/T04/img/15_search_attribute.png)
*Search for specific attributes in LDAP*

### 16. Execute Search Command
![Search Command Execution](Projecte3-EverPIA/Tasques/T04/img/16_search_command.png)
*Run the search command to retrieve data*

## LDAP Account Manager Setup

### 17. Install Account Manager
![Install Account Manager](Projecte3-EverPIA/Tasques/T04/img/17_install_account_manager.png)
*Install LDAP Account Manager package*

### 18. Open LAM Interface
![LAM Login](Projecte3-EverPIA/Tasques/T04/img/18_lam_interface.png)
*Access LDAP Account Manager web interface and edit server profiles*

### 19. Server Profile Password
![Server Profile Password](Projecte3-EverPIA/Tasques/T04/img/19_server_password_lam.png)
*Enter the LAM configuration password: `lam`*

### 20. Account Type Configuration
![Account Types Settings](Projecte3-EverPIA/Tasques/T04/img/20_account_types.png)
*Configure active account types (users/groups)*

## Creating Groups

### 21. Create Group
![Create New Group](Projecte3-EverPIA/Tasques/T04/img/21_create_group.png)
*Create a new group in LDAP*

### 22. Save and Return
![Save Group](Projecte3-EverPIA/Tasques/T04/img/22_save_return.png)
*Save the group configuration and return to main menu*

### 23. Tech Group
![Tech Group](Projecte3-EverPIA/Tasques/T04/img/23_tech_group.png)
*Configure the tech group*

### 24. Groups List
![Groups Listing](Projecte3-EverPIA/Tasques/T04/img/24_groups_list.png)
*View complete list of created groups*

## Creating Users

### 25. New Users Section
![New User Personal](Projecte3-EverPIA/Tasques/T04/img/25_new_user_personal.png)
*Navigate to "New Users" section and fill in personal credentials*

### 26. Unix Password Header
![Unix Password Header](Projecte3-EverPIA/Tasques/T04/img/26_password_unix_header.png)
*Near the password header, check the Unix header and save*

### 27. Unix Section Configuration
![Unix Section](Projecte3-EverPIA/Tasques/T04/img/27_unix_section_save.png)
*Configure and save Unix section settings*

### 28. Create Manager User
![Create Manager](Projecte3-EverPIA/Tasques/T04/img/28_create_manager.png)
*Create a manager user account*

### 29. Manager Unix Settings
![Manager Unix](Projecte3-EverPIA/Tasques/T04/img/29_manager_unix.png)
*Configure Unix settings for manager account*

### 30. Set Manager Password
![Manager Password](Projecte3-EverPIA/Tasques/T04/img/30_manager_password_save.png)
*Set password for manager and save*

### 31. Users List
![Users Listing](Projecte3-EverPIA/Tasques/T04/img/31_users_list.png)
*View complete list of created users*

## Client Configuration (Zorin OS)

### 32. Edit Hosts File
![Edit Hosts](Projecte3-EverPIA/Tasques/T04/img/32_edit_hosts_client.png)
*On the client (ZORIN), edit `/etc/hosts` file*

### 33. Verification Command
![Verify Connection](Projecte3-EverPIA/Tasques/T04/img/33_verify_command.png)
*Run command to verify connectivity*

### 34. Additional Command
![Additional Check](Projecte3-EverPIA/Tasques/T04/img/34_additional_command.png)
*Execute additional verification command*

### 35. Server Name Configuration
![Server Name](Projecte3-EverPIA/Tasques/T04/img/35_server_name_config.png)
*Fill in the missing parts with your server name*

### 36. Further Modifications
![More Modifications](Projecte3-EverPIA/Tasques/T04/img/36_more_modifications.png)
*Make additional configuration modifications*

### 37. Verification Check
![Verify Settings](Projecte3-EverPIA/Tasques/T04/img/37_verify_check.png)
*Verify all configuration settings*

### 38. Configure Client File
![Client File Config](Projecte3-EverPIA/Tasques/T04/img/38_client_file_config.png)
*Configure the client configuration file*

### 39. Remove use_autho Line
![Remove Line](Projecte3-EverPIA/Tasques/T04/img/39_remove_use_autho.png)
*Edit the file and remove the `use_autho` line*

### 40. Perfect Configuration
![Perfect Setup](Projecte3-EverPIA/Tasques/T04/img/40_perfect.png)
*Configuration completed successfully*

### 41. Restart Service
![Restart Service](Projecte3-EverPIA/Tasques/T04/img/41_restart_service.png)
*Restart the LDAP service*

### 42. Reinitialize Service
![Reinit Service](Projecte3-EverPIA/Tasques/T04/img/42_reinit_service.png)
*Reinitialize the service*

### 43. Check Clients
![Check Clients](Projecte3-EverPIA/Tasques/T04/img/43_check_clients.png)
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
