---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/start-azurestorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobCopy.md
ms.openlocfilehash: 054aa003752c27849c44eb00654313c395c255ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763598"
---
# <span data-ttu-id="c5ba6-101">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c5ba6-101">Start-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="c5ba6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5ba6-102">SYNOPSIS</span></span>
<span data-ttu-id="c5ba6-103">Blob kopyalamaya başlar.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-103">Starts to copy a blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5ba6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5ba6-104">SYNTAX</span></span>

### <span data-ttu-id="c5ba6-105">Kapsayıcıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c5ba6-105">ContainerName (Default)</span></span>
```
Start-AzureStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5ba6-106">Blobörneği</span><span class="sxs-lookup"><span data-stu-id="c5ba6-106">BlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5ba6-107">Blobınstancetoblobınstance</span><span class="sxs-lookup"><span data-stu-id="c5ba6-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5ba6-108">Containerınstance</span><span class="sxs-lookup"><span data-stu-id="c5ba6-108">ContainerInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5ba6-109">PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="c5ba6-109">ShareName</span></span>
```
Start-AzureStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5ba6-110">Shareınstance</span><span class="sxs-lookup"><span data-stu-id="c5ba6-110">ShareInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5ba6-111">Dirınstance</span><span class="sxs-lookup"><span data-stu-id="c5ba6-111">DirInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5ba6-112">Fileınstance</span><span class="sxs-lookup"><span data-stu-id="c5ba6-112">FileInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5ba6-113">Fileınstancetoblobınstance</span><span class="sxs-lookup"><span data-stu-id="c5ba6-113">FileInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5ba6-114">Uripipda</span><span class="sxs-lookup"><span data-stu-id="c5ba6-114">UriPipeline</span></span>
```
Start-AzureStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5ba6-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5ba6-115">DESCRIPTION</span></span>
<span data-ttu-id="c5ba6-116">**Start-AzureStorageBlobCopy** cmdlet 'i bir blob kopyalamaya başlar.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-116">The **Start-AzureStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="c5ba6-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5ba6-117">EXAMPLES</span></span>

### <span data-ttu-id="c5ba6-118">Örnek 1: adlandırılmış blob kopyalama</span><span class="sxs-lookup"><span data-stu-id="c5ba6-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="c5ba6-119">Bu komut, contoso, Yüklemeler adlı kapsayıcıdan Contosoarşivleri adlı kapsayıcıya ContosoPlanning2015 adındaki blob kopyalama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="c5ba6-120">Örnek 2: kopyalanacak blob 'ları belirtmek için kapsayıcı alın</span><span class="sxs-lookup"><span data-stu-id="c5ba6-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="c5ba6-121">Bu komut, **contoso-AzureStorageContainer** cmdlet 'ini kullanarak, contosoyüklemelerini ve ardından ardışık düzen işlecini kullanarak kapsayıcıyı geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-121">This command gets the container named ContosoUploads, by using the **Get-AzureStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c5ba6-122">Bu cmdlet, ContosoPlanning2015 adındaki blob 'un kopyalama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="c5ba6-123">Previous cmdlet 'i kaynak kapsayıcıyı sağlar.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="c5ba6-124">*Destcontainer* parametresi, contosoarşivleri hedef kapsayıcı olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="c5ba6-125">Örnek 3: kapsayıcıdaki tüm blob 'ları alma ve kopyalama</span><span class="sxs-lookup"><span data-stu-id="c5ba6-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzureStorageBlob -Container "ContosoUploads" | Start-AzureStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="c5ba6-126">Bu komut, Contosoyüklemelerini, **Get-AzureStorageBlob** cmdlet 'ini kullanarak ve ardından sonuçları ardışık düzen işlecini kullanarak geçerli cmdlet 'e iletir.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzureStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c5ba6-127">Bu cmdlet, Blobun kopyalama işlemini Contosoarşivleri adlı kapsayıcıya başlatır.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="c5ba6-128">Örnek 4: nesne olarak belirtilen blob 'u kopyalama</span><span class="sxs-lookup"><span data-stu-id="c5ba6-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzureStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzureStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzureStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="c5ba6-129">İlk komut, Contosoyüklemeler adlı kapsayıcıda ContosoPlanning2015 adındaki blob 'u alır.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="c5ba6-130">Komut bu nesneyi $SrcBlob değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-130">The command stores that object in the $SrcBlob variable.</span></span>

<span data-ttu-id="c5ba6-131">İkinci komut, Contosoarşivleri adlı kapsayıcıda ContosoPlanning2015Archived adındaki blob 'u alır.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="c5ba6-132">Komut bu nesneyi $DestBlob değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-132">The command stores that object in the $DestBlob variable.</span></span>

<span data-ttu-id="c5ba6-133">Son komut, kaynak kapsayıcısından hedef kapsayıcıya kopyalama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="c5ba6-134">Komut, $SrcBlob ve $DestBlob blob 'ları için **ISES blob** nesnelerini belirtmek için standart nokta gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="c5ba6-135">Örnek 5: bir blob 'u URI 'den kopyalama</span><span class="sxs-lookup"><span data-stu-id="c5ba6-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzureStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="c5ba6-136">Bu komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur ve bu anahtarı $Context değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>

<span data-ttu-id="c5ba6-137">İkinci komut, dosyayı belirtilen URI 'den ContosoArchive adlı kapsayıcıda ContosoPlanning adlı blob 'a kopyalar.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="c5ba6-138">Komut, $Context depolanan bağlamda kopyalama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-138">The command starts the copy operation in the context stored in $Context.</span></span>

## <span data-ttu-id="c5ba6-139">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5ba6-139">PARAMETERS</span></span>

### <span data-ttu-id="c5ba6-140">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="c5ba6-140">-AbsoluteUri</span></span>
<span data-ttu-id="c5ba6-141">Azure depolama blob blob 'una kopyalanacak dosyanın mutlak URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-141">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ba6-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c5ba6-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c5ba6-143">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c5ba6-144">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c5ba6-145">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c5ba6-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="c5ba6-146">-CloudBlob</span></span>
<span data-ttu-id="c5ba6-147">Azure depolama Istemci kitaplığından bir **Cloudblob** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-147">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="c5ba6-148">**Cloudblob** nesnesi edinmek için Get-AzureStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-148">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ba6-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="c5ba6-149">-CloudBlobContainer</span></span>
<span data-ttu-id="c5ba6-150">Azure depolama Istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="c5ba6-151">Bu cmdlet, bu parametrenin belirttiği kapsayıcıdan bir blob kopyalar.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-151">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="c5ba6-152">**Cloudblobcontainer** nesnesi edinmek için Get-AzureStorageContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-152">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ba6-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c5ba6-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c5ba6-154">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c5ba6-155">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c5ba6-156">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c5ba6-157">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c5ba6-158">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-158">The default value is 10.</span></span>

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

### <span data-ttu-id="c5ba6-159">-Context</span><span class="sxs-lookup"><span data-stu-id="c5ba6-159">-Context</span></span>
<span data-ttu-id="c5ba6-160">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c5ba6-161">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ba6-162">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="c5ba6-162">-DestBlob</span></span>
<span data-ttu-id="c5ba6-163">Hedef blob adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-163">Specifies the name of the destination blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ba6-164">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="c5ba6-164">-DestCloudBlob</span></span>
<span data-ttu-id="c5ba6-165">Hedef **Cloudblob** nesnesini belirtir</span><span class="sxs-lookup"><span data-stu-id="c5ba6-165">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ba6-166">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="c5ba6-166">-DestContainer</span></span>
<span data-ttu-id="c5ba6-167">Hedef kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-167">Specifies the name of the destination container.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ba6-168">-DestContext</span><span class="sxs-lookup"><span data-stu-id="c5ba6-168">-DestContext</span></span>
<span data-ttu-id="c5ba6-169">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-169">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c5ba6-170">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-170">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ba6-171">-Force</span><span class="sxs-lookup"><span data-stu-id="c5ba6-171">-Force</span></span>
<span data-ttu-id="c5ba6-172">Bu cmdlet 'in hedef blob 'un üzerine sizden onay istemeden yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-172">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="c5ba6-173">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="c5ba6-173">-PremiumPageBlobTier</span></span>
<span data-ttu-id="c5ba6-174">Premium sayfa blob katmanı</span><span class="sxs-lookup"><span data-stu-id="c5ba6-174">Premium Page Blob Tier</span></span>

```yaml
Type: PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ba6-175">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c5ba6-175">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c5ba6-176">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-176">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="c5ba6-177">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-177">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="c5ba6-178">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="c5ba6-178">-SrcBlob</span></span>
<span data-ttu-id="c5ba6-179">Kaynak bloonun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-179">Specifies the name of the source blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ba6-180">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="c5ba6-180">-SrcContainer</span></span>
<span data-ttu-id="c5ba6-181">Kaynak kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-181">Specifies the name of the source container.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ba6-182">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="c5ba6-182">-SrcDir</span></span>
<span data-ttu-id="c5ba6-183">Azure depolama Istemci kitaplığından bir **Cloudfiledirectory** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-183">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ba6-184">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="c5ba6-184">-SrcFile</span></span>
<span data-ttu-id="c5ba6-185">Azure depolama Istemci kitaplığından bir **Cloudfile** nesnesini belirtimi.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-185">Specifes a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="c5ba6-186">Bunu oluşturabilir veya Get-AzureStorageFile cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-186">You can create it or use Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ba6-187">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="c5ba6-187">-SrcFilePath</span></span>
<span data-ttu-id="c5ba6-188">Kaynak dizinin veya kaynak paylaşımın kaynak dosyası göreli yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-188">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ba6-189">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="c5ba6-189">-SrcShare</span></span>
<span data-ttu-id="c5ba6-190">Azure depolama Istemci kitaplığından bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-190">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="c5ba6-191">Bunu oluşturabilir veya Get-AzureStorageShare cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-191">You can create it or use Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ba6-192">-Srcpaylaşımadı</span><span class="sxs-lookup"><span data-stu-id="c5ba6-192">-SrcShareName</span></span>
<span data-ttu-id="c5ba6-193">Kaynak paylaşımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-193">Specifies the source share name.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ba6-194">-Onay</span><span class="sxs-lookup"><span data-stu-id="c5ba6-194">-Confirm</span></span>
<span data-ttu-id="c5ba6-195">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5ba6-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5ba6-196">-WhatIf</span></span>
<span data-ttu-id="c5ba6-197">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5ba6-198">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5ba6-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5ba6-199">CommonParameters</span></span>
<span data-ttu-id="c5ba6-200">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5ba6-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5ba6-201">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5ba6-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5ba6-202">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5ba6-202">INPUTS</span></span>

### <span data-ttu-id="c5ba6-203">CloudBlob</span><span class="sxs-lookup"><span data-stu-id="c5ba6-203">CloudBlob</span></span>

<span data-ttu-id="c5ba6-204">' CloudBlob ' parametresi ardışık düzenin ' CloudBlob ' türünün değerini kabul ediyor</span><span class="sxs-lookup"><span data-stu-id="c5ba6-204">Parameter 'CloudBlob' accepts value of type 'CloudBlob' from the pipeline</span></span>

### <span data-ttu-id="c5ba6-205">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="c5ba6-205">IStorageContext</span></span>

<span data-ttu-id="c5ba6-206">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c5ba6-206">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="c5ba6-207">CloudFile</span><span class="sxs-lookup"><span data-stu-id="c5ba6-207">CloudFile</span></span>

<span data-ttu-id="c5ba6-208">' SrcFile ' parametresi ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="c5ba6-208">Parameter 'SrcFile' accepts value of type 'CloudFile' from the pipeline</span></span>

## <span data-ttu-id="c5ba6-209">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5ba6-209">OUTPUTS</span></span>

### <span data-ttu-id="c5ba6-210">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c5ba6-210">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="c5ba6-211">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5ba6-211">NOTES</span></span>

## <span data-ttu-id="c5ba6-212">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5ba6-212">RELATED LINKS</span></span>

[<span data-ttu-id="c5ba6-213">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="c5ba6-213">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)

[<span data-ttu-id="c5ba6-214">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c5ba6-214">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)
