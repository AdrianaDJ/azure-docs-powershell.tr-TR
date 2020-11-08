---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 14a6a7932d82d240522d524604a8337e1804c72b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934097"
---
# <span data-ttu-id="9599f-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="9599f-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="9599f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9599f-102">SYNOPSIS</span></span>
<span data-ttu-id="9599f-103">Bir Azure depolama blobundan kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="9599f-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="9599f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9599f-104">SYNTAX</span></span>

### <span data-ttu-id="9599f-105">Ad boru hattı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9599f-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9599f-106">Blobboru hattı</span><span class="sxs-lookup"><span data-stu-id="9599f-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9599f-107">Kapsayıcı boru hattı</span><span class="sxs-lookup"><span data-stu-id="9599f-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="9599f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9599f-108">DESCRIPTION</span></span>
<span data-ttu-id="9599f-109">**Get-AzStorageBlobCopyState** cmdlet 'ı bir Azure depolama blobundan kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="9599f-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="9599f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9599f-110">EXAMPLES</span></span>

### <span data-ttu-id="9599f-111">Örnek 1: blob 'un kopyalama durumunu alma</span><span class="sxs-lookup"><span data-stu-id="9599f-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="9599f-112">Bu komut, ContosoPlanning2015 adındaki blob 'un karşıya yüklemelerini olan kapsayıcıda kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="9599f-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="9599f-113">Örnek 2: ardışık düzeni kullanarak blob 'un kopyalama durumunu alma</span><span class="sxs-lookup"><span data-stu-id="9599f-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="9599f-114">Bu komut, Contosoyüklemelerini ContosoPlanning2015 adlı kapsayıcıda **Get-AzStorageBlob** cmdlet 'ini kullanarak alır ve sonucu ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="9599f-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9599f-115">**Get-AzStorageBlobCopyState** cmdlet 'i söz konusu blob 'un kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="9599f-115">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="9599f-116">Örnek 3: ardışık düzeni kullanarak bir taşıyıcıda blob kopyalama durumunu alma</span><span class="sxs-lookup"><span data-stu-id="9599f-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="9599f-117">Bu komut **Get-AzStorageBlob** cmdlet 'ini kullanarak adlandırılmış kapsayıcıyı alır ve sonucu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="9599f-117">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="9599f-118">**Get-AzStorageContainer** cmdlet 'i, bu kapsayıcıdaki ContosoPlanning2015 adındaki blob için kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="9599f-118">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="9599f-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9599f-119">PARAMETERS</span></span>

### <span data-ttu-id="9599f-120">-Blob</span><span class="sxs-lookup"><span data-stu-id="9599f-120">-Blob</span></span>
<span data-ttu-id="9599f-121">Blob 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9599f-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="9599f-122">Bu cmdlet, bu parametrenin belirttiği Azure Depolama Blobu için blob kopyalama işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="9599f-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="9599f-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9599f-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9599f-124">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="9599f-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9599f-125">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="9599f-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9599f-126">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="9599f-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9599f-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="9599f-127">-CloudBlob</span></span>
<span data-ttu-id="9599f-128">Azure depolama Istemci kitaplığından bir **Cloudblob** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9599f-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="9599f-129">**Cloudblob** nesnesi edinmek için Get-AzStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9599f-129">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="9599f-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="9599f-130">-CloudBlobContainer</span></span>
<span data-ttu-id="9599f-131">Azure depolama Istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9599f-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="9599f-132">Bu cmdlet, bu parametrenin belirttiği kapsayıcıda blob 'un kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="9599f-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="9599f-133">**Cloudblobcontainer** nesnesi edinmek için Get-AzStorageContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9599f-133">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="9599f-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9599f-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9599f-135">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9599f-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9599f-136">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9599f-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9599f-137">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="9599f-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9599f-138">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="9599f-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9599f-139">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="9599f-139">The default value is 10.</span></span>

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

### <span data-ttu-id="9599f-140">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="9599f-140">-Container</span></span>
<span data-ttu-id="9599f-141">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9599f-141">Specifies the name of a container.</span></span>
<span data-ttu-id="9599f-142">Bu cmdlet, bu parametrenin belirttiği kapsayıcıdaki bir blob için kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="9599f-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="9599f-143">-Context</span><span class="sxs-lookup"><span data-stu-id="9599f-143">-Context</span></span>
<span data-ttu-id="9599f-144">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9599f-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9599f-145">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9599f-145">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9599f-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9599f-146">-DefaultProfile</span></span>
<span data-ttu-id="9599f-147">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9599f-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9599f-148">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9599f-148">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9599f-149">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9599f-149">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="9599f-150">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="9599f-150">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="9599f-151">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="9599f-151">-WaitForComplete</span></span>
<span data-ttu-id="9599f-152">Bu cmdlet 'in kopyanın bitmesini beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9599f-152">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="9599f-153">Bu parametreyi belirtmezseniz, bu cmdlet hemen bir sonuç döndürür.</span><span class="sxs-lookup"><span data-stu-id="9599f-153">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="9599f-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9599f-154">CommonParameters</span></span>
<span data-ttu-id="9599f-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9599f-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9599f-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9599f-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9599f-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9599f-157">INPUTS</span></span>

### <span data-ttu-id="9599f-158">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="9599f-158">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="9599f-159">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="9599f-159">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="9599f-160">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="9599f-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9599f-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9599f-161">OUTPUTS</span></span>

### <span data-ttu-id="9599f-162">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9599f-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="9599f-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9599f-163">NOTES</span></span>

## <span data-ttu-id="9599f-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9599f-164">RELATED LINKS</span></span>

[<span data-ttu-id="9599f-165">Başlangıç-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="9599f-165">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="9599f-166">Dur-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="9599f-166">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)

