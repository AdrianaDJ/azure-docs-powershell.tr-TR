---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: c139e1bac6f910a1759e4482abdd7c67d2e7fa55
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108434"
---
# Get-AzVMAccessExtension

## SYNOPSIS
VMAccess uzantısı hakkında bilgi alır.

## INDEKI

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azvmaccessextenma** cmdlet 'ı sanal makine erişimi (VMAccess) sanal makine uzantısı hakkında bilgi alır.

## ÖRNEKLERDEN

### Örnek 1: VMAccess uzantısını alma
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

Bu komut, VirtualMachine07 adındaki sanal makine için ContosoTest adındaki VMAccess uzantısını alır.

### Örnek 2: VMAccess uzantısının örnek görünümünü alma
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

Bu komut, VirtualMachine07 adındaki sanal makine için ContosoTest adındaki VMAccess uzantısının örnek görünümünü alır.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Bu cmdlet 'in aldığı uzantının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Sanal makinenin kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Durum
Bu cmdlet 'in yalnızca uzantının örnek görünümünü aldığını gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Sanal makinenin adını belirtir.
Bu cmdlet, bu parametrenin belirttiği sanal makinede VMAccess hakkında bilgi alır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### System. Management. Automation. SwitchParameter

## ÇıKıŞLAR

### Microsoft. Azure. Commands. COMPUTE. modeller. VirtualMachineAccessExtensionContext

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Remove-azvmaccessexten](./Remove-AzVMAccessExtension.md)

[Set-azvmaccessexten](./Set-AzVMAccessExtension.md)

[Get-Azvmexgeri](./Get-AzVMExtension.md)


