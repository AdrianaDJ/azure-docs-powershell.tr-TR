---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblobcopystate
schema: 2.0.0
ms.openlocfilehash: 3b74b1f68bf6bb990f76d18b73f113e6a0f8e446
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939445"
---
# <span data-ttu-id="075d0-101">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="075d0-101">Get-AzureStorageBlobCopyState</span></span>

## <span data-ttu-id="075d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="075d0-102">SYNOPSIS</span></span>
<span data-ttu-id="075d0-103">Bir Azure depolama blobundan kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="075d0-103">Gets the copy status of an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="075d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="075d0-104">SYNTAX</span></span>

### <span data-ttu-id="075d0-105">Ad boru hattı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="075d0-105">NamePipeline (Default)</span></span>
```
Get-AzureStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="075d0-106">Blobboru hattı</span><span class="sxs-lookup"><span data-stu-id="075d0-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="075d0-107">Kapsayıcı boru hattı</span><span class="sxs-lookup"><span data-stu-id="075d0-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="075d0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="075d0-108">DESCRIPTION</span></span>
<span data-ttu-id="075d0-109">**Get-AzureStorageBlobCopyState** cmdlet 'ı bir Azure depolama blobundan kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="075d0-109">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="075d0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="075d0-110">EXAMPLES</span></span>

### <span data-ttu-id="075d0-111">Örnek 1: blob 'un kopyalama durumunu alma</span><span class="sxs-lookup"><span data-stu-id="075d0-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="075d0-112">Bu komut, ContosoPlanning2015 adındaki blob 'un karşıya yüklemelerini olan kapsayıcıda kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="075d0-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="075d0-113">Örnek 2: ardışık düzeni kullanarak blob 'un kopyalama durumunu alma</span><span class="sxs-lookup"><span data-stu-id="075d0-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzureStorageBlobCopyState
```

<span data-ttu-id="075d0-114">Bu komut, ContosoPlanning2015 adındaki geri yüklemeler adlı kapsayıcıda, **Get-AzureStorageBlob** cmdlet 'ini kullanarak ve sonucu ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="075d0-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="075d0-115">**Get-AzureStorageBlobCopyState** cmdlet 'i söz konusu blob 'un kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="075d0-115">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="075d0-116">Örnek 3: ardışık düzeni kullanarak bir taşıyıcıda blob kopyalama durumunu alma</span><span class="sxs-lookup"><span data-stu-id="075d0-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="075d0-117">Bu komut **Get-AzureStorageBlob** cmdlet 'i kullanarak adlandırılmış kapsayıcıyı alır ve sonucu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="075d0-117">This command gets the container named by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="075d0-118">**Get-AzureStorageContainer** cmdlet 'i, bu kapsayıcıdaki ContosoPlanning2015 adındaki blob için kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="075d0-118">The **Get-AzureStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="075d0-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="075d0-119">PARAMETERS</span></span>

### <span data-ttu-id="075d0-120">-Blob</span><span class="sxs-lookup"><span data-stu-id="075d0-120">-Blob</span></span>
<span data-ttu-id="075d0-121">Blob 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="075d0-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="075d0-122">Bu cmdlet, bu parametrenin belirttiği Azure Depolama Blobu için blob kopyalama işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="075d0-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="075d0-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="075d0-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="075d0-124">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="075d0-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="075d0-125">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="075d0-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="075d0-126">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="075d0-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="075d0-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="075d0-127">-CloudBlob</span></span>
<span data-ttu-id="075d0-128">Azure depolama Istemci kitaplığından bir **Cloudblob** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="075d0-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="075d0-129">**Cloudblob** nesnesi edinmek için Get-AzureStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="075d0-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="075d0-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="075d0-130">-CloudBlobContainer</span></span>
<span data-ttu-id="075d0-131">Azure depolama Istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="075d0-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="075d0-132">Bu cmdlet, bu parametrenin belirttiği kapsayıcıda blob 'un kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="075d0-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="075d0-133">**Cloudblobcontainer** nesnesi edinmek için Get-AzureStorageContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="075d0-133">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="075d0-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="075d0-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="075d0-135">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="075d0-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="075d0-136">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="075d0-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="075d0-137">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="075d0-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="075d0-138">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="075d0-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="075d0-139">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="075d0-139">The default value is 10.</span></span>

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

### <span data-ttu-id="075d0-140">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="075d0-140">-Container</span></span>
<span data-ttu-id="075d0-141">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="075d0-141">Specifies the name of a container.</span></span>
<span data-ttu-id="075d0-142">Bu cmdlet, bu parametrenin belirttiği kapsayıcıdaki bir blob için kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="075d0-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="075d0-143">-Context</span><span class="sxs-lookup"><span data-stu-id="075d0-143">-Context</span></span>
<span data-ttu-id="075d0-144">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="075d0-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="075d0-145">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="075d0-145">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="075d0-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="075d0-146">-DefaultProfile</span></span>
<span data-ttu-id="075d0-147">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="075d0-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="075d0-148">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="075d0-148">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="075d0-149">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="075d0-149">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="075d0-150">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="075d0-150">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="075d0-151">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="075d0-151">-WaitForComplete</span></span>
<span data-ttu-id="075d0-152">Bu cmdlet 'in kopyanın bitmesini beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="075d0-152">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="075d0-153">Bu parametreyi belirtmezseniz, bu cmdlet hemen bir sonuç döndürür.</span><span class="sxs-lookup"><span data-stu-id="075d0-153">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="075d0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="075d0-154">CommonParameters</span></span>
<span data-ttu-id="075d0-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="075d0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="075d0-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="075d0-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="075d0-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="075d0-157">INPUTS</span></span>

### <span data-ttu-id="075d0-158">Microsoft. Windowsazde. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="075d0-158">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="075d0-159">Microsoft. Windowsazde. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="075d0-159">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="075d0-160">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="075d0-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="075d0-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="075d0-161">OUTPUTS</span></span>

### <span data-ttu-id="075d0-162">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="075d0-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="075d0-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="075d0-163">NOTES</span></span>

## <span data-ttu-id="075d0-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="075d0-164">RELATED LINKS</span></span>

[<span data-ttu-id="075d0-165">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="075d0-165">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="075d0-166">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="075d0-166">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)


