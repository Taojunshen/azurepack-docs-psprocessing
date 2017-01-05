---
external help file: Microsoft.WindowsAzure.SqlServer.PowerShell.dll-Help.xml
ms.assetid: F75D1E78-87BF-4C25-BE2A-01850B625279
online version: http://go.microsoft.com/fwlink/?LinkID=321807
schema: 2.0.0
updated_at: 1/3/2017 10:42 PM
ms.date: 1/3/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/SQLServer/v1.0/Add-MgmtSvcSqlHostingServer.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/SQLServer/v1.0/Add-MgmtSvcSqlHostingServer.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/eb7bff1251dc2a22eafa120c35cbbc43529d3762/AzurePack-cmdlets/SQLServer/v1.0/Add-MgmtSvcSqlHostingServer.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Add-MgmtSvcSqlHostingServer

## SYNOPSIS
Adds a SQL Server hosting server to Windows Azure Pack.

## SYNTAX

### ByProperties (Default)
```
Add-MgmtSvcSqlHostingServer [-TotalSpaceMB] <Int32> [-SqlUser] <PSCredential> [-ServerGroupId] <String>
 [-Name] <String> [-NumberOfCpuCores <Int32>] [-TotalMemoryGB <Int32>] [-SupportedIopsPerVolume <Int32>]
 [-MaximumResourcePools <Int32>] [-AdminUri] <Uri> [-Token] <String> [-DisableCertificateValidation] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByObject
```
Add-MgmtSvcSqlHostingServer [-ServerGroupId] <String> [[-HostingServer] <SqlHostingServer>] [-AdminUri] <Uri>
 [-Token] <String> [-DisableCertificateValidation] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-MgmtSvcSqlHostingServer** adds a SQL Server hosting server to Windows Azure Pack for Windows Server.

## EXAMPLES

### Example 1: Add a SQL hosting server
```
PS C:\> $Creds = Get-Credential
PS C:\> Add-MgmtSvcSqlHostingServer -AdminUri "https://Computer01:30004" -Token $Token -Name "SQLServer01.Contoso.com" -TotalSpaceMB 2048 -ServerGroupId "g5sho0" -User $Creds
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

The first command prompts the user for credentials which are stored in the $Creds variable.

The second command uses the credentials provided in the first command to add the SQL Server named SQLServer01.Contoso.com to the SQL Server group with the ID of g5sho0.

## PARAMETERS

### -AdminUri
Specifies the URI of the Windows Azure Pack administrator API.
Use the following format: https://\<computer\>:\<port\>, where \<computer\> is the computer on which the administrator API is installed.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableCertificateValidation
Disables certificate validation for the Windows Azure Pack installation.

If you specify this parameter, you can use self-signed certificates.

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

### -HostingServer
Specifies a SQL Server hosting server object.

```yaml
Type: SqlHostingServer
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaximumResourcePools
Specifies the number of resource pools for the server.

```yaml
Type: Int32
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Specifies the name of a SQL Server.

If you want your application databases to be publically accessible, ensure that you use a publically-accessible IP address or FQDN.

```yaml
Type: String
Parameter Sets: ByProperties
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberOfCpuCores
Specifies the number of CPU cores for the server.

```yaml
Type: Int32
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerGroupId
Specifies the ID for a SQL Server group.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SqlUser
Specifies a user account and password as a **PSCredential** object.
To create a **PSCredential** object, use the **Get-Credential** cmdlet.

```yaml
Type: PSCredential
Parameter Sets: ByProperties
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SupportedIopsPerVolume
Specifies the supported I/O operations per second (IOPS) for the server.

```yaml
Type: Int32
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Token
Specifies an identity token.
To create a token, use the **Get-MgmtSvcToken** cmdlet.

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

### -TotalMemoryGB
Specifies the total amount of memory, in gigabytes, for the server.

```yaml
Type: Int32
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TotalSpaceMB
Specifies the size, in megabytes (MB) of the hosting server.

```yaml
Type: Int32
Parameter Sets: ByProperties
Aliases: 

Required: True
Position: 3
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### SqlHostingServer
You can pipe a **SqlHostingServer** object to this cmdlet.

## OUTPUTS

### SqlHostingServer
This cmdlet emits a **SqlHostingServer** object.

## NOTES

## RELATED LINKS

[Get-MgmtSvcSqlHostingServer](xref:SQLServer/v1.0/Get-MgmtSvcSqlHostingServer.md)

[Set-MgmtSvcSqlHostingServer](xref:SQLServer/v1.0/Set-MgmtSvcSqlHostingServer.md)

[Test-MgmtSvcSqlHostingServer](xref:SQLServer/v1.0/Test-MgmtSvcSqlHostingServer.md)

[Remove-MgmtSvcSqlHostingServer](xref:SQLServer/v1.0/Remove-MgmtSvcSqlHostingServer.md)


