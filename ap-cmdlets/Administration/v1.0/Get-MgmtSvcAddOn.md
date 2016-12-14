---
external help file: Microsoft.WindowsAzure.Admin.PowerShell.dll-Help.xml
ms.assetid: 4AA7A31E-169D-4CA1-8851-53F3C0E7F00B
online version: http://go.microsoft.com/fwlink/?LinkID=316332
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Administration/v1.0/Get-MgmtSvcAddOn.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Administration/v1.0/Get-MgmtSvcAddOn.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Administration/v1.0/Get-MgmtSvcAddOn.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcAddOn

## SYNOPSIS
Gets service add-ons.

## SYNTAX

### ByDisplayName (Default)
```
Get-MgmtSvcAddOn [[-DisplayName] <String[]>] [-AdminUri] <Uri> [-Token] <String>
 [-DisableCertificateValidation] [<CommonParameters>]
```

### ByAddOnId
```
Get-MgmtSvcAddOn [-AddOnId <String>] [-AdminUri] <Uri> [-Token] <String> [-DisableCertificateValidation]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcAddOn** cmdlet gets service add-ons.
By default, all add-ons are returned.
To get a specific add-on, use the *DisplayName* parameter.

## EXAMPLES

### Example 1: Get all service add-ons
```
PS C:\>Get-MgmtSvcAddOn -AdminUri "https://Computer01:30004" -Token $Token
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command gets all add-ons.

### Example 2: Get a specific add-on by display name
```
PS C:\>Get-MgmtSvcAddOn -AdminUri "https://Computer01:30004" -Token $Token -DisplayName "Add-On 01"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command gets the add-on named Add-On 01.

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

### -DisableCertificateValidation
Disables certificate validation for the Windows Azure Pack installation.

If you specifiy this parameter, you can use self-signed certificates.

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

### -DisplayName
Specifies a display name for an add-on.

```yaml
Type: String[]
Parameter Sets: ByDisplayName
Aliases: 

Required: False
Position: 2
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-MgmtSvcAddOn](xref:Administration/v1.0/Add-MgmtSvcAddOn.md)

[Set-MgmtSvcAddOn](xref:Administration/v1.0/Set-MgmtSvcAddOn.md)

[Sync-MgmtSvcAddOn](xref:Administration/v1.0/Sync-MgmtSvcAddOn.md)

[Remove-MgmtSvcAddOn](xref:Administration/v1.0/Remove-MgmtSvcAddOn.md)

[Add-MgmtSvcAddOnService](xref:Administration/v1.0/Add-MgmtSvcAddOnService.md)

[Remove-MgmtSvcAddOnService](xref:Administration/v1.0/Remove-MgmtSvcAddOnService.md)


