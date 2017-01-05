---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 9A0F3F42-37BA-496D-9558-884C6DCC2DB6
online version: http://go.microsoft.com/fwlink/?LinkID=321244
schema: 2.0.0
updated_at: 1/3/2017 9:53 PM
ms.date: 1/3/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/New-WebSitesHostName.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/New-WebSitesHostName.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/9b04ebf7a96dfac95b0cdb4f6ad2c39512dc39eb/AzurePack-cmdlets/Websites/v1.0/New-WebSitesHostName.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# New-WebSitesHostName

## SYNOPSIS
Adds a host name to a website.

## SYNTAX

```
New-WebSitesHostName [-SiteName] <String> [-Name] <String> [-ConnectionString <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-WebSitesHostName** cmdlet adds a host name to website.

## EXAMPLES

### Example 1: Add a host name to a site
```
PS C:\> New-WebSitesHostName -SiteName "Site01" -Name "support.contoso.com"
```

This command adds the host name support.contoso.com to the site Site01.

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

If you do not specify this parameter **New-WebSitesHostName** uses the default instance of the hosting database.

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

### -Name
Specifies the host name being added to the website.
For example:

`-Name "www.contoso.com"`

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

### -SiteName
Specifies the name of the website that the host associated with.
For example:

`-SiteName "ContosoInternal"`

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

[Get-WebSitesHostName](xref:Websites/v1.0/Get-WebSitesHostName.md)

[Remove-WebSitesHostName](xref:Websites/v1.0/Remove-WebSitesHostName.md)


