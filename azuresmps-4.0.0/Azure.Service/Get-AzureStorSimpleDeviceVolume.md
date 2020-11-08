---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 79EE846E-D5BE-4808-BC6F-E3B16A308AB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9d0cd7ef0eacc7ff3e38c4619b60a0bd61f24f1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105566"
---
# Get-AzureStorSimpleDeviceVolume

## SYNOPSIS
Aygıttaki birimleri alır.

## INDEKI

### Identifybyparentobject
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Identifybyname
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureStorSimpleDeviceVolume** cmdlet 'i belirtilen bir birim kapsayıcısının veya belirtilen ada sahip birimdeki birimlerin listesini alır.
Döndürülen nesne aşağıdaki özellikleri içerir: 

- **AccessType**
- **AcrList**
- **AppType**
- **Veri kapsayıcısı**
- **Veri Containerıd**
- **Örnek**
- **Isbackupenabled**
- **Isadefaultbackupenabled**
- **Ismonitoringenabled**
- **Adlandır**
- **Medya**
- **Operationınprogress**
- **SizeInBytes**
- **VSN**

## ÖRNEKLERDEN

### Örnek 1: belirtilen kapsayıcıdaki birimleri alma
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container03" | Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm"
InstanceId             : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c
Name                   : Volume 1 Clone
Online                 : True
SizeInBytes            : 3298534883328
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c

InstanceId             : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe
Name                   : Volume 3 Clone
Online                 : True
SizeInBytes            : 1717986918400
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe

InstanceId             : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
Name                   : Volume 4
Online                 : True
SizeInBytes            : 1610612736000
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
```

Bu komut, **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet 'ini kullanarak Contoso63-AppVm adlı cihazda Container03 adındaki birim kapsayıcısını alır.
Bu komut, bu kapsayıcıyı geçerli cmdlet 'e geçirmek için ardışık düzen işlecini kullanır.
Bu cmdlet, Contoso63-AppVm adlı aygıtta bu kapsayıcıdaki tüm birimleri alır.

### Örnek 2: adını kullanarak bir birimi alma
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18"
InstanceId             : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
Name                   : Volume18
Online                 : True
SizeInBytes            : 2748779069440
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
```

Bu komut, Contoso63-AppVm adındaki cihazda Volume18 adındaki birimi alır.

## PARAMETRELERINE

### -Aygıtadı
Birimlerin alınacağı StorSimple aygıtının adını belirtir.

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

### -Birimkapsayıcısı
Alınacak birimleri içeren bir **datacontainer** nesnesi olarak birim kapsayıcısını belirtir.
**Datacontainer** almak için **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet 'ini kullanın.

```yaml
Type: DataContainer
Parameter Sets: IdentifyByParentObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BirimAdı
Alınacak birimin adını belirtir.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Veri kapsayıcısı
Bu cmdlet, alınacak birimi içeren bir **Datacontainer** nesnesini kabul eder.

## ÇıKıŞLAR

### VirtualDisk, IList\<VirtualDisk\>
Bu cmdlet, *BirimAdı* parametresini belirttiğinizde bir **VirtualDisk** nesnesi döndürür.
*Birimkapsayıcısı* belirtirseniz, bu cmdlet bir **IList \<VirtualDisk\>** nesnesi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureStorSimpleDeviceVolume](./New-AzureStorSimpleDeviceVolume.md)

[Remove-AzureStorSimpleDeviceVolume](./Remove-AzureStorSimpleDeviceVolume.md)

[Set-AzureStorSimpleDeviceVolume](./Set-AzureStorSimpleDeviceVolume.md)

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)


