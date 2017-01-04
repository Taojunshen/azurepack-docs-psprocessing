---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 2989E311-D800-4FC7-BBA7-195667CB4EC8
online version: http://go.microsoft.com/fwlink/?LinkID=321263
schema: 2.0.0
updated_at: 1/3/2017 9:53 PM
ms.date: 1/3/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Reset-WebSitesConnectionString.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Reset-WebSitesConnectionString.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/9b04ebf7a96dfac95b0cdb4f6ad2c39512dc39eb/AzurePack-cmdlets/Websites/v1.0/Reset-WebSitesConnectionString.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Reset-WebSitesConnectionString

## SYNOPSIS
Resets a database connection string.

## SYNTAX

```
Reset-WebSitesConnectionString [-Force] [-Type] <DatabaseType> [-RemoteSettings <RemoteSettings>]
 [-SuppressRequestIdLine] [-WhatIf] [-Confirm] [-ServerRoles] <ServerRole[]> [-WorkerNames <String[]>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Reset-WebSitesConnectionString** cmdlet resets the database connection string for the specified database type.

## EXAMPLES

### Example 1: Reset the connection string for a hosting database
```
PS C:\> Reset-WebSitesConnectionString -Type "Hosting"
```

This command resets the connection string for the hosting database.

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

### -Force
Forces the command to run without asking for user confirmation.

```yaml
Type: SwitchParameter
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

### -ServerRoles
{{Fill ServerRoles Description}}

```yaml
Type: ServerRole[]
Parameter Sets: (All)
Aliases: 
Accepted values: Controller, ManagementServer, FrontEnd, Publisher, Worker

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

### -Type
Specifies the database type.
Valid values are:

- Hosting
- Metering

For example:

`-Type "Metering"`

```yaml
Type: DatabaseType
Parameter Sets: (All)
Aliases: 
Accepted values: Hosting, Metering

Required: True
Position: 0
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

### -WorkerNames
{{Fill WorkerNames Description}}

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-WebSitesConnectionString](xref:Websites/v1.0/Set-WebSitesConnectionString.md)


