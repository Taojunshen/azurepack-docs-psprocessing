---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 13AF7DD1-B4E5-4340-B4BF-9FB92456556F
online version: http://go.microsoft.com/fwlink/?LinkID=321249
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/New-WebSitesSubscription.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/New-WebSitesSubscription.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/New-WebSitesSubscription.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# New-WebSitesSubscription

## SYNOPSIS
Creates a website subscription.

## SYNTAX

```
New-WebSitesSubscription [-AdminId] <String> [-SubscriptionId] <String> [-DesignatedSKUs <String[]>]
 [-TotalAppServicePlansAllowed <Int32>] [-DedicatedAppServicePlansAllowed <Int32>]
 [-SharedAppServicePlansAllowed <Int32>] [-RemoteSettings <RemoteSettings>] [-SuppressRequestIdLine] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-WebSitesSubscription** cmdlet creates a website subscription.

## EXAMPLES

### Example 1: Create a website subscription
```
PS C:\> New-WebSitesSubscription -AdminId "User01" -SubscriptionId eede207d-d263-4212-ad32-fd29b5a1a6ce -Enabled
```

This command creates an enabled website subscription with the ID eede207d-d263-4212-ad32-fd29b5a1a6ce.
This subscription is owned by User01.

## PARAMETERS

### -AdminId
Specifies the owner of the subscription.
For example:

`-AdminId "PattiF"`

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
Specifies  the subscription ID.
For example:

`-SubscriptionId "eede207d-d263-4212-ad32-fd29b5a1a6ce"`

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

[Get-WebSitesSubscription](xref:Websites/v1.0/Get-WebSitesSubscription.md)

[Remove-WebSitesSubscription](xref:Websites/v1.0/Remove-WebSitesSubscription.md)


