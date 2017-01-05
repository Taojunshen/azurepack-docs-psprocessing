---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 916DAC30-3E8E-4797-A9D1-9B765A79353B
online version: http://go.microsoft.com/fwlink/?LinkID=321233
schema: 2.0.0
updated_at: 1/3/2017 9:53 PM
ms.date: 1/3/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesOwnerCertificate.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesOwnerCertificate.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/9b04ebf7a96dfac95b0cdb4f6ad2c39512dc39eb/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesOwnerCertificate.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-WebSitesOwnerCertificate

## SYNOPSIS
Gets information about website certificate ownership.

## SYNTAX

```
Get-WebSitesOwnerCertificate [[-OwnerName] <String>] [-ConnectionString <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-WebSitesOwnerCertificate** cmdlet returns information about website certificate ownership.
Used without any parameters, **Get-WebSitesOwnerCertificate** returns certificate ownership information for all your websites.
Alternatively, you can use the *OwnerName* parameter to limit the returned data to certificates owned by the specified user.

When using **Get-WebSitesOwnerCertificate** you might see owner names similar to this:

`Subscription01+DefaultWebSpace`

This is a calculated name consisting of a website subscription name (Subscription01) and a web space (DefaultWebSpace).
Calculated names are employed if a certificate is not explicitly assigned an owner name.
If you do not assign an owner then the system will derive a calculated name and automatically set the **OwnerName** property to the calculated name.

## EXAMPLES

### Example 1: Get owner certificates
```
PS C:\> Get-WebSitesOwnerCertificates -OwnerName "Subscription01+DefaultWebSpace"
```

This command returns information for all website certificates with the owner Subscription01+DefaultWebSpace.
In this case, that means certificates associated with the website subscription Subscription01 that were not explicitly assigned an owner.

## PARAMETERS

### -ConnectionString
Specifies a connection string for a hosting database.
Connection strings contain information about a data source and how to connect to it; this information includes such things as the server and database name, and the name and password of the user account making the connection.
For example:

`-ConnectionString "Server=tcp:contosodb.database.windows.net;Database=Personel;User ID=admin@contoso.com;Password=p@ssw0rd;Trusted_Connection=False;Encrypt=True;"`

If you do not specify this parameter **Get-WebSitesOwnerCertificate** automatically connects to the default instance of the hosting database.

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
Specifies the name of a certificate owner.
For example:

`-OwnerName "PattiF"`

When this parameter is used, **Get-WebSitesOwnerCertificate** returns information about certificates owned by that user.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

