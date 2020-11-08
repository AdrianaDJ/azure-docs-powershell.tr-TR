---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 97AC691F-3835-4CEE-B47E-430BE9962AF9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 26fcee5f6cb669ef49993a009aa76e9c9522b180
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105700"
---
# Confirm-AzureStorSimpleLegacyVolumeContainerStatus

## SYNOPSIS
Geçirilen birim kapsayıcılarını yürütme veya geri alma işlemini başlatır.

## INDEKI

### MigrateSpecificContainer
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### MigrateAllContainer
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Confirm-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet 'i, eski geçişin bir parçası olarak geçirilen birim kapsayıcılarını yürütme veya geri alma işlemini başlatır.
Geri alma, bu işlemi ilk sahiplik durumuna getirir.
Yürütme, sahipliği hedef uygulamaya atar.

## ÖRNEKLERDEN

### Örnek 1: belirli bir birim kapsayıcısında yürütme işlemi başlatma
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Commit
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

Bu komut belirtilen eski yapılandırma KIMLIĞI için belirtilen birim kapsayıcısında bir yürütme işlemi başlatır.
İşlemin durumunu görmek için **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet 'ini kullanın.

### Örnek 2: belirli bir birim kapsayıcısında geri alma işlemi başlatma
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Rollback
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

Bu komut belirtilen eski yapılandırma KIMLIĞI için belirtilen birim kapsayıcısında geri alma işlemi başlatır.

### Örnek 3: tüm birim kapsayıcılarında yürütme işlemi başlatma
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Commit -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

Bu komut belirtilen eski yapılandırma KIMLIĞI için tüm birim kapsayıcısında bir yürütme işlemi başlatır.

### Örnek 4: tüm birim kapsayıcılarında geri alma işlemi başlatma
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Rollback -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

Bu komut, belirtilen eski yapılandırma KIMLIĞI için tüm birim kapsayıcılarında geri alma işlemi başlatır.

## PARAMETRELERINE

### -Tümü
Bu cmdlet 'in içeri aktarılan yapılandırma dosyasındaki tüm birim kapsayıcılarında geri alma veya tamamlama işlemi başlattığını gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: MigrateAllContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Legacyconfigıd
Eski bir gereç yapılandırmasının benzersiz KIMLIĞINI belirtir.

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

### -LegacyContainerNames
Geçiş planının uygulandığı birim kapsayıcı adları dizisini belirtir.

```yaml
Type: String[]
Parameter Sets: MigrateSpecificContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MigrationOperation
Bu cmdlet 'in yürütme veya geri alma gerçekleştirip gerçekleştirmeyeceğini belirtir.
Geçerli değerler: Commit ve Rollback.

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

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorSimpleLegacyVolumeContainerStatus](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)

[Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


