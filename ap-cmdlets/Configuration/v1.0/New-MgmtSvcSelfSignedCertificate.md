---
external help file: Microsoft.WindowsAzure.Config.PowerShell.dll-Help.xml
ms.assetid: 52D63EC1-0D74-4138-A7BA-41CF19C779DE
online version: http://go.microsoft.com/fwlink/?LinkID=320944
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/New-MgmtSvcSelfSignedCertificate.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Configuration/v1.0/New-MgmtSvcSelfSignedCertificate.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Configuration/v1.0/New-MgmtSvcSelfSignedCertificate.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# New-MgmtSvcSelfSignedCertificate

## SYNOPSIS
Creates a self-signed certificate.

## SYNTAX

```
New-MgmtSvcSelfSignedCertificate -Subject <String> -StoreLocation <StoreLocation> -StoreName <StoreName>
 [-Password <SecureString>] [<CommonParameters>]
```

## DESCRIPTION
The **New-MgmtSvcSelfSignedCertificate** cmdlet creates a self-signed certificate.

## EXAMPLES

### 1:
```
PS C:\>$Password = ConvertTo-SecureString "PassWord01!" -AsPlainText -Force
PS C:\> New-MgmtSvcSelfSignedCertificate -StoreLocation "LocalMachine" -StoreName "Root" -Subject "CN=Admin,DC=Contoso,DC=com" -Password $Password
```

## PARAMETERS

### -Password
Specifies a password as a secure string object.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StoreLocation
Specifies the store location for the certificate.
Valid values for this parameter are:

- CurrentUser
- LocalMachine

```yaml
Type: StoreLocation
Parameter Sets: (All)
Aliases: 
Accepted values: CurrentUser, LocalMachine

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StoreName
Specifies the store name for the certificate.
Valid values for this parameter are:

- AddressBook
- AuthRoot
- CertificateAuthority
- Disallowed
- My
- Root
- TrustedPeople
- TrustedPublisher

```yaml
Type: StoreName
Parameter Sets: (All)
Aliases: 
Accepted values: AddressBook, AuthRoot, CertificateAuthority, Disallowed, My, Root, TrustedPeople, TrustedPublisher

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subject
Specifies a subject for the certificate.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

