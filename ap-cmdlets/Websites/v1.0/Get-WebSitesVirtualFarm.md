---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 5FA90DC7-CD4B-4420-B9EA-049A328E24D8
online version: http://go.microsoft.com/fwlink/?LinkID=321240
schema: 2.0.0
updated_at: 1/3/2017 9:53 PM
ms.date: 1/3/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesVirtualFarm.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesVirtualFarm.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/9b04ebf7a96dfac95b0cdb4f6ad2c39512dc39eb/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesVirtualFarm.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-WebSitesVirtualFarm

## SYNOPSIS
Gets information about a virtual server farm.

## SYNTAX

```
Get-WebSitesVirtualFarm [[-Name] <String>] [-VirtualFarmOwnerName <String>] [-RemoteSettings <RemoteSettings>]
 [-SuppressRequestIdLine] [<CommonParameters>]
```

## DESCRIPTION
The **Get-WebSitesVirtualFarm** cmdlet gets information about a virtual server farm.
A virtual server farm is a networking environment that combines virtual machines running on multiple physical servers.
Virtual servers farms are designed to such things as server consolidation; redundancy for failover; and high availability.

Used without any parameters, **Get-WebSitesVirtualFarm** returns information about all your virtual server farms.
Alternatively, you can do such things as return information for a specific farm, or for all the farms owned by a specified user.

## EXAMPLES

### Example 1: Get information about a virtual farm
```
PS C:\> Get-WebSitesVirtualFarm -Name "DefaultVirtualFarm"
```

This command returns information about the virtual farm named DefaultVirtualFarm.

## PARAMETERS

### -Name
Specifies the name of the virtual server farm being returned.
Valid values include:

- DefaultVirtualFarm
- VirtualDedicatedWorkers
- DefaultServerFarm

For example:

`-Name "VirtualDedicatedWorkers"`

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

### -VirtualFarmOwnerName
Specifies the name of a virtual server farm owner. 
For example:

`-VirtualFarmOwner "PattiF"`

When this parameter is used, Get-WebSitesVirtualFarm returns information for all the server farms owned by this user.

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

[Set-WebSitesVirtualFarm](xref:Websites/v1.0/Set-WebSitesVirtualFarm.md)


