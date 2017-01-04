---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 313837D1-23EE-41D8-A9C6-F7A71CD9DD30
online version: http://go.microsoft.com/fwlink/?LinkID=320945
schema: 2.0.0
updated_at: 1/4/2017 4:35 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcFqdn.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcFqdn.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/676435fba79c23d58e9141828e751b939d2694b8/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcFqdn.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcFqdn

## SYNOPSIS
Gets the FQDN for an Admin or Tenant site.

## SYNTAX

### ConnectionParameters (Default)
```
Get-MgmtSvcFqdn [-Namespace] <String[]> [-PortalConnectionString <String>]
 [-ManagementConnectionString <String>] [-Server <String>] [-UserName <String>] [-Password <String>]
 [<CommonParameters>]
```

### ConnectionString
```
Get-MgmtSvcFqdn [-Namespace] <String[]> [-PortalConnectionString <String>]
 [-ManagementConnectionString <String>] [-ConnectionString <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcFqdn** cmdlet gets the Fully Qualified Domain Name (FQDN) for an Admin or Tenant site.

**Get-MgmtSvcFqdn** now includes the API services in Windows Azure Pack for Windows Server.
However, before these settings can be used, you must run **Set-MgmtSvcFqdn** on each of the API namespaces on a computer where they are installed locally.
After this is complete, you can run **Get-MgmtSvcFqdn** from any computer in the deployment as long as you provide valid connection parameters to the Windows Azure Pack database.
As with other namespaces, you must run **Set-MgmtSvcFqdn** from a computer where the target namespace is installed locally.

## EXAMPLES

### Example 1: Get an FQDN for a Tenant Site
```
PS C:\> Get-MgmtSvcFqdn -Namespace TenantSite -Password "PassWord01!" -Server "Computer01" -UserName "PattiFuller"
```

This command gets the FQDN for a tenant site.

## PARAMETERS

### -ConnectionString
Specifies an SQL connection string.

```yaml
Type: String
Parameter Sets: ConnectionString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementConnectionString
{{Fill ManagementConnectionString Description}}

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Specifies an array of namespaces.
Valid values are: AdminSite, TenantSite.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Password
Specifies a password.

```yaml
Type: String
Parameter Sets: ConnectionParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PortalConnectionString
{{Fill PortalConnectionString Description}}

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Server
Specifies the name of the computer on which the SQL database resides.

```yaml
Type: String
Parameter Sets: ConnectionParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies the name of a user account.

```yaml
Type: String
Parameter Sets: ConnectionParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-MgmtSvcFqdn](xref:Configuration/v1.0/Set-MgmtSvcFqdn.md)


