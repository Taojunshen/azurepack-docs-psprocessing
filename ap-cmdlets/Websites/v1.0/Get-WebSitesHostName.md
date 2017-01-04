---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: FDB60AA7-8FB2-4F96-9120-E544A73735AC
online version: http://go.microsoft.com/fwlink/?LinkID=321231
schema: 2.0.0
updated_at: 1/3/2017 9:53 PM
ms.date: 1/3/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesHostName.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesHostName.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/9b04ebf7a96dfac95b0cdb4f6ad2c39512dc39eb/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesHostName.md
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
Gets host names for a web site.

## SYNTAX

```
Get-WebSitesHostName [[-SiteName] <String>] [-WorkerName <String>] [-OwnerName <String>]
 [-ConnectionString <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-WebSitesHostName** cmdlet gets host names for a website.
Host names are the names that users type into their web browsers in order to access a site; for example, "www.contoso.com" or "support.contoso.net".
A single site can be assigned more than one host name.

Used without any parameters, **Get-WebSitesHostName** returns information about all your website host names.
However, you can also choose to return a subset of host names; for example, you can return all the host names for a specific site or all the host names associated with a specific owner.

## EXAMPLES

### Example 1: Get a host name for a site
```
PS C:\> Get-WebSitesHostName -SiteName "Site01"
```

This command gets the host names for the website named Site01.

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

When this parameter is used **Get-WebSitesHostName** returns host names for the websites owned by the specified user.

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

When this parameter is used **Get-WebSitesHostName** returns all the host names associated with the specified worker.

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

