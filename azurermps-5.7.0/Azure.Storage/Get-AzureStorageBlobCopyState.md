---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
ms.openlocfilehash: fba71dbac836fb6cc6551982945135e8e9410744
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587724"
---
# <span data-ttu-id="8e534-101">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="8e534-101">Get-AzureStorageBlobCopyState</span></span>

## <span data-ttu-id="8e534-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e534-102">SYNOPSIS</span></span>
<span data-ttu-id="8e534-103">Bir Azure depolama blobundan kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="8e534-103">Gets the copy status of an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e534-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e534-104">SYNTAX</span></span>

### <span data-ttu-id="8e534-105">Ad boru hattı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8e534-105">NamePipeline (Default)</span></span>
```
Get-AzureStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="8e534-106">Blobboru hattı</span><span class="sxs-lookup"><span data-stu-id="8e534-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e534-107">Kapsayıcı boru hattı</span><span class="sxs-lookup"><span data-stu-id="8e534-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="8e534-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e534-108">DESCRIPTION</span></span>
<span data-ttu-id="8e534-109">**Get-AzureStorageBlobCopyState** cmdlet 'ı bir Azure depolama blobundan kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="8e534-109">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="8e534-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e534-110">EXAMPLES</span></span>

### <span data-ttu-id="8e534-111">Örnek 1: blob 'un kopyalama durumunu alma</span><span class="sxs-lookup"><span data-stu-id="8e534-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="8e534-112">Bu komut, ContosoPlanning2015 adındaki blob 'un karşıya yüklemelerini olan kapsayıcıda kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="8e534-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="8e534-113">Örnek 2: ardışık düzeni kullanarak blob 'un kopyalama durumunu alma</span><span class="sxs-lookup"><span data-stu-id="8e534-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzureStorageBlobCopyState
```

<span data-ttu-id="8e534-114">Bu komut, ContosoPlanning2015 adındaki geri yüklemeler adlı kapsayıcıda, **Get-AzureStorageBlob** cmdlet 'ini kullanarak ve sonucu ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="8e534-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8e534-115">**Get-AzureStorageBlobCopyState** cmdlet 'i söz konusu blob 'un kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="8e534-115">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="8e534-116">Örnek 3: ardışık düzeni kullanarak bir taşıyıcıda blob kopyalama durumunu alma</span><span class="sxs-lookup"><span data-stu-id="8e534-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="8e534-117">Bu komut **Get-AzureStorageBlob** cmdlet 'i kullanarak adlandırılmış kapsayıcıyı alır ve sonucu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="8e534-117">This command gets the container named by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="8e534-118">**Get-AzureStorageContainer** cmdlet 'i, bu kapsayıcıdaki ContosoPlanning2015 adındaki blob için kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="8e534-118">The **Get-AzureStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="8e534-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e534-119">PARAMETERS</span></span>

### <span data-ttu-id="8e534-120">-Blob</span><span class="sxs-lookup"><span data-stu-id="8e534-120">-Blob</span></span>
<span data-ttu-id="8e534-121">Blob 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e534-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="8e534-122">Bu cmdlet, bu parametrenin belirttiği Azure Depolama Blobu için blob kopyalama işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="8e534-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e534-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8e534-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8e534-124">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e534-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8e534-125">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="8e534-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8e534-126">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="8e534-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8e534-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="8e534-127">-CloudBlob</span></span>
<span data-ttu-id="8e534-128">Azure depolama Istemci kitaplığından bir **Cloudblob** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e534-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="8e534-129">**Cloudblob** nesnesi edinmek için Get-AzureStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8e534-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e534-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="8e534-130">-CloudBlobContainer</span></span>
<span data-ttu-id="8e534-131">Azure depolama Istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e534-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="8e534-132">Bu cmdlet, bu parametrenin belirttiği kapsayıcıda blob 'un kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="8e534-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="8e534-133">**Cloudblobcontainer** nesnesi edinmek için Get-AzureStorageContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8e534-133">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e534-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8e534-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8e534-135">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e534-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8e534-136">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e534-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8e534-137">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="8e534-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8e534-138">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="8e534-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8e534-139">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="8e534-139">The default value is 10.</span></span>

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

### <span data-ttu-id="8e534-140">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="8e534-140">-Container</span></span>
<span data-ttu-id="8e534-141">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e534-141">Specifies the name of a container.</span></span>
<span data-ttu-id="8e534-142">Bu cmdlet, bu parametrenin belirttiği kapsayıcıdaki bir blob için kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="8e534-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e534-143">-Context</span><span class="sxs-lookup"><span data-stu-id="8e534-143">-Context</span></span>
<span data-ttu-id="8e534-144">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e534-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8e534-145">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8e534-145">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8e534-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8e534-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8e534-147">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e534-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="8e534-148">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="8e534-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="8e534-149">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="8e534-149">-WaitForComplete</span></span>
<span data-ttu-id="8e534-150">Bu cmdlet 'in kopyanın bitmesini beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e534-150">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="8e534-151">Bu parametreyi belirtmezseniz, bu cmdlet hemen bir sonuç döndürür.</span><span class="sxs-lookup"><span data-stu-id="8e534-151">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e534-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e534-152">CommonParameters</span></span>
<span data-ttu-id="8e534-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e534-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e534-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e534-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e534-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e534-155">INPUTS</span></span>

### <span data-ttu-id="8e534-156">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="8e534-156">IStorageContext</span></span>

<span data-ttu-id="8e534-157">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8e534-157">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="8e534-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e534-158">OUTPUTS</span></span>

### <span data-ttu-id="8e534-159">CopyState</span><span class="sxs-lookup"><span data-stu-id="8e534-159">CopyState</span></span>

## <span data-ttu-id="8e534-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e534-160">NOTES</span></span>

## <span data-ttu-id="8e534-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e534-161">RELATED LINKS</span></span>

[<span data-ttu-id="8e534-162">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8e534-162">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="8e534-163">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8e534-163">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)


