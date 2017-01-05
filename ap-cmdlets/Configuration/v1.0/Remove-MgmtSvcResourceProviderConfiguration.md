---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 86E5D057-3350-404B-8543-37B0B421261F
online version: http://go.microsoft.com/fwlink/?LinkID=296553
schema: 2.0.0
updated_at: 1/4/2017 4:35 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Remove-MgmtSvcResourceProviderConfiguration.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Remove-MgmtSvcResourceProviderConfiguration.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/676435fba79c23d58e9141828e751b939d2694b8/AzurePack-cmdlets/Configuration/v1.0/Remove-MgmtSvcResourceProviderConfiguration.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Remove-MgmtSvcResourceProviderConfiguration

## SYNOPSIS
Removes a resource provider from a management store database.

## SYNTAX

```
Remove-MgmtSvcResourceProviderConfiguration [-Name] <String> [-InstanceId] <String>
 [-ConnectionString <String>] [-EncryptionKey <String>] [-EncryptionAlgorithm <String>] [-As <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-MgmtSvcResourceProviderConfiguration** cmdlet removes an entry for a resource provider from the management store database.
You can run this cmdlet from any computer in the deployment.

If this cmdlet is run on the computer on which the Admin API service is installed and Web.config file contains values for ConnectionString, EncryptionKey, and EncryptionAlgorithm, then those values are used.

## EXAMPLES

### Example 1: Remove a resource provider
```
PS C:\> Remove-MgmtSvcResourceProviderConfiguration -Name "RP01" -InstanceId "0602c550-0853-48fc-bfbb-dc1f84ac08a3"
```

This command removes the resource provider with the name RP01 and instance ID of 0602c550-0853-48fc-bfbb-dc1f84ac08a3.

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

### -InstanceId
Specifies an ID for an instance of a resource provider.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a resource provider.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
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

[New-MgmtSvcResourceProviderConfiguration](xref:Configuration/v1.0/New-MgmtSvcResourceProviderConfiguration.md)

[Add-MgmtSvcResourceProviderConfiguration](xref:Configuration/v1.0/Add-MgmtSvcResourceProviderConfiguration.md)

[Get-MgmtSvcResourceProviderConfiguration](xref:Configuration/v1.0/Get-MgmtSvcResourceProviderConfiguration.md)


