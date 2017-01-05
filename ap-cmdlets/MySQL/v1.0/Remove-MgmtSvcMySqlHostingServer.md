---
external help file: Microsoft.WindowsAzure.MySql.PowerShell.dll-Help.xml
ms.assetid: 6F89F01C-9517-4086-A990-D87D5D198B82
online version: http://go.microsoft.com/fwlink/?LinkID=321825
schema: 2.0.0
updated_at: 1/4/2017 6:34 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/MySQL/v1.0/Remove-MgmtSvcMySqlHostingServer.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/MySQL/v1.0/Remove-MgmtSvcMySqlHostingServer.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/9ea7de3be93c45294ed2319f140bd6d622b027db/AzurePack-cmdlets/MySQL/v1.0/Remove-MgmtSvcMySqlHostingServer.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Remove-MgmtSvcMySqlHostingServer

## SYNOPSIS
Removes a MySQL hosting server from Windows Azure Pack.

## SYNTAX

```
Remove-MgmtSvcMySqlHostingServer [-HostingServerId] <String> [-AdminUri] <Uri> [-Token] <String>
 [-DisableCertificateValidation] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-MgmtSvcMySqlHostingServer** cmdlet removes a MySQL hosting server from Windows Azure Pack for Windows Server.

## EXAMPLES

### Example 1: Remove a MySql hosting server
```
PS C:\> Remove-MgmtSvcMySqlHostingServer -AdminUri "https://Computer01:30004" -Token $Token -HostingServerId "v48l25"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command removes the MySQL hosting server with the ID of v48l25.

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

If you specify this parameter, you can use self-signed certificates.

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

### -HostingServerId
Specifies the ID of a MySQL hosting server.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Token
Specifies an identity token.
To create a token, use the **Get-MgmtSvcToken** cmdlet.

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

[Add-MgmtSvcMySqlHostingServer](xref:MySQL/v1.0/Add-MgmtSvcMySqlHostingServer.md)

[Get-MgmtSvcMySqlHostingServer](xref:MySQL/v1.0/Get-MgmtSvcMySqlHostingServer.md)

[Set-MgmtSvcMySqlHostingServer](xref:MySQL/v1.0/Set-MgmtSvcMySqlHostingServer.md)

[Test-MgmtSvcMySqlHostingServer](xref:MySQL/v1.0/Test-MgmtSvcMySqlHostingServer.md)


