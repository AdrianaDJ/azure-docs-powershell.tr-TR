---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 6f9b08b59ff4b89243a26442b793bf2cf70f73d3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096714"
---
# <span data-ttu-id="7fcea-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="7fcea-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="7fcea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fcea-102">SYNOPSIS</span></span>
<span data-ttu-id="7fcea-103">Bir Azure depolama blobundan kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="7fcea-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="7fcea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7fcea-104">SYNTAX</span></span>

### <span data-ttu-id="7fcea-105">Ad boru hattı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7fcea-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7fcea-106">Blobboru hattı</span><span class="sxs-lookup"><span data-stu-id="7fcea-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7fcea-107">Kapsayıcı boru hattı</span><span class="sxs-lookup"><span data-stu-id="7fcea-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="7fcea-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7fcea-108">DESCRIPTION</span></span>
<span data-ttu-id="7fcea-109">**Get-AzStorageBlobCopyState** cmdlet 'ı bir Azure depolama blobundan kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="7fcea-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="7fcea-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7fcea-110">EXAMPLES</span></span>

### <span data-ttu-id="7fcea-111">Örnek 1: blob 'un kopyalama durumunu alma</span><span class="sxs-lookup"><span data-stu-id="7fcea-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="7fcea-112">Bu komut, ContosoPlanning2015 adındaki blob 'un karşıya yüklemelerini olan kapsayıcıda kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="7fcea-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="7fcea-113">Örnek 2: ardışık düzeni kullanarak blob 'un kopyalama durumunu alma</span><span class="sxs-lookup"><span data-stu-id="7fcea-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="7fcea-114">Bu komut, Contosoyüklemelerini ContosoPlanning2015 adlı kapsayıcıda **Get-AzStorageBlob** cmdlet 'ini kullanarak alır ve sonucu ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="7fcea-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7fcea-115">**Get-AzStorageBlobCopyState** cmdlet 'i söz konusu blob 'un kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="7fcea-115">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="7fcea-116">Örnek 3: ardışık düzeni kullanarak bir taşıyıcıda blob kopyalama durumunu alma</span><span class="sxs-lookup"><span data-stu-id="7fcea-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="7fcea-117">Bu komut **Get-AzStorageBlob** cmdlet 'ini kullanarak adlandırılmış kapsayıcıyı alır ve sonucu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="7fcea-117">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="7fcea-118">**Get-AzStorageContainer** cmdlet 'i, bu kapsayıcıdaki ContosoPlanning2015 adındaki blob için kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="7fcea-118">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="7fcea-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7fcea-119">PARAMETERS</span></span>

### <span data-ttu-id="7fcea-120">-Blob</span><span class="sxs-lookup"><span data-stu-id="7fcea-120">-Blob</span></span>
<span data-ttu-id="7fcea-121">Blob 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7fcea-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="7fcea-122">Bu cmdlet, bu parametrenin belirttiği Azure Depolama Blobu için blob kopyalama işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="7fcea-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fcea-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7fcea-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7fcea-124">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="7fcea-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7fcea-125">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="7fcea-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7fcea-126">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="7fcea-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7fcea-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="7fcea-127">-CloudBlob</span></span>
<span data-ttu-id="7fcea-128">Azure depolama Istemci kitaplığından bir **Cloudblob** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7fcea-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="7fcea-129">**Cloudblob** nesnesi edinmek için Get-AzStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7fcea-129">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fcea-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="7fcea-130">-CloudBlobContainer</span></span>
<span data-ttu-id="7fcea-131">Azure depolama Istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7fcea-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="7fcea-132">Bu cmdlet, bu parametrenin belirttiği kapsayıcıda blob 'un kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="7fcea-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="7fcea-133">**Cloudblobcontainer** nesnesi edinmek için Get-AzStorageContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7fcea-133">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fcea-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7fcea-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7fcea-135">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7fcea-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7fcea-136">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7fcea-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7fcea-137">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="7fcea-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7fcea-138">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="7fcea-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7fcea-139">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="7fcea-139">The default value is 10.</span></span>

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

### <span data-ttu-id="7fcea-140">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="7fcea-140">-Container</span></span>
<span data-ttu-id="7fcea-141">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7fcea-141">Specifies the name of a container.</span></span>
<span data-ttu-id="7fcea-142">Bu cmdlet, bu parametrenin belirttiği kapsayıcıdaki bir blob için kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="7fcea-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fcea-143">-Context</span><span class="sxs-lookup"><span data-stu-id="7fcea-143">-Context</span></span>
<span data-ttu-id="7fcea-144">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7fcea-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7fcea-145">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7fcea-145">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7fcea-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fcea-146">-DefaultProfile</span></span>
<span data-ttu-id="7fcea-147">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7fcea-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fcea-148">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7fcea-148">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7fcea-149">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7fcea-149">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="7fcea-150">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="7fcea-150">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="7fcea-151">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="7fcea-151">-WaitForComplete</span></span>
<span data-ttu-id="7fcea-152">Bu cmdlet 'in kopyanın bitmesini beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7fcea-152">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="7fcea-153">Bu parametreyi belirtmezseniz, bu cmdlet hemen bir sonuç döndürür.</span><span class="sxs-lookup"><span data-stu-id="7fcea-153">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="7fcea-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fcea-154">CommonParameters</span></span>
<span data-ttu-id="7fcea-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7fcea-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fcea-156">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fcea-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fcea-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7fcea-157">INPUTS</span></span>

### <span data-ttu-id="7fcea-158">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="7fcea-158">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="7fcea-159">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="7fcea-159">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="7fcea-160">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="7fcea-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7fcea-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7fcea-161">OUTPUTS</span></span>

### <span data-ttu-id="7fcea-162">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="7fcea-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="7fcea-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7fcea-163">NOTES</span></span>

## <span data-ttu-id="7fcea-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7fcea-164">RELATED LINKS</span></span>

[<span data-ttu-id="7fcea-165">Başlangıç-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7fcea-165">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="7fcea-166">Dur-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7fcea-166">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)


