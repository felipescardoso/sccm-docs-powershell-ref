<<<<<<< HEAD
---
title: Disable-CMAlert
titleSuffix: Configuration Manager
description: Disables alerts in Configuration Manager.
ms.date: 04/29/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
=======
﻿---
external help file: AdminUI.PS.Alerts.dll-Help.xml
ms.assetid: 57F5F380-5A44-42B2-8CCE-EC72F4D3E701
online version: https://go.microsoft.com/fwlink/?linkid=833935
schema: 2.0.0
>>>>>>> master
---

# Disable-CMAlert

## SYNOPSIS

Disables alerts in Configuration Manager.

## SYNTAX

### SearchByValueMandatory (Default)

```powershell
Disable-CMAlert -InputObject <IResultObject> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory

```powershell
Disable-CMAlert -Id <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory

```powershell
Disable-CMAlert -Name <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Disable-CMAlert** cmdlet disables one or more alerts in Microsoft System Center Configuration Manager.

System Center Configuration Manager does not evaluate the condition for a disabled alert and does not update a disabled alert, even if the state of the alert changes.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Disable an alert by using alert ID

```powershell
PS XYZ:\>Disable-CMAlert -Id "16777218"
```

This command disables an alert that has the ID 16777218.

### Example 2: Disable an alert by using alert object variable

```powershell
PS XYZ:\> $AlertObj = Get-CMAlert -Id "16777221"
PS XYZ:\> Disable-CMAlert -InputObject $AlertObj
```

The first command gets an alert object that has the ID 16777221, and then stores it in the $AlertObj variable.

The second command disables the alert stored in the $AlertObj variable.

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

### -DisableWildcardHandling

DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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

### -ForceWildcardHandling

ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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

### -Id

Specifies an alert ID.
You can obtain the ID of an alert by using the [Get-CMAlert](Get-CMAlert.md) cmdlet.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specifies a **CMAlert** object.
To obtain a **CMAlert** object, use **Get-CMAlert**.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: Alert

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specifies the name of an alert.
You can obtain the name of an alert by using **Get-CMAlert**.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

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

[Enable-CMAlert](Enable-CMAlert.md)

[Get-CMAlert](Get-CMAlert.md)

[Remove-CMAlert](Remove-CMAlert.md)

[Set-CMAlert](Set-CMAlert.md)

[Suspend-CMAlert](Suspend-CMAlert.md)
