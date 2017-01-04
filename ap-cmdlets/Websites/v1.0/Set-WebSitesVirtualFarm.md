---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 9414226F-4F36-4D5A-BD53-B39505CFE762
online version: http://go.microsoft.com/fwlink/?LinkID=321274
schema: 2.0.0
updated_at: 1/3/2017 9:53 PM
ms.date: 1/3/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Set-WebSitesVirtualFarm.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Set-WebSitesVirtualFarm.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/9b04ebf7a96dfac95b0cdb4f6ad2c39512dc39eb/AzurePack-cmdlets/Websites/v1.0/Set-WebSitesVirtualFarm.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Set-WebSitesVirtualFarm

## SYNOPSIS
Sets the property values of a virtual server farm.

## SYNTAX

```
Set-WebSitesVirtualFarm [-Name] <String> [-OwnerName <String>] [-MaximumSiteWeight <Int32>]
 [-ExclusiveAssignment <Boolean>] [-TargetNumberOfWorkers <Int32>] [-TargetWorkerSize <Int32>]
 [-RemoteSettings <RemoteSettings>] [-SuppressRequestIdLine] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-WebSitesVirtualFarm** cmdlet sets the property values of a virtual server farm.
A virtual server farm is a networking environment that combines virtual machines running on multiple physical servers.
Virtual servers farms are designed to provide capabilities like: server consolidation; redundancy for failover; and high availability.
This cmdlet enables you to do such things as manage the workers assigned to a farm; change the name of a farm; and assign ownership of a farm.

## EXAMPLES

### Example 1: Modify a virtual server farm
```
PS C:\> Set-WebSitesVirtualFarm -Name "Farm01" -ExclusiveAssignment $True -TargetWorkerSize "Large"
```

This command updates the virtual server farm Farm01, setting the target worker size to Large and specifying that Farm01 workers cannot be simultaneously assigned to other servers farms.

## PARAMETERS

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

### -ExclusiveAssignment
Indicates whether a worker is exclusive to the virtual server farm.
Set this value to True ($True) to limit workers to the specified farm.
Set this value to False ($False) to allow workers to process tasks for other server farms.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaximumSiteWeight
Specifies the maximum site weight for the virtual server farm.
Site weights are used in load balancing, with higher values  taking priority over lower values.
For example:

`-MaximumSiteWeight 25`

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of the virtual server farm being modified.

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

### -OwnerName
Specifies the name of the farm owner.
For example:

`-OwnerName "PattiF"`

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

### -TargetNumberOfWorkers
Specifies the number of web workers allocated to the server farm.
The number of allowed works varies depending on the site mode:

- If the site mode is Free, you can allocate 1 worker to the site. 
- If the site mode is Shared, you can allocate between 1 and 6 workers, inclusive, to the site.
- If the site mode is Standard, you can allocate between 1 and 10 workers, inclusive, to the site.

This parameter is ignored if a site is in reserve mode.

For example:

`-TargetNumberOfWorkers 3`

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetWorkerSize
Specifies the size of the target worker for the virtual server farm.
Valid values are:

- Small
- Medium
- Large

For example:

`-TargetWorkerSize "Medium"`

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

[Get-WebSitesVirtualFarm](xref:Websites/v1.0/Get-WebSitesVirtualFarm.md)


