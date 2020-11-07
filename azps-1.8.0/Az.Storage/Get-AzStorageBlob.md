---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: ebcd1b1534504cf533ab7f3cfb8cfa3bf07611ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758675"
---
# <span data-ttu-id="60f7d-101">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="60f7d-101">Get-AzStorageBlob</span></span>

## <span data-ttu-id="60f7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="60f7d-103">Kapsayıcıdaki blob 'ları listeler.</span><span class="sxs-lookup"><span data-stu-id="60f7d-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="60f7d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="60f7d-104">SYNTAX</span></span>

### <span data-ttu-id="60f7d-105">BlobName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="60f7d-105">BlobName (Default)</span></span>
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="60f7d-106">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="60f7d-106">BlobPrefix</span></span>
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="60f7d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="60f7d-107">DESCRIPTION</span></span>
<span data-ttu-id="60f7d-108">**Get-AzStorageBlob** cmdlet 'ı bir Azure depolama hesabında belirtilen kapsayıcıdaki blob 'ları listeler.</span><span class="sxs-lookup"><span data-stu-id="60f7d-108">The **Get-AzStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="60f7d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="60f7d-109">EXAMPLES</span></span>

### <span data-ttu-id="60f7d-110">Örnek 1: blob adına göre blob alma</span><span class="sxs-lookup"><span data-stu-id="60f7d-110">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="60f7d-111">Bu komut, blob almak için blob adı ve joker karakter kullanır.</span><span class="sxs-lookup"><span data-stu-id="60f7d-111">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="60f7d-112">Örnek 2: ardışık düzeni kullanarak kapsayıcıda blob alma</span><span class="sxs-lookup"><span data-stu-id="60f7d-112">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="60f7d-113">Bu komut, bir kapsayıcıya tüm blob 'ları (silinmiş durumda blob 'ları ekleme) almak için ardışık düzeni kullanır.</span><span class="sxs-lookup"><span data-stu-id="60f7d-113">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="60f7d-114">Örnek 3: ad önekine göre blob alma</span><span class="sxs-lookup"><span data-stu-id="60f7d-114">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="60f7d-115">Bu komut, blob almak için bir ad öneki kullanır.</span><span class="sxs-lookup"><span data-stu-id="60f7d-115">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="60f7d-116">Örnek 4: çoklu toplu işlemlerdeki blob 'ları listeleme</span><span class="sxs-lookup"><span data-stu-id="60f7d-116">Example 4: List blobs in multiple batches</span></span>
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

<span data-ttu-id="60f7d-117">Bu örnekte, Azure depolama bloblarını birden çok toplu işlem halinde listelemek için *maxCount* ve *continuationtoken* parametreleri kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="60f7d-117">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="60f7d-118">İlk dört komut, örnekte kullanılacak değişkenlere değerler atar.</span><span class="sxs-lookup"><span data-stu-id="60f7d-118">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="60f7d-119">Beşinci komut, blob almak için **Get-AzStorageBlob** cmdlet 'Ini kullanan **do-while** deyimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="60f7d-119">The fifth command specifies a **Do-While** statement that uses the **Get-AzStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="60f7d-120">Bu ifadede $Token değişkeninde depolanan devam belirteci yer alır.</span><span class="sxs-lookup"><span data-stu-id="60f7d-120">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="60f7d-121">Döngü çalışırken $Token değişir.</span><span class="sxs-lookup"><span data-stu-id="60f7d-121">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="60f7d-122">Daha fazla bilgi için yazın `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="60f7d-122">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="60f7d-123">Final komutu, toplam görüntülemek için **echo** komutunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="60f7d-123">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="60f7d-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="60f7d-124">PARAMETERS</span></span>

### <span data-ttu-id="60f7d-125">-Blob</span><span class="sxs-lookup"><span data-stu-id="60f7d-125">-Blob</span></span>
<span data-ttu-id="60f7d-126">Joker karakter aramasında kullanılabilecek ad veya ad desenini belirtir.</span><span class="sxs-lookup"><span data-stu-id="60f7d-126">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="60f7d-127">Blob adı belirtilmezse cmdlet, belirtilen kapsayıcıdaki tüm blob 'ları listeler.</span><span class="sxs-lookup"><span data-stu-id="60f7d-127">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="60f7d-128">Bu parametre için bir değer belirtilmişse cmdlet, Bu parametreyle eşleşen adlara sahip tüm blob 'ları listeler.</span><span class="sxs-lookup"><span data-stu-id="60f7d-128">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60f7d-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="60f7d-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="60f7d-130">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="60f7d-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="60f7d-131">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="60f7d-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="60f7d-132">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="60f7d-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="60f7d-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="60f7d-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="60f7d-134">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60f7d-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="60f7d-135">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="60f7d-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="60f7d-136">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="60f7d-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="60f7d-137">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="60f7d-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="60f7d-138">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="60f7d-138">The default value is 10.</span></span>

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

### <span data-ttu-id="60f7d-139">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="60f7d-139">-Container</span></span>
<span data-ttu-id="60f7d-140">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60f7d-140">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="60f7d-141">-Context</span><span class="sxs-lookup"><span data-stu-id="60f7d-141">-Context</span></span>
<span data-ttu-id="60f7d-142">Blob listesi almak istediğiniz Azure Depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60f7d-142">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="60f7d-143">Depolama bağlamı oluşturmak için New-AzStorageContext cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="60f7d-143">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="60f7d-144">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="60f7d-144">-ContinuationToken</span></span>
<span data-ttu-id="60f7d-145">Blob listesi için bir devam belirteci belirtir.</span><span class="sxs-lookup"><span data-stu-id="60f7d-145">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="60f7d-146">Birden çok toplu işlemdeki blob 'ları listelemek için bu parametreyi ve *maxCount* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="60f7d-146">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60f7d-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60f7d-147">-DefaultProfile</span></span>
<span data-ttu-id="60f7d-148">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="60f7d-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60f7d-149">-Includedeleted</span><span class="sxs-lookup"><span data-stu-id="60f7d-149">-IncludeDeleted</span></span>
<span data-ttu-id="60f7d-150">Silinmiş blob 'u içer varsayılan olarak blob silinmiş blob 'u içermez.</span><span class="sxs-lookup"><span data-stu-id="60f7d-150">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="60f7d-151">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="60f7d-151">-MaxCount</span></span>
<span data-ttu-id="60f7d-152">Bu cmdlet 'in döndürdüğü en fazla nesne sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60f7d-152">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="60f7d-153">-Önek</span><span class="sxs-lookup"><span data-stu-id="60f7d-153">-Prefix</span></span>
<span data-ttu-id="60f7d-154">Almak istediğiniz blob adları için bir önek belirtir.</span><span class="sxs-lookup"><span data-stu-id="60f7d-154">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="60f7d-155">Bu parametre, aramada normal ifadeler veya joker karakterler kullanılmasını desteklemez.</span><span class="sxs-lookup"><span data-stu-id="60f7d-155">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="60f7d-156">Bu, kapsayıcıda yalnızca "My", "MyBlob1" ve "MyBlob2" adlı blob varsa ve "-prefix My \*" ifadesini belirtirseniz, cmdlet hiçbir blob döndürmez.</span><span class="sxs-lookup"><span data-stu-id="60f7d-156">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="60f7d-157">Ancak, "-önek" ifadesini belirtirseniz cmdlet, "benim", "MyBlob1" ve "MyBlob2" döndürür.</span><span class="sxs-lookup"><span data-stu-id="60f7d-157">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

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

### <span data-ttu-id="60f7d-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="60f7d-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="60f7d-159">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60f7d-159">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="60f7d-160">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="60f7d-160">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="60f7d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f7d-161">CommonParameters</span></span>
<span data-ttu-id="60f7d-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="60f7d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f7d-163">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60f7d-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f7d-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="60f7d-164">INPUTS</span></span>

### <span data-ttu-id="60f7d-165">System. String</span><span class="sxs-lookup"><span data-stu-id="60f7d-165">System.String</span></span>

### <span data-ttu-id="60f7d-166">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="60f7d-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="60f7d-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="60f7d-167">OUTPUTS</span></span>

### <span data-ttu-id="60f7d-168">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="60f7d-168">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="60f7d-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="60f7d-169">NOTES</span></span>

## <span data-ttu-id="60f7d-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="60f7d-170">RELATED LINKS</span></span>

[<span data-ttu-id="60f7d-171">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="60f7d-171">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="60f7d-172">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="60f7d-172">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)

[<span data-ttu-id="60f7d-173">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="60f7d-173">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)


