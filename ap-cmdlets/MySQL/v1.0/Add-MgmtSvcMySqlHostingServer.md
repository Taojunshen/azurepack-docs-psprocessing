---
external help file: Microsoft.WindowsAzure.MySql.PowerShell.dll-Help.xml
ms.assetid: A4ABE179-F145-448C-9B98-46C1E2214236
online version: http://go.microsoft.com/fwlink/?LinkID=321818
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/MySQL/v1.0/Add-MgmtSvcMySqlHostingServer.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/MySQL/v1.0/Add-MgmtSvcMySqlHostingServer.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/MySQL/v1.0/Add-MgmtSvcMySqlHostingServer.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Add-MgmtSvcMySqlHostingServer

## SYNOPSIS
Adds a MySQL hosting server to Windows Azure Pack.

## SYNTAX

### ByProperties (Default)
```
Add-MgmtSvcMySqlHostingServer [-ServerGroupId] <String> [-Name] <String> [-TotalSpaceMB] <Int32>
 [-User] <PSCredential> [-AdminUri] <Uri> [-Token] <String> [-DisableCertificateValidation] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByObject
```
Add-MgmtSvcMySqlHostingServer [-ServerGroupId] <String> [[-HostingServer] <MySqlHostingServer>]
 [-AdminUri] <Uri> [-Token] <String> [-DisableCertificateValidation] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The Add-MgmtSvcMySqlHostingServer cmdlet adds a MySQL hosting server to Windows Azure Pack for Windows Server.

## EXAMPLES

### Example 1: Add a MySQL hosting server
```
PS C:\>$Creds = Get-Credential
PS C:\> Add-MgmtSvcMySqlHostingServer -AdminUri "https://Computer01:30004" -Token $Token -Name "MySQLServer01.Contoso.com" -TotalSpaceMB 2048 -ServerGroupId "foe629" -User $Creds
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

The first command prompts the user for credentials which are stored in the $Creds variable.

The second command uses the credentials provided in the first command to add the MySQL server named MySQLServer01.Contoso.com to the MySQL server group with the ID of foe629.

## PARAMETERS

### -AdminUri
Specifies the URI of the Windows Azure Pack administrator API.
Use the following format: https://\<computer\>:\<port\>, where \<computer\> is the computer on which the administrator API is installed.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -DisableCertificateValidation
Disables certificate validation for the Windows Azure Pack installation.

If you specifiy this parameter, you can use self-signed certificates.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostingServer
Specifies a MySQL hosting server object.

```yaml
Type: MySqlHostingServer
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a SQL server.

If you want your application databases to be publically accessible, ensure that you use a publically-accessible IP address or FQDN.

```yaml
Type: String
Parameter Sets: ByProperties
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerGroupId
Specifies the ID for a SQL server group.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Token
Specifies an identity token.
To create a token, use the Get-MgmtSvcToken cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TotalSpaceMB
Specifies the size, in megabytes (MB) of the hosting server.

```yaml
Type: Int32
Parameter Sets: ByProperties
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -User
Specifies a user account and password as a PSCredential object.
To create a PSCredential object, use the Get-Credential cmdlet.

```yaml
Type: PSCredential
Parameter Sets: ByProperties
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
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

[Get-MgmtSvcMySqlHostingServer](xref:MySQL/v1.0/Get-MgmtSvcMySqlHostingServer.md)

[Set-MgmtSvcMySqlHostingServer](xref:MySQL/v1.0/Set-MgmtSvcMySqlHostingServer.md)

[Test-MgmtSvcMySqlHostingServer](xref:MySQL/v1.0/Test-MgmtSvcMySqlHostingServer.md)

[Remove-MgmtSvcMySqlHostingServer](xref:MySQL/v1.0/Remove-MgmtSvcMySqlHostingServer.md)


