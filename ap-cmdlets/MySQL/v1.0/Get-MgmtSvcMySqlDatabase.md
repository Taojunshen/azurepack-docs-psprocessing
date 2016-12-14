---
external help file: Microsoft.WindowsAzure.MySql.PowerShell.dll-Help.xml
ms.assetid: A0AFE331-B416-42B8-ADE7-14C7E0A08292
online version: http://go.microsoft.com/fwlink/?LinkID=321820
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/MySQL/v1.0/Get-MgmtSvcMySqlDatabase.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/MySQL/v1.0/Get-MgmtSvcMySqlDatabase.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/MySQL/v1.0/Get-MgmtSvcMySqlDatabase.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcMySqlDatabase

## SYNOPSIS
Gets a MySQL database.

## SYNTAX

```
Get-MgmtSvcMySqlDatabase [-HostingServerId] <String> [[-Name] <String>] [-Skip <Int32>] [-First <Int32>]
 [-Descending] [-AdminUri] <Uri> [-Token] <String> [-DisableCertificateValidation] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcMySqlDatabase** cmdlet gets MySQL databases.
By default, all MySQL databases for a hosting server are returned.
To get a specific MySQL database, use the *Name* parameter.

## EXAMPLES

### Example 1: Get a MySQL database by name
```
PS C:\>Get-MgmtSvcMySqlDatabase -AdminUri "https://Computer01:30004" -Token $Token -HostingServerId "v48l25" -Name "MYSQLDB01"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command gets the database named MYSQLDB01 on the hosting server with the ID v48l25.

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

### -Descending
Indicates that the returned databases are displayed in descending order.

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

### -First
Gets only the specified number of MySQL databases.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Name
Specifies the name of a MySQL hosting server.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Skip
Skips the specified number of MySQL databases.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-MgmtSvcMySqlHostingServer](xref:MySQL/v1.0/Get-MgmtSvcMySqlHostingServer.md)


