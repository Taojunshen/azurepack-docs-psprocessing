---
external help file: Microsoft.WindowsAzure.SqlServer.PowerShell.dll-Help.xml
ms.assetid: F6BA3574-BF29-412A-BF15-48DA8EB92EE9
online version: http://go.microsoft.com/fwlink/?LinkID=321811
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/SQLServer/v1.0/Get-MgmtSvcSqlHostingServerByGroup.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/SQLServer/v1.0/Get-MgmtSvcSqlHostingServerByGroup.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/SQLServer/v1.0/Get-MgmtSvcSqlHostingServerByGroup.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcSqlHostingServerByGroup

## SYNOPSIS
Gets hosting servers by SQL Server group.

## SYNTAX

```
Get-MgmtSvcSqlHostingServerByGroup [-ServerGroupId] <String> [[-Name] <String[]>] [-AdminUri] <Uri>
 [-Token] <String> [-DisableCertificateValidation] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcSqlHostingServerByGroup** gets SQL Server hosting servers by SQL Server group.
By default, all SQL Server hosting servers for a group are returned.
To get a specific hosting server, use the *Name* parameter.

## EXAMPLES

### Example 1: Get all SQL hosting servers for a group
```
PS C:\>Get-MgmtSvcSqlHostingServerByGroup -AdminUri "https://Computer01:30004" -Token $Token -ServerGroupId "g5sho0"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command gets all SQL Server hosting servers in the group with the ID of g5sho0.

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

### -Name
Specifies an array of SQL Server hosting server names.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerGroupId
Specifies the ID of a SQL Server group.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### SqlHostingServerList
This cmdlet emits a **SqlHostingServerList** object.

## NOTES

## RELATED LINKS

[Get-MgmtSvcSqlHostingServer](xref:SQLServer/v1.0/Get-MgmtSvcSqlHostingServer.md)


