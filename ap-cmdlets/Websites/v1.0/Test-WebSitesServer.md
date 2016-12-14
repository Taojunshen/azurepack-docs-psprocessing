---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: A0CCECFD-0CEA-4807-B180-4CF8ED025CF5
online version: http://go.microsoft.com/fwlink/?LinkID=321276
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Test-WebSitesServer.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Test-WebSitesServer.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/Test-WebSitesServer.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Test-WebSitesServer

## SYNOPSIS
Tests connectivity to a remote server.

## SYNTAX

```
Test-WebSitesServer [[-Name] <String>] [-UserName <String>] [-Password <String>] [-ConnectionString <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Test-WebSitesServer** cmdlet tests Windows Management Instrumentation (WMI) connectivity to a remote server.

## EXAMPLES

### Example 1: Test a connection to a remote server
```
PS C:\> Test-WebSitesServer -Name "WSERVER01" -UserName "Administrator" -Password "Password01"
True
```

This command tests the connection to the server WSERVER01.

## PARAMETERS

### -ConnectionString
Specifies a connection string for a hosting database.
Connection strings contain information about a data source and how to connect to it; this information includes such things as the server and database name, and the name and password of the user account making the connection.
For example:

`-ConnectionString "Server=tcp:contosodb.database.windows.net;Database=Personel;User ID=admin@contoso.com;Password=p@ssw0rd;Trusted_Connection=False;Encrypt=True;"`

If you do not specify this parameter **Test-WebSitesServer** uses the default instance of the hosting database.

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

### -Name
Specifies the name of the server being tested.
For example:

`-Name "ContosoServer"`

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Password
Specifies password for the user account used to connect to the remote server.
For example:

`-Password "p@ssw0rd"`

If you include the *Password* parameter you must also include the *UserName* parameter in order to specify the user account for the test.
If you do not use the *UserName* and *Password* parameters the test is conducted using the credentials that the Windows PowerShell session is running under.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserName
Specifies the name of a user account used to connect to the remote server.
For example:

`-UserName "PattiF"`

If you include the *UserName* parameter you must also include the *Password* parameter in order to specify the user account password.
If you do not use these two parameters the test is conducted using the credentials that the Windows PowerShell session is running under.

```yaml
Type: String
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

[New-WebSitesServer](xref:Websites/v1.0/New-WebSitesServer.md)

[Get-WebSitesServer](xref:Websites/v1.0/Get-WebSitesServer.md)

[Set-WebSitesServer](xref:Websites/v1.0/Set-WebSitesServer.md)

[Restart-WebSitesServer](xref:Websites/v1.0/Restart-WebSitesServer.md)

[Repair-WebSitesServer](xref:Websites/v1.0/Repair-WebSitesServer.md)

[Remove-WebSitesServer](xref:Websites/v1.0/Remove-WebSitesServer.md)


