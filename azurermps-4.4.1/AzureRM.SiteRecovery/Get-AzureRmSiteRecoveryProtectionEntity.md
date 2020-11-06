---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 511D2401-5415-4EC6-AA75-E9D2D4D6D19C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 706b1ba37d7ac31215e5ecb07f3941e7e89ede5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594562"
---
# Get-AzureRmSiteRecoveryProtectionEntity

## SYNOPSIS
Geçerli site kurtarma kasasındaki korunabilir veya korunan varlıkların listesini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ByObject (varsayılan)
```
Get-AzureRmSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectWithName
```
Get-AzureRmSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectWithFriendlyName
```
Get-AzureRmSiteRecoveryProtectionEntity -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmSiteRecoveryProtectionEntity** cmdlet 'ı geçerli Azure Site Recovery kasasındaki sanal makineler gibi korunabilir veya korumalı varlıkların bir listesini alır.

## ÖRNEKLERDEN

## PARAMETRELERINE

### -FriendlyName
Koruma varlığının kolay adını belirtir.

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Koruma varlığının adını belirtir.

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionContainer
Koruma kapsayıcısı nesnesini belirtir.

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### ASRProtectionContainer
' ProtectionContainer ' parametresi ardışık düzenin ' ASRProtectionContainer ' türünün değerini kabul eder

## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRProtectionEntity]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Set-AzureRmSiteRecoveryProtectionEntity](./Set-AzureRmSiteRecoveryProtectionEntity.md)
