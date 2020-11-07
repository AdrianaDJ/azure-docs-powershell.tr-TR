---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 01edb18c72487ada7c51408ce38502b6e87b2f56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761810"
---
# <span data-ttu-id="89c9b-101">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="89c9b-101">Start-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="89c9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89c9b-102">SYNOPSIS</span></span>
<span data-ttu-id="89c9b-103">Blob kopyalamaya başlar.</span><span class="sxs-lookup"><span data-stu-id="89c9b-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="89c9b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89c9b-104">SYNTAX</span></span>

### <span data-ttu-id="89c9b-105">Kapsayıcıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="89c9b-105">ContainerName (Default)</span></span>
```
Start-AzureStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89c9b-106">Blobörneği</span><span class="sxs-lookup"><span data-stu-id="89c9b-106">BlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89c9b-107">Blobınstancetoblobınstance</span><span class="sxs-lookup"><span data-stu-id="89c9b-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob> [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89c9b-108">Containerınstance</span><span class="sxs-lookup"><span data-stu-id="89c9b-108">ContainerInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89c9b-109">PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="89c9b-109">ShareName</span></span>
```
Start-AzureStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89c9b-110">Shareınstance</span><span class="sxs-lookup"><span data-stu-id="89c9b-110">ShareInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89c9b-111">Dirınstance</span><span class="sxs-lookup"><span data-stu-id="89c9b-111">DirInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89c9b-112">Fileınstance</span><span class="sxs-lookup"><span data-stu-id="89c9b-112">FileInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89c9b-113">Fileınstancetoblobınstance</span><span class="sxs-lookup"><span data-stu-id="89c9b-113">FileInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89c9b-114">Uripipda</span><span class="sxs-lookup"><span data-stu-id="89c9b-114">UriPipeline</span></span>
```
Start-AzureStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89c9b-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="89c9b-115">DESCRIPTION</span></span>
<span data-ttu-id="89c9b-116">**Start-AzureStorageBlobCopy** cmdlet 'i bir blob kopyalamaya başlar.</span><span class="sxs-lookup"><span data-stu-id="89c9b-116">The **Start-AzureStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="89c9b-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89c9b-117">EXAMPLES</span></span>

### <span data-ttu-id="89c9b-118">Örnek 1: adlandırılmış blob kopyalama</span><span class="sxs-lookup"><span data-stu-id="89c9b-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="89c9b-119">Bu komut, contoso, Yüklemeler adlı kapsayıcıdan Contosoarşivleri adlı kapsayıcıya ContosoPlanning2015 adındaki blob kopyalama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="89c9b-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="89c9b-120">Örnek 2: kopyalanacak blob 'ları belirtmek için kapsayıcı alın</span><span class="sxs-lookup"><span data-stu-id="89c9b-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="89c9b-121">Bu komut, **contoso-AzureStorageContainer** cmdlet 'ini kullanarak, contosoyüklemelerini ve ardından ardışık düzen işlecini kullanarak kapsayıcıyı geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="89c9b-121">This command gets the container named ContosoUploads, by using the **Get-AzureStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="89c9b-122">Bu cmdlet, ContosoPlanning2015 adındaki blob 'un kopyalama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="89c9b-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="89c9b-123">Previous cmdlet 'i kaynak kapsayıcıyı sağlar.</span><span class="sxs-lookup"><span data-stu-id="89c9b-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="89c9b-124">*Destcontainer* parametresi, contosoarşivleri hedef kapsayıcı olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="89c9b-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="89c9b-125">Örnek 3: kopyalanacak blob alma</span><span class="sxs-lookup"><span data-stu-id="89c9b-125">Example 3: Get a blob to copy</span></span>
```
C:\PS>Get-AzureStorageBlob -Container "ContosoUploads" | Start-AzureStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="89c9b-126">Bu komut, Contosoyüklemelerini, **Get-AzureStorageBlob** cmdlet 'ini kullanarak ve ardından sonuçları ardışık düzen işlecini kullanarak geçerli cmdlet 'e iletir.</span><span class="sxs-lookup"><span data-stu-id="89c9b-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzureStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="89c9b-127">Bu cmdlet, Blobun kopyalama işlemini Contosoarşivleri adlı kapsayıcıya başlatır.</span><span class="sxs-lookup"><span data-stu-id="89c9b-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="89c9b-128">Örnek 4: nesne olarak belirtilen blob 'u kopyalama</span><span class="sxs-lookup"><span data-stu-id="89c9b-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzureStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzureStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzureStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="89c9b-129">İlk komut, Contosoyüklemeler adlı kapsayıcıda ContosoPlanning2015 adındaki blob 'u alır.</span><span class="sxs-lookup"><span data-stu-id="89c9b-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="89c9b-130">Komut bu nesneyi $SrcBlob değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="89c9b-130">The command stores that object in the $SrcBlob variable.</span></span>

<span data-ttu-id="89c9b-131">İkinci komut, Contosoarşivleri adlı kapsayıcıda ContosoPlanning2015Archived adındaki blob 'u alır.</span><span class="sxs-lookup"><span data-stu-id="89c9b-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="89c9b-132">Komut bu nesneyi $DestBlob değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="89c9b-132">The command stores that object in the $DestBlob variable.</span></span>

<span data-ttu-id="89c9b-133">Son komut, kaynak kapsayıcısından hedef kapsayıcıya kopyalama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="89c9b-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="89c9b-134">Komut, $SrcBlob ve $DestBlob blob 'ları için **ISES blob** nesnelerini belirtmek için standart nokta gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="89c9b-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="89c9b-135">Örnek 5: bir blob 'u URI 'den kopyalama</span><span class="sxs-lookup"><span data-stu-id="89c9b-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzureStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="89c9b-136">Bu komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur ve bu anahtarı $Context değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="89c9b-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>

<span data-ttu-id="89c9b-137">İkinci komut, dosyayı belirtilen URI 'den ContosoArchive adlı kapsayıcıda ContosoPlanning adlı blob 'a kopyalar.</span><span class="sxs-lookup"><span data-stu-id="89c9b-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="89c9b-138">Komut, $Context depolanan bağlamda kopyalama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="89c9b-138">The command starts the copy operation in the context stored in $Context.</span></span>

## <span data-ttu-id="89c9b-139">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89c9b-139">PARAMETERS</span></span>

### <span data-ttu-id="89c9b-140">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="89c9b-140">-AbsoluteUri</span></span>
<span data-ttu-id="89c9b-141">Azure depolama blob blob 'una kopyalanacak dosyanın mutlak URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="89c9b-141">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="89c9b-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="89c9b-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="89c9b-143">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="89c9b-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="89c9b-144">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="89c9b-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="89c9b-145">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="89c9b-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="89c9b-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="89c9b-146">-CloudBlob</span></span>
<span data-ttu-id="89c9b-147">Azure depolama Istemci kitaplığından bir **Cloudblob** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="89c9b-147">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="89c9b-148">**Cloudblob** nesnesi edinmek için Get-AzureStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="89c9b-148">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="89c9b-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="89c9b-149">-CloudBlobContainer</span></span>
<span data-ttu-id="89c9b-150">Azure depolama Istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="89c9b-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="89c9b-151">Bu cmdlet, bu parametrenin belirttiği kapsayıcıdan bir blob kopyalar.</span><span class="sxs-lookup"><span data-stu-id="89c9b-151">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="89c9b-152">**Cloudblobcontainer** nesnesi edinmek için Get-AzureStorageContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="89c9b-152">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="89c9b-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="89c9b-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="89c9b-154">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89c9b-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="89c9b-155">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="89c9b-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="89c9b-156">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="89c9b-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="89c9b-157">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="89c9b-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="89c9b-158">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="89c9b-158">The default value is 10.</span></span>

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

### <span data-ttu-id="89c9b-159">-Context</span><span class="sxs-lookup"><span data-stu-id="89c9b-159">-Context</span></span>
<span data-ttu-id="89c9b-160">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89c9b-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="89c9b-161">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="89c9b-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="89c9b-162">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="89c9b-162">-DestBlob</span></span>
<span data-ttu-id="89c9b-163">Hedef blob adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89c9b-163">Specifies the name of the destination blob.</span></span>

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

### <span data-ttu-id="89c9b-164">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="89c9b-164">-DestCloudBlob</span></span>
<span data-ttu-id="89c9b-165">Hedef **Cloudblob** nesnesini belirtir</span><span class="sxs-lookup"><span data-stu-id="89c9b-165">Specifies a destination **CloudBlob** object</span></span>

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

### <span data-ttu-id="89c9b-166">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="89c9b-166">-DestContainer</span></span>
<span data-ttu-id="89c9b-167">Hedef kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89c9b-167">Specifies the name of the destination container.</span></span>

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

### <span data-ttu-id="89c9b-168">-DestContext</span><span class="sxs-lookup"><span data-stu-id="89c9b-168">-DestContext</span></span>
<span data-ttu-id="89c9b-169">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89c9b-169">Specifies an Azure storage context.</span></span>
<span data-ttu-id="89c9b-170">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="89c9b-170">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="89c9b-171">-Force</span><span class="sxs-lookup"><span data-stu-id="89c9b-171">-Force</span></span>
<span data-ttu-id="89c9b-172">Bu cmdlet 'in hedef blob 'un üzerine sizden onay istemeden yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="89c9b-172">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="89c9b-173">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="89c9b-173">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="89c9b-174">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89c9b-174">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="89c9b-175">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="89c9b-175">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="89c9b-176">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="89c9b-176">-SrcBlob</span></span>
<span data-ttu-id="89c9b-177">Kaynak bloonun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89c9b-177">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="89c9b-178">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="89c9b-178">-SrcContainer</span></span>
<span data-ttu-id="89c9b-179">Kaynak kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89c9b-179">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="89c9b-180">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="89c9b-180">-SrcDir</span></span>
<span data-ttu-id="89c9b-181">Azure depolama Istemci kitaplığından bir **Cloudfiledirectory** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="89c9b-181">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

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

### <span data-ttu-id="89c9b-182">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="89c9b-182">-SrcFile</span></span>
<span data-ttu-id="89c9b-183">Azure depolama Istemci kitaplığından bir **Cloudfile** nesnesini belirtimi.</span><span class="sxs-lookup"><span data-stu-id="89c9b-183">Specifes a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="89c9b-184">Bunu oluşturabilir veya Get-AzureStorageFile cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="89c9b-184">You can create it or use Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="89c9b-185">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="89c9b-185">-SrcFilePath</span></span>
<span data-ttu-id="89c9b-186">Kaynak dizinin veya kaynak paylaşımın kaynak dosyası göreli yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="89c9b-186">Specifies the source file relative path of source directory or source share.</span></span>

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

### <span data-ttu-id="89c9b-187">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="89c9b-187">-SrcShare</span></span>
<span data-ttu-id="89c9b-188">Azure depolama Istemci kitaplığından bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="89c9b-188">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="89c9b-189">Bunu oluşturabilir veya Get-AzureStorageShare cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="89c9b-189">You can create it or use Get-AzureStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="89c9b-190">-Srcpaylaşımadı</span><span class="sxs-lookup"><span data-stu-id="89c9b-190">-SrcShareName</span></span>
<span data-ttu-id="89c9b-191">Kaynak paylaşımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89c9b-191">Specifies the source share name.</span></span>

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

### <span data-ttu-id="89c9b-192">-Onay</span><span class="sxs-lookup"><span data-stu-id="89c9b-192">-Confirm</span></span>
<span data-ttu-id="89c9b-193">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="89c9b-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89c9b-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89c9b-194">-WhatIf</span></span>
<span data-ttu-id="89c9b-195">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="89c9b-195">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89c9b-196">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="89c9b-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89c9b-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89c9b-197">CommonParameters</span></span>
<span data-ttu-id="89c9b-198">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89c9b-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89c9b-199">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89c9b-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89c9b-200">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89c9b-200">INPUTS</span></span>

## <span data-ttu-id="89c9b-201">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89c9b-201">OUTPUTS</span></span>

## <span data-ttu-id="89c9b-202">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89c9b-202">NOTES</span></span>

## <span data-ttu-id="89c9b-203">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89c9b-203">RELATED LINKS</span></span>

[<span data-ttu-id="89c9b-204">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="89c9b-204">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)

[<span data-ttu-id="89c9b-205">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="89c9b-205">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)
