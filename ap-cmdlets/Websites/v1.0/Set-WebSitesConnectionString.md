---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 54389FA9-F7AE-4E4A-BCB9-A453CF5AA265
online version: http://go.microsoft.com/fwlink/?LinkID=321267
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Set-WebSitesConnectionString.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Set-WebSitesConnectionString.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/Set-WebSitesConnectionString.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Set-WebSitesConnectionString

## SYNOPSIS
Sets a database connection string.

## SYNTAX

```
Set-WebSitesConnectionString [-ConnectionString] <String> [-Type] <DatabaseType>
 [-RemoteSettings <RemoteSettings>] [-SuppressRequestIdLine] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-WebSitesConnectionString** cmdlet sets a database connection string for the specified database type.
You can set connection strings for either a hosting database or a metering database.

## EXAMPLES

### Example 1: Set a hosting database connection string
```
PS C:\> Set-WebSitesConnectionString -Type "Hosting" -ConnectionString "Data Source=CN-SERVER01;Initial Catalog=Hosting;User ID=Hosting_HostingAdmin;Password=Password01!"
```

This command modifies the connection string for the hosting database.

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
Specifies a connection string for a hosting database.
Connection strings contain information about a data source and how to connect to it; this information includes such things as the server and database name, and the name and password of the user account making the connection.
For example:

`-ConnectionString "Server=tcp:contosodb.database.windows.net;Database=Personel;User ID=admin@contoso.com;Password=p@ssw0rd;Trusted_Connection=False;Encrypt=True;"`

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

### -Type
Specifies the database type.
Valid values are:

- Hosting
- Metering

For example:

`-Type "Hosting"`

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Reset-WebSitesConnectionString](xref:Websites/v1.0/Reset-WebSitesConnectionString.md)


