---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 298443c4b962a2be6c5cf3849657d0fe8bbaf978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587456"
---
# Update-AzureRmRecoveryServicesAsrvCenter

## SYNOPSIS
Kaydettirilmiş bir vCenter için keşif ayrıntılarını güncelleştirme.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Varsayılan (varsayılan)
```
Update-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Byresourceıd
```
Update-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Update-AzureRmRecoveryServicesAsrvCenter** cmdlet 'i, kaydedilen bir vCenter için keşif ayrıntılarını güncelleştirir.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Update-AzureRmRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

Kaydettirilmiş bir vCenter için keşif ayrıntılarını güncelleştirme.

## PARAMETRELERINE

### -Hesap
vCenter oturum açma kimlik bilgileri hesabı.

```yaml
Type: ASRRunAsAccount
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -InputObject
Keşif ayrıntılarını güncelleştirmek için vCenter Server nesnesi.

```yaml
Type: ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Bağlantı noktası
Bulma için kullanılacak vCenter sunucusundaki TCP bağlantı noktası.

```yaml
Type: Int32
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RESOURCEID
VCenter 'ın RESOURCEID 'nı belirtir.

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter

## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Sıterecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
