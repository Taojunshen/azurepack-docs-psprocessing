---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: C562B403-9822-47FE-BDAB-6136F92677E2
online version: http://go.microsoft.com/fwlink/?LinkID=321238
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesSubscription.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesSubscription.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesSubscription.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-WebSitesSubscription

## SYNOPSIS
Gets information about website subscriptions.

## SYNTAX

```
Get-WebSitesSubscription [[-SubscriptionId] <String>] [-RemoteSettings <RemoteSettings>]
 [-SuppressRequestIdLine] [<CommonParameters>]
```

## DESCRIPTION
The **Get-WebSitesSubscription** cmdlet gets information about the subscriptions associated with your websites.
To return information for a single subscription, include the *SubscriptionId* parameter.

## EXAMPLES

### Example 1: Get a specific subscription
```
PS C:\> Get-WebSitesSubscription -SubscriptionId "eede207d-d263-4212-ad32-fd29b5a1a6ce"
```

This command returns information for the website subscription eede207d-d263-4212-ad32-fd29b5a1a6ce.

## PARAMETERS

### -RemoteSettings
{{Fill RemoteSettings Description}}

```yaml
Type: RemoteSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Specifies the ID of a subscription.
For example:

`-SubscriptionId "eede207d-d263-4212-ad32-fd29b5a1a6ce"`

When this parameter is used, information is only returned for the specified website subscription.

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

### -SuppressRequestIdLine
{{Fill SuppressRequestIdLine Description}}

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-WebSitesSubscription](xref:Websites/v1.0/New-WebSitesSubscription.md)

[Set-WebSitesSubscription](xref:Websites/v1.0/Set-WebSitesSubscription.md)

[Remove-WebSitesSubscription](xref:Websites/v1.0/Remove-WebSitesSubscription.md)


