---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278134"
---
# New-AzBatchResourceFile

## SYNOPSIS
Tarafından kullanım için bir kaynak dosyası oluşturur `New-AzBatchTask` .

## INDEKI

### HttpUrl (varsayılan)
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StorageContainerUrl 'Si
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AutoStorageContainerName
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Tarafından kullanım için bir kaynak dosyası oluşturur `New-AzBatchTask` .

## ÖRNEKLERDEN

### Örnek 1: tek bir dosyaya işaret eden bir HTTP URL 'sinden kaynak dosyası oluşturma
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

`PSResourceFile`Http url 'sine başvuru oluşturur.

### Örnek 2: Azure depolama kapsayıcısı URL 'sinden kaynak dosyası oluşturma
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

`PSResourceFile`Azure depolama kapsayıcısı URL 'sine başvuru oluşturur. Kapsayıcıdaki tüm dosyalar belirtilen klasöre indirilir.

### Örnek 3: otomatik depolama kapsayıcısı adından kaynak dosyası oluşturma
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Bir `PSResourceFile` Otomatik depolama kapsayıcısı adına başvuru oluşturur. Kapsayıcıdaki tüm dosyalar belirtilen klasöre indirilir.

## PARAMETRELERINE

### -AutoStorageContainerName
Otomatik depolama hesabındaki depolama kapsayıcısı adı.

```yaml
Type: System.String
Parameter Sets: AutoStorageContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlobPrefix
Bir Azure depolama kapsayıcısından blob indirme sırasında kullanılacak blob önekini alır.
Yalnızca adları belirtilen önekle başlayan blob indirilir.
Bu önek bir kısmi dosya adı veya alt dizin olabilir.
Bir önek belirtilmemişse, kapsayıcıdaki tüm dosyalar indirilir.

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
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

### -FileMode
Dosya izin modu özniteliğini sekizlik biçimde alır.
Bu özellik yalnızca kaynak dosyası bir Linux düğümüne indirildiğinde uygulanabilir.
Linux düğümü için bu özellik belirtilmemişse, varsayılan değer 0770 olur.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DosyaYolu
Görevin çalışma diziniyle göreli olarak dosyaların indirileceği işlem düğümündeki konum. HttpUrl parametresi belirtilmişse, DosyaYolu gereklidir ve dosya adı da içinde olmak üzere dosyanın indirileceği yolu açıklar. Aksi takdirde, AutoStorageContainerName veya StorageContainerUrl parametreleri belirtilmişse, DosyaYolu isteğe bağlıdır ve dosyaların indirileceği dizindir. DosyaYolu 'nin bir dizin olarak kullanıldığı durumlarda, giriş verileriyle ilişkilendirilmiş olan tüm dizin yapısı tam olarak korunur ve belirtilen FilePath dizinine eklenir. Belirtilen göreli yol görevin çalışma dizinini kesemezsiniz (örneğin, '.. ' kullanarak).

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpUrl
İndirilecek dosyanın URL 'SI.
URL, Azure Blob depolama ise, anonim erişim kullanılarak okunabilir olmalıdır; Yani, toplu Iş hizmeti, blob indirilirken herhangi bir kimlik bilgisi sunmaz.
Azure Storage 'da blob için böyle bir URL almanın iki yolu vardır: blob 'a okuma izinleri veren paylaşılan erişim Imzasını (SAS) ekleme veya blob veya kapsayıcısının ACL 'sini genel erişime izin verecek şekilde ayarlama.

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainerUrl 'Si
Azure Blob depolama içindeki blob kapsayıcısının URL 'SI.
Anonim erişim kullanılarak bu URL okunabilir ve kararlı olmalıdır; Yani, toplu Iş hizmeti kapsayıcıdan blob 'ları indirirken herhangi bir kimlik bilgisi sunmaz.
Azure Storage 'daki bir kapsayıcının URL 'sini almanın iki yolu vardır: kapsayıcıya bir paylaşılan erişim Imzası (SAS) ekleme veya kapsayıcının ACL 'sini genel erişime izin verecek şekilde ayarlama.

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft.Azure.Commands.Batch. Modeller. PSResourceFile

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzBatchTask](./New-AzBatchTask.md)