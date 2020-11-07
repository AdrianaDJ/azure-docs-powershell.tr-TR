---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/stop-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
ms.openlocfilehash: e644d1d4813aeea30624576a3b4f1d3fb2cbc672
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758520"
---
# <span data-ttu-id="b11db-101">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b11db-101">Stop-AzStorageBlobCopy</span></span>

## <span data-ttu-id="b11db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b11db-102">SYNOPSIS</span></span>
<span data-ttu-id="b11db-103">Kopyalama işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="b11db-103">Stops a copy operation.</span></span>

## <span data-ttu-id="b11db-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b11db-104">SYNTAX</span></span>

### <span data-ttu-id="b11db-105">Ad boru hattı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b11db-105">NamePipeline (Default)</span></span>
```
Stop-AzStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b11db-106">Blobboru hattı</span><span class="sxs-lookup"><span data-stu-id="b11db-106">BlobPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b11db-107">Kapsayıcı boru hattı</span><span class="sxs-lookup"><span data-stu-id="b11db-107">ContainerPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b11db-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b11db-108">DESCRIPTION</span></span>
<span data-ttu-id="b11db-109">**Stop-AzStorageBlobCopy** cmdlet 'i, kopyalama işlemini belirtilen hedef blob 'a durdurur.</span><span class="sxs-lookup"><span data-stu-id="b11db-109">The **Stop-AzStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="b11db-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b11db-110">EXAMPLES</span></span>

### <span data-ttu-id="b11db-111">Örnek 1: ada göre kopyalama işlemini durdurma</span><span class="sxs-lookup"><span data-stu-id="b11db-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="b11db-112">Bu komut kopyalama işlemini ada göre durdurur.</span><span class="sxs-lookup"><span data-stu-id="b11db-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="b11db-113">Örnek 2: ardışık düzeni kullanarak kopyalama işlemini durdurma</span><span class="sxs-lookup"><span data-stu-id="b11db-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Stop-AzStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="b11db-114">Bu komut, **Get-AzStorageContainer** değerinden ardışık düzene geçirerek kopyalama işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="b11db-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="b11db-115">Örnek 3: ardışık düzeni ve Get-AzStorageBlob kullanarak kopyalama işlemini durdurma</span><span class="sxs-lookup"><span data-stu-id="b11db-115">Example 3: Stop copy operation by using the pipeline and Get-AzStorageBlob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" | Stop-AzStorageBlobCopy -Force
```

<span data-ttu-id="b11db-116">Bu örnekte kopyalama işlemi, ardışık düzenin kapsayıcısını Get-AzStorageBlob cmdlet 'ten geçirerek durdurulur.</span><span class="sxs-lookup"><span data-stu-id="b11db-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzStorageBlob cmdlet.</span></span>

## <span data-ttu-id="b11db-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b11db-117">PARAMETERS</span></span>

### <span data-ttu-id="b11db-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="b11db-118">-Blob</span></span>
<span data-ttu-id="b11db-119">Blob 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b11db-119">Specifies the name of the blob.</span></span>

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

### <span data-ttu-id="b11db-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b11db-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b11db-121">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="b11db-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b11db-122">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="b11db-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b11db-123">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="b11db-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b11db-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b11db-124">-CloudBlob</span></span>
<span data-ttu-id="b11db-125">Azure depolama Istemci kitaplığından bir **Cloudblob** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="b11db-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="b11db-126">**Cloudblob** nesnesi edinmek için Get-AzStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b11db-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="b11db-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b11db-127">-CloudBlobContainer</span></span>
<span data-ttu-id="b11db-128">Azure depolama Istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="b11db-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="b11db-129">Nesneyi oluşturabilir veya Get-AzStorageContainer cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b11db-129">You can create the object or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="b11db-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b11db-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b11db-131">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b11db-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b11db-132">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b11db-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b11db-133">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="b11db-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b11db-134">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="b11db-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b11db-135">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="b11db-135">The default value is 10.</span></span>

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

### <span data-ttu-id="b11db-136">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="b11db-136">-Container</span></span>
<span data-ttu-id="b11db-137">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b11db-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="b11db-138">-Context</span><span class="sxs-lookup"><span data-stu-id="b11db-138">-Context</span></span>
<span data-ttu-id="b11db-139">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b11db-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b11db-140">Bağlamı, New-AzStorageContext cmdlet 'ini kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b11db-140">You can create the context by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b11db-141">-Copyıd</span><span class="sxs-lookup"><span data-stu-id="b11db-141">-CopyId</span></span>
<span data-ttu-id="b11db-142">Kopya KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b11db-142">Specifies the copy ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b11db-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b11db-143">-DefaultProfile</span></span>
<span data-ttu-id="b11db-144">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b11db-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b11db-145">-Force</span><span class="sxs-lookup"><span data-stu-id="b11db-145">-Force</span></span>
<span data-ttu-id="b11db-146">Belirtilen blobdaki geçerli kopyalama görevini, onay istemeden durdurur.</span><span class="sxs-lookup"><span data-stu-id="b11db-146">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b11db-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b11db-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b11db-148">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b11db-148">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="b11db-149">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="b11db-149">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="b11db-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="b11db-150">-Confirm</span></span>
<span data-ttu-id="b11db-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b11db-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b11db-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b11db-152">-WhatIf</span></span>
<span data-ttu-id="b11db-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b11db-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b11db-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b11db-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b11db-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b11db-155">CommonParameters</span></span>
<span data-ttu-id="b11db-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b11db-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b11db-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b11db-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b11db-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b11db-158">INPUTS</span></span>

### <span data-ttu-id="b11db-159">Microsoft. Windowsazde. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b11db-159">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="b11db-160">Microsoft. Windowsazde. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b11db-160">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="b11db-161">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="b11db-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b11db-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b11db-162">OUTPUTS</span></span>

### <span data-ttu-id="b11db-163">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b11db-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="b11db-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b11db-164">NOTES</span></span>

## <span data-ttu-id="b11db-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b11db-165">RELATED LINKS</span></span>

[<span data-ttu-id="b11db-166">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b11db-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="b11db-167">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b11db-167">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="b11db-168">Başlangıç-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b11db-168">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="b11db-169">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="b11db-169">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)