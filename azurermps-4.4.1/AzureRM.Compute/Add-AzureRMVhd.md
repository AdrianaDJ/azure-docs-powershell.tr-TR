---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRMVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRMVhd.md
ms.openlocfilehash: 106f6d9ed794ac2e4595f480616fa2c64663e554
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594810"
---
# Add-AzureRmVhd

## SYNOPSIS
Azure 'daki bulut depolama hesabında bir şirket içi sanal makineden blob 'a sanal sabit disk yükler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Add-AzureRmVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Add-AzureRmVhd** cmdlet 'i, şirket içi sanal sabit diskleri. vhd dosya biçiminde, bir BLOB depolama hesabına sabit sanal sabit diskler olarak yükler.
Kullanılacak olan Uploader iş parçacıklarının sayısını, belirtilen hedef URI 'de var olan bir bloonun üzerine yazacak şekilde yapılandırabilirsiniz.
Ayrıca desteklenen şirket içi. vhd dosyasının düzeltme eki yüklenmiş bir sürümünü karşıya yükleyebilir.
Bir temel sanal sabit disk zaten karşıya yüklendiğinde, temel görüntüyü içeren fark kayıt disklerini üst öğe olarak yükleyebilirsiniz.
Paylaşılan erişim imzası (SAS) URI 'SI de desteklenir.

## ÖRNEKLERDEN

### Örnek 1: VHD dosyası ekleme
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

Bu komut bir depolama hesabına. vhd dosyası ekler.

### Örnek 2: VHD dosyası ekleme ve hedefin üzerine yazma
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

Bu komut bir depolama hesabına. vhd dosyası ekler.
Komut mevcut bir dosyanın üzerine yazılır.

### Örnek 3: VHD dosyası ekleme ve iş parçacıklarının sayısını belirtme
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

Bu komut bir depolama hesabına. vhd dosyası ekler.
Komut, dosyayı karşıya yüklemek için kullanılacak iş parçacıklarının sayısını belirtir.

### Örnek 4: VHD dosyası ekleme ve SAS URI 'sini belirtme
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

Bu komut bir depolama hesabına. vhd dosyası ekler ve SAS URI 'sini belirtir.

## PARAMETRELERINE

### -Baseımageuritopatch
Azure Blob depolamada temel görüntü blob 'una URI 'yi belirtir.
Bu parametrenin değeri olarak SAS belirtilebilir.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hedef
BLOB depolama alanındaki bir blob URI 'sini belirtir.
Parametre SAS URI 'yi destekler, ancak düzeltme senaryoları hedefi SAS URI olamaz.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LocalFilePath
Yerel. vhd dosyasının yolunu belirtir.

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Numberofof Loaderthreads
. Vhd dosyası yüklenirken kullanılacak Uploader iş parçacıklarının sayısını belirtir.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OverWrite
Bu cmdlet 'in belirtilen hedef URI 'de var olan bir blobın üzerine yazabileceğini gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Sanal makinenin kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
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

[Kaydet-AzureRmVhd](./Save-AzureRmVhd.md)


