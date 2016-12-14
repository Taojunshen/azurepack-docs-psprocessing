---
external help file: Microsoft.WindowsAzure.MySql.PowerShell.dll-Help.xml
ms.assetid: BD108AB2-A278-4A81-A30E-F70DB3A094A9
online version: http://go.microsoft.com/fwlink/?LinkID=321821
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/MySQL/v1.0/Get-MgmtSvcMySqlHostingServer.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/MySQL/v1.0/Get-MgmtSvcMySqlHostingServer.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/MySQL/v1.0/Get-MgmtSvcMySqlHostingServer.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcMySqlHostingServer

## SYNOPSIS
Gets a MySQL hosting server.

## SYNTAX

```
Get-MgmtSvcMySqlHostingServer [[-Name] <String>] [-Skip <Int32>] [-First <Int32>] [-Descending]
 [-AdminUri] <Uri> [-Token] <String> [-DisableCertificateValidation] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcMySqlHostingServer** cmdlet gets a MySQL hosting server.
By default, all hosting servers are returned.
To get a specific hosting server, use the *Name* parameter.
You can also get a specified number of servers by using the *First* and *Skip* parameters.

## EXAMPLES

### Example 1: Get a specific MySQL hosting server by name
```
PS C:\>Get-MgmtSvcMySqlHostingServer -AdminUri "https://Computer01:30004" -Token $Token -Name "MySQLServer01.Contoso.com"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command gers the MySQL hosting server named MySQLServer01.Contoso.com.

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
Indicates that the returned servers are displayed in descending order.

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
Gets only the specified number of SQL hosting servers.

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

### -Name
Specifies the name of a SQL hosting server.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Skip
Skips the specified number of SQL hosting servers.

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

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-MgmtSvcMySqlHostingServer](xref:MySQL/v1.0/Add-MgmtSvcMySqlHostingServer.md)

[Set-MgmtSvcMySqlHostingServer](xref:MySQL/v1.0/Set-MgmtSvcMySqlHostingServer.md)

[Test-MgmtSvcMySqlHostingServer](xref:MySQL/v1.0/Test-MgmtSvcMySqlHostingServer.md)

[Remove-MgmtSvcMySqlHostingServer](xref:MySQL/v1.0/Remove-MgmtSvcMySqlHostingServer.md)

[Get-MgmtSvcMySqlHostingServerByGroup](xref:MySQL/v1.0/Get-MgmtSvcMySqlHostingServerByGroup.md)


