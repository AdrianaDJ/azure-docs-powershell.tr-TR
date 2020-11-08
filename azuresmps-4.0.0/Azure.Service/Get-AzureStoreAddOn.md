---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 61CF7F95-F0BB-4282-A971-537CB73708B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d5774213054f3e9e56e9804a9319e31f095f868
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105547"
---
# Get-AzureStoreAddOn

## SYNOPSIS
Kullanılabilir Azure Mağazası eklentilerini alır.

## INDEKI

### ListAvailable
```
Get-AzureStoreAddOn [-ListAvailable] [-Country <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### GetAddOn
```
Get-AzureStoreAddOn [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

Azure Mağazası 'ndan satın almak için tüm kullanılabilir eklentileri alır veya geçerli aboneliğin mevcut eklenti örneklerini alır.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzureStoreAddOn
```

Bu örnekte, geçerli aboneliğin satın alınan tüm eklenti örnekleri alınır.

### Örnek 2
```
PS C:\> Get-AzureStoreAddOn -ListAvailable
```

Bu örnekte, Azure Mağazası 'ndan Amerika Birleşik Devletleri 'nde satın almak için sağlanan tüm eklentiler alınır.

### Örnek 3
```
PS C:\> Get-AzureStoreAddOn -Name MyAddOn
```

Bu örnekte, geçerli abonelikteki satın alınan eklenti örneğindeki MyAddOn adlı bir eklenti alınır.

## PARAMETRELERINE

### -Ülke
Belirtilmişse yalnızca belirtilen ülkedeki Azure Mağazası eklenti örneklerini döndürür.
Varsayılan "US" dir.

```yaml
Type: String
Parameter Sets: ListAvailable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ListAvailable
Belirtilmişse, Azure Mağazası 'ndan satın almak için kullanılabilir eklentileri alır.

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailable
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Belirtilen adla eşleşen eklentiyi döndürür.

```yaml
Type: String
Parameter Sets: GetAddOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

[New-AzureStoreAddOn](./New-AzureStoreAddOn.md)

[Remove-AzureStoreAddOn](./Remove-AzureStoreAddOn.md)

[Set-AzureStoreAddOn](./Set-AzureStoreAddOn.md)


