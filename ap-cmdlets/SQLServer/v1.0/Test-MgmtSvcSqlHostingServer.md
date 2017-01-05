---
external help file: Microsoft.WindowsAzure.SqlServer.PowerShell.dll-Help.xml
ms.assetid: F2395B4B-1CCF-4E2E-9FCC-552B093EACD7
online version: http://go.microsoft.com/fwlink/?LinkID=321817
schema: 2.0.0
updated_at: 1/3/2017 11:17 PM
ms.date: 1/3/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/SQLServer/v1.0/Test-MgmtSvcSqlHostingServer.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/SQLServer/v1.0/Test-MgmtSvcSqlHostingServer.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/d67623ef81fb4ed9ee02ac9c9b01bb34ad6d33e2/AzurePack-cmdlets/SQLServer/v1.0/Test-MgmtSvcSqlHostingServer.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Test-MgmtSvcSqlHostingServer

## SYNOPSIS
Verifies a SQL Server hosting server can be created.

## SYNTAX

### ByProperties (Default)
```
Test-MgmtSvcSqlHostingServer [-TotalSpaceMB] <Int32> [-SqlUser] <PSCredential> [-ServerGroupId] <String>
 [-Name] <String> [-NumberOfCpuCores <Int32>] [-TotalMemoryGB <Int32>] [-SupportedIopsPerVolume <Int32>]
 [-MaximumResourcePools <Int32>] [-AdminUri] <Uri> [-Token] <String> [-DisableCertificateValidation]
 [<CommonParameters>]
```

### ByObject
```
Test-MgmtSvcSqlHostingServer [-ServerGroupId] <String> [[-HostingServer] <SqlHostingServer>] [-AdminUri] <Uri>
 [-Token] <String> [-DisableCertificateValidation] [<CommonParameters>]
```

## DESCRIPTION
The **Test-MgmtSvcSqlHostingServer** cmdlet verifies that a SQL Server hosting server can be created, and that the specified login credentials are correct.
This cmdlet verifies that no server with the same name is already registered.

## EXAMPLES

### Example 1: Verify a SQL Server hosting server
```
PS C:\> $Creds = Get-Credential
PS C:\> Test-MgmtSvcSqlHostingServer -AdminUri "https://Computer01:30004" -Token $Token -Name "SQLServer01.Contoso.com" -TotalSpaceMB 2048 -User $Creds -ServerGroupId "g5sho0"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

The first command prompts the user for credentials and stores the provided user name and password in the $Credential variable.

The second command tests the SQL Server hosting server named SQLServer01.Contoso.com, using the credentials provided in the first command.

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

[Set-MgmtSvcSqlHostingServer](xref:SQLServer/v1.0/Set-MgmtSvcSqlHostingServer.md)

[Remove-MgmtSvcSqlHostingServer](xref:SQLServer/v1.0/Remove-MgmtSvcSqlHostingServer.md)


