---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 9595E785-6DBF-433C-83B3-8506A3B49B13
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 242dfd46b179d1e7d55613d938eddf5b691da6c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764513"
---
# Get-AzureRmSiteRecoveryVaultSettingsFile

## SYNOPSIS
Site Recovery kasa ayarları dosyasını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ByParam (varsayılan)
```
Get-AzureRmSiteRecoveryVaultSettingsFile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Varsayýlan
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Forsıte
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> -SiteIdentifier <String> -SiteFriendlyName <String>
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmSiteRecoveryVaultSettingsFile** cmdlet 'ı bir Azure Site Recovery Kasası için ayarlar dosyasını alır.

## ÖRNEKLERDEN

## PARAMETRELERINE

### -Yol
Site Recovery kasa ayarları dosyasının yolunu belirtir.
Bu dosyayı yerel olarak depolamak için, komut tamamlandığında site kurtarma Kasası portalında indirin.

```yaml
Type: System.String
Parameter Sets: Default, ForSite
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteFriendlyName
Site bir Hyper-V sitesi olduğunda kasanın kolay adını belirtir.

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sitetanımlayıcısı
Site bir Hyper-V sitesi olduğunda kasaya ait site tanımlayıcısını belirtir.

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kasa
Sitenin kasa nesnesini belirtir.

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: Default, ForSite
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

### Asrkasa
Parametre ' kasa ', ardışık düzenin ' Asrkasa ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Azure. Commands. SiteRecovery. VaultSettingsFilePath

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[İçeri aktarma-AzureRmSiteRecoveryVaultSettingsFile](./Import-AzureRmSiteRecoveryVaultSettingsFile.md)

[Set-AzureRmSiteRecoveryVaultSettings](./Set-AzureRmSiteRecoveryVaultSettings.md)
