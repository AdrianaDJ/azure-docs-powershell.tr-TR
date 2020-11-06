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
# <span data-ttu-id="76c51-101">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="76c51-101">Get-AzureStorageBlob</span></span>

## <span data-ttu-id="76c51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76c51-102">SYNOPSIS</span></span>
<span data-ttu-id="76c51-103">Kapsayıcıdaki blob 'ları listeler.</span><span class="sxs-lookup"><span data-stu-id="76c51-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="76c51-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76c51-104">SYNTAX</span></span>

### <span data-ttu-id="76c51-105">BlobName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="76c51-105">BlobName (Default)</span></span>
```
Get-AzureStorageBlob [[-Blob] <String>] [-Container] <String> [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="76c51-106">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="76c51-106">BlobPrefix</span></span>
```
Get-AzureStorageBlob [-Prefix <String>] [-Container] <String> [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="76c51-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="76c51-107">DESCRIPTION</span></span>
<span data-ttu-id="76c51-108">**Get-AzureStorageBlob** cmdlet 'ı bir Azure depolama hesabında belirtilen kapsayıcıdaki blob 'ları listeler.</span><span class="sxs-lookup"><span data-stu-id="76c51-108">The **Get-AzureStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="76c51-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76c51-109">EXAMPLES</span></span>

### <span data-ttu-id="76c51-110">Örnek 1: blob adına göre blob alma</span><span class="sxs-lookup"><span data-stu-id="76c51-110">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="76c51-111">Bu komut, blob almak için blob adı ve joker karakter kullanır.</span><span class="sxs-lookup"><span data-stu-id="76c51-111">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="76c51-112">Örnek 2: ardışık düzeni kullanarak blob alma</span><span class="sxs-lookup"><span data-stu-id="76c51-112">Example 2: Get a blob by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container* | Get-AzureStorageBlob
```

<span data-ttu-id="76c51-113">Bu komut, bir blob almak için ardışık düzeni kullanır.</span><span class="sxs-lookup"><span data-stu-id="76c51-113">This command uses the pipeline to get a blob.</span></span>

### <span data-ttu-id="76c51-114">Örnek 3: ad önekini kullanarak blob alma</span><span class="sxs-lookup"><span data-stu-id="76c51-114">Example 3: Get a blob by name prefix</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="76c51-115">Bu komut, blob almak için bir ad öneki kullanır.</span><span class="sxs-lookup"><span data-stu-id="76c51-115">This command uses a name prefix to get a blob.</span></span>

### <span data-ttu-id="76c51-116">Örnek 4: çoklu toplu işlemlerdeki blob 'ları listeleme</span><span class="sxs-lookup"><span data-stu-id="76c51-116">Example 4: List blobs in multiple batches</span></span>
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

<span data-ttu-id="76c51-117">Bu örnekte, Azure depolama bloblarını birden çok toplu işlem halinde listelemek için *maxCount* ve *continuationtoken* parametreleri kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="76c51-117">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="76c51-118">İlk dört komut, örnekte kullanılacak değişkenlere değerler atar.</span><span class="sxs-lookup"><span data-stu-id="76c51-118">The first four commands assign values to variables to use in the example.</span></span>

<span data-ttu-id="76c51-119">Beşinci komut, blob almak için **Get-AzureStorageBlob** cmdlet 'ini kullanan bir **do-while** ifadesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="76c51-119">The fifth command specifies a **Do-While** statement that uses the **Get-AzureStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="76c51-120">Bu ifadede $Token değişkeninde depolanan devam belirteci yer alır.</span><span class="sxs-lookup"><span data-stu-id="76c51-120">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="76c51-121">Döngü çalışırken $Token değişir.</span><span class="sxs-lookup"><span data-stu-id="76c51-121">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="76c51-122">Daha fazla bilgi için yazın `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="76c51-122">For more information, type `Get-Help About_Do`.</span></span>

<span data-ttu-id="76c51-123">Final komutu, toplam görüntülemek için **echo** komutunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="76c51-123">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="76c51-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76c51-124">PARAMETERS</span></span>

### <span data-ttu-id="76c51-125">-Blob</span><span class="sxs-lookup"><span data-stu-id="76c51-125">-Blob</span></span>
<span data-ttu-id="76c51-126">Joker karakter aramasında kullanılabilecek ad veya ad desenini belirtir.</span><span class="sxs-lookup"><span data-stu-id="76c51-126">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="76c51-127">Blob adı belirtilmezse cmdlet, belirtilen kapsayıcıdaki tüm blob 'ları listeler.</span><span class="sxs-lookup"><span data-stu-id="76c51-127">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="76c51-128">Bu parametre için bir değer belirtilmişse cmdlet, Bu parametreyle eşleşen adlara sahip tüm blob 'ları listeler.</span><span class="sxs-lookup"><span data-stu-id="76c51-128">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span>

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

### <span data-ttu-id="76c51-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="76c51-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="76c51-130">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="76c51-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="76c51-131">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="76c51-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="76c51-132">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="76c51-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="76c51-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="76c51-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="76c51-134">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="76c51-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="76c51-135">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="76c51-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="76c51-136">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="76c51-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="76c51-137">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="76c51-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="76c51-138">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="76c51-138">The default value is 10.</span></span>

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

### <span data-ttu-id="76c51-139">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="76c51-139">-Container</span></span>
<span data-ttu-id="76c51-140">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="76c51-140">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="76c51-141">-Context</span><span class="sxs-lookup"><span data-stu-id="76c51-141">-Context</span></span>
<span data-ttu-id="76c51-142">Blob listesi almak istediğiniz Azure Depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="76c51-142">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="76c51-143">Depolama bağlamı oluşturmak için New-AzureStorageContext cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="76c51-143">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="76c51-144">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="76c51-144">-ContinuationToken</span></span>
<span data-ttu-id="76c51-145">Blob listesi için bir devam belirteci belirtir.</span><span class="sxs-lookup"><span data-stu-id="76c51-145">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="76c51-146">Birden çok toplu işlemdeki blob 'ları listelemek için bu parametreyi ve *maxCount* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="76c51-146">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

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

### <span data-ttu-id="76c51-147">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="76c51-147">-MaxCount</span></span>
<span data-ttu-id="76c51-148">Bu cmdlet 'in döndürdüğü en fazla nesne sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="76c51-148">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="76c51-149">-Önek</span><span class="sxs-lookup"><span data-stu-id="76c51-149">-Prefix</span></span>
<span data-ttu-id="76c51-150">Almak istediğiniz blob adları için bir önek belirtir.</span><span class="sxs-lookup"><span data-stu-id="76c51-150">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="76c51-151">Bu parametre, aramada normal ifadeler veya joker karakterler kullanılmasını desteklemez.</span><span class="sxs-lookup"><span data-stu-id="76c51-151">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="76c51-152">Bu, kapsayıcıda yalnızca "My", "MyBlob1" ve "MyBlob2" adlı blob varsa ve "-prefix My \*" ifadesini belirtirseniz, cmdlet hiçbir blob döndürmez.</span><span class="sxs-lookup"><span data-stu-id="76c51-152">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="76c51-153">Ancak, "-önek" ifadesini belirtirseniz cmdlet, "benim", "MyBlob1" ve "MyBlob2" döndürür.</span><span class="sxs-lookup"><span data-stu-id="76c51-153">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

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

### <span data-ttu-id="76c51-154">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="76c51-154">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="76c51-155">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="76c51-155">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="76c51-156">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="76c51-156">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="76c51-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c51-157">CommonParameters</span></span>
<span data-ttu-id="76c51-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76c51-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c51-159">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76c51-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c51-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76c51-160">INPUTS</span></span>

## <span data-ttu-id="76c51-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76c51-161">OUTPUTS</span></span>

### <span data-ttu-id="76c51-162">AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="76c51-162">AzureStorageBlob</span></span>

## <span data-ttu-id="76c51-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76c51-163">NOTES</span></span>
* <span data-ttu-id="76c51-164">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76c51-164">SYNOPSIS</span></span>

## <span data-ttu-id="76c51-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76c51-165">RELATED LINKS</span></span>

[<span data-ttu-id="76c51-166">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="76c51-166">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="76c51-167">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="76c51-167">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)

[<span data-ttu-id="76c51-168">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="76c51-168">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)


