---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C2DAFB2C-A58B-406C-8349-8728771B279E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59aef29c27d7eb96834d270c2fce48ff3acb9554
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106392"
---
# Add-AzureNodeWebRole

## SYNOPSIS
Node.js uygulaması için gerekli dosyaları ve klasörleri oluşturur.

## INDEKI

```
Add-AzureNodeWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

**Add-AzureNodeWebRole** , bazen, bir Node.js uygulamasının IIS aracılığıyla bulutta barındırılması için scafkatlama olarak da adlandırılır.

## ÖRNEKLERDEN

### Örnek 1: tek örnekli web rolü
```
PS C:\> Add-AzureNodeWebRole -Name MyWebRole
```

Bu örnek, **MyWebRole** adındaki tek bir Web rolü için geçerli uygulamaya scafkatlama ekler.

### Örnek 2: birden çok örnek Web rolü
```
PS C:\> Add-AzureNodeWebRole MyWebRole -I 2
```

Bu örnek, **MyWebRole** adlı yeni bir Web rolü için, rol örneği sayısı 2 olan bir rol örneği ekler.

## PARAMETRELERINE

### -Örnekler
Bu web rolü için rol örneklerinin sayısını belirtir.
Varsayılan değer 1 ' dir.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Web rolünün adını belirtir.
Ayrıca, Web rolünde barındırılan node.js uygulamasının scaflesi içeren dizinin adını da belirler.
Varsayılan WebRole # ' dır, burada # hizmette Web rollerinin sayısını gösterir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureNodeWorkerRole](./Add-AzureNodeWorkerRole.md)

[New-AzureServiceProject](./New-AzureServiceProject.md)


