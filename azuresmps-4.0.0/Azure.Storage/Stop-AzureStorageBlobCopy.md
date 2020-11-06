---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9bdb5a02f474f575f90406ad9026b4437194dffb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572461"
---
# <span data-ttu-id="1efbd-101">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1efbd-101">Stop-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="1efbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1efbd-102">SYNOPSIS</span></span>
<span data-ttu-id="1efbd-103">Kopyalama işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="1efbd-103">Stops a copy operation.</span></span>

## <span data-ttu-id="1efbd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1efbd-104">SYNTAX</span></span>

### <span data-ttu-id="1efbd-105">Ad boru hattı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1efbd-105">NamePipeline (Default)</span></span>
```
Stop-AzureStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1efbd-106">Blobboru hattı</span><span class="sxs-lookup"><span data-stu-id="1efbd-106">BlobPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1efbd-107">Kapsayıcı boru hattı</span><span class="sxs-lookup"><span data-stu-id="1efbd-107">ContainerPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1efbd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1efbd-108">DESCRIPTION</span></span>
<span data-ttu-id="1efbd-109">**Stop-AzureStorageBlobCopy** cmdlet 'i, kopyalama işlemini belirtilen hedef blob 'a durdurur.</span><span class="sxs-lookup"><span data-stu-id="1efbd-109">The **Stop-AzureStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="1efbd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1efbd-110">EXAMPLES</span></span>

### <span data-ttu-id="1efbd-111">Örnek 1: ada göre kopyalama işlemini durdurma</span><span class="sxs-lookup"><span data-stu-id="1efbd-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzureStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="1efbd-112">Bu komut kopyalama işlemini ada göre durdurur.</span><span class="sxs-lookup"><span data-stu-id="1efbd-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="1efbd-113">Örnek 2: ardışık düzeni kullanarak kopyalama işlemini durdurma</span><span class="sxs-lookup"><span data-stu-id="1efbd-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Stop-AzureStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="1efbd-114">Bu komut, **Get-AzureStorageContainer** 'daki ardışık düzene geçirerek kopyalama işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="1efbd-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="1efbd-115">Örnek 3: ardışık düzeni ve Get-AzureStorageBlob kullanarak kopyalama işlemini durdurma</span><span class="sxs-lookup"><span data-stu-id="1efbd-115">Example 3: Stop copy operation by using the pipeline and Get-AzureStorageBlob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" | Stop-AzureStorageBlobCopy -Force
```

<span data-ttu-id="1efbd-116">Bu örnekte kopyalama işlemi, ardışık düzenin kapsayıcısını Get-AzureStorageBlob cmdlet 'ten geçirerek durdurulur.</span><span class="sxs-lookup"><span data-stu-id="1efbd-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzureStorageBlob cmdlet.</span></span>

## <span data-ttu-id="1efbd-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1efbd-117">PARAMETERS</span></span>

### <span data-ttu-id="1efbd-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="1efbd-118">-Blob</span></span>
<span data-ttu-id="1efbd-119">Blob 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1efbd-119">Specifies the name of the blob.</span></span>

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

### <span data-ttu-id="1efbd-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1efbd-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1efbd-121">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="1efbd-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1efbd-122">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="1efbd-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1efbd-123">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="1efbd-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1efbd-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="1efbd-124">-CloudBlob</span></span>
<span data-ttu-id="1efbd-125">Azure depolama Istemci kitaplığından bir **Cloudblob** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="1efbd-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="1efbd-126">**Cloudblob** nesnesi edinmek için Get-AzureStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1efbd-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="1efbd-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="1efbd-127">-CloudBlobContainer</span></span>
<span data-ttu-id="1efbd-128">Azure depolama Istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="1efbd-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="1efbd-129">Nesneyi oluşturabilir veya Get-AzureStorageContainer cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1efbd-129">You can create the object or use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="1efbd-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1efbd-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1efbd-131">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1efbd-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1efbd-132">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1efbd-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1efbd-133">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="1efbd-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1efbd-134">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="1efbd-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1efbd-135">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="1efbd-135">The default value is 10.</span></span>

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

### <span data-ttu-id="1efbd-136">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="1efbd-136">-Container</span></span>
<span data-ttu-id="1efbd-137">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1efbd-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="1efbd-138">-Context</span><span class="sxs-lookup"><span data-stu-id="1efbd-138">-Context</span></span>
<span data-ttu-id="1efbd-139">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1efbd-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="1efbd-140">Bağlamı, New-AzureStorageContext cmdlet 'ini kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1efbd-140">You can create the context by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1efbd-141">-Copyıd</span><span class="sxs-lookup"><span data-stu-id="1efbd-141">-CopyId</span></span>
<span data-ttu-id="1efbd-142">Kopya KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1efbd-142">Specifies the copy ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1efbd-143">-Force</span><span class="sxs-lookup"><span data-stu-id="1efbd-143">-Force</span></span>
<span data-ttu-id="1efbd-144">Belirtilen blobdaki geçerli kopyalama görevini, onay istemeden durdurur.</span><span class="sxs-lookup"><span data-stu-id="1efbd-144">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="1efbd-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1efbd-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1efbd-146">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1efbd-146">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="1efbd-147">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="1efbd-147">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="1efbd-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="1efbd-148">-Confirm</span></span>
<span data-ttu-id="1efbd-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1efbd-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1efbd-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1efbd-150">-WhatIf</span></span>
<span data-ttu-id="1efbd-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1efbd-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1efbd-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1efbd-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1efbd-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1efbd-153">CommonParameters</span></span>
<span data-ttu-id="1efbd-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1efbd-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1efbd-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1efbd-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1efbd-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1efbd-156">INPUTS</span></span>

## <span data-ttu-id="1efbd-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1efbd-157">OUTPUTS</span></span>

## <span data-ttu-id="1efbd-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1efbd-158">NOTES</span></span>

## <span data-ttu-id="1efbd-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1efbd-159">RELATED LINKS</span></span>

[<span data-ttu-id="1efbd-160">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="1efbd-160">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="1efbd-161">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1efbd-161">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="1efbd-162">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1efbd-162">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="1efbd-163">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="1efbd-163">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)
