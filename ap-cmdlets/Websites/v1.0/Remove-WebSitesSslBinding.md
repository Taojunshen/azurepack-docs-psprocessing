---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 7F0AE95A-C070-47E1-ACCA-AA2F0D636201
online version: http://go.microsoft.com/fwlink/?LinkID=321259
schema: 2.0.0
updated_at: 1/3/2017 9:53 PM
ms.date: 1/3/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Remove-WebSitesSslBinding.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Remove-WebSitesSslBinding.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/9b04ebf7a96dfac95b0cdb4f6ad2c39512dc39eb/AzurePack-cmdlets/Websites/v1.0/Remove-WebSitesSslBinding.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Remove-WebSitesSslBinding

## SYNOPSIS
Removes an SSL binding.

## SYNTAX

```
Remove-WebSitesSslBinding [-ConnectionString <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-WebSitesSslBinding** cmdlet removes a Secure Sockets Layer (SSL) binding.
SSL provides a way for browsers to communicate with web servers over a secure, encrypted channel; this is done by using SSL certificates.
An SSL binding associates an SSL certificate with entities such as a website or TCP/IP port.

## EXAMPLES

### Example 1: Remove an SSL binding
```
PS C:\> Remove-WebSitesSslBinding -FrontEndName "FESERVER01" -IPAddress "FD4A:29CD:184F:3A2C:D07A:489A:1EC4:E2CD" -Port 8443
```

This command removes an SSL binding from the front-end server named FESERVER01.
The binding has the IP address FD4A:29CD:184F:3A2C:D07A:489A:1EC4:E2CD and is assigned to port 8443.

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
Specifies a connection string for a hosting database.
Connection strings contain information about a data source and how to connect to it; this information includes such things as the server and database name, and the name and password of the user account making the connection.
For example:

`-ConnectionString "Server=tcp:contosodb.database.windows.net;Database=Personel;User ID=admin@contoso.com;Password=p@ssw0rd;Trusted_Connection=False;Encrypt=True;"`

If you do not specify this parameter, **Remove-WebSitesSslBinding** uses the default instance of the hosting database.

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

[New-WebSitesSslBinding](xref:Websites/v1.0/New-WebSitesSslBinding.md)

[Get-WebSitesSslBinding](xref:Websites/v1.0/Get-WebSitesSslBinding.md)


