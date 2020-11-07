---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVhd.md
ms.openlocfilehash: f1af93009c905e8d66bd081ef8aa288c9acc0c05
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752737"
---
# Save-AzVhd

## SYNOPSIS
İndirilen. vhd yansımalarını yerel olarak kaydeder.

## INDEKI

### ResourceGroupParameterSetName
```
Save-AzVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### StorageKeyParameterSetName
```
Save-AzVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfThreads] <Int32>]
 [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Save-AzVhd** cmdlet 'i, bir dosyada depolanan bir blob 'dan. vhd yansımalarını kaydeder.
İşlemin kullandığı Downloader iş parçacıklarının sayısını ve var olan bir dosyayı değiştirip değiştirmeyeceğinizi belirtebilirsiniz.
Bu cmdlet içeriği olduğu gibi indirir.
Herhangi bir sanal sabit disk (VHD) biçim dönüştürmesi uygulamaz.

## ÖRNEKLERDEN

### Örnek 1: resim Indirme
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

Bu komut. vhd dosyasını indirir ve C:\vhd\win7ımage.vhdyerel yolunda depolar.

### Örnek 2: bir resmi Indirme ve yerel dosyanın üzerine yazma
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

Bu komut. vhd dosyasını indirir ve yerel yolda depolar.
Komut, *overwrite* parametresini içerir.
Bu nedenle, C:\vhd\wın7ımage.VHD zaten varsa bu komut bunu değiştirir.

### Örnek 3: belirtilen sayıda iş parçacığı kullanarak görüntü Indirme
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

Bu komut. vhd dosyasını indirir ve yerel yolda depolar.
Komut, *NesneSayısı* parametresi için 32 değerini belirtir.
Bu nedenle, cmdlet bu eylem için 32 iş parçacıklarını kullanır.

### Örnek 4: bir resmi Indirme ve depolama tuşunu belirtme
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

Bu komut. vhd dosyasını indirir ve depolama anahtarını belirtir.

## PARAMETRELERINE

### -Iş
Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

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
Depolama hesabının kaynak grubunun adını belirtir.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### System. Uri

## ÇıKıŞLAR

### Microsoft. Azure. Commands. COMPUTE. model. VhdDownloadContext

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzVhd](./Add-AzVhd.md)


