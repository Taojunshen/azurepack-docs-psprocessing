---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: DE1708F2-569C-4098-BCED-20B175DBD884
online version: http://go.microsoft.com/fwlink/?LinkID=321275
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Start-WebSitesOperation.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Start-WebSitesOperation.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/Start-WebSitesOperation.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Start-WebSitesOperation

## SYNOPSIS
Starts a DWAS operation.

## SYNTAX

```
Start-WebSitesOperation [-OperatorName] <String> [-OperationName] <String> [-Parameters] <Hashtable>
 [-WaitForCompletion] [[-Timeout] <TimeSpan>] [-RemoteSettings <RemoteSettings>] [-SuppressRequestIdLine]
 [<CommonParameters>]
```

## DESCRIPTION
The **Start-WebSitesOperation** cmdlet starts a Dynamic Windows Activation Service (DWAS) operation.
DWAS is designed to carry out such tasks as:

- Provisioning and activating sites. 
- Starting and monitoring worker processes. 
- Shutting down and deprovisioning sites. 
- Overseeing sandbox and security measures.

## EXAMPLES

### Example 1: Start an upgrade on all front-end servers
```
PS C:\> Start-WebSitesOperation -OperatorName "WFF" -OperationName "Upgrade" -Parameters @{"WebFarmName"="FrontEndServers"}
```

This command starts an upgrade operation on front-end servers.

### Example 2: Start an upgrade on a specific worker server
```
PS C:\>Start-Operation -OperatorName "WFF" -OperationName "Upgrade" -Parameters @{"WebFarmName"="WorkerServers";ServerName="SERVER01"}
```

This command starts an upgrade operation on the server named Server01.

## PARAMETERS

### -OperationName
Specifies the name of the operation being started.
For example:

`-OperationName "Upgrade"`

The most commonly-used operations are Upgrade and Repair.

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

### -OperatorName
Specifies the name of the operator under which the role runs.
For example:

`-OperatorName "WFF"`

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Parameters
Specifies a hash table containing parameters for the operation.
These parameters typically consist of a server farm name and/or a server name For example, this syntax uses a single parameter (WebFarmName) that specifies a web farm:

`-Parameters @{"WebFarmName"="FrontEndServers"}`

To use multiple parameters, separate the parameters by using a semicolon.
For example, this syntax uses two parameters (WebFarmName and ServerName):

`-Parameters @{"WebFarmName"="WorkerServers";ServerName="SERVER01"}`

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
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

### -Timeout
Specifies the maximum time (in seconds) to wait for the operation to finish.

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WaitForCompletion
Indicates that the cmdlet waits for the operation to finish before it returns control to the Windows PowerShell console or the calling script.
If not specified, control returns immediately, and the command runs in the background.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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

[Get-WebSitesOperation](xref:Websites/v1.0/Get-WebSitesOperation.md)

[Remove-WebSitesOperation](xref:Websites/v1.0/Remove-WebSitesOperation.md)


