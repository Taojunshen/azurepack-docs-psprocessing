---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: BF21888B-803E-4ED6-A536-DF9E6E379B9F
online version: http://go.microsoft.com/fwlink/?LinkID=320109
schema: 2.0.0
updated_at: 1/4/2017 4:35 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Remove-MgmtSvcAdminUser.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Configuration/v1.0/Remove-MgmtSvcAdminUser.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/676435fba79c23d58e9141828e751b939d2694b8/AzurePack-cmdlets/Configuration/v1.0/Remove-MgmtSvcAdminUser.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Remove-MgmtSvcAdminUser

## SYNOPSIS
Removes an administrative principal from the database.

## SYNTAX

### ConnectionParameters (Default)
```
Remove-MgmtSvcAdminUser [-Principal] <String> [-EncryptionKey <String>] [-EncryptionAlgorithm <String>]
 [-Database <String>] [-Server <String>] [-UserName <String>] [-Password <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ConnectionString
```
Remove-MgmtSvcAdminUser [-Principal] <String> [-EncryptionKey <String>] [-EncryptionAlgorithm <String>]
 [-ConnectionString <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-MgmgSvcAdminUser** cmdlet removes an administrative user from the database.

If this cmdlet is run on the computer on which the Admin API service is installed and the Web.config file contains values for EncrptionKey and EncryptionAlgorithm, then those values are used.

## EXAMPLES

### Example 1: Remove a principal by using a connection string
```
PS C:\> Remove-MgmtSvcAdminUser -Principal "PattiFuller@Contoso.com" -ConnectionString 'Server=.\sqlexpress;Initial Catalog=Contoso.MgmtSvc.Store;User Id=sa;Password=PassWord;'
```

This command removes the principal named Patti Fuller by using a connection string to connect to the database.

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

### -ConnectionString
Specifies an SQL connection string.

```yaml
Type: String
Parameter Sets: ConnectionString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database
Specifies a database name.

```yaml
Type: String
Parameter Sets: ConnectionParameters
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

### -Password
Specifies a password.

```yaml
Type: String
Parameter Sets: ConnectionParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Principal
Specifies an administrative user or group.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Server
Specifies the name of the computer on which the SQL database resides.

```yaml
Type: String
Parameter Sets: ConnectionParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies the name of a user account.

```yaml
Type: String
Parameter Sets: ConnectionParameters
Aliases: 

Required: False
Position: Named
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

[Add-MgmtSvcAdminUser](xref:Configuration/v1.0/Add-MgmtSvcAdminUser.md)

[Get-MgmtSvcAdminUser](xref:Configuration/v1.0/Get-MgmtSvcAdminUser.md)


