---
external help file: Microsoft.WindowsAzure.SqlServer.PowerShell.dll-Help.xml
ms.assetid: B3C2EEFC-46F9-4352-A52C-249235E327CD
online version: http://go.microsoft.com/fwlink/?LinkID=321810
schema: 2.0.0
updated_at: 1/3/2017 10:42 PM
ms.date: 1/3/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/SQLServer/v1.0/Get-MgmtSvcSqlHostingServer.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/SQLServer/v1.0/Get-MgmtSvcSqlHostingServer.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/eb7bff1251dc2a22eafa120c35cbbc43529d3762/AzurePack-cmdlets/SQLServer/v1.0/Get-MgmtSvcSqlHostingServer.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcSqlHostingServer

## SYNOPSIS
Gets a SQL Server hosting server.

## SYNTAX

```
Get-MgmtSvcSqlHostingServer [[-Name] <String>] [-Skip <Int32>] [-First <Int32>] [-Descending] [-AdminUri] <Uri>
 [-Token] <String> [-DisableCertificateValidation] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcSqlHostingServer** cmdlet gets a SQL Server hosting server.
By default, all hosting servers are returned.
To get a specific hosting server, use the *Name* parameter.
You can also get a specified number of servers by using the *First* and *Skip* parameters.

## EXAMPLES

### Example 1: Get a specific SQL hosting server by name
```
PS C:\> Get-MgmtSvcSqlHostingServer -AdminUri "https://Computer01:30004" -Token $Token -Name "SQLServer01.Contoso.com"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command gets the SQL Server hosting server named SQLServer01.Contoso.com.

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

### -First
{{Fill First Description}}

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
Specifies the name of a SQL Server hosting server.

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
{{Fill Skip Description}}

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

### None

## OUTPUTS

### SqlHostingServer
This cmdlet emits a **SqlHostingServer** object.

## NOTES

## RELATED LINKS

[Add-MgmtSvcSqlHostingServer](xref:SQLServer/v1.0/Add-MgmtSvcSqlHostingServer.md)

[Set-MgmtSvcSqlHostingServer](xref:SQLServer/v1.0/Set-MgmtSvcSqlHostingServer.md)

[Test-MgmtSvcSqlHostingServer](xref:SQLServer/v1.0/Test-MgmtSvcSqlHostingServer.md)

[Remove-MgmtSvcSqlHostingServer](xref:SQLServer/v1.0/Remove-MgmtSvcSqlHostingServer.md)

[Get-MgmtSvcSqlHostingServerByGroup](xref:SQLServer/v1.0/Get-MgmtSvcSqlHostingServerByGroup.md)


