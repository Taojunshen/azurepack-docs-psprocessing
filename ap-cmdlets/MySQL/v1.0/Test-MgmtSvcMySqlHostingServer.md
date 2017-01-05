---
external help file: Microsoft.WindowsAzure.MySql.PowerShell.dll-Help.xml
ms.assetid: 970950D0-3CC2-47C8-A0AE-E7881B4BEB35
online version: http://go.microsoft.com/fwlink/?LinkID=321828
schema: 2.0.0
updated_at: 1/4/2017 6:34 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/MySQL/v1.0/Test-MgmtSvcMySqlHostingServer.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/MySQL/v1.0/Test-MgmtSvcMySqlHostingServer.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/9ea7de3be93c45294ed2319f140bd6d622b027db/AzurePack-cmdlets/MySQL/v1.0/Test-MgmtSvcMySqlHostingServer.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Test-MgmtSvcMySqlHostingServer

## SYNOPSIS
Verifies a MySQL hosting server.

## SYNTAX

### ByProperties (Default)
```
Test-MgmtSvcMySqlHostingServer [-ServerGroupId] <String> [-Name] <String> [-TotalSpaceMB] <Int32>
 [-User] <PSCredential> [-AdminUri] <Uri> [-Token] <String> [-DisableCertificateValidation]
 [<CommonParameters>]
```

### ByObject
```
Test-MgmtSvcMySqlHostingServer [-ServerGroupId] <String> [[-HostingServer] <MySqlHostingServer>]
 [-AdminUri] <Uri> [-Token] <String> [-DisableCertificateValidation] [<CommonParameters>]
```

## DESCRIPTION
The **Test-MgmtSvcMySqlHostingServer** cmdlet verifies a MySQL hosting server.

## EXAMPLES

### Example 1: Verify a MySQL hosting server
```
PS C:\> $Creds = Get-Credential
PS C:\> Test-MgmtSvcMySqlHostingServer -AdminUri "https://Computer01:30004" -Token $Token -Name "MySQLServer01.Contoso.com" -TotalSpaceMB 2048 -User $Creds -ServerGroupId "foe629"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

The first command prompts the user for credentials and stores the provided user name and password in the $Credential variable.

The second command tests the MySQL hosting server named MySQLServer01.Contoso.com, using the credentials provided in the first command.

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
Specifies the name of a MySQL server.

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
To create a PSCredential object, use the **Get-Credential** cmdlet.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-MgmtSvcMySqlHostingServer](xref:MySQL/v1.0/Add-MgmtSvcMySqlHostingServer.md)

[Get-MgmtSvcMySqlHostingServer](xref:MySQL/v1.0/Get-MgmtSvcMySqlHostingServer.md)

[Set-MgmtSvcMySqlHostingServer](xref:MySQL/v1.0/Set-MgmtSvcMySqlHostingServer.md)

[Remove-MgmtSvcMySqlHostingServer](xref:MySQL/v1.0/Remove-MgmtSvcMySqlHostingServer.md)


