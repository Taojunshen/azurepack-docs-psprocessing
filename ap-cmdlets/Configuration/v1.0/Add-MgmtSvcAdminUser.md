---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 30CDDD58-8F87-4EBB-9BD2-1F59A50B85BB
online version: http://go.microsoft.com/fwlink/?LinkID=306481
schema: 2.0.0
updated_at: 1/4/2017 4:35 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Add-MgmtSvcAdminUser.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Add-MgmtSvcAdminUser.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/676435fba79c23d58e9141828e751b939d2694b8/AzurePack-cmdlets/Configuration/v1.0/Add-MgmtSvcAdminUser.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Add-MgmtSvcAdminUser

## SYNOPSIS
Adds an administrative principal to the database.

## SYNTAX

### ConnectionParameters (Default)
```
Add-MgmtSvcAdminUser [-Principal] <String> [-EncryptionKey <String>] [-EncryptionAlgorithm <String>]
 [-Database <String>] [-Server <String>] [-UserName <String>] [-Password <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ConnectionString
```
Add-MgmtSvcAdminUser [-Principal] <String> [-EncryptionKey <String>] [-EncryptionAlgorithm <String>]
 [-ConnectionString <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-MgmtSvcAdminUser** cmdlet adds an administrative user or group to the database.
The cmdlet grants the principal permissions to access the management portal for administrators and Windows Azure Pack administrator API.

If this cmdlet is run on the computer on which the Admin API service is installed and the Web.config file contains values for *EncrptionKey* and *EncryptionAlgorithm*, then those values are used.

## EXAMPLES

### Example 1: Add a principal by using a connection string
```
PS C:\> Add-MgmtSvcAdminUser -Principal "PattiFuller@Contoso.com" -ConnectionString 'Server=.\sqlexpress;Initial Catalog=Microsoft.MgmtSvc.Store;User Id=sa;Password=PassWord;'
```

This command adds the specified user as an administrative principal to the database.
The command uses the specified connection string to connect to the database.

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
Specifies a database.
If a value is not provided for this parameter, the cmdlet uses the management database (Microsoft.MgmtSvc.Store).

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
Specifies a server.
If a value is not provided for this parameter, the cmdlet uses localhost (or '.').

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
Specifies a user name.
If a value is not provided for this parameter, the cmdlet uses integrated security.

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

[Get-MgmtSvcAdminUser](xref:Configuration/v1.0/Get-MgmtSvcAdminUser.md)

[Remove-MgmtSvcAdminUser](xref:Configuration/v1.0/Remove-MgmtSvcAdminUser.md)


