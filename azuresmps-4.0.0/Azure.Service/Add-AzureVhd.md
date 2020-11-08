---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 99DC239C-EA68-4830-9345-762CD6A3F68C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 320b95add2806f48121151a71bdf36a572fa05a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105718"
---
# Add-AzureVhd

## SYNOPSIS
Azure 'daki bulut depolama hesabında bir şirket içi bilgisayardan bir blob 'a VHD dosyası yükler.

## INDEKI

```
Add-AzureVhd [-Destination] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfUploaderThreads] <Int32>]
 [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**Add-AzureVhd** cmdlet 'i şirket içi sanal sabit DISK (VHD) görüntülerine, sabit. vhd yansımaları olarak bir BLOB depolama hesabına yükler.
Belirtilen hedef URI 'de zaten varolan bir blob 'un kullanacağı Uploader iş parçacıklarının sayısını belirtmek gibi karşıya yükleme işlemini yapılandırmak için parametreler içerir.
Şirket içi VHD görüntülerinde, daha önce karşıya yüklenen temel görüntülerin karşıya yüklenebilmesi gerekmeden fark Disk görüntülerinin yüklenebilmesi için düzeltme eki senaryosu da desteklenmektedir. Paylaşılan erişim Imzası (SAS) URI 'SI de desteklenir.

## ÖRNEKLERDEN

### Örnek 1: VHD dosyası ekleme
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

Bu komut bir depolama hesabına. vhd dosyası ekler.

### Örnek 2: VHD dosyası ekleme ve hedefin üzerine yazma
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

Bu komut bir depolama hesabına. vhd dosyası ekler.

### Örnek 3: VHD dosyası ekleme ve iş parçacıklarının sayısını belirtme
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

Bu komut bir depolama hesabına. vhd dosyası ekler ve dosyayı karşıya yüklemek için kullanılacak iş parçacıklarının sayısını belirtir.

### Örnek 4: VHD dosyası ekleme ve SAS URI 'sini belirtme
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01-09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveOSIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

Bu komut bir depolama hesabına. vhd dosyası ekler ve SAS URI 'sini belirtir.

## PARAMETRELERINE

### -Baseımageuritopatch
Azure Blob depolamada temel görüntü blob 'una bir URI belirtir.
URI girişinde SAS girişi de desteklenir.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hedef
Microsoft Azure Blob depolamada bir blob URI 'SI belirtir.
URI girişinde SAS desteklenir.
Ancak, düzeltme eki senaryolarında hedef SAS URI 'SI olamaz.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -LocalFilePath
Türleri. vhd dosyasının dosya yolu.

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Numberofof Loaderthreads
Karşıya yükleme için kullanılacak iş parçacıklarının sayısını belirtir.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OverWrite
Varsa, bu cmdlet 'in belirtilen hedef URI 'de var olan blobu sildiğini belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Save-AzureVhd](./Save-AzureVhd.md)


