---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
ms.openlocfilehash: 467b430232805da132b568918ac0a1ed7b6db5c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587613"
---
# Remove-AzureRmAvailabilitySet

## SYNOPSIS
Azure 'dan bir kullanılabilirlik kümesini kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**Remove-AzureRmAvailabilitySet** cmdlet 'i Azure 'dan bir kullanılabilirlik kümesini kaldırır.

## ÖRNEKLERDEN

### Örnek 1: kullanılabilirlik kümesini kaldırma
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

Bu komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki bir kullanılabilirlik kümesini kaldırır.

## PARAMETRELERINE

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Kullanılabilirlik kümesi adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubunun adını belirtir.

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

[Get-AzureRmAvailabilitySet](./Get-AzureRmAvailabilitySet.md)

[Yeni-AzureRmAvailabilitySet](./New-AzureRmAvailabilitySet.md)


