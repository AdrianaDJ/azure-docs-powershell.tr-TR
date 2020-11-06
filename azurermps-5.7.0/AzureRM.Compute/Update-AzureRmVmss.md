---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: 4511aadaad23e47018a12365f6fb8fb346117b0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586761"
---
# Update-AzureRmVmss

## SYNOPSIS
Bir VMSUBNET 'in durumunu güncelleştirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Update-AzureRmVmss [-ResourceGroupName] <String> -VMScaleSetName <String>
 [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Update-AzureRmVmss** cmdlet 'ı sanal makine ölçek kümesi 'nın (VMSS) durumunu yerel BIR VMSS nesnesinin durumuna güncelleştirir.

## ÖRNEKLERDEN

### Örnek 1: bir VMSS durumunu yerel bir VMSS nesnesinin durumuna güncelleyin.
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet "LocalVMSS"
```

Bu komut, Group001 adındaki kaynak grubuna ait olan ve VMSS001 adındaki kaynak grubuna ait olan, LocalVMSS adlı yerel bir VMSS nesnesinin durumuna ait durumunu güncelleştirir.

## PARAMETRELERINE

### -ResourceGroupName
VMSS 'nin ait olduğu kaynak grubunun adını belirtir.

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

### -VirtualMachineScaleSet
Yerel bir VMSS nesnesini belirtir.
Bir VMSS nesnesi edinmek için Get-AzureRmVmss cmdlet 'ini kullanın.
Bu sanal makine nesnesi, VMSS 'nin güncelleştirilmiş durumunu içerir.

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VMScaleSetName
Bu cmdlet 'in oluşturduğu VMSS 'nin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

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

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.

Cmdlet çalışmaz.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmVmss](./Get-AzureRmVmss.md)

[Yeni-AzureRmVmss](./New-AzureRmVmss.md)

[Remove-AzureRmVmss](./Remove-AzureRmVmss.md)

[Restart-AzureRmVmss](./Restart-AzureRmVmss.md)

[Set-AzureRmVmss](./Set-AzureRmVmss.md)

[Başlangıç-AzureRmVmss](./Start-AzureRmVmss.md)

[Dur-AzureRmVmss](./Stop-AzureRmVmss.md)


