---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F420A47F-D036-4B31-AA59-97CFC9C79E75
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a53d0821832b29f0f1f6a0b2ab5f1353e3331a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106198"
---
# New-AzureVMImageDiskConfigSet

## SYNOPSIS
Disk yapılandırma kümesi nesnesi oluşturur.

## INDEKI

```
New-AzureVMImageDiskConfigSet [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Tanım
**New-AzureVMImageDiskConfigSet** cmdlet 'i, resim Güncelleştirme cmdlet 'ine geçirilen bir disk yapılandırma kümesi nesnesi oluşturur.
OSDiskConfig ve DataDiskConfig nesnesini kapsüller.
Sanal makine görüntüsünün işletim sistemi disk ve veri diski özelliklerini ayarlamak için **set-AzureVMImageOSDiskConfig** ve **set-AzureVMImageDataDiskConfig** cmdlet 'lerini kullanın.

## ÖRNEKLERDEN

### Örnek 1: disk yapılandırma kümesi nesnesi oluşturma
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

Bu komut, bir disk yapılandırma kümesi nesnesi oluşturur ve sonuçları $Disk adlı değişkende depolar.
Disk yapılandırması oluşturulduktan sonra, OSDiskConfig ve DataDiskConfig 'yi ayarlamak için kullanılır.
Ardından sanal makine yapılandırmayla güncelleştirilir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. Windowsazde. Commands. ServiceManagement. model. Virtualmachineımagediskconfigset

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureVMImageDiskConfigSet](./Get-AzureVMImageDiskConfigSet.md)

[Set-AzureVMImageOSDiskConfig](./Set-AzureVMImageOSDiskConfig.md)

[Set-AzureVMImageDataDiskConfig](./Set-AzureVMImageDataDiskConfig.md)


