---
external help file: Microsoft.Web.Hosting.Powershell.dll-Help.xml
ms.assetid: C26169DA-E6AC-4D21-96EB-AA567D49D533
online version: http://go.microsoft.com/fwlink/?LinkID=321271
schema: 2.0.0
updated_at: 12/12/2016 9:25 PM
ms.date: 12/12/2016
content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Set-WebSitesPolicy.md
original_content_git_url: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/master/AzurePack-cmdlets/Websites/v1.0/Set-WebSitesPolicy.md
gitcommit: https://github.com/MicrosoftDocs/azurepack-docs-powershell/blob/b83cde31c8e8df3140400b62cc6698cfc8f37a47/AzurePack-cmdlets/Websites/v1.0/Set-WebSitesPolicy.md
ms.topic: reference
author: tarameyer
ms.author: sngun
keywords: powershell, cmdlet
manager: byronr
open_to_public_contributors: true
ms.service: Azure-pack
---

# Set-WebSitesPolicy

## SYNOPSIS
Modifies a website site policy.

## SYNTAX

```
Set-WebSitesPolicy [-PlanName] <String> [-ComputeMode] <ComputeModeOptions> [-SiteMode] <String>
 [[-CpuLimitPercentage] <Double>] [[-CpuLimitPeriodInMinutes] <Int32>] [[-CpuLimitAction] <Int32>]
 [[-MemoryLimitInMB] <Int32>] [[-MemoryLimitWorkingSetInMB] <Int32>] [[-FailProtectionLimit] <Int32>]
 [[-FailProtectionPeriodInSeconds] <Int32>] [[-FailProtectionPenaltyPeriodInSeconds] <Int32>]
 [[-IdleTimeoutInMinutes] <Int32>] [[-IdleTimeoutAction] <IdleTimeoutActionOptions>] [[-IdlePriority] <Int32>]
 [[-WorkerProcessLimit] <Int32>] [[-FastCgiProcessLimit] <Int32>] [[-HttpQueueLength] <Int32>]
 [[-CustomDomainsEnabled] <Boolean>] [[-SniBasedSslEnabled] <Boolean>] [[-IpBasedSslEnabled] <Boolean>]
 [[-FtpEnabled] <Boolean>] [[-FtpsEnabled] <Boolean>] [[-CsmOverHTTPEnabled] <Boolean>]
 [[-CsmOverHTTPsEnabled] <Boolean>] [[-WebDeployOverHTTPEnabled] <Boolean>]
 [[-WebDeployOverHTTPsEnabled] <Boolean>] [[-KuduOverHTTPEnabled] <Boolean>]
 [[-KuduOverHTTPsEnabled] <Boolean>] [[-IpBasedSslMode] <IpBasedSslModeOptions>]
 [[-WorkerProcess64BitEnabled] <Boolean>] [[-WorkerProcess64BitAsDefault] <Boolean>]
 [[-WebSocketsEnabled] <Boolean>] [[-AlwaysOnEnabled] <Boolean>] [[-AppConcurrentRequestLimit] <Int32>]
 [[-WebSocketConcurrentRequestLimit] <Int32>] [-RemoteSettings <RemoteSettings>] [-SuppressRequestIdLine]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-WebSitesPolicy** cmdlet modifies a website site policy.

## EXAMPLES

### Example 1: Configure a site policy
```
PS C:\> Set-WebSitesPolicy -PlanName "04838e4a-7b3f-4360-a122-41739ef9f3bb" -ComputeMode "Shared" -SiteMode "Basic" -MemoryLimitInMB 384 -MemoryLimitWorkingSetInMB 256 -HttpQueueLength 2000 -CustomDomainsEnabled $True -SniBasedSslEnabled $True -IpBasedSslEnabled $True -IpBasedSslMode "Ipv4AndIpv6" -WorkerProcess64BitEnabled $True -WorkerProcess64BitAsDefault $False -WebSocketsEnabled $True -AppConcurrentRequestLimit 6000 -IdleTimeoutAction "Suspend"
```

This command configures the site policy for sites in Basic mode that have the plan name 04838e4a-7b3f-4360-a122-41739ef9f3bb (this plan name corresponds to the subscription ID).

## PARAMETERS

### -AlwaysOnEnabled
{{Fill AlwaysOnEnabled Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 32
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AppConcurrentRequestLimit
Specifies the maximum number of concurrent HTTP requests that a single worker process can service.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 33
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ComputeMode
Specifies the type of hosting environment that the web site runs in.
Valid values are:

- Shared. The web site runs in a shared/multi-tenant hosting environment. 

- Dedicated. The web site runs in its own dedicated hosting environment.

For example:

`-ComputeMode "Shared"`

```yaml
Type: ComputeModeOptions
Parameter Sets: (All)
Aliases: 
Accepted values: Shared, Dedicated

Required: True
Position: 1
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

### -CpuLimitAction
{{Fill CpuLimitAction Description}}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CpuLimitPercentage
Specifies the CPU limit percentage for sites under this policy.
This parameter is used with the *CpuLimitPeriod* parameter to prevent a single worker process from using a large amount of CPU resources over an extended period of time.

For example, suppose you specify a value of 80 for the CpuLimitPercentage property and a value of 3 minutes for the CpuLimitPeriod property.
If a worker process consumes 80% or more of CPU resources over a period of 3 minutes, the worker process will be "throttled" in order to reduce its CPU usage.

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CpuLimitPeriodInMinutes
{{Fill CpuLimitPeriodInMinutes Description}}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CsmOverHTTPEnabled
{{Fill CsmOverHTTPEnabled Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CsmOverHTTPsEnabled
{{Fill CsmOverHTTPsEnabled Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 23
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomDomainsEnabled
Indicates that sites can use custom domain names.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FailProtectionLimit
Specifies the number of times a worker process can fail before it is suspended.
Fail protection works by specifying values for three properties:

-- FailProtectionLimit (for example, 5 failures) 
- FailProtectionPeriod (for example 2 minutes) 
- FailProtectionPenaltyPeriod (for example, 10 minutes)

The system then monitors a process for 2 minutes (the time specified by the FailProtectionPeriod property).
Should 5 failures (the number specified by the FailProtectionLimit property) occur during that time span, the process will be shut down.
The system then waits 10 minutes (the time specified by FailProtectionPenaltyPeriod property) before restarting the process.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FailProtectionPenaltyPeriodInSeconds
{{Fill FailProtectionPenaltyPeriodInSeconds Description}}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FailProtectionPeriodInSeconds
{{Fill FailProtectionPeriodInSeconds Description}}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FastCgiProcessLimit
Specifies the maximum number of FastCGI processes that a single worker process can create.
FastCGI is a programming interface that facilitates communication between a web server and an application.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FtpEnabled
{{Fill FtpEnabled Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FtpsEnabled
{{Fill FtpsEnabled Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HttpQueueLength
Specifies the maximum number of HTTP requests that can be in the HTTP queue at any one time.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdlePriority
{{Fill IdlePriority Description}}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdleTimeoutAction
Specifies the action taken on idle worker processes.
Valid values are:

- 0 or Shutdown. The process is shut down. 

- 1 or Suspend. Thus process is suspended. This value can only be used with Windows Server 2012 R2.

For example:

`-IdleTimeOutAction "Suspend"`

```yaml
Type: IdleTimeoutActionOptions
Parameter Sets: (All)
Aliases: 
Accepted values: Terminate, Suspend

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdleTimeoutInMinutes
{{Fill IdleTimeoutInMinutes Description}}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpBasedSslEnabled
Indicates that IP-based SSL is enabled.
IP-based SSL associates a certificate and a domain name by mapping the public IP address of the server to the domain name.
Among other things, this means that all of your servers must have a dedicated IP address.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpBasedSslMode
Specifies the supported IP address types.
Valid values are:

- Ipv4

- Ipv6

- Ipv4AndIpv6

For example:

`-IpBasedSslMode "IPv6"`

```yaml
Type: IpBasedSslModeOptions
Parameter Sets: (All)
Aliases: 
Accepted values: Ipv4, Ipv6, Ipv4AndIpv6

Required: False
Position: 28
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KuduOverHTTPEnabled
{{Fill KuduOverHTTPEnabled Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 26
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KuduOverHTTPsEnabled
{{Fill KuduOverHTTPsEnabled Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 27
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MemoryLimitInMB
Specifies the amount of memory, in megabytes, assigned to.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MemoryLimitWorkingSetInMB
Specifies the amount of memory, in megabytes, that a working set can use.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PlanName
Specifies a name for the plan.
For example:

`-PlanName "Standard"`

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

### -SiteMode
Specifies the site mode of the policy.
Valid values are:

- Basic. Used with the Shared, Basic, and Standard plans. 

- Limited. Used with the Free plan.

For example:

`-SiteMode "Basic"`

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Limited, Dedicated

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SniBasedSslEnabled
Indicates that SNI-based (Server Name Indication) SSL is enabled.
SNI allows a server to associate multiple SSL certificates with a single IP address.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 18
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

### -WebDeployOverHTTPEnabled
{{Fill WebDeployOverHTTPEnabled Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 24
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WebDeployOverHTTPsEnabled
{{Fill WebDeployOverHTTPsEnabled Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 25
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WebSocketConcurrentRequestLimit
{{Fill WebSocketConcurrentRequestLimit Description}}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 34
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WebSocketsEnabled
Indicates that WebSockets are enabled.
Web sockets facilitate bidirectional communication between a client and a server.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 31
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

### -WorkerProcess64BitAsDefault
Indicates that sites run 64-bit worker processes by default.
When enabled, administrators who do not want to use 64-bit worker processes must manually modify a site to allow 32-bit processing.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 30
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WorkerProcess64BitEnabled
Indicates that sites can run 64-bit worker processes.
When enabled, sites will continue to use 32-bit processing by default.
However, administrators can manually enable 64-bit processing for a site.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 29
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WorkerProcessLimit
Specifies the maximum number of worker processes that can run on a single worker.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
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

[New-WebSitesPolicy](xref:Websites/v1.0/New-WebSitesPolicy.md)

[Get-WebSitesPolicy](xref:Websites/v1.0/Get-WebSitesPolicy.md)

[Remove-WebSitesPolicy](xref:Websites/v1.0/Remove-WebSitesPolicy.md)


