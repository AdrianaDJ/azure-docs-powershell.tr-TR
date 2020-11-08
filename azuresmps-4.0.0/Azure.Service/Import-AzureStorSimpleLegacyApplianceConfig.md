---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F41E3B17-A33C-4FBF-B532-2E86F1AAE2B8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4bc3e4245e3d223d95c3ec5d793a53d5d3bfbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106259"
---
# Import-AzureStorSimpleLegacyApplianceConfig

## SYNOPSIS
Yapılandırma dosyasını içeri aktarır.

## INDEKI

```
Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath <String> -TargetDeviceName <String>
 -ConfigDecryptionKey <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Import-AzureStorSimpleLegacyApplianceConfig** cmdlet 'i, eski olan gereç yapılandırma dosyasını içeri aktarır.
Bu dosya, Azure StorSimple hizmeti için birim kapsayıcıları, yedekleme ilkeleri ve depolama hesabı kimlik bilgileri hakkında bilgi içerir.
Bu cmdlet, eski gereç yapılandırma meta verilerini döndürür.

## ÖRNEKLERDEN

### Örnek 1: yapılandırma dosyasını Içeri aktarma
```
PS C:\>Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath "C:\MigrationData\LegacyStorSimpleConfig.sse" -TargetDeviceName "8100-123456789" -ConfigDecryptionKey "fWs793hHVhR90NKdDYTeNq"
LegacyConfigId      : e2d5c9b1-b528-4c21-b8ae-533feefc8a41
ImportedOn          : 4/8/2015 7:23:04 PM
ConfigFile          : D:\configs\StorSimpleConfig_27_Mar_15_12_19.xml.sse
TargetApplianceName : Arunkm-N4
Details             : Available Cloud Configuration(s) for migration : 
                          Cloud Configuration(s) 1    : TC8Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 2    : fulle_cc4
                          Cloud Configuration(s) 3    : fulle_cc2
                          Cloud Configuration(s) 4    : fulle_cc3
                          Cloud Configuration(s) 5    : TC9Cloud[Stingray18-FP3] 
                          Cloud Configuration(s) 6    : fulle_cc1
                          Cloud Configuration(s) 7    : Container-New[Stingray19-FP6] 
                          Cloud Configuration(s) 8    : TC6Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 9    : TC7Cloud[Stingray18-FP3] 

Result              : Successfully imported config from the legacy appliance! 
Save the legacy config id and cloud configuration(s) for future reference.
```

Bu komut, yapılandırma dosyasını belirtilen yolda içeri aktarır.
Komut dosyanın şifresini çözme anahtarını içerir.

## PARAMETRELERINE

### -ConfigDecryptionKey
Eski gereç yapılandırması için şifre çözme anahtarını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConfigFilePath
Alınacak yapılandırma dosyasının mutlak yolunu belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: FilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Bir Azure profili belirtir.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Targetaygıtadı
Portalda gösterilen hedef aygıtın adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Yasallık yapılandırma
Bu cmdlet, yapılandırmanın ayrıntılarını döndürür.
**Yasallık Plianceconfiguration** nesnesi şu bilgileri içerir: yapılandırma kimliği, birim kapsayıcı adları, erişim denetim kayıtları, yedekleme ilkeleri, bant genişliği ayarları, birim kapsayıcıları, depolama hesabı kimlik bilgileri ve birimler.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[İçeri aktarma-AzureStorSimpleLegacyVolumeContainer](./Import-AzureStorSimpleLegacyVolumeContainer.md)


