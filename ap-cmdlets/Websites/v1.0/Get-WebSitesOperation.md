---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 801E3101-6C0D-4E85-860A-342602E36955
online version: http://go.microsoft.com/fwlink/?LinkID=321232
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesOperation.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesOperation.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesOperation.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-WebSitesOperation

## SYNOPSIS
Gets information about Dynamic Windows Process Activation Service   operations.

## SYNTAX

```
Get-WebSitesOperation [[-OperatorName] <String>] [-Completed] [-RemoteSettings <RemoteSettings>]
 [-SuppressRequestIdLine] [<CommonParameters>]
```

## DESCRIPTION
The **Get-WebSitesOperation** cmdlet returns information about Dynamic Windows Process Activation Service (DWAS) operations.
DWAS is designed to carry out such tasks as:

- Provisioning and activating sites. 
- Starting and monitoring worker processes. 
- Shutting down and deprovisioning sites. 
- Overseeing sandbox and security measures.

## EXAMPLES

### Example 1: Get DWAS operations
```
PS C:\> Get-WebSitesOperation -OperatorName "WFF" -Completed
```

This command returns information for all completed operations that ran under the name WFF.

## PARAMETERS

### -Completed
Indicates that only completed operations are returned.
If you do not specify this parameter only running operations are returned.

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

### -OperatorName
Specifies the name under which DWAS operations were run or are currently running.
For example:

`-OperatorName "WebsiteBackup"`

When this parameter is used, **Get-WebSitesOperation** returns information for operations run under this name.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Start-WebSitesOperation](xref:Websites/v1.0/Start-WebSitesOperation.md)

[Remove-WebSitesOperation](xref:Websites/v1.0/Remove-WebSitesOperation.md)


