---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssVM.md
ms.openlocfilehash: 8d24aadd185a58472268fc4edf9ca504e7592bb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588977"
---
# Get-AzureRmVmssVM

## SYNOPSIS
Bir VMSS sanal makinesinin özelliklerini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### DefaultParameter (varsayılan)
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [<CommonParameters>]
```

### Kolay Yöntem
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [<CommonParameters>]
```

## Tanım
**Get-AzureRmVmssVM** cmdlet 'ı, sanal makine ölçeği KÜMESI (VMSS) sanal makinesinin model görünümünü ve örnek görünümünü alır.
Model görünümü, Kullanıcı tarafından belirtilen sanal makinenin özellikleridir.
Örnek görünümü sanal makinenin örnek düzeyi durumudur.
Bir sanal makinenin yalnızca örnek görünümüne ulaşmak için *durum* parametresini belirtin.

## ÖRNEKLERDEN

### Örnek 1: VMSS sanal makinesinin özelliklerini alma
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS sanal makinesinin özelliklerini alır.
Komut, *InstanceView* anahtar parametresini belirtmediğinden, cmdlet sanal makinenin model görünümünü alır.

### Örnek 2: bir VMSS sanal makinesinin model görünümü özelliklerini alma
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

Bu komut, Group002 adındaki kaynak grubuna ait olan VMSS004 adındaki VMSS sanal makinesinin özelliklerini alır.
Bu komut, $ID değişkeninde depolanan örnek KIMLIĞINI model görünümünün alınacağı şekilde alır.

### Örnek 3: bir VMSS sanal makinesinin örnek görünümü özelliklerini alma
```
PS C:\> Get-AzureRmVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

Bu komut, Group002 adındaki kaynak grubuna ait olan VMSS004 adındaki VMSS sanal makinesinin özelliklerini alır.
Komut, *InstanceView* Switch parametresini belirttiğinden cmdlet sanal makinenin örnek görünümünü alır.
Komut, örnek görünümünün alınacağı değişken $ID depolanan örnek KIMLIĞINI alır.

## PARAMETRELERINE

### -InstanceId
Model görünümünün alınacağı örnek KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceView
Bu cmdlet 'in yalnızca sanal makinenin örnek görünümünü aldığını gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
VMSS 'nin kaynak grubunun adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
Türleri, VMSS 'nin adını.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Bu cmdlet hiçbir çıkış üretmez.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Set-AzureRmVmssVM](./Set-AzureRmVmssVM.md)

[Get-AzureRmVmss](./Get-AzureRmVmss.md)


