---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: 534919a404ad415963408816b78e9bbf1f349965
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268097"
---
# Get-AzBatchNodeFileContent

## SYNOPSIS
Bir toplu Iş düğümü dosyası alır.

## INDEKI

### Task_Id_Path
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Task_Id_Stream
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ComputeNode_Id_Path
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ComputeNode_Id_Stream
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject_Path
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject_Stream
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-AzBatchNodeFileContent** cmdlet 'ı bir Azure toplu iş düğümü dosyası alır ve bunu bir dosya veya akışa kaydeder.

## ÖRNEKLERDEN

### Örnek 1: görevle ilişkilendirilmiş bir toplu Iş düğümü dosyası alma ve dosyayı kaydetme
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Bu komut, StdOut.txt adlı düğüm dosyasını alır ve yerel bilgisayardaki E:\PowerShell\StdOut.txt dosya yoluna kaydeder.
StdOut.txt düğümü, KIMLIĞI Job01 olan iş için KIMLIĞI Task01 olan görevle ilişkilendirilir.
$Context değişkenine bağlam atamak için Get-AzBatchAccountKey cmdlet 'ini kullanın.

### Örnek 2: bir toplu Iş düğümü dosyası alın ve ardışık düzeni kullanarak belirtilen dosya yoluna kaydedin
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Bu komut, StdErr.txt adındaki düğüm dosyasını Get-AzBatchNodeFile cmdlet 'i kullanarak alır.
Komut, ardışık düzen işlecini kullanarak bu dosyayı geçerli cmdlet 'e geçirir.
Geçerli cmdlet, dosyayı yerel bilgisayardaki E:\PowerShell\StdOut.txt dosya yoluna kaydeder.
StdOut.txt düğümü, KIMLIĞI Job02 olan iş için KIMLIĞI Task02 olan görevle ilişkilendirilir.

### Örnek 3: görevle ilişkilendirilmiş bir toplu Iş düğümü dosyası alma ve bunu bir akışa yönlendirme
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

İlk komut New-Object cmdlet 'ini kullanarak bir akış oluşturur ve $Stream değişkeninde depolar.
İkinci komut, KIMLIĞI Job03 olan iş için KIMLIĞI Task11 olan görevden StdOut.txt adlı düğüm dosyasını alır.
Komut dosya içeriğini $Stream akışa yönlendirir.

### Örnek 4: işlem düğümünden bir düğüm dosyası alma ve kaydetme
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Bu komut, ComputeNode01 kimliğine sahip havuzda KIMLIK Pool01 olan işlem düğümünden düğüm dosyası Startup\StdOut.txt alır.
Komut dosyayı yerel bilgisayardaki E:\PowerShell\StdOut.txt dosya yoluna kaydeder.

### Örnek 5: işlem düğümünden bir düğüm dosyası alın ve bunu ardışık düzen kullanarak kaydedin
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Bu komut, ComputeNode01 KIMLIĞINE sahip işlem düğümünden Get-AzBatchNodeFile kullanarak düğüm dosyası Startup\StdOut.txt alır.
Compute düğümü, KIMLIK Pool01 havuzunda.
Komut bu düğüm dosyasını geçerli cmdlet 'e geçirir.
Bu cmdlet dosyayı yerel bilgisayardaki E:\PowerShell\StdOut.txt dosya yoluna kaydeder.

### Örnek 6: işlem düğümünden bir düğüm dosyası alın ve bunu bir akışa yönlendirin
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

İlk komut New-Object cmdlet 'ini kullanarak bir akış oluşturur ve $Stream değişkeninde depolar.
İkinci komut, KIMLIĞI Pool01 olan havuzda KIMLIĞI ComputeNode01 olan COMPUTE düğümünden StdOut.txt adlı düğüm dosyasını alır.
Komut dosya içeriğini $Stream akışa yönlendirir.

## PARAMETRELERINE

### -BatchContext
Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.
BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır. Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın. Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır. Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ByteRangeEnd
İndirilecek bayt aralığının sonu.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ByteRangeStart
İndirilecek bayt aralığının başlangıcı.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Computenodeıd
Bu cmdlet 'in döndürdüğü düğüm dosyasını içeren COMPUTE düğümünün KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -DestinationPath
Bu cmdlet 'in düğüm dosyasını kaydettiği dosya yolunu belirtir.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationStream
Bu cmdlet 'in düğüm dosyası içeriğini yazdığı akışı belirtir.
Bu cmdlet bu akışı kapatmaz veya geri sarmaz.

```yaml
Type: System.IO.Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Bu cmdlet 'in aldığı dosyayı, **Psnodefile** nesnesi olarak belirtir.
Düğüm dosyası nesnesi edinmek için Get-AzBatchNodeFile cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Hedef görevi içeren işin KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Yol
İndirilecek olan düğüm dosyasının yolu.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
Bu cmdlet 'in aldığı düğüm dosyasını içeren COMPUTE düğümünü içeren havuzun KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TaskID
Görevin KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### Microsoft.Azure.Commands.Batch. Modeller. PSNodeFile

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## ÇıKıŞLAR

### System. void

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchNodeFile](./Get-AzBatchNodeFile.md)

[Azure toplu Iş cmdlet 'Leri](/powershell/module/Az.Batch/)
