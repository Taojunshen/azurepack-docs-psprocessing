---
external help file: Microsoft.WindowsAzure.Admin.PowerShell.dll-Help.xml
ms.assetid: AFC2DA88-8EE1-4AA7-939D-E19C1856C07C
online version: http://go.microsoft.com/fwlink/?LinkID=316337
schema: 2.0.0
updated_at: 1/4/2017 5:31 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Administration/v1.0/Get-MgmtSvcResourceProvider.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Administration/v1.0/Get-MgmtSvcResourceProvider.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/93767eba34ad89edb3696359a7595e41769e0346/AzurePack-cmdlets/Administration/v1.0/Get-MgmtSvcResourceProvider.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcResourceProvider

## SYNOPSIS
Gets a resource provider from the management store database.

## SYNTAX

```
Get-MgmtSvcResourceProvider [[-Name] <String[]>] [-IncludeSystemResourceProviders] [-AdminUri] <Uri>
 [-Token] <String> [-DisableCertificateValidation] [<CommonParameters>]
```

## DESCRIPTION
The **Get-ResourceProvider** cmdlet gets a resource provider entry from a management store database.
By default, this cmdlet returns all resource providers.
To get a specific resource provider, use the *Name* parameter.

You can run this cmdlet from any machine in the deployment.

## EXAMPLES

### Example 1: Get all resource providers
```
PS C:\> Get-MgmtSvcResourceProvider -AdminUri "https://Computer01:30004" -Token $Token
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

### Example 2: Get a specific resource provider by its name
```
PS C:\> Get-MgmtSvcResourceProvider -AdminUri https://Computer01:30004 -Token $Token -Name "ResourceProvider02"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

## PARAMETERS

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

### -IncludeSystemResourceProviders
Indicates that the system resource providers are returned.

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

### -Name
Specifies an array of names of resource providers.
You can use wildcard characters.

```yaml
Type: String[]
Parameter Sets: (All)
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

[Add-MgmtSvcResourceProvider](xref:Administration/v1.0/Add-MgmtSvcResourceProvider.md)

[Set-MgmtSvcResourceProvider](xref:Administration/v1.0/Set-MgmtSvcResourceProvider.md)

[Test-MgmtSvcResourceProvider](xref:Administration/v1.0/Test-MgmtSvcResourceProvider.md)

[Remove-MgmtSvcResourceProvider](xref:Administration/v1.0/Remove-MgmtSvcResourceProvider.md)


