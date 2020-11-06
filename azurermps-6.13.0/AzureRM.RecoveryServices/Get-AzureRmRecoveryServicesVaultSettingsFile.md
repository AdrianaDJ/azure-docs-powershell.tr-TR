---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: a0572e73d270a37b3c705018a38b4a88fe88d1e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593917"
---
# Get-AzureRmRecoveryServicesVaultSettingsFile

## SYNOPSIS
Azure Site Recovery kasa ayarları dosyasını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Forsıte
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByDefault
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ForBackupVaultType
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azurermrecoveryservicesvaultsettingsfıle** cmdlet 'i, bir Azure Site Recovery Kasası için ayarlar dosyasını alır.

## ÖRNEKLERDEN

### Örnek 1: Azure yedekleme için Windows Server veya DPM makinesini kaydettirme
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

İlk komut Testkasası adlı kasayı alır ve $Vault 01 değişkeninde depolar.
İkinci komut $CredsPath değişkenini C:\downloadolarak ayarlar.
Son komut, Azure yedekleme için $CredsPath 'daki kimlik bilgilerini kullanarak $Vault 01 kasa kimlik bilgileri dosyasını alır.

### Örnek 2:
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

Komut $Vault 01 kasa türü siteRecovery için kasa kimlik bilgileri dosyasını alır.

### Örnek 3: Azure yedekleme için Windows Server veya DPM makinesini kaydettirme
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

Komut $Vault 01 için kasa kimlik bilgileri dosyasını alır.

## PARAMETRELERINE

### -Yedekleme
Kasa kimlik bilgileri dosyasının Azure yedekleme 'ye uygun olduğunu gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultType
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

### -Yol
Azure Site Recovery kasa ayarları dosyasının yolunu belirtir.
Bu dosyayı Azure Site Recovery kasa portalından indirebilir ve yerel olarak depolayabilirsiniz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteFriendlyName
Sitenin kolay adını belirtir.
Bir Hyper-V sitesinin kasa kimlik bilgilerini indiriyorsunuz bu parametreyi kullanın.

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
Site tanımlayıcısını belirtir.
Bir Hyper-V sitesinin kasa kimlik bilgilerini indiriyorsunuz bu parametreyi kullanın.

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

### -Siterecoçok
Kasa kimlik bilgileri dosyasının Azure Site Recovery için geçerli olduğunu gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kasa
Azure Site Recovery kasa nesnesini belirtir.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. RecoveryServices. Arskasa
Parametreler: kasa (ByValue)

## ÇıKıŞLAR

### Microsoft. Azure. Commands. RecoveryServices. VaultSettingsFilePath

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermrecoveryserviceskasası](./Get-AzureRmRecoveryServicesVault.md)

[Yeni-Azurermrecoveryserviceskasası](./New-AzureRmRecoveryServicesVault.md)

[Remove-Azurermrecoveryserviceskasası](./Remove-AzureRmRecoveryServicesVault.md)


