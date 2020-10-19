Easily obtain AccessToken(Bearer) from an existing Az/AzureRM PowerShell session
================================================================================

            
The problematic

What you'll see on the Internet as a solution for this is creating an Application in your AAD with a ServicePrincipal, then use the ServicePrincipal credentials to obtain the AccessToken. Then problem is that this is very dependant on what RBAC permissions
 you give to your application, this is not what I really want, manage another entity permission just to get AccessTokens.


You also have a version that'll use the well-known PowerShell clientId & redirectUrl, preventing you from creating a new app in Azure AD but you'll still need to provide a username & password or clientId/password


 

Updates

2019-01-14 - Added support for both AzureRM & Az modules


 

What is proposed

You'll find in this function an easy way to extract the information required for you to build a Bearer token and all this from YOUR credentials within an authenticated PowerShell Azure session. You can then use this token to talk to Azure Resource Manager
 REST API.


 

An easier way to obtain your AccessToken

Include the code from included profile1.ps1 into your personnal PowerShell profile to make it easier to call the helper function when needed


Usually your personal PowerShell Profile should be at the following location: 
$Home\[My ]Documents\WindowsPowerShell\Profile.ps1


 

Overview

This is an overview of the code of the cmdlet *Get-AzCachedAccessToken*

 
Usage
 
Requirements

Tested with Az.Accounts Version 1.x


Tested with AzureRM.Profile Version 2.x to 5.x


 


More information here:


https://www.codeisahighway.com/how-to-easily-and-silently-obtain-accesstoken-bearer-from-an-existing-azure-powershell-session/


        
    
Note: TechNet gallery is retiring! This script was migrated from TechNet script center to GitHub by Microsoft Azure Automation product group.
