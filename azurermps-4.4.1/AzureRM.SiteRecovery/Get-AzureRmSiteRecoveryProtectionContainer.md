---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 77F1556C-323D-49CA-BD6C-75B2D4E0F894
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
ms.openlocfilehash: 2595d8feaa01c2f3ccd9f16ca193be195a8e303a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594169"
---
# Get-AzureRmSiteRecoveryProtectionContainer

## SYNOPSIS
Geçerli site kurtarma Kasası için koruma kapsayıcılarını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Varsayılan (varsayılan)
```
Get-AzureRmSiteRecoveryProtectionContainer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectWithName
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectWithNameLegacy
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByObjectWithFriendlyName
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectWithFriendlyNameLegacy
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFabricObject
```
Get-AzureRmSiteRecoveryProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureRmSiteRecoveryProtectionContainer** cmdlet 'ı geçerli Azure Site Recovery Kasası için koruma kapsayıcılarını alır.
Koruma kapsayıcısı sanal makineler gibi korumalı nesneler için mantıksal bir kapsayıcıdır.
Koruma ilkeleri, korumalı öğeler için çoğaltma ayarlarını tanımlar ve bir koruma konteyneriyle ilişkilendirilebilir ve korumalı bir varlığa uygulanabilir.

## ÖRNEKLERDEN

## PARAMETRELERINE

### -Kumaş
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName, ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -FriendlyName
Koruma kapsayıcısının kolay adını belirtir.

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName, ByObjectWithFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Koruma kapsayıcısının adını belirtir.

```yaml
Type: System.String
Parameter Sets: ByObjectWithName, ByObjectWithNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### ASRFabric
Parametre ' Fabric ', ardışık düzenin ' ASRFabric ' türünün değerini kabul eder

## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRProtectionContainer]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

