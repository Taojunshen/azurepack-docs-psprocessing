---
external help file: Microsoft.WindowsAzure.Admin.PowerShell.dll-Help.xml
ms.assetid: 13B21138-8A17-4319-88DE-9556A8C0361C
online version: http://go.microsoft.com/fwlink/?LinkID=316342
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Administration/v1.0/Get-MgmtSvcToken.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Administration/v1.0/Get-MgmtSvcToken.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Administration/v1.0/Get-MgmtSvcToken.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcToken

## SYNOPSIS
Creates an identity token.

## SYNTAX

```
Get-MgmtSvcToken [-Type] <TokenType> [-AuthenticationSite] <Uri> [-ClientRealm] <Uri> [-User <PSCredential>]
 [-AdfsAddress <Uri>] [-AdfsRealm <Uri>] [-DisableCertificateValidation] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcToken** creates an identity token.
Tokens are used by several of the Windows Azure Pack for Windows Server cmdlets.
You can create a token and store it in a variable for use with other cmdlets.

## EXAMPLES

### Example 1: Create an identity token
```
PS C:\>$Credential = Get-Credential
PS C:\> $Token = Get-MgmtSvcToken -Type Windows -AuthenticationSite "https://Computer01:30072" -ClientRealm "http://azureservices/AdminSite" -User $Credential -DisableCertificateValidation
```

The first command prompts the user for credentials and stores the provided user name and password in the $Credential variable.

The second command creates a Windows token for the user provided in $Credential.

## PARAMETERS

### -AdfsAddress
Specifies the URI of the AD FS address.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdfsRealm
Specifies the URI of the AD FS realm.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AuthenticationSite
Specifies the URI of the authentication site.
Use the following format: https://\<computer\>:\<port\>.
For example: https://Computer01:30072.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ClientRealm
Specifies the URI of the client realm.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisableCertificateValidation
Disables certificate validation for the Windows Azure Pack installation.

If you specifiy this parameter, you can use self-signed certificates.

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
Specifies the type for the token.
Valid values are:

- Windows
- WindowsAdfs
- Membership
- MembershipAdfs

```yaml
Type: TokenType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, WindowsAdfs, Membership, MembershipAdfs, Adfs

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -User
Specifies a user account and password as a PSCredential object.
To create a PSCredential object, use the **Get-Credential** cmdlet.

```yaml
Type: PSCredential
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

