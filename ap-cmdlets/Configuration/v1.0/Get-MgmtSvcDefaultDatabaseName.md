---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 99786B8C-21E7-45D1-9FE5-90C86522F149
online version: http://go.microsoft.com/fwlink/?LinkID=320108
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcDefaultDatabaseName.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcDefaultDatabaseName.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcDefaultDatabaseName.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcDefaultDatabaseName

## SYNOPSIS
Gets the names of the default databases.

## SYNTAX

```
Get-MgmtSvcDefaultDatabaseName [[-Name] <String[]>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcDefaultDatabaseName** cmdlet gets the names of the default databases.
If you use this cmdlet without specifying a parameter, all default database names are returned.
To get a specific default database name, use the *Name* parameter.

## EXAMPLES

### Example 1: Get a default database name
```
PS C:\>Get-MgmtSvcDefaultDatabaseName -Name "Microsoft.MgmtSvc.Config","Microsoft.MgmtSvc.Store"
```

This example returns information about the default databases named Microsoft.MgmtSvc.Config and Microsoft.MgmtSvc.Store.

## PARAMETERS

### -Name
Specifies an array of names for default databases.

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

