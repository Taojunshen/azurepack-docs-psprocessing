---
external help file: Microsoft.WindowsAzure.Admin.PowerShell.dll-Help.xml
ms.assetid: 8ED191AE-CDDF-4ED5-9A4F-253A07303BBD
online version: http://go.microsoft.com/fwlink/?LinkID=316338
schema: 2.0.0
updated_at: 1/4/2017 5:31 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Administration/v1.0/Get-MgmtSvcSubscription.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Administration/v1.0/Get-MgmtSvcSubscription.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/93767eba34ad89edb3696359a7595e41769e0346/AzurePack-cmdlets/Administration/v1.0/Get-MgmtSvcSubscription.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcSubscription

## SYNOPSIS
Gets a subscription.

## SYNTAX

### ByUserName (Default)
```
Get-MgmtSvcSubscription [[-UserName] <String>] [-Skip <Int32>] [-First <Int32>] [-SortProperty <String>]
 [-Descending] [-AdminUri] <Uri> [-Token] <String> [-DisableCertificateValidation] [<CommonParameters>]
```

### ByAddOnId
```
Get-MgmtSvcSubscription [[-UserName] <String>] [-AddOnId <String>] [-Skip <Int32>] [-First <Int32>]
 [-SortProperty <String>] [-Descending] [-AdminUri] <Uri> [-Token] <String> [-DisableCertificateValidation]
 [<CommonParameters>]
```

### ByPlanId
```
Get-MgmtSvcSubscription [[-UserName] <String>] [-PlanId <String>] [-Skip <Int32>] [-First <Int32>]
 [-SortProperty <String>] [-Descending] [-AdminUri] <Uri> [-Token] <String> [-DisableCertificateValidation]
 [<CommonParameters>]
```

### BySubscriptionId
```
Get-MgmtSvcSubscription [-SubscriptionId <Guid>] [-Skip <Int32>] [-First <Int32>] [-SortProperty <String>]
 [-Descending] [-AdminUri] <Uri> [-Token] <String> [-DisableCertificateValidation] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcSubscription** cmdlet gets a subscription.

## EXAMPLES

### Example 1: Get a subscription by user name
```
PS C:\> Get-MgmtSvcSubscription -UserName 'admin@Contoso.com' -AdminUri "https://Computer01:30004" -Token $Token -DisableCertificateValidation
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command gets the subscription for the user admin@Contoso.com.

## PARAMETERS

### -AddOnId
Specifies the ID of an add-on.

```yaml
Type: String
Parameter Sets: ByAddOnId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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
Indicates that the subscriptions are returned in descending order.

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
Gets only the specified number of objects.
Enter the number of objects to get.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PlanId
Specifies the ID for a plan.

```yaml
Type: String
Parameter Sets: ByPlanId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Skip
Ignores the specified number of objects and then gets the remaining objects.
Enter the number of objects to skip.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SortProperty
Specifies the property by which to sort results.

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

### -SubscriptionId
Specifies, as a GUID, the ID of a subscription.

```yaml
Type: Guid
Parameter Sets: BySubscriptionId
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

### -UserName
Specifies a user name.

```yaml
Type: String
Parameter Sets: ByUserName, ByAddOnId, ByPlanId
Aliases: 

Required: False
Position: 2
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

[Add-MgmtSvcSubscription](xref:Administration/v1.0/Add-MgmtSvcSubscription.md)

[Get-MgmtSvcSubscription](xref:Administration/v1.0/Get-MgmtSvcSubscription.md)

[Disable-MgmtSvcSubscription](xref:Administration/v1.0/Disable-MgmtSvcSubscription.md)

[Enable-MgmtSvcSubscription](xref:Administration/v1.0/Enable-MgmtSvcSubscription.md)

[Move-MgmtSvcSubscription](xref:Administration/v1.0/Move-MgmtSvcSubscription.md)

[Sync-MgmtSvcSubscription](xref:Administration/v1.0/Sync-MgmtSvcSubscription.md)

[Remove-MgmtSvcSubscription](xref:Administration/v1.0/Remove-MgmtSvcSubscription.md)


