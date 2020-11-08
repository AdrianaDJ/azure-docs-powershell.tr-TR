---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7317DAC1-B535-4650-86BF-73E96F61EECD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23bb8e09fac8ec4fe0e8ff5b3c23ab995f03694c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106191"
---
# New-AzureVMSqlServerAutoPatchingConfig

## SYNOPSIS
Sanal makine otomatik düzeltme eki için yapılandırma nesnesi oluşturur.

## INDEKI

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**New-AzureVMSqlServerAutoPatchingConfig** cmdlet 'i, sanal makine otomatik düzeltme eki için bir yapılandırma nesnesi oluşturur.

## ÖRNEKLERDEN

### Örnek 1: otomatik düzeltme 'yi yapılandırmak için yapılandırma nesnesi oluşturma
```
PS C:\> $APS = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
          Enable                        : True
          DayOfWeek                     : Thursday
          MaintenanceWindowStartingHour : 11
          MaintenanceWindowDuration     : 120
          PatchCategory                 : Important
```

Bu komut, set-AzureVMSqlServerExtension kullanarak otomatik düzeltme eki yapılandırmak için kullanılabilecek yapılandırma nesnesi oluşturur.

## PARAMETRELERINE

### -DayOfWeek
Güncelleştirmelerin yüklenmesi gereken haftanın gününü belirtir.

Bu parametre için kabul edilebilir değerler şunlardır:

- Gününü
- Den
- Salı
- Günü
- Per
- Cuma
- Günü
- Sıradışı

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable
Sanal makine için otomatik düzeltme özelliğinin etkinleştirildiğini gösterir.
Otomatik Düzeltme 'yi etkinleştirirseniz cmdlet Windows güncelleştirmesini etkileşimli moda koyar.
Otomatik Düzeltme ekini devre dışı bırakırsanız, Windows Update ayarları değişmez.

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

### -Informationaction
Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.

Bu parametre için kabul edilebilir değerler şunlardır:

- 'A
- Manıza
- Sorgulamak
- Sustlıkdevam
- Durdurduğunuzda
- Biliriz

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Informationvariable
Bir bilgi değişkeni belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindowDuration
Bakım penceresinin süresini belirtir.
Otomatik Düzeltme Eki, bu pencerenin dışında bir sanal makine kullanılabilirliğini etkileyebilecek bir eylem gerçekleştirmekten kaçınacaktır.
Yalnızca 30 dakikalık artış vardır.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindowStartingHour
Bakım penceresinin başladığı günün saatini belirtir.
Bu kez, güncelleştirmelerin yüklenmeye başlaması ve saate yuvarlanacağını tanımlar.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PatchCategory
Önemli güncelleştirmelerin dahil edilip edilmeyeceğini belirtir.

```yaml
Type: String
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

### AutoPatchingSettings
Bu cmdlet, otomatik düzeltme için ayarlar içerir.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Set-AzureVMSqlServerExtension](./Set-AzureVMSqlServerExtension.md)

[Remove-AzureVMSqlServerExtension](./Remove-AzureVMSqlServerExtension.md)

[Set-AzureVMSqlServerExtension](./Set-AzureVMSqlServerExtension.md)


