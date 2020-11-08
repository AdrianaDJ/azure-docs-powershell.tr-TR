---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 92E2409B-14BC-428F-8BAF-60D8DAFA5F57
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1adaafdfdd4331bbba86530eb532964430ed7c69
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105935"
---
# Test-AzureTrafficManagerDomainName

## SYNOPSIS
Bir etki alanı adının Traffic Manager profili olarak kullanılıp kullanılmayacağını denetler.

## INDEKI

```
Test-AzureTrafficManagerDomainName -DomainName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Test-AzureTrafficManagerDomainName** cmdlet 'i bir etki alanı adının Microsoft Azure Traffic Manager profili olarak kullanılıp kullanılmayacağını denetler.
Etki alanı adı kullanılabiliyorsa, bu cmdlet $True değerini döndürür.

## ÖRNEKLERDEN

### Örnek 1: etki alanı adının kullanılabilir olup olmadığını denetleme
```
PS C:\>Test-AzureTrafficManagerDomainName -DomainName "ContosoApp.trafficmanager.net"
$True
```

Bu komut, ContosoApp.trafficmanager.net etki alanı adı 'nın bir Traffic Manager profili olarak kullanılabildiğini denetler.

## PARAMETRELERINE

### -EtkiAlanıAdı
Sınanacak etki alanı adını belirtir.
Aşağıdaki dizeyi eklemelisiniz: 

. trafficmanager.net

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir. Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

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

### System. Boolean
Bu cmdlet $True veya $False oluşturur.
Etki alanı adı kullanılabiliyorsa, bu cmdlet $True değerini döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

