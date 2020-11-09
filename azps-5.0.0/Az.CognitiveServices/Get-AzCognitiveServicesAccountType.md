---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: a99ca4bb636ba1767fc5f50611d3c5a9eb991312
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322250"
---
# Get-AzCognitiveServicesAccountType

## SYNOPSIS
Kullanılabilir öğrenme hizmeti hesap türlerini alır.

## INDEKI

### GetAccountTypes (varsayılan)
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetAccountTypeWithName
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-Azöğretici Iveservicesaccounttype** cmdlet 'i, bu aboneliğin altındaki kullanılabilir öğretici hizmet hesap türlerini alır.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

Kullanılabilir türlerin listesini alın.

### Örnek 2
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

Westus 'de kullanılabilir türlerin listesini alın.

### Örnek 3
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

`Face`Geçerli bir tür adı olup olmadığını denetleyin, ad geçerli bir adise döndürülür.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Konum
Öğretici hizmetler hesap konumu.

```yaml
Type: System.String
Parameter Sets: GetAccountTypes
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeName
Öğretici hizmetler hesap türü adı.

```yaml
Type: System.String
Parameter Sets: GetAccountTypeWithName
Aliases: CognitiveServicesAccountTypeName, AccountTypeName, KindName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### System. String []

### System. String

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
