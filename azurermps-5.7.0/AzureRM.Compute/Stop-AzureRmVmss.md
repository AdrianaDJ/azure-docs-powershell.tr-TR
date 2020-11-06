---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 3798590f3b4df738bc38231018adabf99ba39237
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594113"
---
# Stop-AzureRmVmss

## SYNOPSIS
VMSS 'yi veya VMSS içindeki sanal makinelerin kümesini durdurur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### DefaultParameter (varsayılan)
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Kolay Yöntem
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Stop-AzureRmVmss** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) veya sanal makine kümesi içindeki tüm sanal makineleri durdurur.
*InstanceId* parametresini kullanarak bir sanal makine kümesi seçebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: VMSS içindeki tüm sanal makineleri durdurma
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

Bu komut, ContosoVMSS adlı VMSS 'ye ait tüm sanal makineleri durdurur.

### Örnek 2: VMSS içinde belirli bir sanal makine kümesini durdurma
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

Bu komut, ContosoVMSS adlı VMSS 'ye ait örnek KIMLIĞI dizesi dizisiyle belirtilen belirli bir sanal makine kümesini durdurur.

## PARAMETRELERINE

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceId
Bu cmdlet 'in durdurduğu sanal makine örneklerinin KIMLIĞINI veya kimliklerini dize dizisi olarak belirtir.
Örneğin: `-InstanceId "0", "3"` .

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

### -ResourceGroupName
VMSS 'nin kaynak grubunun adını belirtir.

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

### -Staysağlandı
Belirtilmişse, sanal makine durdurulmuş duruma girer. Belirtilmezse, sanal makine durduruldu-serbest işlem durumuna girer. Kullanıcı hala durdurulmuş durumda VM 'Ler için ücretlendirilecek, ancak durdurulan serbest durumda VM 'Ler için kullanılmaz.


```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMScaleSetName
Bu cmdlet 'in sanal makineleri durdurduğu VMSS adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
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

[Güncelleştirme-AzureRmVmss](./Update-AzureRmVmss.md)


