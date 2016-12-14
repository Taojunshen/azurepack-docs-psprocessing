---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: B43B758C-925D-45BE-8149-14106FA97EBE
online version: http://go.microsoft.com/fwlink/?LinkID=296543
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcResourceProviderConfiguration.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcResourceProviderConfiguration.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcResourceProviderConfiguration.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcResourceProviderConfiguration

## SYNOPSIS
Gets a resource provider configuration.

## SYNTAX

```
Get-MgmtSvcResourceProviderConfiguration [[-Name] <String[]>] [-ConnectionString <String>]
 [-EncryptionKey <String>] [-EncryptionAlgorithm <String>] [-As <String>] [-DecryptPassword]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcResourceProviderConfiguration** cmdlet gets a resource provider configuration.
If you run this cmdlet without specifying any parameters, all resource provider configurations are returned.
To get a specific resource provider configuration, specify one or more values for the *Name* parameter.

## EXAMPLES

### Example 1: Get all resource provider configurations
```
PS C:\>Get-MgmtSvcResourceProviderConfiguration -As XmlString
```

This command gets all resource provider configurations and returns their information in XML format.

### Example 2: Get specific resource provider configurations by their name
```
PS C:\>Get-MgmtSvcResourceProviderConfiguration -Name "SqlServers","marketplace"
```

This command gets only the resource provider configurations named SqlServers and marketplace, and returns information about the configurations to the user.

## PARAMETERS

### -As
Specifies an output format.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Xml, XDocument, XmlString

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionString
Specifies an SQL connection string.

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

### -DecryptPassword
{{Fill DecryptPassword Description}}

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

### -EncryptionAlgorithm
Specifies an encryption algorithm.

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

### -EncryptionKey
Specifies an encryption key, as a hexadecimal string.

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
Specifies an array of names of resource providers.
You can use wildcards.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
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

[New-MgmtSvcResourceProviderConfiguration](xref:Configuration/v1.0/New-MgmtSvcResourceProviderConfiguration.md)

[Add-MgmtSvcResourceProviderConfiguration](xref:Configuration/v1.0/Add-MgmtSvcResourceProviderConfiguration.md)

[Remove-MgmtSvcResourceProviderConfiguration](xref:Configuration/v1.0/Remove-MgmtSvcResourceProviderConfiguration.md)


