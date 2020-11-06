---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
ms.openlocfilehash: 774166f88e4ca94e5e21c2b96817596c082a429c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586973"
---
# Remove-AzureRmVMDataDisk

## SYNOPSIS
Sanal makineden veri diskini kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Remove-Azurermvmdatadısk** cmdlet 'i, bir sanal makineden veri diskini kaldırır.

## ÖRNEKLERDEN

### Örnek 1: sanal makineden veri diskini kaldırma
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

İlk komut VirtualMachine07 adındaki sanal makineyi **Get-AzureRmVM** cmdlet 'ini kullanarak alır.
Komut, $VirtualMachine değişkeninde sanal makineyi depolar.

İkinci komut, $VirtualMachine depolanan sanal makineden disk3 adlı veri diskini kaldırır.

Son komutu, ResourceGroup11 'da $VirtualMachine depolanan sanal makinenin durumunu güncelleştirir.

## PARAMETRELERINE

### -DataDiskNames
Bu cmdlet 'in kaldırdığı bir veya birden çok veri diskine ait adları belirtir.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Veri diskinin kaldırılacağı yerel sanal makine nesnesini belirtir.
Sanal makine nesnesi edinmek için Get-AzureRmVM cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureRmVMDataDisk](./Add-AzureRmVMDataDisk.md)

[Get-AzureRmVM](./Get-AzureRmVM.md)


