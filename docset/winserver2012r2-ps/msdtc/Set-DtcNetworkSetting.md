---
external help file: MSFT_DtcNetworkSettingTask_v1.0.cdxml-help.xml
Module Name: MsDtc
online version: 
schema: 2.0.0
title: Set-DtcNetworkSetting
description: 
keywords: powershell, cmdlet
author: brianlic
manager: alanth
ms.date: 2017-10-29
ms.topic: reference
ms.prod: powershell
ms.technology: powershell
ms.assetid: 104F9A14-DBE9-4C5B-9F66-54E2A1C95761
---

# Set-DtcNetworkSetting

## SYNOPSIS
Modifies DTC network and security configuration for a DTC instance.

## SYNTAX

### NetworkSettings
```
Set-DtcNetworkSetting [-DtcName <String>] [-InboundTransactionsEnabled <Boolean>]
 [-OutboundTransactionsEnabled <Boolean>] [-RemoteClientAccessEnabled <Boolean>]
 [-RemoteAdministrationAccessEnabled <Boolean>] [-XATransactionsEnabled <Boolean>]
 [-LUTransactionsEnabled <Boolean>] [-AuthenticationLevel <String>] [-CimSession <CimSession[]>]
 [-ThrottleLimit <Int32>] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisableNetwork
```
Set-DtcNetworkSetting [-DtcName <String>] [-DisableNetworkAccess] [-CimSession <CimSession[]>]
 [-ThrottleLimit <Int32>] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-DtcNetworkSetting** cmdlet modifies the Distributed Transaction Coordinator (DTC) network and security configuration for the DTC instance specified by the **DtcName** parameter.
This cmdlet also restarts the DTC instance.

## EXAMPLES

### Example 1: Modify network and security settings
```
PS C:\> Set-DtcNetworkSetting -DtcName "Local" -AuthenticationLevel "Incoming" -InboundTransactionsEnabled $False
PS C:\> Get-DtcNetworkSetting -DtcName "Local"
__GENUS                           : 2
__CLASS                           : DtcNetworkSettings
__SUPERCLASS                      :
__DYNASTY                         : DtcNetworkSettings
__RELPATH                         : 
__PROPERTY_COUNT                  : 7
__DERIVATION                      : {}
__SERVER                          :
__NAMESPACE                       :
__PATH                            :
AuthenticationLevel               : Mutual
InboundTransactionsEnabled        : True
LUTransactionsEnabled             : True
OutboundTransactionsEnabled       : True
RemoteAdministrationAccessEnabled : True
RemoteClientAccessEnabled         : True
XATransactionsEnabled             : True
```

The first command modifies the DTC network and security settings for the local DTC instance.
The second command verifies the changes.

## PARAMETERS

### -AsJob
{{Fill AsJob Description}}

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

### -AuthenticationLevel
Sets the network authentication level of the DTC instance to NoAuth, Incoming, or Mutual.

```yaml
Type: String
Parameter Sets: NetworkSettings
Aliases: 
Accepted values: NoAuth, Incoming, Mutual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CimSession
Runs the cmdlet in a remote session or on a remote computer.
Enter a computer name or a session object, such as the output of a New-CimSessionhttp://go.microsoft.com/fwlink/p/?LinkId=227967 or Get-CimSessionhttp://go.microsoft.com/fwlink/p/?LinkId=227966 cmdlet.
The default is the current session on the local computer.

```yaml
Type: CimSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -DisableNetworkAccess
Specifies whether to disable network access for the DTC instance.

```yaml
Type: SwitchParameter
Parameter Sets: DisableNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DtcName
Specifies a DTC instance.
If you do not specify this parameter, or if you specify a value of Local, this cmdlet modifies the local DTC instance.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -InboundTransactionsEnabled
Indicates whether to enable inbound transactions to the DTC instance.

```yaml
Type: Boolean
Parameter Sets: NetworkSettings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LUTransactionsEnabled
Indicates whether to enable LU transactions in the DTC instance.

```yaml
Type: Boolean
Parameter Sets: NetworkSettings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutboundTransactionsEnabled
Indicates whether to enable outbound transactions from the DTC instance.

```yaml
Type: Boolean
Parameter Sets: NetworkSettings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteAdministrationAccessEnabled
Indicates whether to enable remote administration access for the DTC instance.

```yaml
Type: Boolean
Parameter Sets: NetworkSettings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteClientAccessEnabled
Indicates whether to enable remote client access for the DTC instance.

```yaml
Type: Boolean
Parameter Sets: NetworkSettings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThrottleLimit
Specifies the maximum number of concurrent operations that can be established to run the cmdlet.
If this parameter is omitted or a value of `0` is entered, then Windows PowerShell® calculates an optimum throttle limit for the cmdlet based on the number of CIM cmdlets that are running on the computer.
The throttle limit applies only to the current cmdlet, not to the session or to the computer.

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

### -XATransactionsEnabled
Indicates whether to enable XA transactions in the DTC instance.

```yaml
Type: Boolean
Parameter Sets: NetworkSettings
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

[Get-DtcNetworkSetting](./Get-DtcNetworkSetting.md)
