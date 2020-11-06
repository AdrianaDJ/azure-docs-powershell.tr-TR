---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 4de1861c3db804e7ffd4371f4e35c241843374cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587211"
---
# Remove-AzureRmRecoveryServicesAsrServicesProvider

## SYNOPSIS
Belirtilen Azure Site Recovery kurtarma hizmetleri sağlayıcısını kurtarma hizmetleri kasasından siler/kaydını kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Remove-AzureRmRecoveryServicesAsrServicesProvider** cmdlet 'i, kasadan belirtilen Azure Site Recovery kurtarma hizmetleri sağlayıcısını kaldırır.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

Belirtilen Azure Site Recovery Hizmetleri sağlayıcısının silinmesini/kaydını başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.

## PARAMETRELERINE

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

### -Force
Ek bir uyarı vermeden komutu çalıştırmaya zorlayın.

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

### -InputObject
Cmdlet 'e giriş nesnesi: ASR kurtarma hizmetleri sağlayıcısının silinmesine karşılık gelen ASR kurtarma hizmetleri sağlayıcısı nesnesi.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Onay
Onayın gerekli olup olmadığını belirtin. Onayı atlamak için Confirm parametresinin değerini $false olarak ayarlayın.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet gerçekten yürütülmeden çalıştırıldığında ne olacağını gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
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

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider

## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Sıterecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermrecoveryservicesasrservices sağlayıcısı](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[Update-Azurermrecoveryservicesasrservices sağlayıcısı](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
