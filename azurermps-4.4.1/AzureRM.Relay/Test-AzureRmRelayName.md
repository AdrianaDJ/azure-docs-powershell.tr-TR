---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: 4b3afc0b41f6eaf68e7ec0c4f8ed976b36267c97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587803"
---
# Test-AzureRmRelayName

## SYNOPSIS
Verilen ad alanı adının uygunluk durumunu denetler

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Test-AzureRmRelayName** cmdlet 'ı ad alanı adının kullanılabilirliğini denetler

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability
```

### Örnek 2
```
PS C:\> Test-AzureRmRelayName -Namespace Testi
```

### Örnek 3
```
PS C:\> Test-AzureRmRelayName -Namespace Test123
```

Ad alanı adının uygunluk durumunu verir

## PARAMETRELERINE

### -Namespace
Geçiş ad alanı adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### -Namespace
 System. String

## ÇıKıŞLAR

### [Microsoft. Azure. Commands. Relay. modeller. Checknamekullanılabilirliği Bilityresultattributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]

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

