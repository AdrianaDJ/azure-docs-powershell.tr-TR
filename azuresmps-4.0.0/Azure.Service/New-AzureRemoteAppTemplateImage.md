---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DBC4A0B8-A34A-47AC-930B-EFE23A95A216
online version: ''
schema: 2.0.0
ms.openlocfilehash: 178349299767eefb1d89c31a0199f53373bd2ae2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105995"
---
# New-AzureRemoteAppTemplateImage

## SYNOPSIS
Bir Azure RemoteApp şablonu resmini karşıya yükler veya içeri aktarır.

## INDEKI

### UploadLocalVhd (varsayılan)
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> [-Path] <String> [-Resume]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### AzureVmUpload
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> -AzureVmImageName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Yeni-Azureremoteapptemplateımage** cmdlet 'i karşıya yükler veya bir Azure RemoteApp şablonu görüntüsü alır.

## ÖRNEKLERDEN

### Örnek 1: şablon görüntüsü oluşturmak için VHD dosyasını karşıya yükleme
```
PS C:\> New-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -Location "North Europe" -Path "C:\RemoteAppImages\ContosoApps.vhd"
```

Bu komut C:\remoteappımages\contosoapps.vhd 'yi karşıya yükler ve Kuzey Avrupa veri merkezinde ContosoApps adlı bir şablon görüntüsü oluşturur.

## PARAMETRELERINE

### -AzureVmImageName
Şablon görüntüsü olarak kullanılacak Azure sanal makinesinin adını belirtir.

```yaml
Type: String
Parameter Sets: AzureVmUpload
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GörüntüAdı
Azure RemoteApp şablonu görüntüsünün adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Konum
Şablon görüntüsünün Azure bölgesini belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Yol
Şablon görüntüsünün dosya yolunu belirtir.

```yaml
Type: String
Parameter Sets: UploadLocalVhd
Aliases: 

Required: True
Position: 3
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

### -Özgeçmiş
Şablon görüntüsünün karşıya yüklenmesi kesintiye uğrarsa bu cmdlet 'in devam ettiğini gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: UploadLocalVhd
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

[Get-Azureremoteapptemplateımage](./Get-AzureRemoteAppTemplateImage.md)

[Remove-Azureremoteapptemplateımage](./Remove-AzureRemoteAppTemplateImage.md)

[Rename-Azureremoteapptemplateımage](./Rename-AzureRemoteAppTemplateImage.md)


