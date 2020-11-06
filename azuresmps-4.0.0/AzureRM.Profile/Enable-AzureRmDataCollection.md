---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 678e08df94d7ea828b04d55892cb66e1c0a62349
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571757"
---
# Enable-AzureRmDataCollection

## SYNOPSIS
AzurePowerShell cmdlet 'leriyle Kullanıcı deneyimini geliştirmek için Azure PowerShell 'in veri toplamasını olanaklı kılar.
Geçerli bilgisayarda geçerli kullanıcının veri koleksiyonunda bu cmdlet 'i yürütme.
Açıkça kabul edilmedikçe veri toplanmaz.

## INDEKI

```
Enable-AzureRmDataCollection [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
Veri toplamayı kullanarak Microsoft bulut ve Azure PowerShell 'i kullanma deneyimini geliştirebilirsiniz.
Azure PowerShell, izniniz olmadan verileri toplamaz; Enable-AzureRmDataCollection 'ı yürüterek veya Evet 'i yanıtlayarak, Azure PowerShell ilk kez cmdlet 'i yürüttüğünüzde veri toplama konusunda sizi uyarır.
Microsoft toplanan verileri, yaygın sorunları belirlemek ve Azure PowerShell kullanma deneyimini iyileştirmek için toplanan verileri toplar.
Microsoft Azure PowerShell herhangi bir özel veri veya herhangi bir kişisel bilgileri toplamaz.

Geçerli makinedeki geçerli kullanıcının veri toplamayı etkinleştirmek için Enable-AzureRMDataCollection cmdlet 'ini çalıştırın.
Bu, geçerli kullanıcıdan veri toplama hakkında bilgi gönderilmesini önleyecektir; ilk cmdlet 'ler yürütülür.

Geçerli kullanıcının veri toplamayı devre dışı bırakmak için Disable-AzureRmDataCollection cmdlet 'ini çalıştırın.

## ÖRNEKLERDEN

### Örnek 1: geçerli kullanıcı için veri toplamayı etkinleştirme
```
PS C:\> Enable-AzureRmDataCollection
```

Bu örnekte, geçerli kullanıcı için veri toplamayı etkinleştirme gösterilmektedir.

## PARAMETRELERINE

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
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

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

## ÇıKıŞLAR

### Yabilirsiniz

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Disable-AzureRmDataCollection]()

