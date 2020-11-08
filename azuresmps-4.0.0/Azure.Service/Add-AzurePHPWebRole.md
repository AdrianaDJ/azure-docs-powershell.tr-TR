---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F9A06B8B-55DB-48A5-B246-53347E759E64
online version: ''
schema: 2.0.0
ms.openlocfilehash: 050c05f2cdad546388744bcebca4f28a12a03038
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106390"
---
# Add-AzurePHPWebRole

## SYNOPSIS
Bir PHP uygulaması için gerekli dosyaları ve yapılandırmayı oluşturur.

## INDEKI

```
Add-AzurePHPWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

**Add-AzurePHPWebRole** cmdlet 'i, bazen, IIS aracılığıyla Azure 'da BARıNDıRıLAN bir php uygulaması için, dosya ve yapılandırmayı oluşturur.

## ÖRNEKLERDEN

### Örnek 1: varsayılan değerleri kullanarak Web rolü ekleme
```
PS C:\> Add-AzurePHPWebRole
```

Bu örnek, 1 örneğiyle "WebRole1" adlı hizmetin varsayılan değerlerini kullanarak yeni web rolü için gerekli dosyaları ve yapılandırmayı ekler.

### Örnek 2: birden çok örneğe sahip web rolü ekleme
```
PS C:\> Add-AzurePHPWebRole MyWebRole -I 2
```

Bu örnek, "MyWebRole" adını ve 2 ' nin rol örneği sayısını kullanarak, geçerli uygulamaya yeni bir Web rolü için gerekli dosyaları ve yapılandırmayı ekler.

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
Ad, PHP uygulaması için gerekli dosyaları ve yapılandırmayı içeren dizinin adını belirler.
Varsayılan WebRole # ' dır; burada #, hizmetin Web rollerinin sayısıdır.

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

[Add-AzurePHPWorkerRole](./Add-AzurePHPWorkerRole.md)

[New-AzureServiceProject](./New-AzureServiceProject.md)


