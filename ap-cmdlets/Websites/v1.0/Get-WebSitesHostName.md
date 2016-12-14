---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: FDB60AA7-8FB2-4F96-9120-E544A73735AC
online version: http://go.microsoft.com/fwlink/?LinkID=321231
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesHostName.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesHostName.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesHostName.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-WebSitesHostName

## SYNOPSIS
Gets hostnames for a web site.

## SYNTAX

```
Get-WebSitesHostName [[-SiteName] <String>] [-WorkerName <String>] [-OwnerName <String>]
 [-ConnectionString <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-WebSitesHostName** cmdlet gets hostnames for a website.
Hostnames are the names that users type into their web browsers in order to access a site; for example, "www.contoso.com" or "support.contoso.net".
A single site can be assigned more than one hostname.

Used without any parameters, **Get-WebSitesHostName** returns information about all your website hostnames.
However, you can also choose to return a subset of hostnames; for example, you can return all the hostnames for a specific site or all the hostnames associated with a specific owner.

## EXAMPLES

### Example 1: Get t hostname for a site
```
PS C:\> Get-WebSitesHostName -SiteName "Site01"
```

This command gets the hostnames for the website named Site01.

## PARAMETERS

### -ConnectionString
Specifies a connection string for a hosting database.
Connection strings contain information about a data source and how to connect to it; this information includes such things as the server and database name, and the name and password of the user account making the connection.
For example:

`-ConnectionString "Server=tcp:contosodb.database.windows.net;Database=Personel;User ID=admin@contoso.com;Password=p@ssw0rd;Trusted_Connection=False;Encrypt=True;"`

If you do not specify this parameter **Get-WebSitesHostName** automatically connects to the default instance of the hosting database.

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

### -OwnerName
Specifies the name of a website owner. 
For example:

`-OwnerName "PattiF"`

When this parameter is used **Get-WebSitesHostName** returns hostnames for the websites owned by the specified user.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SiteName
Specifies the name of the site from which the host names are retrieved.
For example:

`-Site "ContosoInternal"`

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WorkerName
Specifies the name of a website worker (workers perform background processing for websites).
For example:

`-WorkerName "ContosoWorker1"`

When this parameter is used Get-WebSitesHostName returns all the hostnames associated with the specified worker.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

[New-WebSitesHostName](xref:Websites/v1.0/New-WebSitesHostName.md)

[Remove-WebSitesHostName](xref:Websites/v1.0/Remove-WebSitesHostName.md)


