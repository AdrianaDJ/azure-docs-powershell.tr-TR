---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 23272A36-8F55-41A8-AFC9-2EEE0FA55DA3
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd341437019b6adbe6c2a5a93076baff61e1f0d7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106258"
---
# Import-AzureStorSimpleLegacyVolumeContainer

## SYNOPSIS
Birim kapsayıcılarının geçişini başlatır.

## INDEKI

### MigrateSpecificContainer
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> -LegacyContainerNames <String[]>
 [-SkipACRs] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### MigrateAllContainer
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> [-All] [-SkipACRs] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Import-AzureStorSimpleLegacyVolumeContainer** cmdlet 'i eski bir gereç ile hedef bir gereç arasında birim kapsayıcıları geçişini başlatır.

## ÖRNEKLERDEN

### Örnek 1: eski birim kapsayıcısını Içeri aktarma
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

Bu komut, adlandırılmış kapsayıcı için eski birim kapsayıcısını içeri aktarır.
Cmdlet içeri aktarmayı başlatır ve bir ileti döndürür.

### Örnek 2: tüm eski birim kapsayıcılarını Içeri aktarma
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

Bu komut, alınan yapılandırma dosyasından tüm eski birim kapsayıcılarını içeri aktarır.
Cmdlet içeri aktarmayı başlatır ve bir ileti döndürür.

## PARAMETRELERINE

### -Tümü
Bu cmdlet 'in içeri aktarılan yapılandırma dosyasındaki tüm birim kapsayıcılarını hedef cihaza aktardığını gösterir.

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

### -Force
Bu cmdlet 'in birim kapsayıcısını farklı bir cihaza içeri aktardığını ve farklı bir cihazda birim kapsayıcısı alınmış olsa bile, bu cmdlet 'in birim kapsayıcısını aldığını gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
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

### -SkipACRs
İçeri aktarma işleminin geçiş için Access denetim kayıtlarını aldığını gösterir.

```yaml
Type: SwitchParameter
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

### Dizisi
Bu komut, Gereç içeri aktarma birimi kapsayıcı işinin, Gereç içinde başarıyla başlatılmış olması durumunda durumunu döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorSimpleLegacyVolumeContainerStatus](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[İçeri aktarma-AzureStorSimpleLegacyApplianceConfig](./Import-AzureStorSimpleLegacyApplianceConfig.md)


