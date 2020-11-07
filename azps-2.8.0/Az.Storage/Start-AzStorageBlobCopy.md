---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: a990b168fcaf32deffd495b5eeb0f9a813f2f093
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933510"
---
# <span data-ttu-id="f2716-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f2716-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="f2716-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2716-102">SYNOPSIS</span></span>
<span data-ttu-id="f2716-103">Blob kopyalamaya başlar.</span><span class="sxs-lookup"><span data-stu-id="f2716-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="f2716-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2716-104">SYNTAX</span></span>

### <span data-ttu-id="f2716-105">Kapsayıcıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f2716-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2716-106">Blobörneği</span><span class="sxs-lookup"><span data-stu-id="f2716-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2716-107">Blobınstancetoblobınstance</span><span class="sxs-lookup"><span data-stu-id="f2716-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2716-108">Containerınstance</span><span class="sxs-lookup"><span data-stu-id="f2716-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2716-109">PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="f2716-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2716-110">Shareınstance</span><span class="sxs-lookup"><span data-stu-id="f2716-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2716-111">Dirınstance</span><span class="sxs-lookup"><span data-stu-id="f2716-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2716-112">Fileınstance</span><span class="sxs-lookup"><span data-stu-id="f2716-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2716-113">Fileınstancetoblobınstance</span><span class="sxs-lookup"><span data-stu-id="f2716-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2716-114">Uripipda</span><span class="sxs-lookup"><span data-stu-id="f2716-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2716-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2716-115">DESCRIPTION</span></span>
<span data-ttu-id="f2716-116">**Start-AzStorageBlobCopy** cmdlet 'i bir blob kopyalamaya başlar.</span><span class="sxs-lookup"><span data-stu-id="f2716-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="f2716-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2716-117">EXAMPLES</span></span>

### <span data-ttu-id="f2716-118">Örnek 1: adlandırılmış blob kopyalama</span><span class="sxs-lookup"><span data-stu-id="f2716-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="f2716-119">Bu komut, contoso, Yüklemeler adlı kapsayıcıdan Contosoarşivleri adlı kapsayıcıya ContosoPlanning2015 adındaki blob kopyalama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="f2716-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="f2716-120">Örnek 2: kopyalanacak blob 'ları belirtmek için kapsayıcı alın</span><span class="sxs-lookup"><span data-stu-id="f2716-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="f2716-121">Bu komut, **Get-AzStorageContainer** cmdlet 'Ini kullanarak contosoyüklemelerini ve ardından ardışık düzen işlecini kullanarak kapsayıcıyı geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="f2716-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f2716-122">Bu cmdlet, ContosoPlanning2015 adındaki blob 'un kopyalama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="f2716-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="f2716-123">Previous cmdlet 'i kaynak kapsayıcıyı sağlar.</span><span class="sxs-lookup"><span data-stu-id="f2716-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="f2716-124">*Destcontainer* parametresi, contosoarşivleri hedef kapsayıcı olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2716-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="f2716-125">Örnek 3: kapsayıcıdaki tüm blob 'ları alma ve kopyalama</span><span class="sxs-lookup"><span data-stu-id="f2716-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="f2716-126">Bu komut, Contosoyüklemelerini, **Get-AzStorageBlob** cmdlet 'ini kullanarak ve ardından sonuçları ardışık düzen işlecini kullanarak geçerli cmdlet 'e iletir.</span><span class="sxs-lookup"><span data-stu-id="f2716-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f2716-127">Bu cmdlet, Blobun kopyalama işlemini Contosoarşivleri adlı kapsayıcıya başlatır.</span><span class="sxs-lookup"><span data-stu-id="f2716-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="f2716-128">Örnek 4: nesne olarak belirtilen blob 'u kopyalama</span><span class="sxs-lookup"><span data-stu-id="f2716-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="f2716-129">İlk komut, Contosoyüklemeler adlı kapsayıcıda ContosoPlanning2015 adındaki blob 'u alır.</span><span class="sxs-lookup"><span data-stu-id="f2716-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="f2716-130">Komut bu nesneyi $SrcBlob değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f2716-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="f2716-131">İkinci komut, Contosoarşivleri adlı kapsayıcıda ContosoPlanning2015Archived adındaki blob 'u alır.</span><span class="sxs-lookup"><span data-stu-id="f2716-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="f2716-132">Komut bu nesneyi $DestBlob değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f2716-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="f2716-133">Son komut, kaynak kapsayıcısından hedef kapsayıcıya kopyalama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="f2716-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="f2716-134">Komut, $SrcBlob ve $DestBlob blob 'ları için **ISES blob** nesnelerini belirtmek için standart nokta gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="f2716-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="f2716-135">Örnek 5: bir blob 'u URI 'den kopyalama</span><span class="sxs-lookup"><span data-stu-id="f2716-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="f2716-136">Bu komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur ve bu anahtarı $Context değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f2716-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="f2716-137">İkinci komut, dosyayı belirtilen URI 'den ContosoArchive adlı kapsayıcıda ContosoPlanning adlı blob 'a kopyalar.</span><span class="sxs-lookup"><span data-stu-id="f2716-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="f2716-138">Komut, $Context depolanan bağlamda kopyalama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="f2716-138">The command starts the copy operation in the context stored in $Context.</span></span>

### <span data-ttu-id="f2716-139">Örnek 6: blok blob 'u hedef kapsayıcıya yeni bir blob adıyla kopyalama ve hedef blob Standartblobkatmanını arşiv olarak ayarlama, en yüksek olarak yeniden doldurma</span><span class="sxs-lookup"><span data-stu-id="f2716-139">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Archive, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Archive
```

<span data-ttu-id="f2716-140">Bu komut, blok blob 'ın kopyalama işlemini hedef kapsayıcıya yeni bir blob adıyla başlatır ve hedef blob Standartblobkatmanını arşiv olarak ayarla, yeniden doldurma</span><span class="sxs-lookup"><span data-stu-id="f2716-140">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Archive, RehydratePriority as High</span></span>

## <span data-ttu-id="f2716-141">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2716-141">PARAMETERS</span></span>

### <span data-ttu-id="f2716-142">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="f2716-142">-AbsoluteUri</span></span>
<span data-ttu-id="f2716-143">Azure depolama blob blob 'una kopyalanacak dosyanın mutlak URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2716-143">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2716-144">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f2716-144">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f2716-145">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2716-145">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f2716-146">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="f2716-146">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f2716-147">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="f2716-147">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f2716-148">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="f2716-148">-CloudBlob</span></span>
<span data-ttu-id="f2716-149">Azure depolama Istemci kitaplığından bir **Cloudblob** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2716-149">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="f2716-150">**Cloudblob** nesnesi edinmek için Get-AzStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f2716-150">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2716-151">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="f2716-151">-CloudBlobContainer</span></span>
<span data-ttu-id="f2716-152">Azure depolama Istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2716-152">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="f2716-153">Bu cmdlet, bu parametrenin belirttiği kapsayıcıdan bir blob kopyalar.</span><span class="sxs-lookup"><span data-stu-id="f2716-153">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="f2716-154">**Cloudblobcontainer** nesnesi edinmek için Get-AzStorageContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f2716-154">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2716-155">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f2716-155">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f2716-156">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2716-156">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f2716-157">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f2716-157">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f2716-158">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="f2716-158">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f2716-159">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="f2716-159">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f2716-160">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="f2716-160">The default value is 10.</span></span>

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

### <span data-ttu-id="f2716-161">-Context</span><span class="sxs-lookup"><span data-stu-id="f2716-161">-Context</span></span>
<span data-ttu-id="f2716-162">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2716-162">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f2716-163">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f2716-163">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2716-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2716-164">-DefaultProfile</span></span>
<span data-ttu-id="f2716-165">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f2716-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2716-166">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="f2716-166">-DestBlob</span></span>
<span data-ttu-id="f2716-167">Hedef blob adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2716-167">Specifies the name of the destination blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2716-168">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="f2716-168">-DestCloudBlob</span></span>
<span data-ttu-id="f2716-169">Hedef **Cloudblob** nesnesini belirtir</span><span class="sxs-lookup"><span data-stu-id="f2716-169">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2716-170">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="f2716-170">-DestContainer</span></span>
<span data-ttu-id="f2716-171">Hedef kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2716-171">Specifies the name of the destination container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2716-172">-DestContext</span><span class="sxs-lookup"><span data-stu-id="f2716-172">-DestContext</span></span>
<span data-ttu-id="f2716-173">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2716-173">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f2716-174">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f2716-174">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2716-175">-Force</span><span class="sxs-lookup"><span data-stu-id="f2716-175">-Force</span></span>
<span data-ttu-id="f2716-176">Bu cmdlet 'in hedef blob 'un üzerine sizden onay istemeden yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f2716-176">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f2716-177">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="f2716-177">-PremiumPageBlobTier</span></span>
<span data-ttu-id="f2716-178">Premium sayfa blob katmanı</span><span class="sxs-lookup"><span data-stu-id="f2716-178">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2716-179">-Rehitepriority</span><span class="sxs-lookup"><span data-stu-id="f2716-179">-RehydratePriority</span></span>
<span data-ttu-id="f2716-180">Blob Reaktpriority 'yi engelle.</span><span class="sxs-lookup"><span data-stu-id="f2716-180">Block Blob RehydratePriority.</span></span> <span data-ttu-id="f2716-181">Arşivlenmiş bir blob 'u yeniden doldurma önceliğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f2716-181">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="f2716-182">Geçerli değerler yüksek/standart.</span><span class="sxs-lookup"><span data-stu-id="f2716-182">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2716-183">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f2716-183">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f2716-184">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2716-184">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="f2716-185">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="f2716-185">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="f2716-186">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="f2716-186">-SrcBlob</span></span>
<span data-ttu-id="f2716-187">Kaynak bloonun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2716-187">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2716-188">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="f2716-188">-SrcContainer</span></span>
<span data-ttu-id="f2716-189">Kaynak kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2716-189">Specifies the name of the source container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2716-190">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="f2716-190">-SrcDir</span></span>
<span data-ttu-id="f2716-191">Azure depolama Istemci kitaplığından bir **Cloudfiledirectory** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2716-191">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2716-192">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="f2716-192">-SrcFile</span></span>
<span data-ttu-id="f2716-193">Azure depolama Istemci kitaplığından bir **Cloudfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2716-193">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="f2716-194">Bunu oluşturabilir veya Get-AzStorageFile cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f2716-194">You can create it or use Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2716-195">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="f2716-195">-SrcFilePath</span></span>
<span data-ttu-id="f2716-196">Kaynak dizinin veya kaynak paylaşımın kaynak dosyası göreli yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2716-196">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2716-197">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="f2716-197">-SrcShare</span></span>
<span data-ttu-id="f2716-198">Azure depolama Istemci kitaplığından bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2716-198">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="f2716-199">Bunu oluşturabilir veya Get-AzStorageShare cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f2716-199">You can create it or use Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2716-200">-Srcpaylaşımadı</span><span class="sxs-lookup"><span data-stu-id="f2716-200">-SrcShareName</span></span>
<span data-ttu-id="f2716-201">Kaynak paylaşımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2716-201">Specifies the source share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2716-202">-Standartblobkatmanı</span><span class="sxs-lookup"><span data-stu-id="f2716-202">-StandardBlobTier</span></span>
<span data-ttu-id="f2716-203">Blob katmanını engelle, geçerli değerler kolay/serin/arşiv.</span><span class="sxs-lookup"><span data-stu-id="f2716-203">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="f2716-204">Ayrıntılara bakın https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="f2716-204">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="f2716-205">-Onay</span><span class="sxs-lookup"><span data-stu-id="f2716-205">-Confirm</span></span>
<span data-ttu-id="f2716-206">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f2716-206">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2716-207">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2716-207">-WhatIf</span></span>
<span data-ttu-id="f2716-208">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f2716-208">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2716-209">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f2716-209">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2716-210">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2716-210">CommonParameters</span></span>
<span data-ttu-id="f2716-211">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2716-211">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2716-212">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2716-212">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2716-213">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2716-213">INPUTS</span></span>

### <span data-ttu-id="f2716-214">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="f2716-214">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="f2716-215">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="f2716-215">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="f2716-216">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="f2716-216">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="f2716-217">System. String</span><span class="sxs-lookup"><span data-stu-id="f2716-217">System.String</span></span>

### <span data-ttu-id="f2716-218">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="f2716-218">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f2716-219">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2716-219">OUTPUTS</span></span>

### <span data-ttu-id="f2716-220">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="f2716-220">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="f2716-221">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2716-221">NOTES</span></span>

## <span data-ttu-id="f2716-222">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2716-222">RELATED LINKS</span></span>

[<span data-ttu-id="f2716-223">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="f2716-223">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="f2716-224">Dur-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f2716-224">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
