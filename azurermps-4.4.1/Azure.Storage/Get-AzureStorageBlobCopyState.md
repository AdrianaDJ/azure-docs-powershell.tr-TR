---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 6a61e076bf91d1ed994f9745d18a6f4832925250
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763422"
---
# <span data-ttu-id="a9e36-101">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="a9e36-101">Get-AzureStorageBlobCopyState</span></span>

## <span data-ttu-id="a9e36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9e36-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e36-103">Bir Azure depolama blobundan kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="a9e36-103">Gets the copy status of an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9e36-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9e36-104">SYNTAX</span></span>

### <span data-ttu-id="a9e36-105">Ad boru hattı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a9e36-105">NamePipeline (Default)</span></span>
```
Get-AzureStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a9e36-106">Blobboru hattı</span><span class="sxs-lookup"><span data-stu-id="a9e36-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9e36-107">Kapsayıcı boru hattı</span><span class="sxs-lookup"><span data-stu-id="a9e36-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a9e36-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9e36-108">DESCRIPTION</span></span>
<span data-ttu-id="a9e36-109">**Get-AzureStorageBlobCopyState** cmdlet 'ı bir Azure depolama blobundan kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="a9e36-109">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="a9e36-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9e36-110">EXAMPLES</span></span>

### <span data-ttu-id="a9e36-111">Örnek 1: blob 'un kopyalama durumunu alma</span><span class="sxs-lookup"><span data-stu-id="a9e36-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="a9e36-112">Bu komut, ContosoPlanning2015 adındaki blob 'un karşıya yüklemelerini olan kapsayıcıda kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="a9e36-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="a9e36-113">Örnek 2: ardışık düzeni kullanarak blob 'un kopyalama durumunu alma</span><span class="sxs-lookup"><span data-stu-id="a9e36-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzureStorageBlobCopyState
```

<span data-ttu-id="a9e36-114">Bu komut, ContosoPlanning2015 adındaki geri yüklemeler adlı kapsayıcıda, **Get-AzureStorageBlob** cmdlet 'ini kullanarak ve sonucu ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="a9e36-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a9e36-115">**Get-AzureStorageBlobCopyState** cmdlet 'i söz konusu blob 'un kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="a9e36-115">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="a9e36-116">Örnek 3: ardışık düzeni kullanarak bir taşıyıcıda blob kopyalama durumunu alma</span><span class="sxs-lookup"><span data-stu-id="a9e36-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="a9e36-117">Bu komut **Get-AzureStorageBlob** cmdlet 'i kullanarak adlandırılmış kapsayıcıyı alır ve sonucu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="a9e36-117">This command gets the container named by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="a9e36-118">**Get-AzureStorageContainer** cmdlet 'i, bu kapsayıcıdaki ContosoPlanning2015 adındaki blob için kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="a9e36-118">The **Get-AzureStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="a9e36-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9e36-119">PARAMETERS</span></span>

### <span data-ttu-id="a9e36-120">-Blob</span><span class="sxs-lookup"><span data-stu-id="a9e36-120">-Blob</span></span>
<span data-ttu-id="a9e36-121">Blob 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9e36-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="a9e36-122">Bu cmdlet, bu parametrenin belirttiği Azure Depolama Blobu için blob kopyalama işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="a9e36-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="a9e36-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a9e36-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a9e36-124">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9e36-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a9e36-125">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="a9e36-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a9e36-126">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="a9e36-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a9e36-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a9e36-127">-CloudBlob</span></span>
<span data-ttu-id="a9e36-128">Azure depolama Istemci kitaplığından bir **Cloudblob** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9e36-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="a9e36-129">**Cloudblob** nesnesi edinmek için Get-AzureStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a9e36-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="a9e36-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a9e36-130">-CloudBlobContainer</span></span>
<span data-ttu-id="a9e36-131">Azure depolama Istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9e36-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="a9e36-132">Bu cmdlet, bu parametrenin belirttiği kapsayıcıda blob 'un kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="a9e36-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="a9e36-133">**Cloudblobcontainer** nesnesi edinmek için Get-AzureStorageContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a9e36-133">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="a9e36-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a9e36-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a9e36-135">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9e36-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a9e36-136">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9e36-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a9e36-137">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="a9e36-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a9e36-138">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="a9e36-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a9e36-139">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="a9e36-139">The default value is 10.</span></span>

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

### <span data-ttu-id="a9e36-140">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="a9e36-140">-Container</span></span>
<span data-ttu-id="a9e36-141">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9e36-141">Specifies the name of a container.</span></span>
<span data-ttu-id="a9e36-142">Bu cmdlet, bu parametrenin belirttiği kapsayıcıdaki bir blob için kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="a9e36-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="a9e36-143">-Context</span><span class="sxs-lookup"><span data-stu-id="a9e36-143">-Context</span></span>
<span data-ttu-id="a9e36-144">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9e36-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a9e36-145">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a9e36-145">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a9e36-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a9e36-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a9e36-147">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9e36-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="a9e36-148">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="a9e36-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a9e36-149">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="a9e36-149">-WaitForComplete</span></span>
<span data-ttu-id="a9e36-150">Bu cmdlet 'in kopyanın bitmesini beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9e36-150">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="a9e36-151">Bu parametreyi belirtmezseniz, bu cmdlet hemen bir sonuç döndürür.</span><span class="sxs-lookup"><span data-stu-id="a9e36-151">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="a9e36-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e36-152">CommonParameters</span></span>
<span data-ttu-id="a9e36-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9e36-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e36-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9e36-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e36-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9e36-155">INPUTS</span></span>

### <span data-ttu-id="a9e36-156">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="a9e36-156">IStorageContext</span></span>

<span data-ttu-id="a9e36-157">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="a9e36-157">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="a9e36-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9e36-158">OUTPUTS</span></span>

### <span data-ttu-id="a9e36-159">CopyState</span><span class="sxs-lookup"><span data-stu-id="a9e36-159">CopyState</span></span>

## <span data-ttu-id="a9e36-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9e36-160">NOTES</span></span>

## <span data-ttu-id="a9e36-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9e36-161">RELATED LINKS</span></span>

[<span data-ttu-id="a9e36-162">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a9e36-162">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="a9e36-163">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a9e36-163">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)


