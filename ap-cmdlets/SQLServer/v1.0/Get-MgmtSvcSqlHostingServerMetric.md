---
external help file: Microsoft.WindowsAzure.SqlServer.PowerShell.dll-Help.xml
ms.assetid: 29BD5519-E221-492E-B64C-13330CEA3FC0
online version: http://go.microsoft.com/fwlink/?LinkID=321812
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/SQLServer/v1.0/Get-MgmtSvcSqlHostingServerMetric.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/SQLServer/v1.0/Get-MgmtSvcSqlHostingServerMetric.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/SQLServer/v1.0/Get-MgmtSvcSqlHostingServerMetric.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-MgmtSvcSqlHostingServerMetric

## SYNOPSIS
Gets capacity metrics for a SQL Server hosting server.

## SYNTAX

```
Get-MgmtSvcSqlHostingServerMetric [-HostingServerId] <String> [[-MetricName] <String[]>]
 [[-StartTime] <DateTime>] [[-EndTime] <DateTime>] [-AdminUri] <Uri> [-Token] <String>
 [-DisableCertificateValidation] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MgmtSvcSqlHostingServerMetric** cmdlet gets metrics for a SQL Server hosting server.
By default, all metrics for a specified hosting server are returned.
To get a specific metric, use the *MetricName* parameter.
You can also narrow your results by using the *StartTime* and *EndTime* parameters to specify a date range.

## EXAMPLES

### Example 1: Get the metrics for DatabaseCount
```
PS C:\>Get-MgmtSvcSqlHostingServerMetric -AdminUri "https://Computer01:30004" -Token $Token -HostingServerId "u37k25" -MetricName DatabaseCount
```

NOTE: This example assumes that you have created a token by using **Get-MgmtSvcToken** and have stored it in a variable named $Token.

This command gets the DatabaseCount metrics for the hosting server with the ID of u37k25.

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

### -EndTime
Specifies the end time of the date range as a **DateTime** object.
To create a **DateTime** object, use the **Get-Date** cmdlet.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HostingServerId
Specifies the ID of a SQL Server hosting server.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MetricName
Specifies an array of metric names.
You can get the following metrics: DatabaseCount, TotalAllottedSpace.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartTime
Specifies the start time of the date range as a **DateTime** object.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### ResourceMetricSets
This cmdlet emits a **ResourceMetricSets** object.

## NOTES

## RELATED LINKS

[Get-MgmtSvcSqlHostingServer](xref:SQLServer/v1.0/Get-MgmtSvcSqlHostingServer.md)


