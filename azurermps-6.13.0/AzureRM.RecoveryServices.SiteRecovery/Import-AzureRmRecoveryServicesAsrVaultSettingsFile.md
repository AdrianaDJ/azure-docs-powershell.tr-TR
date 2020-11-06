---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/import-azurermrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: 7bb92a55f366d90eb5993cfe1520d1b516214372
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587219"
---
# Import-AzureRmRecoveryServicesAsrVaultSettingsFile

## SYNOPSIS
PowerShell oturumunda sonraki ASR işlemleri için kasa bağlamını (PowerShell oturum bağlamı) ayarlamak üzere belirtilen ASR kasa ayarları dosyasını içeri aktarır. 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Import-AzureRmRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Import-Azurermrecoveryservicesasrvaultsettingsfıle** cmdlet 'ı, Azure Site Recovery kasa ayarları dosyasını içeri aktarır. Kasa ayarları dosyası, geçerli oturumdaki sonraki Azure Site kurtarma işlemleri için kasa bağlamını ayarlamak üzere kullanılır.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> $VaultSettings = Import-AzureRmRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

Belirtilen kurtarma hizmetleri Kasası ayarları dosyasını içeri aktarır ve içeri aktarılan kasanın ayarlarını döndürür.

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

### -Yol
ASR kasa ayarları dosyasının klasör yolunu belirtir.
Bu dosya, Kurtarma Hizmetleri kasa portalından indirilebilir ve yerel olarak depolanabilir.

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

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

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
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

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

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmRecoveryServicesAsrVaultSettingsFile](./Get-AzureRmRecoveryServicesAsrVaultSettingsFile.md)
