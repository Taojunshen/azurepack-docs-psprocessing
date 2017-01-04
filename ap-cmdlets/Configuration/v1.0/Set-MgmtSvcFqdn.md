---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: FF16E656-A9DD-4C52-AC13-C1D6DD4689E7
online version: http://go.microsoft.com/fwlink/?LinkID=320946
schema: 2.0.0
updated_at: 1/4/2017 4:35 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Set-MgmtSvcFqdn.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Set-MgmtSvcFqdn.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/676435fba79c23d58e9141828e751b939d2694b8/AzurePack-cmdlets/Configuration/v1.0/Set-MgmtSvcFqdn.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Set-MgmtSvcFqdn

## SYNOPSIS
Sets the FQDN for an Admin or Tenant site.

## SYNTAX

### ConnectionParameters (Default)
```
Set-MgmtSvcFqdn [-FullyQualifiedDomainName <String>] [-Port <Int32>] [-Scheme <String>] [-Namespace] <String[]>
 [-PortalConnectionString <String>] [-ManagementConnectionString <String>] [-Server <String>]
 [-UserName <String>] [-Password <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ConnectionString
```
Set-MgmtSvcFqdn [-FullyQualifiedDomainName <String>] [-Port <Int32>] [-Scheme <String>] [-Namespace] <String[]>
 [-PortalConnectionString <String>] [-ManagementConnectionString <String>] [-ConnectionString <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-MgmtSvcFqdn** cmdlet sets the Fully Qualified Domain Name (FQDN) for an Admin or Tenant site.

**Set-MgmtSvcFqdn** now includes the API services in Windows Azure Pack for Windows Server.
However, before these settings can be used, you must run **Set-MgmtSvcFqdn** on each of the API namespaces on a computer where they are installed locally.
After this is complete, you can run **Get-MgmtSvcFqdn** from any computer in the deployment as long as you provide valid connection parameters to the Windows Azure Pack database.
As with other namespaces, you must run **Set-MgmtSvcFqdn** from a computer where the target namespace is installed locally.

## EXAMPLES

### Example 1: Set the FQDN of a tenant site.
```
PS C:\> Set-MgmtSvcFqdn -Namespace "TenantSite" -FullyQualifiedDomainName "Computer01.Contoso.com" -Password "PassWord01!" -Port 30081 -Server "SQLComputer01" -UserName "PattiFuller"
```

This command sets the FQDN for a tenant site.

## PARAMETERS

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -FullyQualifiedDomainName
Specifies a Fully Qualified Domain Name (FQDN).

```yaml
Type: String
Parameter Sets: (All)
Aliases: FQDN

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

### -Port
Specifies a port number.

```yaml
Type: Int32
Parameter Sets: (All)
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

### -Scheme
{{Fill Scheme Description}}

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

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-MgmtSvcFqdn](xref:Configuration/v1.0/Get-MgmtSvcFqdn.md)


