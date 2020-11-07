---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: 892177efebb3a62e40f79b80b1ac67c488e048d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764225"
---
# Test-AzureRmServiceBusName

## SYNOPSIS
Verilen ad alanı adının uygunluk durumunu denetler

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Test-AzureRmServiceBusName [-Namespace] <String>
```

## Tanım
**Test-AzureRmServiceBusName** cmdlet 'ı ad alanı adının kullanılabilirliğini denetler

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Test-AzureRmServiceBusName -Namespace TestingtheAvailability
```

### Örnek 2
```
PS C:\> Test-AzureRmServiceBusName -Namespace Testi
```

### Örnek 3
```
PS C:\> Test-AzureRmServiceBusName -Namespace Test123
```

Ad alanı adının uygunluk durumunu verir

## PARAMETRELERINE

### -Namespace
ServiceBus ad alanı adı.

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
### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### -Namespace
 System. String

## ÇıKıŞLAR

### [Microsoft. Azure. Commands. ServiceBus. modeller. Checknamekullanılabilirliği Bilityresultattributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.1.0.0, Culture = neutral = neutral = NULL]

### Örnek 1
Ad kullanılabilir neden Iletisi
------------- ------ -------
         True   None

### Örnek 2
Ad kullanılabilir neden Iletisi
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### Örnek 3
Ad kullanılabilir neden Iletisi
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
