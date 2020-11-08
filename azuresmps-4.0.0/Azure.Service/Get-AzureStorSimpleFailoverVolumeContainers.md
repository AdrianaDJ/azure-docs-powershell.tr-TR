---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BABBA19E-5833-452C-9E36-811EAE7C20F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb326281058f0ff9280c4b87c0530241ece801e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105561"
---
# Get-AzureStorSimpleFailoverVolumeContainers

## SYNOPSIS
Cihaz yük devretmesi için birim kapsayıcı gruplarını alır.

## INDEKI

### Identifybyıd
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Identifybyname
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureStorSimpleFailoverVolumeContainers** cmdlet 'i cihaz yük devretmesi için birim kapsayıcı gruplarını alır.
**Start-AzureStorSimpleDeviceFailover** cmdlet 'ine tek bir **birimkapsayıcısı** grubu veya **birimkapsayıcısı** gruplar dizisi geçirin.
Yalnızca **ısdcgroupeligıblefordr** özelliği için $true değeri olan gruplar yük devretmeye uygundur.

## ÖRNEKLERDEN

### Örnek 1: yük devretme birimi kapsayıcılarını alma
```
PS C:\>Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7"

DCGroup                    IneligibilityMessage          IsDCGroupEligibleForDR
-------                    --------------------          ----------------------
{VolumeContainer1889078...                                                 True
{VC_01}                    No cloud snapshot found                        False
{VolumeContainer7306959}   No cloud snapshot found                        False
{VolumeContainer407850151} No cloud snapshot found                        False
```

Bu komut, yük devretme birimi kapsayıcılarını alır.
Yalnızca **ısdcgroupeligıblefordr** özelliği için $true değeri olan dcgroups cihaz yük devretmesi için kullanılabilir.

## PARAMETRELERINE

### -DeviceID
Cmdlet 'in çalıştırılacağı StorSimple aygıtının örnek KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Aygıtadı
Cmdlet 'in çalıştırılacağı StorSimple aygıtının adını belirtir.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### 'Te\<DataContainerGroup\>
Bu cmdlet, **Birimkapsayıcısı** gruplarının listesini döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Start-AzureStorSimpleDeviceFailoverJob](./Start-AzureStorSimpleDeviceFailoverJob.md)

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)


