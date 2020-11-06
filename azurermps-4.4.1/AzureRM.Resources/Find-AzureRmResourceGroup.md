---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: EFBBFB60-D972-47B8-997E-B737F0CA007E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
ms.openlocfilehash: 029404938ba7a253b5130f5c807e4b66c3847d43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589127"
---
# Find-AzureRmResourceGroup

## SYNOPSIS
Kaynak gruplarını arar.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Find-AzureRmResourceGroup [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Find-AzureRmResourceGroup** cmdlet 'i belirtilen parametreleri kullanarak kaynak gruplarını arar.

## ÖRNEKLERDEN

### Örnek 1: tüm kaynak gruplarını bulma
```
PS C:\>Find-AzureRmResourceGroup
```

Bu komut tüm kaynak gruplarını bulur.

### Örnek 2: etiket adına göre kaynak gruplarını bulma
```
PS C:\>Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
```

Bu komut testtag adlı etikete sahip tüm kaynak gruplarını bulur.

### Örnek 3: etiket adına göre kaynak gruplarını bulma
```
PS C:\>Find-AzureRmResourceGroup -Tag @{"testtag" = "testval" }
```

Bu komut testtag adlı etikete ve TestVal değerine sahip tüm kaynak gruplarını bulur.

## PARAMETRELERINE

### -Apıversion
Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir. Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre-
Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Etiketli
Sonuçlarınızı filtrelemek için etiket bilgilerini karma tablo olarak belirtir. Aşağıdaki biçimleri kullanın:

@ {tagName = $null} veya @ {tagName = ' tagValue '}.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

## ÇıKıŞLAR

### System. Management. Automation. PSObject

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

