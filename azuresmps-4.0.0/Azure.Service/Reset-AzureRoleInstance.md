---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2AEA385F-E180-4564-A62A-9E913C665801
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fff3ea97c51ee5597e585f3275b25e513c22008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105480"
---
# Reset-AzureRoleInstance

## SYNOPSIS
Tek bir rol örneğinin veya belirli bir rolün tüm rol örneklerinin yeniden başlatılmasını veya yeniden yansımasını ister.

## INDEKI

```
Reset-AzureRoleInstance [-ServiceName] <String> -Slot <String> -InstanceName <String> [-Reboot] [-Reimage]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Tanım
**Reset-Azureroleınstance** cmdlet 'i, dağıtımda çalışan bir rol örneğinin yeniden başlatılmasını veya yeniden yansımasını ister.
Bu işlem eşzamanlı olarak yürütülür.
Bir rol örneğini yeniden başlattığınızda, Azure bu örneği çevrimdışı olarak alır, bu örnek için temel işletim sistemini yeniden başlatır ve örneği çevrimiçi duruma getirir.
Yerel diske yazılan tüm veriler yeniden başlatmalar genelinde devam edilir.
Bellekteki veriler kaybedilir.

Rol örneği yeniden Imaging rol türüne bağlı olarak farklı davranışlara neden olacak.
Web veya işçi rolünde, rol yeniden görüntülendiğinde, Azure rolü çevrimdışı olarak alır ve sanal makineye Azure Konuk işletim sisteminin yeni yüklemesini yazar.
Rol yeniden çevrimiçi duruma getirilir.
VM rolü için, rol yeniden görüntülendiğinde, Azure rolü çevrimdışı olarak alır, onun için sağladığınız özel resmi yeniden uygular ve rolü çevrimiçine geri getirir.

Azure, rol yeniden görüntülendiğinde yerel depolama kaynaklarındaki verileri bakımını yapmaya çalışır; Ancak, geçici bir donanım arızası durumunda, yerel depolama kaynağı kaybolabilir.
Uygulamanız verilerin kalıcı olmasını gerektiriyorsa, Azure sürücüsü gibi dayanıklı bir veri kaynağına yazma önerilir.
Yerel depolama kaynağı tarafından tanımlandıkları yerel dizine yazılan tüm veriler, rol yeniden görüntülendiğinde kaybedilir.

## ÖRNEKLERDEN

### Örnek 1: rol örneğini yeniden yükleme
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -InstanceName "MyWebRole_IN_0" -Reboot
```

Bu komut, MySvc01 hizmetinin hazırlama dağıtımında MyWebRole_IN_0 adlı rol örneğini yeniden başlatır.

### Örnek 2: bir rol örneğini yeniden görüntüler
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -Reimage
```

Bu komut, MySvc01 bulut hizmetinin hazırlama dağıtımında rol örneklerini yeniden görüntüler.

### Örnek 3: tüm rol örneklerini yeniden görüntüler
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc1" -Slot "Production" -Reimage
```

Bu komut, MySvc01 hizmetinin üretim dağıtımındaki tüm rol örneklerini yeniden görüntüler.

## PARAMETRELERINE

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

### -InstanceName
Yeniden görüntü veya yeniden başlatma için rol örneğinin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Reboot
Bu cmdlet 'in belirtilen rol örneğini veya belirtilmemişse, tüm rol örneklerini yeniden önolduğunu belirtir.
*Yeniden başlatma* veya *yeniden görüntü* parametresi eklemeniz gerekir, ancak ikisini birden içeremez.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Yeniden görüntü
Bu cmdlet 'in belirtilen rol örneğinin veya belirtilmemişse, tüm rol örneklerinin yeniden yansımasını belirtir.
*Yeniden başlatma* veya *yeniden görüntü* parametresi eklemeniz gerekir, ancak ikisini birden içeremez.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HizmetAdı
Hizmetin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Yuvalı
Rol örneklerinin çalıştırdığı dağıtım ortamını belirtir.
Geçerli değerler: üretim ve hazırlama.
*DeploymentName* veya *yuva* parametresini ekleyebilirsiniz, ancak ikisini birden içeremez.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Set-AzureRole](./Set-AzureRole.md)


