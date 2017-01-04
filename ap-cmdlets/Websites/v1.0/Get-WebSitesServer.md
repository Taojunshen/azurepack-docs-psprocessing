---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: 857FADA8-4DE9-4B1F-BCE5-1045E100DEE9
online version: http://go.microsoft.com/fwlink/?LinkID=321234
schema: 2.0.0
updated_at: 1/3/2017 9:53 PM
ms.date: 1/3/2017
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesServer.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesServer.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/9b04ebf7a96dfac95b0cdb4f6ad2c39512dc39eb/AzurePack-cmdlets/Websites/v1.0/Get-WebSitesServer.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Get-WebSitesServer

## SYNOPSIS
Gets configuration information for a website server.

## SYNTAX

```
Get-WebSitesServer [[-Name] <String>] [[-ServerType] <ServerRole>] [-RemoteSettings <RemoteSettings>]
 [-SuppressRequestIdLine] [<CommonParameters>]
```

## DESCRIPTION
The **Get-WebSitesServer** cmdlet returns information about your website servers.
Used without any parameters, **Get-WebSitesServer** returns information for all your servers.
However, if you want to limit the returned data to a single server, you can include the *Name* parameter and specify the name of that server.
You can also use the *ServerType* parameter to return information for specific types of servers.
Available server types include:

- Controller. Manages and provisions other website roles. 

- ManagementServer. Manages the website infrastructure. 

- LoadBalancer. Distributes and manages web traffic. 

- WebWorker. Hosts websites. 

- Publisher. Publishes content to file servers. 

- FileServer. Stores website content.

## EXAMPLES

### Example 1: Get information for a server
```
PS C:\> Get-WebSitesServer -Name "WServer01"
```

This command returns information for the server named WServer01.

### Example 2: Get information for a server type
```
PS C:\> Get-WebSitesServer -ServerType "WebWorker"
```

This command returns information for all servers assigned the WebWorker role.

## PARAMETERS

### -Name
Specifies the host name of the server whose configuration information is being retrieved.
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

### -ServerType
Specifies the type of server for which information is being returned.
Valid values are:

- Controller. Manages and provisions other website roles. 
- ManagementServer. Manages the website infrastructure. 
- LoadBalancer. Distributes and manages web traffic. 
- WebWorker. Hosts websites. 
- Publisher. Publishes content to file servers. 
- FileServer. Stores website content.

For example:

`-ServerType "FileServer"`

If this parameter is not used, **Get-WebSitesServer** returns information for all server roles.

```yaml
Type: ServerRole
Parameter Sets: (All)
Aliases: 
Accepted values: Controller, ManagementServer, LoadBalancer, WebWorker, Publisher, FileServer, MultiRole

Required: False
Position: 1
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

[New-WebSitesServer](xref:Websites/v1.0/New-WebSitesServer.md)

[Set-WebSitesServer](xref:Websites/v1.0/Set-WebSitesServer.md)

[Test-WebSitesServer](xref:Websites/v1.0/Test-WebSitesServer.md)

[Restart-WebSitesServer](xref:Websites/v1.0/Restart-WebSitesServer.md)

[Repair-WebSitesServer](xref:Websites/v1.0/Repair-WebSitesServer.md)

[Remove-WebSitesServer](xref:Websites/v1.0/Remove-WebSitesServer.md)


