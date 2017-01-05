---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 239D6D67-FB9E-47B7-992E-5872E62F9FCD
online version: http://go.microsoft.com/fwlink/?LinkID=321230
schema: 2.0.0
updated_at: 1/4/2017 6:14 PM
ms.date: 1/4/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesEvent.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/live/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesEvent.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/34620cb46df1eb18f9e1c9a42639b53390ad35e3/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesEvent.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-WebSitesEvent

## SYNOPSIS
Gets events from the event log.

## SYNTAX

```
Get-WebSitesEvent [[-ComputerName] <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-InUtc] [-Loop]
 [-RemoteSettings <RemoteSettings>] [-SuppressRequestIdLine] [<CommonParameters>]
```

## DESCRIPTION
The **Get-WebSitesEvent** cmdlet gets website events from your event logs.
Used without any parameters, **Get-WebSitesEvent** returns event log events from all your website servers.
Alternatively, you can choose to return events from a specified server.
By default, **Get-WebSitesEvent** returns all the events in an event log.
However, you can use the *StartTime* and *EndTime* parameters to limit the returned data to events recorded during a specified timeframe.
For example, you might return only those events recorded on a specific day or during a specific hour.

## EXAMPLES

### Example 1: Get all events
```
PS C:\> Get-WebSitesEvent
```

This command returns all the website events from all of the servers in the farm.

### Example 2: Get all events for a server
```
PS C:\> Get-WebSitesEvent -ComputerName "Server01"
```

This command returns all the website events for Server01.

### Example 3: Get all events for a specified timeframe
```
PS C:\> Get-WebSitesEvent -StartTime "7/25/2013 10:57:10 PM" -EndTime "7/25/2013 10:57:12 PM"
```

This command returns all the events recorded in the specified timeframe for all your servers.

### Example 4: Get specified events for a server
```
PS C:\> Get-WebSitesEvent -StartTime "7/25/2013 10:57:10 PM" -EndTime "7/25/2013 10:57:12 PM" -ComputerName "Server01"
```

This command returns all the events recorded in the specified timeframe on Server01.

## PARAMETERS

### -ComputerName
Specifies the name of the server for which events are returned.
For example:

`-ComputerName "ContosoServer"`

If this parameter is not used **Get-WebSitesEvent** returns events from all your servers.

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

### -EndTime
Specifies the ending date and time for events returned for a specific timespan.
For example, if you want to only return events that occurred between March 1, 2016 and March 10, 2016, the *EndTime* parameter syntax would look similar to this (the exact format depends on how you have configured your computer's Region settings):

`-EndTime "3/10/2016"`

This parameter can only be used in conjunction with the *StartTime* parameter, and the end time must be later than the start time.

If you omit the *EndTime* and *StartTime* parameters **Get-WebSitesEvent** returns all the available events.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InUtc
{{Fill InUtc Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Loop
{{Fill Loop Description}}

```yaml
Type: SwitchParameter
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

### -StartTime
Specifies the starting date and time for events returned for a specific timespan.
For example, if you want to only return events that occurred between March 1, 2016 and March 10, 2016, the *StartTime* parameter syntax would look similar to this (the exact format depends on how you have configured your computer's Region settings):

`-StartTime "3/1/2016"`

This parameter can only be used in conjunction with the *EndTime* parameter, and the start time must be earlier than the end time.

If you omit the *EndTime* and *StartTime* parameters **Get-WebSitesEvent** returns all the available events.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

