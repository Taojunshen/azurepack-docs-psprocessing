---
external help file: Microsoft.WindowsAzure.Admin.PowerShell.dll-Help.xml
ms.assetid: F495C983-3A44-419C-9E52-E00A8DE4731A
online version: http://go.microsoft.com/fwlink/?LinkID=316356
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Administration/v1.0/Set-MgmtSvcUser.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Administration/v1.0/Set-MgmtSvcUser.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Administration/v1.0/Set-MgmtSvcUser.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Set-MgmtSvcUser

## SYNOPSIS
Updates the properties of a user.

## SYNTAX

### ByProperties (Default)
```
Set-MgmtSvcUser [-Name] <String> [-Email] <String> [[-State] <UserState>]
 [[-ActivationSyncState] <ActivationSyncState>] [-AdminUri] <Uri> [-Token] <String>
 [-DisableCertificateValidation] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObject
```
Set-MgmtSvcUser [[-User] <User>] [-AdminUri] <Uri> [-Token] <String> [-DisableCertificateValidation] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-MgmtSvcUser** cmdlet updates the properties of a user.
To add a user to Windows Azure Pack for Windows Server, use the **Add-MgmtSvcUser** cmdlet.

## EXAMPLES

### Example 1: Suspend a user
```
PS C:\>Set-MgmtSvcUser -AdminUri "https://Computer01:30004" -Token $Token -Name "Patti Fuller" -Email "PattiFuller@Contoso.com" -State "Suspended"
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command changes the state of the user named Patti Fuller to Suspended.

## PARAMETERS

### -ActivationSyncState
Specifies the activation synchronization state.
Valid values are:

- InSync
- Synching
- OutOfSync

```yaml
Type: ActivationSyncState
Parameter Sets: ByProperties
Aliases: 
Accepted values: InSync, Syncing, OutOfSync

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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
Default value: False
Accept pipeline input: False
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

### -Email
Specifies the email address for the user.

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

### -Name
Specifies a name for the user.

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

### -State
Specifies a state for the user.
Valid values are:

- PendingValidation
- Active
- Suspended
- DeletePending

```yaml
Type: UserState
Parameter Sets: ByProperties
Aliases: 
Accepted values: PendingValidation, Active, Suspended, DeletePending

Required: False
Position: 4
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

### -User
Specifies a user object.

```yaml
Type: User
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
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

[Add-MgmtSvcUser](xref:Administration/v1.0/Add-MgmtSvcUser.md)

[Get-MgmtSvcUser](xref:Administration/v1.0/Get-MgmtSvcUser.md)

[Set-MgmtSvcUser](xref:Administration/v1.0/Set-MgmtSvcUser.md)

[Remove-MgmtSvcUser](xref:Administration/v1.0/Remove-MgmtSvcUser.md)


