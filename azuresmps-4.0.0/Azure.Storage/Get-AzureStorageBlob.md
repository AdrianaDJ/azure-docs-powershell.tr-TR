---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: ''
schema: 2.0.0
ms.openlocfilehash: f7b68be6981343d14f7d1d8530a0af3c3eee199c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572409"
---
# Get-AzureStorageBlob

## SYNOPSIS
Kapsayıcıdaki blob 'ları listeler.

## INDEKI

### BlobName (varsayılan)
```
Get-AzureStorageBlob [[-Blob] <String>] [-Container] <String> [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### BlobPrefix
```
Get-AzureStorageBlob [-Prefix <String>] [-Container] <String> [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Tanım
**Get-AzureStorageBlob** cmdlet 'ı bir Azure depolama hesabında belirtilen kapsayıcıdaki blob 'ları listeler.

## ÖRNEKLERDEN

### Örnek 1: blob adına göre blob alma
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob blob*
```

Bu komut, blob almak için blob adı ve joker karakter kullanır.

### Örnek 2: ardışık düzeni kullanarak blob alma
```
PS C:\>Get-AzureStorageContainer -Name container* | Get-AzureStorageBlob
```

Bu komut, bir blob almak için ardışık düzeni kullanır.

### Örnek 3: ad önekini kullanarak blob alma
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Prefix "blob"
```

Bu komut, blob almak için bir ad öneki kullanır.

### Örnek 4: çoklu toplu işlemlerdeki blob 'ları listeleme
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzureStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

Bu örnekte, Azure depolama bloblarını birden çok toplu işlem halinde listelemek için *maxCount* ve *continuationtoken* parametreleri kullanılmaktadır.
İlk dört komut, örnekte kullanılacak değişkenlere değerler atar.

Beşinci komut, blob almak için **Get-AzureStorageBlob** cmdlet 'ini kullanan bir **do-while** ifadesi belirtir.
Bu ifadede $Token değişkeninde depolanan devam belirteci yer alır.
Döngü çalışırken $Token değişir.
Daha fazla bilgi için yazın `Get-Help About_Do` .

Final komutu, toplam görüntülemek için **echo** komutunu kullanır.

## PARAMETRELERINE

### -Blob
Joker karakter aramasında kullanılabilecek ad veya ad desenini belirtir.
Blob adı belirtilmezse cmdlet, belirtilen kapsayıcıdaki tüm blob 'ları listeler.
Bu parametre için bir değer belirtilmişse cmdlet, Bu parametreyle eşleşen adlara sahip tüm blob 'ları listeler.

```yaml
Type: String
Parameter Sets: BlobName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientTimeoutPerRequest
Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.
Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.
Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Maksimum eşzamanlı ağ çağrılarını belirtir.
Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.
Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.
Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.
Varsayılan değer 10 ' dır.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Kapsayıcı
Kapsayıcının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Context
Blob listesi almak istediğiniz Azure Depolama hesabını belirtir.
Depolama bağlamı oluşturmak için New-AzureStorageContext cmdlet 'ini kullanabilirsiniz.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ContinuationToken
Blob listesi için bir devam belirteci belirtir.
Birden çok toplu işlemdeki blob 'ları listelemek için bu parametreyi ve *maxCount* parametresini kullanın.

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCount
Bu cmdlet 'in döndürdüğü en fazla nesne sayısını belirtir.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Önek
Almak istediğiniz blob adları için bir önek belirtir.
Bu parametre, aramada normal ifadeler veya joker karakterler kullanılmasını desteklemez.
Bu, kapsayıcıda yalnızca "My", "MyBlob1" ve "MyBlob2" adlı blob varsa ve "-prefix My *" ifadesini belirtirseniz, cmdlet hiçbir blob döndürmez.
Ancak, "-önek" ifadesini belirtirseniz cmdlet, "benim", "MyBlob1" ve "MyBlob2" döndürür.

```yaml
Type: String
Parameter Sets: BlobPrefix
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.
Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.

```yaml
Type: Int32
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

### AzureStorageBlob

## NOTLARıNDA
* SYNOPSIS

## ILGILI BAĞLANTıLAR

[Get-AzureStorageBlobContent](./Get-AzureStorageBlobContent.md)

[Remove-AzureStorageBlob](./Remove-AzureStorageBlob.md)

[Set-AzureStorageBlobContent](./Set-AzureStorageBlobContent.md)


