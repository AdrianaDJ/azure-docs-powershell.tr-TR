---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: 9f4c20c29012609c773d176fb2f80c585bd9a851
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096722"
---
# <span data-ttu-id="79e88-101">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="79e88-101">Get-AzStorageBlob</span></span>

## <span data-ttu-id="79e88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79e88-102">SYNOPSIS</span></span>
<span data-ttu-id="79e88-103">Kapsayıcıdaki blob 'ları listeler.</span><span class="sxs-lookup"><span data-stu-id="79e88-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="79e88-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79e88-104">SYNTAX</span></span>

### <span data-ttu-id="79e88-105">BlobName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="79e88-105">BlobName (Default)</span></span>
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="79e88-106">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="79e88-106">BlobPrefix</span></span>
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="79e88-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="79e88-107">DESCRIPTION</span></span>
<span data-ttu-id="79e88-108">**Get-AzStorageBlob** cmdlet 'ı bir Azure depolama hesabında belirtilen kapsayıcıdaki blob 'ları listeler.</span><span class="sxs-lookup"><span data-stu-id="79e88-108">The **Get-AzStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="79e88-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79e88-109">EXAMPLES</span></span>

### <span data-ttu-id="79e88-110">Örnek 1: blob adına göre blob alma</span><span class="sxs-lookup"><span data-stu-id="79e88-110">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="79e88-111">Bu komut, blob almak için blob adı ve joker karakter kullanır.</span><span class="sxs-lookup"><span data-stu-id="79e88-111">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="79e88-112">Örnek 2: ardışık düzeni kullanarak kapsayıcıda blob alma</span><span class="sxs-lookup"><span data-stu-id="79e88-112">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="79e88-113">Bu komut, bir kapsayıcıya tüm blob 'ları (silinmiş durumda blob 'ları ekleme) almak için ardışık düzeni kullanır.</span><span class="sxs-lookup"><span data-stu-id="79e88-113">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="79e88-114">Örnek 3: ad önekine göre blob alma</span><span class="sxs-lookup"><span data-stu-id="79e88-114">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="79e88-115">Bu komut, blob almak için bir ad öneki kullanır.</span><span class="sxs-lookup"><span data-stu-id="79e88-115">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="79e88-116">Örnek 4: çoklu toplu işlemlerdeki blob 'ları listeleme</span><span class="sxs-lookup"><span data-stu-id="79e88-116">Example 4: List blobs in multiple batches</span></span>
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

<span data-ttu-id="79e88-117">Bu örnekte, Azure depolama bloblarını birden çok toplu işlem halinde listelemek için *maxCount* ve *continuationtoken* parametreleri kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="79e88-117">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="79e88-118">İlk dört komut, örnekte kullanılacak değişkenlere değerler atar.</span><span class="sxs-lookup"><span data-stu-id="79e88-118">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="79e88-119">Beşinci komut, blob almak için **Get-AzStorageBlob** cmdlet 'Ini kullanan **do-while** deyimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79e88-119">The fifth command specifies a **Do-While** statement that uses the **Get-AzStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="79e88-120">Bu ifadede $Token değişkeninde depolanan devam belirteci yer alır.</span><span class="sxs-lookup"><span data-stu-id="79e88-120">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="79e88-121">Döngü çalışırken $Token değişir.</span><span class="sxs-lookup"><span data-stu-id="79e88-121">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="79e88-122">Daha fazla bilgi için yazın `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="79e88-122">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="79e88-123">Final komutu, toplam görüntülemek için **echo** komutunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="79e88-123">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="79e88-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79e88-124">PARAMETERS</span></span>

### <span data-ttu-id="79e88-125">-Blob</span><span class="sxs-lookup"><span data-stu-id="79e88-125">-Blob</span></span>
<span data-ttu-id="79e88-126">Joker karakter aramasında kullanılabilecek ad veya ad desenini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79e88-126">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="79e88-127">Blob adı belirtilmezse cmdlet, belirtilen kapsayıcıdaki tüm blob 'ları listeler.</span><span class="sxs-lookup"><span data-stu-id="79e88-127">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="79e88-128">Bu parametre için bir değer belirtilmişse cmdlet, Bu parametreyle eşleşen adlara sahip tüm blob 'ları listeler.</span><span class="sxs-lookup"><span data-stu-id="79e88-128">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span> <span data-ttu-id="79e88-129">Bu parametre, dizede herhangi bir yerde joker karakterini destekler.</span><span class="sxs-lookup"><span data-stu-id="79e88-129">This parameter supports wildcards anywhere in the string.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="79e88-130">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="79e88-130">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="79e88-131">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="79e88-131">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="79e88-132">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="79e88-132">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="79e88-133">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="79e88-133">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79e88-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="79e88-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="79e88-135">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79e88-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="79e88-136">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79e88-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="79e88-137">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="79e88-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="79e88-138">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="79e88-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="79e88-139">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="79e88-139">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79e88-140">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="79e88-140">-Container</span></span>
<span data-ttu-id="79e88-141">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79e88-141">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79e88-142">-Context</span><span class="sxs-lookup"><span data-stu-id="79e88-142">-Context</span></span>
<span data-ttu-id="79e88-143">Blob listesi almak istediğiniz Azure Depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79e88-143">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="79e88-144">Depolama bağlamı oluşturmak için New-AzStorageContext cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79e88-144">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79e88-145">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="79e88-145">-ContinuationToken</span></span>
<span data-ttu-id="79e88-146">Blob listesi için bir devam belirteci belirtir.</span><span class="sxs-lookup"><span data-stu-id="79e88-146">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="79e88-147">Birden çok toplu işlemdeki blob 'ları listelemek için bu parametreyi ve *maxCount* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="79e88-147">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79e88-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79e88-148">-DefaultProfile</span></span>
<span data-ttu-id="79e88-149">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="79e88-149">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79e88-150">-Includedeleted</span><span class="sxs-lookup"><span data-stu-id="79e88-150">-IncludeDeleted</span></span>
<span data-ttu-id="79e88-151">Silinmiş blob 'u içer varsayılan olarak blob silinmiş blob 'u içermez.</span><span class="sxs-lookup"><span data-stu-id="79e88-151">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="79e88-152">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="79e88-152">-MaxCount</span></span>
<span data-ttu-id="79e88-153">Bu cmdlet 'in döndürdüğü en fazla nesne sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79e88-153">Specifies the maximum number of objects that this cmdlet returns.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79e88-154">-Önek</span><span class="sxs-lookup"><span data-stu-id="79e88-154">-Prefix</span></span>
<span data-ttu-id="79e88-155">Almak istediğiniz blob adları için bir önek belirtir.</span><span class="sxs-lookup"><span data-stu-id="79e88-155">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="79e88-156">Bu parametre, aramada normal ifadeler veya joker karakterler kullanılmasını desteklemez.</span><span class="sxs-lookup"><span data-stu-id="79e88-156">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="79e88-157">Bu, kapsayıcıda yalnızca "My", "MyBlob1" ve "MyBlob2" adlı blob varsa ve "-prefix My \*" ifadesini belirtirseniz, cmdlet hiçbir blob döndürmez.</span><span class="sxs-lookup"><span data-stu-id="79e88-157">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="79e88-158">Ancak, "-önek" ifadesini belirtirseniz cmdlet, "benim", "MyBlob1" ve "MyBlob2" döndürür.</span><span class="sxs-lookup"><span data-stu-id="79e88-158">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79e88-159">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="79e88-159">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="79e88-160">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79e88-160">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="79e88-161">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="79e88-161">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79e88-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79e88-162">CommonParameters</span></span>
<span data-ttu-id="79e88-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79e88-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79e88-164">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79e88-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79e88-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79e88-165">INPUTS</span></span>

### <span data-ttu-id="79e88-166">System. String</span><span class="sxs-lookup"><span data-stu-id="79e88-166">System.String</span></span>

### <span data-ttu-id="79e88-167">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="79e88-167">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="79e88-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79e88-168">OUTPUTS</span></span>

### <span data-ttu-id="79e88-169">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="79e88-169">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="79e88-170">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79e88-170">NOTES</span></span>

## <span data-ttu-id="79e88-171">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79e88-171">RELATED LINKS</span></span>

[<span data-ttu-id="79e88-172">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="79e88-172">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="79e88-173">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="79e88-173">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)

[<span data-ttu-id="79e88-174">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="79e88-174">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)


