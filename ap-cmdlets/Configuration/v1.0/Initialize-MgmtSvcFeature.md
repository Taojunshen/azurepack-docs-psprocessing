---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 2721C05E-93A9-4E73-A0B4-11857C28FA97
online version: http://go.microsoft.com/fwlink/?LinkID=296544
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Initialize-MgmtSvcFeature.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Initialize-MgmtSvcFeature.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Configuration/v1.0/Initialize-MgmtSvcFeature.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Initialize-MgmtSvcFeature

## SYNOPSIS
Configures a management service feature.

## SYNTAX

### ConnectionParameters (Default)
```
Initialize-MgmtSvcFeature [-Name] <String> [[-Settings] <Hashtable>] [-Passphrase <String>]
 [-EnableCeip <EnableCeip>] [-Server <String>] [-UserName <String>] [-Password <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ConnectionString
```
Initialize-MgmtSvcFeature [-Name] <String> [[-Settings] <Hashtable>] [-Passphrase <String>]
 [-EnableCeip <EnableCeip>] [-ConnectionString <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Initialize-MgmtSvcFeature** cmdlet configures a management service feature.

The feature can be initialized only if it is installed locally.

## EXAMPLES

### Example 1: Configure a management service feature
```
PS C:\>$Settings = @{dbServer='mysqlservermc';dbAdminUserName='sa';dbAdminPassword='#######';configStorePassphrase='########';}
PS C:\> Initialize-MgmtSvcFeature -Name "AdminSite" -Settings $Settings -EnableCeip Yes
```

The first command specifies the settings for a management service feature, and stores the settings in the $Settings variable.

The second command configures the management service feature named AdminSite by using the settings stored in $Settings for the feature.

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
This parameter overrides Settings\["connectionString"\].

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

### -EnableCeip
Enables, when set to Yes, participation in the Customer Experience Improvement Program (CEIP).
To disable participation in CEIP, set this value to No.
This parameter overrides Settings\["enableCeip"\].

```yaml
Type: EnableCeip
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a management service feature.

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

### -Passphrase
Specifies a passphrase.

The passphrase must have more than eight characters and contain at least one non-alphanumeric character.
Remember to protect the passphrase.
You cannot recover the passphrase.
This parameter overrides Settings\["configStorePassphrase"\].

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
This parameter overrides Settings\["dbAdminPassword"\].

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

### -Server
Specifies the name of the computer on which the SQL database resides.
This parameter overrides Settings\["dbServer"\].

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

### -Settings
Specifies a collection of key/value pairs for the feature settings.
When possible, you should use the named parameters instead of this parameter.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies the name of a user account.
This parameter overrides Settings\["dbAdminUserName"\].

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

[Get-MgmtSvcFeature](xref:Configuration/v1.0/Get-MgmtSvcFeature.md)


