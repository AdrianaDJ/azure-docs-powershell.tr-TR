---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 53580FF1-D905-40FD-A5F0-D5FBCD036E0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a51fd8210d2fe7fb224ed43650a354e383ed4e54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105776"
---
# Start-AzureStorSimpleDeviceFailoverJob

## SYNOPSIS
Birim kapsayıcı gruplarının bir yük devretme işlemini başlatır.

## INDEKI

### Boş (varsayılan)
```
Start-AzureStorSimpleDeviceFailoverJob
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Identifybyıd
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceId <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Identifybyname
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceName <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceName <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Start-AzureStorSimpleDeviceFailoverJob** cmdlet 'i bir cihazdan diğerine bir veya daha fazla birim kapsayıcı grubundan bir yük devretme işlemi başlatır.

## ÖRNEKLERDEN

### Örnek 1: adlandırılmış bir cihaz ve adlandırılmış hedef cihaz için bir yük devretme işi başlatma
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Start-AzureStorSimpleDeviceFailoverJob -DeviceName "ChewD_App7" -TargetDeviceName "Fuller05" -Force
a3d902be-8ffb-42a4-bbf8-0a1b30db71b2_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

Bu komut, **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet 'ini kullanarak ChewD_App7 adlı cihazın yük devretme birimi kapsayıcılarını alır.
Bu komut sonuçları, **ısdcgroupeligiblefordr** özelliği için $true dışında bir değer içeren kapsayıcıları geçen **nesne** cmdlet 'ine geçirir.
Daha fazla bilgi için yazın `Get-Help Where-Object` .
Geçerli cmdlet kalan çalışma bölümü kapsayıcılarının yük devretme işlerini başlatır.
Komut, cihaz adını ve hedef cihaz adını belirtir.
Komut, cmdlet 'in başladığı işin örnek KIMLIĞINI döndürür.

### Örnek 2: KIMLIĞI belirtilen bir cihaz ve hedef cihaz için bir yük devretme işi başlatma
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Select-Object -First 1 | Start-AzureStorSimpleDeviceFailoverJob -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925" -TargetDeviceId "0ee59ae9-0293-46e2-ae56-bc308c8e5520" -Force
4c5ac0d0-4b66-465c-98f5-aec90505ad12_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

Bu komut, **Get-AzureStorSimpleFailoverVolumeContainers** kullanarak ChewD_App7 adlı cihaz için yük devretme birimi kapsayıcılarını alır.
Bu komut sonuçları, **ısdcgroupeligiblefordr** özelliği için $true dışında bir değer içeren bu Containters geçen **nesneye** geçirir.
Cmdlet sonuçları geçerli cmdlet 'e geçilecek ilk nesneyi seçen **seçme-nesne** cmdlet 'ine geçirir.
Daha fazla bilgi için yazın `Get-Help Select-Object` .
Geçerli cmdlet, seçili yük devretme birimi kapsayıcısının yük devretme işlerini başlatır.
Komut, cihaz KIMLIĞINI ve hedef cihaz KIMLIĞINI belirtir.
Komut, cmdlet 'in başladığı işin örnek KIMLIĞINI döndürür.

## PARAMETRELERINE

### -DeviceID
Birim kapsayıcı gruplarının var olduğu StorSimple aygıtının örnek KIMLIĞINI belirtir.

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
Birim kapsayıcı gruplarının var olduğu StorSimple aygıtının adını belirtir.

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

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

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

### -Targetdeviceıd
Bu cmdlet 'in birim kapsayıcı grupları üzerinde başarısız olduğu StorSimple aygıtının örnek KIMLIĞINI belirtir.

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

### -Targetaygıtadı
Bu cmdlet 'in birim kapsayıcı grupları üzerinde başarısız olduğu StorSimple aygıtının adını belirtir.

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

### -Birimcontainergroups
Başka bir cihaza bu cmdlet 'in başarısız olduğu birim kapsayıcı gruplarının listesini belirtir.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Listeniz\<DataContainerGroup\>
Birim kapsayıcı gruplarının listesini bu cmdlet 'e boru edebilirsiniz.

## ÇıKıŞLAR

### Dizisi

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorSimpleFailoverVolumeContainers](./Get-AzureStorSimpleFailoverVolumeContainers.md)


