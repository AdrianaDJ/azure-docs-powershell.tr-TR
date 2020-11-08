---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FEFBF1EF-FBCE-45D8-8455-F3F8662F1F36
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ddf78f30cb6938571fc967d510e4ab99a0cfc80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106387"
---
# Add-AzurePHPWorkerRole

## SYNOPSIS
php.exe Azure 'da barındırılan bir PHP uygulaması için gerekli dosyaları ve yapılandırmayı oluşturur.

## INDEKI

```
Add-AzurePHPWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

php.exe Azure 'da barındırılan bir PHP uygulaması için, bazen scafkatlama olarak da adlandırılır.

## ÖRNEKLERDEN

### Örnek 1: tek bir örnek içeren bir çalışan rolü oluşturma
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole
```

Bu örnek, geçerli uygulamaya MyWorkerRole adlı tek bir çalışan rolü için gerekli dosyaları ve yapılandırmayı ekler.

### Örnek 2: birden çok örneğe sahip bir çalışan rolü oluşturma
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole -I 2
```

Bu örnek, rol örneği sayısı 2 olan MyWorkerRole adını kullanarak, yeni bir işçi için gerekli dosyaları ve yapılandırmayı geçerli uygulamaya ekler.

## PARAMETRELERINE

### -Örnekler
Bu çalışan rolünün rol örneklerinin sayısını belirtir.
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
Çalışan rolünün adını belirtir.
Ad, çalışan rolünde barındırılan PHP hizmeti için gerekli dosyaları ve yapılandırmayı içeren klasör adını belirler.
Varsayılan WorkerRole1.

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

[New-AzureServiceProject](./New-AzureServiceProject.md)

[Add-AzurePHPWebRole](./Add-AzurePHPWebRole.md)


