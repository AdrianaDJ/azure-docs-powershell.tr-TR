---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
ms.openlocfilehash: 034681ad8ce4fbd30b10b959eda024f1a375c366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587163"
---
# Get-AzureRmSecurityLocation

## SYNOPSIS
Belirli bir aboneliğin Azure Güvenlik Merkezi tarafından otomatik olarak kaydedileceği konumu alır

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### SubscriptionScope (varsayılan)
```
Get-AzureRmSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelResource
```
Get-AzureRmSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Içermiyor
```
Get-AzureRmSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
Azure Güvenlik Merkezi, bazı verilerinizi kaydetmek için otomatik olarak bir konuma karar versin.
Bu yeri bulmak için bu cmdlet 'i kullanın.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> Get-AzureRmSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

Azure Güvenlik Merkezi 'nin hesaplanan güvenlik verilerini kaydettiği konumu alır.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Kaynak adı.

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RESOURCEID
Kaynak KIMLIĞI.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Security. modeller. locations. PSSecurityLocation

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
