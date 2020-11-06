---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVhd.md
ms.openlocfilehash: cc43308f0e0051a050b3983968d9c86f67ec66b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594770"
---
# Save-AzureRmVhd

## SYNOPSIS
İndirilen. vhd yansımalarını yerel olarak kaydeder.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ResourceGroupParameterSetName
```
Save-AzureRmVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StorageKeyParameterSetName
```
Save-AzureRmVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Save-AzureRmVhd** cmdlet 'i, bir dosyada depolanan bir blob 'dan. vhd resimlerini kaydeder.
İşlemin kullandığı Downloader iş parçacıklarının sayısını ve var olan bir dosyayı değiştirip değiştirmeyeceğinizi belirtebilirsiniz.

Bu cmdlet içeriği olduğu gibi indirir.
Herhangi bir sanal sabit disk (VHD) biçim dönüştürmesi uygulamaz.

## ÖRNEKLERDEN

### Örnek 1: resim Indirme
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

Bu komut. vhd dosyasını indirir ve C:\vhd\win7ımage.vhdyerel yolunda depolar.

### Örnek 2: bir resmi Indirme ve yerel dosyanın üzerine yazma
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

Bu komut. vhd dosyasını indirir ve yerel yolda depolar.
Komut, *overwrite* parametresini içerir.
Bu nedenle, C:\vhd\wın7ımage.VHD zaten varsa bu komut bunu değiştirir.

### Örnek 3: belirtilen sayıda iş parçacığı kullanarak görüntü Indirme
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

Bu komut. vhd dosyasını indirir ve yerel yolda depolar.
Komut, *NesneSayısı* parametresi için 32 değerini belirtir.
Bu nedenle, cmdlet bu eylem için 32 iş parçacıklarını kullanır.

### Örnek 4: bir resmi Indirme ve depolama tuşunu belirtme
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw=="
```

Bu komut. vhd dosyasını indirir ve depolama anahtarını belirtir.

## PARAMETRELERINE

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

### -LocalFilePath
Kaydedilen yansımanın yerel dosya yolunu belirtir.

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Iş parçacıkları
İndirme sırasında bu cmdlet 'in kullandığı indirme iş parçacıklarının sayısını belirtir.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverWrite
Bu cmdlet 'in, varsa *LocalFilePath* dosyası tarafından belirtilen dosyayı değiştirdiği anlamına gelir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Sanal makinenin kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceUri
Blob 'un içindeki Tekdüzen Kaynak tanımlayıcısını (URI) belirtir `Azure` .

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKey
BLOB depolama hesabının depolama anahtarını belirtir.
Bir anahtar belirtmezseniz, bu cmdlet Azure 'dan *SourceUri* 'deki hesabın depolama anahtarını belirlemeye çalışır.

```yaml
Type: System.String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
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

[Add-AzureRmVhd](./Add-AzureRMVhd.md)


