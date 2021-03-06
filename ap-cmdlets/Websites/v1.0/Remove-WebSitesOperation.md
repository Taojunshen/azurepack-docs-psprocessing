---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 9EFBDEA7-16EB-487B-8C24-3CE723EEEC9A
online version: http://go.microsoft.com/fwlink/?LinkID=321255
schema: 2.0.0
updated_at: 1/3/2017 9:53 PM
ms.date: 1/3/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Remove-WebSitesOperation.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Remove-WebSitesOperation.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/9b04ebf7a96dfac95b0cdb4f6ad2c39512dc39eb/AzurePack-cmdlets/Websites/v1.0/Remove-WebSitesOperation.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Remove-WebSitesOperation

## SYNOPSIS
Removes a DWAS operation.

## SYNTAX

```
Remove-WebSitesOperation -OperationId <Int32> [-TimeOut <TimeSpan>] [-RemoteSettings <RemoteSettings>]
 [-SuppressRequestIdLine] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-WebSitesOperation** cmdlet removes a Dynamic Windows Activation Service (DWAS) operation.
DWAS is designed to carry out such tasks as:

- Provisioning and activating sites. 
- Starting and monitoring worker processes. 
- Shutting down and deprovisioning sites. 
- Overseeing sandbox and security measures.

## EXAMPLES

### Example 1: Remove a DWAS operation
```
PS C:\> Remove-WebSitesOperation -OperationId 1
```

This command removes the DWAS operation with the ID 1.

## PARAMETERS

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

### -OperationId
Specifies the ID of the operation to be removed.
For example:

`-OperationId 13`

You can return the IDs for all your current web site operations by using the [Get-WebSitesOperation](./Get-WebSitesOperation.md) cmdlet:

`Get-WebSitesOperation`

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
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

### -TimeOut
Specifies the maximum time to wait for the operation to finish.

```yaml
Type: TimeSpan
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

[Start-WebSitesOperation](xref:Websites/v1.0/Start-WebSitesOperation.md)

[Get-WebSitesOperation](xref:Websites/v1.0/Get-WebSitesOperation.md)


