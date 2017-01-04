---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: EF1E4495-4DF5-43E0-83DF-B18B47B908E0
online version: http://go.microsoft.com/fwlink/?LinkID=320107
schema: 2.0.0
updated_at: 1/4/2017 4:35 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcAdminUser.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcAdminUser.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/676435fba79c23d58e9141828e751b939d2694b8/AzurePack-cmdlets/Configuration/v1.0/Get-MgmtSvcAdminUser.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcAdminUser

## SYNOPSIS
Gets an administrative principal from the database.

## SYNTAX

### ConnectionParameters (Default)
```
Get-MgmtSvcAdminUser [[-Principal] <String[]>] [-EncryptionKey <String>] [-EncryptionAlgorithm <String>]
 [-Database <String>] [-Server <String>] [-UserName <String>] [-Password <String>] [<CommonParameters>]
```

### ConnectionString
```
Get-MgmtSvcAdminUser [[-Principal] <String[]>] [-EncryptionKey <String>] [-EncryptionAlgorithm <String>]
 [-ConnectionString <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcAdminUser** cmdlet gets an administrative user from the database.

If this cmdlet is run on the computer on which the Admin API service is installed and the Web.config file contains values for EncryptionKey and EncryptionAlgorithm, then those values are used.

You must use the *Server*, *UserName*, *Password*, and *Database* parameters, or a SQL connection string.
If you specify a connection string by using the *ConnectionString* parameter, that value takes precedence over the *Server*, *UserName*, *Password*, and *Database* parameters.

## EXAMPLES

### Example 1: Get a principal by using a connection string
```
PS C:\> Get-MgmtSvcAdminUser -Principal "PattiFuller@Contoso.com" -ConnectionString 'Server=.\sqlexpress;Initial Catalog=Contoso.MgmtSvc.Store;User Id=sa;Password=PassWord;'
```

This command gets the principal named Patti Fuller by using a connection string to connect to the database.

## PARAMETERS

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
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-MgmtSvcAdminUser](xref:Configuration/v1.0/Add-MgmtSvcAdminUser.md)

[Remove-MgmtSvcAdminUser](xref:Configuration/v1.0/Remove-MgmtSvcAdminUser.md)


