---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 7487C7BC-6926-43D5-85CF-2267805AEC7A
online version: http://go.microsoft.com/fwlink/?LinkID=306486
schema: 2.0.0
updated_at: 1/4/2017 4:35 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Set-MgmtSvcIdentityProviderSettings.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/Set-MgmtSvcIdentityProviderSettings.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/676435fba79c23d58e9141828e751b939d2694b8/AzurePack-cmdlets/Configuration/v1.0/Set-MgmtSvcIdentityProviderSettings.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Set-MgmtSvcIdentityProviderSettings

## SYNOPSIS
Configures an administrator authentication site or a tenant authentication site to use AD FS.

## SYNTAX

### ConnectionParameters (Default)
```
Set-MgmtSvcIdentityProviderSettings [-ConfigureSecondary] [-Target] <String[]> [-MetadataEndpoint <Uri>]
 [-MetadataFile <String>] [-DisableCertificateValidation] [-PortalConnectionString <String>]
 [-ManagementConnectionString <String>] [-Server <String>] [-UserName <String>] [-Password <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ConnectionString
```
Set-MgmtSvcIdentityProviderSettings [-ConfigureSecondary] [-Target] <String[]> [-MetadataEndpoint <Uri>]
 [-MetadataFile <String>] [-DisableCertificateValidation] [-PortalConnectionString <String>]
 [-ManagementConnectionString <String>] [-ConnectionString <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-MgmtSvcIdentityProviderSettings** cmdlet configures an administrator authentication site or a tenant authentication site to use Active Directory Federation Services (AD FS).
Specify one or more namespaces and an endpoint for metadata.

You can run this cmdlet from any computer in the deployment.
However, this cmdlet assumes that the database is on the local computer.
If the database is on another computer, you must use the *Server*, *UserName*, *Password*, and *Database* parameters, or a SQL connection string.
If you specify a connection string by using the *ConnectionString* parameter, that value takes precedence over the *Server*, *UserName*, *Password*, and *Database* parameters.

## EXAMPLES

### Example 1: Configure a tenant authentication site
```
PS C:\> $ConnectionString = 'Data Source=rd-sdfre4;Initial Catalog=Microsoft.MgmtSvc.Config;User ID=SysAdmin;Password=PassWord'
PS C:\> Set-MgmtSvcIdentityProviderSettings -Target Management -MetadataEndpoint "https://Server07.Contoso.com/FederationMetadata/2007-06/FederationMetadata.xml" -PortalConnectionString $ConnectionString -DisableCertificateValidation
```

The first command stores a connection string in the $ConnectionString variable.

The second command configures a tenant authentication The command uses the connection string stored in the $ConnectionString variable.
The command also specifies an endpoint for the metadata and disables certificate validation.

## PARAMETERS

### -ConfigureSecondary
Indicates that secondary identity provider settings are set.

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

### -DisableCertificateValidation
Indicates that the cmdlet disables certificate validation.

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

### -ManagementConnectionString
Specifies a connection string for the Admin Auth Site.

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

### -MetadataEndpoint
Specifies an endpoint for identity provider metadata.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MetadataFile
{{Fill MetadataFile Description}}

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

### -PortalConnectionString
Specifies a connection string for the Tenant Auth Site.

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

### -Target
Specifies the target site.
Valid values are:

- Membership. This value indicates that the target is the Tenant Auth Site.
- Windows. This value indicates that the target is the Admin Auth Site.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

