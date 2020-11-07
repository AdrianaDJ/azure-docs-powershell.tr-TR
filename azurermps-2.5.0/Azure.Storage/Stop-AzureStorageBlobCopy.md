---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/stop-azurestorageblobcopy
schema: 2.0.0
ms.openlocfilehash: 2a338773ae8745ae6412014bfd176e5b29fa380f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939427"
---
# <span data-ttu-id="92048-101">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="92048-101">Stop-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="92048-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92048-102">SYNOPSIS</span></span>
<span data-ttu-id="92048-103">Kopyalama işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="92048-103">Stops a copy operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92048-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="92048-104">SYNTAX</span></span>

### <span data-ttu-id="92048-105">Ad boru hattı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="92048-105">NamePipeline (Default)</span></span>
```
Stop-AzureStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92048-106">Blobboru hattı</span><span class="sxs-lookup"><span data-stu-id="92048-106">BlobPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92048-107">Kapsayıcı boru hattı</span><span class="sxs-lookup"><span data-stu-id="92048-107">ContainerPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92048-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="92048-108">DESCRIPTION</span></span>
<span data-ttu-id="92048-109">**Stop-AzureStorageBlobCopy** cmdlet 'i, kopyalama işlemini belirtilen hedef blob 'a durdurur.</span><span class="sxs-lookup"><span data-stu-id="92048-109">The **Stop-AzureStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="92048-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="92048-110">EXAMPLES</span></span>

### <span data-ttu-id="92048-111">Örnek 1: ada göre kopyalama işlemini durdurma</span><span class="sxs-lookup"><span data-stu-id="92048-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzureStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="92048-112">Bu komut kopyalama işlemini ada göre durdurur.</span><span class="sxs-lookup"><span data-stu-id="92048-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="92048-113">Örnek 2: ardışık düzeni kullanarak kopyalama işlemini durdurma</span><span class="sxs-lookup"><span data-stu-id="92048-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Stop-AzureStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="92048-114">Bu komut, **Get-AzureStorageContainer** 'daki ardışık düzene geçirerek kopyalama işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="92048-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="92048-115">Örnek 3: ardışık düzeni ve Get-AzureStorageBlob kullanarak kopyalama işlemini durdurma</span><span class="sxs-lookup"><span data-stu-id="92048-115">Example 3: Stop copy operation by using the pipeline and Get-AzureStorageBlob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" | Stop-AzureStorageBlobCopy -Force
```

<span data-ttu-id="92048-116">Bu örnekte kopyalama işlemi, ardışık düzenin kapsayıcısını Get-AzureStorageBlob cmdlet 'ten geçirerek durdurulur.</span><span class="sxs-lookup"><span data-stu-id="92048-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzureStorageBlob cmdlet.</span></span>

## <span data-ttu-id="92048-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="92048-117">PARAMETERS</span></span>

### <span data-ttu-id="92048-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="92048-118">-Blob</span></span>
<span data-ttu-id="92048-119">Blob 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92048-119">Specifies the name of the blob.</span></span>

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

### <span data-ttu-id="92048-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="92048-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="92048-121">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="92048-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="92048-122">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="92048-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="92048-123">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="92048-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="92048-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="92048-124">-CloudBlob</span></span>
<span data-ttu-id="92048-125">Azure depolama Istemci kitaplığından bir **Cloudblob** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="92048-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="92048-126">**Cloudblob** nesnesi edinmek için Get-AzureStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="92048-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="92048-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="92048-127">-CloudBlobContainer</span></span>
<span data-ttu-id="92048-128">Azure depolama Istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="92048-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="92048-129">Nesneyi oluşturabilir veya Get-AzureStorageContainer cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="92048-129">You can create the object or use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="92048-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="92048-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="92048-131">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92048-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="92048-132">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="92048-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="92048-133">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="92048-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="92048-134">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="92048-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="92048-135">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="92048-135">The default value is 10.</span></span>

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

### <span data-ttu-id="92048-136">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="92048-136">-Container</span></span>
<span data-ttu-id="92048-137">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92048-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="92048-138">-Context</span><span class="sxs-lookup"><span data-stu-id="92048-138">-Context</span></span>
<span data-ttu-id="92048-139">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92048-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="92048-140">Bağlamı, New-AzureStorageContext cmdlet 'ini kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="92048-140">You can create the context by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="92048-141">-Copyıd</span><span class="sxs-lookup"><span data-stu-id="92048-141">-CopyId</span></span>
<span data-ttu-id="92048-142">Kopya KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="92048-142">Specifies the copy ID.</span></span>

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

### <span data-ttu-id="92048-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92048-143">-DefaultProfile</span></span>
<span data-ttu-id="92048-144">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="92048-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92048-145">-Force</span><span class="sxs-lookup"><span data-stu-id="92048-145">-Force</span></span>
<span data-ttu-id="92048-146">Belirtilen blobdaki geçerli kopyalama görevini, onay istemeden durdurur.</span><span class="sxs-lookup"><span data-stu-id="92048-146">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="92048-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="92048-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="92048-148">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92048-148">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="92048-149">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="92048-149">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="92048-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="92048-150">-Confirm</span></span>
<span data-ttu-id="92048-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="92048-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92048-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92048-152">-WhatIf</span></span>
<span data-ttu-id="92048-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="92048-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92048-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="92048-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92048-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92048-155">CommonParameters</span></span>
<span data-ttu-id="92048-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="92048-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92048-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92048-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92048-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="92048-158">INPUTS</span></span>

### <span data-ttu-id="92048-159">Microsoft. Windowsazde. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="92048-159">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="92048-160">Microsoft. Windowsazde. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="92048-160">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="92048-161">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="92048-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="92048-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="92048-162">OUTPUTS</span></span>

### <span data-ttu-id="92048-163">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="92048-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="92048-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="92048-164">NOTES</span></span>

## <span data-ttu-id="92048-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="92048-165">RELATED LINKS</span></span>

[<span data-ttu-id="92048-166">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="92048-166">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="92048-167">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="92048-167">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="92048-168">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="92048-168">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="92048-169">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="92048-169">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)
