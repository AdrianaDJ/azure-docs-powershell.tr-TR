---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 6F31F2B4-6131-4B11-B074-CA05CE3A56F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: f928ecba8f92badc1eb87e47aee16515f1684fce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105773"
---
# Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan

## SYNOPSIS
Geçiş planı oluşturmayı başlatır.

## INDEKI

### MigrateSpecificContainer
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### MigrateAllContainer
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet 'i, geçiş planı oluşturmayı başlatır.
Geçiş planı oluşturma işlemi eşzamansız.
Geçiş planının durumunu görmek için **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet 'ini kullanın.

## ÖRNEKLERDEN

### Örnek 1: geçiş planı başlatma
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

Bu komut, OneSDKAzureCloud adlı eski kapsayıcı için geçiş planı oluşturmaya başlar.
Komut, planın durumu hakkında bir ileti ve güncel bilgi için **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet 'ini kullanmaktır.

### Örnek 2: tüm birim kapsayıcıları için geçiş planını Başlat
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

Bu komut, içeri aktarılan yapılandırma dosyasındaki tüm eski birim kapsayıcıları için geçiş planı oluşturmayı başlatır.

## PARAMETRELERINE

### -Tümü
Bu cmdlet 'in içeri aktarılan yapılandırma dosyasındaki tüm birim kapsayıcıları için geçiş süresi tahminlerini başladığını gösterir.

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
Geçiş planı oluşturacağınız birim kapsayıcı adları dizisini belirtir.

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

### Yabilirsiniz

## ÇıKıŞLAR

### Dizisi
Bu cmdlet, Gereç planı işinin, Gereç içinde başarıyla başlatılmış olması durumunda durumunu döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


