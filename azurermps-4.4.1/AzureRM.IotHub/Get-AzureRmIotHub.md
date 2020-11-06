---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
ms.openlocfilehash: 890180c024a004652406e04530a7e3291def13ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594662"
---
# Get-AzureRmIotHub

## SYNOPSIS
Bir abonelikteki ıothubs hakkında bilgi alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ListIotHubsByResourceGroup (varsayılan)
```
Get-AzureRmIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Getilebilirlik Ubbyname
```
Get-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
Bir abonelikteki ıothubs hakkında bilgi alır.
Bir abonelikteki tüm IotHub örneklerini görüntüleyebilir ya da sonuçlarınızı kaynak grubuna veya belirli bir IotHub adına göre filtreleyebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzureRmIotHub
```

Abonelikteki tüm ıothubleri alır.

### Örnek 2
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup"
```

Aboneliğindeki tüm ıothubleri "myresourcegroup" adlı resourcegroup 'a ait olarak alır.

### Örnek 3
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

"Myiothub" adındaki IotHub hakkında bilgi alır.

## PARAMETRELERINE

### -Ad
IotHub adı

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
ResourceGroup

```yaml
Type: System.String
Parameter Sets: ListIotHubsByResourceGroup
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
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

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub
System. Koleksiyonlar. Generic. LIST \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotub, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

