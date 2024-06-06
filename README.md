# O365-InvestigationTooling

## Get-AllTenantRulesAndForms.ps1

This script is a modified version of [OfficeDev/O365-InvestigationTooling](https://github.com/OfficeDev/O365-InvestigationTooling/blob/master/Get-AllTenantRulesAndForms.ps1), tailored to support OAuth authentication.

### Setting Up an OAuth Application

1. Navigate to the Azure Portal and select "App registrations" -> "New registration" to create a new application.
2. Within the new application, navigate to "API permissions" -> "Add a permission" -> "Office 365 Exchange Online" -> "Application permissions" and select `full_access_as_app`. Then, click on "Add permissions".
3. Use a Global Admin account to grant admin consent for your organization.
4. Generate a client secret by navigating to "Certificates & secrets" -> "New client secret".

### Getting Started with Hunting

1. Replace `REPLACE_HERE` with the corresponding values obtained in the previous step.
2. Replace `mailboxes.txt` with the path to the mailbox list file.

```powershell
$tenantId = "REPLACE_HERE"
$clientId = "REPLACE_HERE"
$clientSecret = "REPLACE_HERE"
$scope = "https://outlook.office.com/.default"
$listMailboxes = "mailboxes.txt"
```

3. Open PowerShell and execute the script.
