---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 30EF4EBD-BE4A-4D2A-AD33-58A8499EDA54
online version: http://go.microsoft.com/fwlink/?LinkID=321237
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesSslBinding.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesSslBinding.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesSslBinding.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-WebSitesSslBinding

## SYNOPSIS
Gets information about website SSL bindings.

## SYNTAX

```
Get-WebSitesSslBinding [-ConnectionString <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-WebSitesSslBinding** cmdlet returns information about the Secure Sockets Layer (SSL) bindings assigned to your websites.
SSL provides a way for browsers to communicate with web servers over a secure, encrypted channel; this is done by using SSL certificates.
An SSL binding associates an SSL certificate with entities such as a website or TCP/IP port.

## EXAMPLES

### Example 1: Get SSL bindings for a front-end server
```
PS C:\> Get-WebSitesSslBinding -FrontEndName "FESERVER01"
```

This command returns information about the SSL bindings for the front-end server FESERVER01.

## PARAMETERS

### -ConnectionString
Specifies a connection string for a hosting database.
Connection strings contain information about a data source and how to connect to it; this information includes such things as the server and database name, and the name and password of the user account making the connection.
For example:

`-ConnectionString "Server=tcp:contosodb.database.windows.net;Database=Personel;User ID=admin@contoso.com;Password=p@ssw0rd;Trusted_Connection=False;Encrypt=True;"`

If you do not specify this parameter **Get-WebSitesSslBinding** automatically connects to the default instance of the hosting database.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-WebSitesSslBinding](xref:Websites/v1.0/New-WebSitesSslBinding.md)

[Remove-WebSitesSslBinding](xref:Websites/v1.0/Remove-WebSitesSslBinding.md)


