---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 25C25AE3-DC86-44D1-8E97-D5D3E3B30AAF
online version: http://go.microsoft.com/fwlink/?LinkID=321272
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Set-WebSitesSubscription.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Set-WebSitesSubscription.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/Set-WebSitesSubscription.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Set-WebSitesSubscription

## SYNOPSIS
Sets property values for a website subscription.

## SYNTAX

```
Set-WebSitesSubscription [-SubscriptionId] <String> [-Name <String>] [-Active <Boolean>] [-Quota <String>]
 [-DesignatedSKUs <String[]>] [-TotalAppServicePlansAllowed <Int32>] [-DedicatedAppServicePlansAllowed <Int32>]
 [-SharedAppServicePlansAllowed <Int32>] [-RemoteSettings <RemoteSettings>] [-SuppressRequestIdLine] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-WebSitesSubscription** cmdlet set web site subscription property values.

## EXAMPLES

### Example 1: Suspend a subscription
```
PS C:\> Set-WebSitesSubscription -SubscriptionId "eede207d-d263-4212-ad32-fd29b5a1a6ce"-Active $False
```

This command suspends the subscription Subscription01.
This is done by setting the Active property to False ($False).

## PARAMETERS

### -Active
Indicates whether the subscription is active.
Set this value to True ($True) to make this an active subscription, or set the value to False ($False) to make the subscription inactive.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -DedicatedAppServicePlansAllowed
{{Fill DedicatedAppServicePlansAllowed Description}}

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

### -DesignatedSKUs
{{Fill DesignatedSKUs Description}}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Specifies a name for the subscription.
For example:

`-Name "ContosoInternalSubscription"`

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

### -Quota
Specifies a quota for the subscription.
Valid values are:

- CpuTime
- Memory
- BytesReceived
- BytesSent
- NumberOfInstances
- NumberOfSites
- WebsiteStorageSize
- CustomDomainSupport
- WebSockets
- ConcurrentAccessLimit
- Worker64BitsSupport
- SslSupport
- SiteCpuLimit
- SiteMemory
- SiteMemoryWorkingSet
- SiteIdleTimeout

For example:

`-Quota "BytesSent"`

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

### -SharedAppServicePlansAllowed
{{Fill SharedAppServicePlansAllowed Description}}

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

### -SubscriptionId
Specifies the ID of the subscription being modified.
For example:

`-SubscriptionId "eede207d-d263-4212-ad32-fd29b5a1a6ce"`

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

### -TotalAppServicePlansAllowed
{{Fill TotalAppServicePlansAllowed Description}}

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

[New-WebSitesSubscription](xref:Websites/v1.0/New-WebSitesSubscription.md)

[Get-WebSitesSubscription](xref:Websites/v1.0/Get-WebSitesSubscription.md)

[Remove-WebSitesSubscription](xref:Websites/v1.0/Remove-WebSitesSubscription.md)


