---
updated_at: 12/14/2016 10:37 PM
ms.date: 12/14/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/AboutTopics/vlatest/about_WAP_Updating_Help.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/AboutTopics/vlatest/about_WAP_Updating_Help.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/3f345488b04d8f330b58e68d7d888239b31d75d3/AzurePack-cmdlets/AboutTopics/vlatest/about_WAP_Updating_Help.md
uid: AboutTopics/vlatest/about_WAP_Updating_Help.md
ms.topic: conceptual
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# About WAP Updating Help

## TOPIC 
## about_WAP_Updating_Help  
  
## SHORT DESCRIPTION  
    Provides information about how to install and update Windows Azure   
    Pack cmdlet help.  
  
## LONG DESCRIPTION  
    Windows PowerShell 3.0 introduced a new cmdlet that you can use to   
    install and update cmdlet help: Update-Help. Windows Azure Pack  
    uses this method to deliver to you the most up-to-date cmdlet help.  
  
    The Update-Help cmdlet downloads the newest cmdlet help files and   
    installs them on your computer. These help files are in the format   
    that the Get-Help cmdlet displays.   
  
  Updating Windows Azure Pack Cmdlet Help from the Internet  
  
      To install the Windows Azure Pack cmdlet help from the Internet,   
      open a Windows PowerShell command shell with the "Run as   
      Administrator" option. Then, type the following at the command   
      prompt:  
  
      Update-Help -Module MgmtSvcConfig  
  
      The Update-Help cmdlet checks the version of the help files on your   
      computer and, if you do not have any help files or do not have the  
      newest help files, it downloads the newest help files from the Internet  
      and installs them on your computer. This command updates the help  
      for the Windows Azure Pack cmdlets. To update the help for the  
      other Windows Azure Pack cmdlet modules, type one of the following:  
  
        Module             Name  
        ----------         ------------  
        Administrative     MgmtSvcAdmin  
        SQL Server         MgmtSvcSqlServer  
        MySQL              MgmtSvcMySql  
  
      To see the updated help topics, use the Get-Help cmdlet. You do not  
      need to restart the Windows PowerShell Command Shell to make the   
      changes effective.  
  
      For more information about updating help, type "Get-Help Update-Help".  
  
  Updating Windows Azure Pack Cmdlet Help from a File Share  
  
      If you run Windows Azure Pack cmdlets from computers that are not   
      connected to the Internet, you can use the Save-Help cmdlet to download  
      the newest Windows Azure Pack cmdlet help files from a computer that  
      has access to the Internet, and then save the files to a directory  
      that you specify.   
  
      To download and save the Windows Azure Pack cmdlet help files to a  
      file share, open a Windows PowerShell command shell and type the   
      following at the command prompt, changing the destination path to a  
      path suitable for your environment:   
  
      Save-Help -DestinationPath "\\Server01\FileShare01" -Module MgmtSvcConfig  
  
      The Save-Help cmdlet checks the version of any help files in the  
      destination directory and, if newer help files have been released,  
      it downloads the newest Windows Azure Pack cmdlet help files from the   
      Internet and saves them in the directory. The Save-Help cmdlet works  
      just like the Update-Help cmdlet, except that it saves the downloaded  
      cabinet (.cab) files in a directory, instead of extracting the help files  
      from the cabinet files and installing them on the computer.  
  
      To install the saved help files on a computer on which the Windows Azure  
      Pack modules are installed, open the Windows PowerShell command shell   
      with the "Run as Administrator" option. Then, use the Update-Help cmdlet  
      with the SourcePath parameter to specify the directory in which you saved  
      the help files. For example:  
  
      Update-Help -SourcePath "\\Server01\FileShare01" -Module MgmtSvcConfig  
  
      For more information about downloading and saving help, type "Get-Help   
      Save-Help".  
  
## SEE ALSO  
    Update-Help  
    Save-Help  
    Import-Module  
    Get-Module

