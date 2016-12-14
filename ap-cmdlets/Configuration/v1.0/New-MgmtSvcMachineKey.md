---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 8AB908B4-87D2-4C33-9574-40B8935B8601
online version: http://go.microsoft.com/fwlink/?LinkID=296547
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/New-MgmtSvcMachineKey.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/New-MgmtSvcMachineKey.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Configuration/v1.0/New-MgmtSvcMachineKey.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# New-MgmtSvcMachineKey

## SYNOPSIS
Creates a machine key element.

## SYNTAX

```
New-MgmtSvcMachineKey [-Validation <String>] [-Decryption <String>] [-DecryptionKeySize <Int32>] [-Base64]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-MachineKey** cmdlet creates a \<machineKey\> configuration element for use in the web.config file.
The **Initialize-MgmtSvcFeature** cmdlet calls this cmdlet to generate the initial keys stored during configuration.

A machine key can be a validation key to confirm the integrity of data, or a decryption key to encrypt or decrypt forms authentication data.
This cmdlet generates a value in memory.
It is recommended that you periodically rotate the machine keys.
For example, once per year.

## EXAMPLES

### Example 1: Create a machine key
```
PS C:\>([xml](New-MgmtSvcMachineKey)).OuterXml
```

This command creates a machine key configuration element by using the Hash-based Message Authentication Code (HMAC) SHA256 (HMACSHA256) for validation and the Advanced Encryption Standard (AES) encryption method for decryption.

## PARAMETERS

### -Base64
Indicates that the validation and decryption values are Base64 encoded.

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

### -Decryption
Specifies an algorithm to encrypt and decrypt forms authentication data.

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

### -DecryptionKeySize
Specifies a key size, in bits, of the algorithm used to encrypt and decrypt forms authentication data.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Validation
Specifies a hash algorithm used to validate data.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

