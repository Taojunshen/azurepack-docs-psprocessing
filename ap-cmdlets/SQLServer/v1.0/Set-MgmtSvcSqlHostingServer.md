---
external help file: Microsoft.WindowsAzure.SqlServer.PowerShell.dll-Help.xml
ms.assetid: 1C956C91-F09F-4A1D-838A-962D2DC5E99D
online version: http://go.microsoft.com/fwlink/?LinkID=321816
schema: 2.0.0
updated_at: 1/3/2017 11:17 PM
ms.date: 1/3/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/SQLServer/v1.0/Set-MgmtSvcSqlHostingServer.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/SQLServer/v1.0/Set-MgmtSvcSqlHostingServer.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/d67623ef81fb4ed9ee02ac9c9b01bb34ad6d33e2/AzurePack-cmdlets/SQLServer/v1.0/Set-MgmtSvcSqlHostingServer.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Set-MgmtSvcSqlHostingServer

## SYNOPSIS
Updates a SQL Server hosting server.

## SYNTAX

### ByProperties (Default)
```
Set-MgmtSvcSqlHostingServer [-HostingServerId] <String> [-SqlUser <PSCredential>] [[-TotalSpaceMB] <Int32>]
 [-Name] <String> [-NumberOfCpuCores <Int32>] [-TotalMemoryGB <Int32>] [-SupportedIopsPerVolume <Int32>]
 [-MaximumResourcePools <Int32>] [-AdminUri] <Uri> [-Token] <String> [-DisableCertificateValidation] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByObject
```
Set-MgmtSvcSqlHostingServer [[-HostingServer] <SqlHostingServer>] [-AdminUri] <Uri> [-Token] <String>
 [-DisableCertificateValidation] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-MgmtSvcSqlHostingServer** cmdlet updates a SQL Server hosting server.

## EXAMPLES

### Example 1: Update a SQL hosting server
```
PS C:\> $Creds = Get-Credential
PS C:\> Set-MgmtSvcSqlHostingServer -AdminUri "https://Computer01:30004" -Token $Token -Name "SQLServer01.Contoso.com" -TotalSpaceMB 4096 -User $Creds -HostingServerId "u37k25"
PS C:\> Set-MgmtSvcSqlHostingServer -AdminUri "https://Computer01:30004" -Token $Token -Name "SQLServer01.Contoso.com" -TotalSpaceMB 4096 -NumberOfCpuCores 4 -TotalMemoryGB 12 -SupportedIopsPerVolume 500 -MaximumResourcePools 12 -HostingServerId "u37k25"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

The first command prompts the user for credentials and stores the provided user name and password in the $Credential variable.
The *SqlUser* parameter is only required if the hosting server's connection must be repaired.

The second command updates the total space to 4096 MB for the hosting server named SQLServer01.Contoso.com.

The third command updates the values of total space, CPU core, memory, supported IOPS per volume, and maximum resource pools allowed in the server.

## PARAMETERS

### -AdminUri
Specifies the URI of the Windows Azure Pack administrator API.
Use the following format: https://\< computer\>:\<port\>, where \<computer\> is the computer on which the administrator API is installed.

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

### -HostingServerId
Specifies the ID of a SQL Server hosting server.

```yaml
Type: String
Parameter Sets: ByProperties
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Specifies the name of a SQL Server hosting server.

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

### -SqlUser
Specifies a SQL user account and password as a **PSCredential** object.
To create a **PSCredential** object, use the **Get-Credential** cmdlet.

```yaml
Type: PSCredential
Parameter Sets: ByProperties
Aliases: 

Required: False
Position: Named
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

Required: False
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

[Add-MgmtSvcSqlHostingServer](xref:SQLServer/v1.0/Add-MgmtSvcSqlHostingServer.md)

[Get-MgmtSvcSqlHostingServer](xref:SQLServer/v1.0/Get-MgmtSvcSqlHostingServer.md)

[Test-MgmtSvcSqlHostingServer](xref:SQLServer/v1.0/Test-MgmtSvcSqlHostingServer.md)

[Remove-MgmtSvcSqlHostingServer](xref:SQLServer/v1.0/Remove-MgmtSvcSqlHostingServer.md)


