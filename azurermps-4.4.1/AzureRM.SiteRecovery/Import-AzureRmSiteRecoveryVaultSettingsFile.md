---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 070DA86E-9EA4-4777-9D53-64B58B4401B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 42863e0dbf6982ced1f77f916c97ed4fc19d6979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594168"
---
# Import-AzureRmSiteRecoveryVaultSettingsFile

## SYNOPSIS
Site Recovery kasa ayarları dosyasını içeri aktarır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Import-AzureRmSiteRecoveryVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Import-AzureRmSiteRecoveryVaultSettingsFile** cmdlet 'i, geçerli oturumdaki sonraki site kurtarma işlemleri için kasa bağlamını ayarlamak üzere bir Azure Site Recovery kasa ayarları dosyası alır.

## ÖRNEKLERDEN

## PARAMETRELERINE

### -Yol
Site Recovery kasa ayarları dosyasının yolunu belirtir.
Bu dosya, Site Recovery kasa portalından indirilebilir ve yerel olarak depolanabilir.

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

## ÇıKıŞLAR

### Microsoft. Azure. Commands. SiteRecovery. ASRVaultSettings

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmSiteRecoveryVaultSettingsFile](./Get-AzureRmSiteRecoveryVaultSettingsFile.md)
