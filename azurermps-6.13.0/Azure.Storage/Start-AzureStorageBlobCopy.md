---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/start-azurestorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobCopy.md
ms.openlocfilehash: 9c0b679c95515fcde31caa4e7a772f6f9ce36d71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591492"
---
# <span data-ttu-id="bf59e-101">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="bf59e-101">Start-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="bf59e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf59e-102">SYNOPSIS</span></span>
<span data-ttu-id="bf59e-103">Blob kopyalamaya başlar.</span><span class="sxs-lookup"><span data-stu-id="bf59e-103">Starts to copy a blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf59e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf59e-104">SYNTAX</span></span>

### <span data-ttu-id="bf59e-105">Kapsayıcıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bf59e-105">ContainerName (Default)</span></span>
```
Start-AzureStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf59e-106">Blobörneği</span><span class="sxs-lookup"><span data-stu-id="bf59e-106">BlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf59e-107">Blobınstancetoblobınstance</span><span class="sxs-lookup"><span data-stu-id="bf59e-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf59e-108">Containerınstance</span><span class="sxs-lookup"><span data-stu-id="bf59e-108">ContainerInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf59e-109">PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="bf59e-109">ShareName</span></span>
```
Start-AzureStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf59e-110">Shareınstance</span><span class="sxs-lookup"><span data-stu-id="bf59e-110">ShareInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf59e-111">Dirınstance</span><span class="sxs-lookup"><span data-stu-id="bf59e-111">DirInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf59e-112">Fileınstance</span><span class="sxs-lookup"><span data-stu-id="bf59e-112">FileInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf59e-113">Fileınstancetoblobınstance</span><span class="sxs-lookup"><span data-stu-id="bf59e-113">FileInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf59e-114">Uripipda</span><span class="sxs-lookup"><span data-stu-id="bf59e-114">UriPipeline</span></span>
```
Start-AzureStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf59e-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf59e-115">DESCRIPTION</span></span>
<span data-ttu-id="bf59e-116">**Start-AzureStorageBlobCopy** cmdlet 'i bir blob kopyalamaya başlar.</span><span class="sxs-lookup"><span data-stu-id="bf59e-116">The **Start-AzureStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="bf59e-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf59e-117">EXAMPLES</span></span>

### <span data-ttu-id="bf59e-118">Örnek 1: adlandırılmış blob kopyalama</span><span class="sxs-lookup"><span data-stu-id="bf59e-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="bf59e-119">Bu komut, contoso, Yüklemeler adlı kapsayıcıdan Contosoarşivleri adlı kapsayıcıya ContosoPlanning2015 adındaki blob kopyalama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="bf59e-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="bf59e-120">Örnek 2: kopyalanacak blob 'ları belirtmek için kapsayıcı alın</span><span class="sxs-lookup"><span data-stu-id="bf59e-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="bf59e-121">Bu komut, **contoso-AzureStorageContainer** cmdlet 'ini kullanarak, contosoyüklemelerini ve ardından ardışık düzen işlecini kullanarak kapsayıcıyı geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="bf59e-121">This command gets the container named ContosoUploads, by using the **Get-AzureStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bf59e-122">Bu cmdlet, ContosoPlanning2015 adındaki blob 'un kopyalama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="bf59e-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="bf59e-123">Previous cmdlet 'i kaynak kapsayıcıyı sağlar.</span><span class="sxs-lookup"><span data-stu-id="bf59e-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="bf59e-124">*Destcontainer* parametresi, contosoarşivleri hedef kapsayıcı olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf59e-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="bf59e-125">Örnek 3: kapsayıcıdaki tüm blob 'ları alma ve kopyalama</span><span class="sxs-lookup"><span data-stu-id="bf59e-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzureStorageBlob -Container "ContosoUploads" | Start-AzureStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="bf59e-126">Bu komut, Contosoyüklemelerini, **Get-AzureStorageBlob** cmdlet 'ini kullanarak ve ardından sonuçları ardışık düzen işlecini kullanarak geçerli cmdlet 'e iletir.</span><span class="sxs-lookup"><span data-stu-id="bf59e-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzureStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bf59e-127">Bu cmdlet, Blobun kopyalama işlemini Contosoarşivleri adlı kapsayıcıya başlatır.</span><span class="sxs-lookup"><span data-stu-id="bf59e-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="bf59e-128">Örnek 4: nesne olarak belirtilen blob 'u kopyalama</span><span class="sxs-lookup"><span data-stu-id="bf59e-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzureStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzureStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzureStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="bf59e-129">İlk komut, Contosoyüklemeler adlı kapsayıcıda ContosoPlanning2015 adındaki blob 'u alır.</span><span class="sxs-lookup"><span data-stu-id="bf59e-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="bf59e-130">Komut bu nesneyi $SrcBlob değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="bf59e-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="bf59e-131">İkinci komut, Contosoarşivleri adlı kapsayıcıda ContosoPlanning2015Archived adındaki blob 'u alır.</span><span class="sxs-lookup"><span data-stu-id="bf59e-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="bf59e-132">Komut bu nesneyi $DestBlob değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="bf59e-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="bf59e-133">Son komut, kaynak kapsayıcısından hedef kapsayıcıya kopyalama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="bf59e-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="bf59e-134">Komut, $SrcBlob ve $DestBlob blob 'ları için **ISES blob** nesnelerini belirtmek için standart nokta gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="bf59e-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="bf59e-135">Örnek 5: bir blob 'u URI 'den kopyalama</span><span class="sxs-lookup"><span data-stu-id="bf59e-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzureStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="bf59e-136">Bu komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur ve bu anahtarı $Context değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="bf59e-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="bf59e-137">İkinci komut, dosyayı belirtilen URI 'den ContosoArchive adlı kapsayıcıda ContosoPlanning adlı blob 'a kopyalar.</span><span class="sxs-lookup"><span data-stu-id="bf59e-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="bf59e-138">Komut, $Context depolanan bağlamda kopyalama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="bf59e-138">The command starts the copy operation in the context stored in $Context.</span></span>

## <span data-ttu-id="bf59e-139">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf59e-139">PARAMETERS</span></span>

### <span data-ttu-id="bf59e-140">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="bf59e-140">-AbsoluteUri</span></span>
<span data-ttu-id="bf59e-141">Azure depolama blob blob 'una kopyalanacak dosyanın mutlak URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf59e-141">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="bf59e-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bf59e-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bf59e-143">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf59e-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bf59e-144">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="bf59e-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bf59e-145">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="bf59e-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bf59e-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="bf59e-146">-CloudBlob</span></span>
<span data-ttu-id="bf59e-147">Azure depolama Istemci kitaplığından bir **Cloudblob** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf59e-147">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="bf59e-148">**Cloudblob** nesnesi edinmek için Get-AzureStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bf59e-148">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf59e-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="bf59e-149">-CloudBlobContainer</span></span>
<span data-ttu-id="bf59e-150">Azure depolama Istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf59e-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="bf59e-151">Bu cmdlet, bu parametrenin belirttiği kapsayıcıdan bir blob kopyalar.</span><span class="sxs-lookup"><span data-stu-id="bf59e-151">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="bf59e-152">**Cloudblobcontainer** nesnesi edinmek için Get-AzureStorageContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bf59e-152">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf59e-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bf59e-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bf59e-154">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf59e-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bf59e-155">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bf59e-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bf59e-156">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="bf59e-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bf59e-157">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="bf59e-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bf59e-158">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="bf59e-158">The default value is 10.</span></span>

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

### <span data-ttu-id="bf59e-159">-Context</span><span class="sxs-lookup"><span data-stu-id="bf59e-159">-Context</span></span>
<span data-ttu-id="bf59e-160">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf59e-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bf59e-161">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bf59e-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bf59e-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf59e-162">-DefaultProfile</span></span>
<span data-ttu-id="bf59e-163">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bf59e-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf59e-164">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="bf59e-164">-DestBlob</span></span>
<span data-ttu-id="bf59e-165">Hedef blob adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf59e-165">Specifies the name of the destination blob.</span></span>

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

### <span data-ttu-id="bf59e-166">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="bf59e-166">-DestCloudBlob</span></span>
<span data-ttu-id="bf59e-167">Hedef **Cloudblob** nesnesini belirtir</span><span class="sxs-lookup"><span data-stu-id="bf59e-167">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf59e-168">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="bf59e-168">-DestContainer</span></span>
<span data-ttu-id="bf59e-169">Hedef kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf59e-169">Specifies the name of the destination container.</span></span>

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

### <span data-ttu-id="bf59e-170">-DestContext</span><span class="sxs-lookup"><span data-stu-id="bf59e-170">-DestContext</span></span>
<span data-ttu-id="bf59e-171">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf59e-171">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bf59e-172">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bf59e-172">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bf59e-173">-Force</span><span class="sxs-lookup"><span data-stu-id="bf59e-173">-Force</span></span>
<span data-ttu-id="bf59e-174">Bu cmdlet 'in hedef blob 'un üzerine sizden onay istemeden yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bf59e-174">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="bf59e-175">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="bf59e-175">-PremiumPageBlobTier</span></span>
<span data-ttu-id="bf59e-176">Premium sayfa blob katmanı</span><span class="sxs-lookup"><span data-stu-id="bf59e-176">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf59e-177">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bf59e-177">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bf59e-178">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf59e-178">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="bf59e-179">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="bf59e-179">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="bf59e-180">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="bf59e-180">-SrcBlob</span></span>
<span data-ttu-id="bf59e-181">Kaynak bloonun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf59e-181">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="bf59e-182">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="bf59e-182">-SrcContainer</span></span>
<span data-ttu-id="bf59e-183">Kaynak kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf59e-183">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="bf59e-184">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="bf59e-184">-SrcDir</span></span>
<span data-ttu-id="bf59e-185">Azure depolama Istemci kitaplığından bir **Cloudfiledirectory** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf59e-185">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf59e-186">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="bf59e-186">-SrcFile</span></span>
<span data-ttu-id="bf59e-187">Azure depolama Istemci kitaplığından bir **Cloudfile** nesnesini belirtimi.</span><span class="sxs-lookup"><span data-stu-id="bf59e-187">Specifes a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="bf59e-188">Bunu oluşturabilir veya Get-AzureStorageFile cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bf59e-188">You can create it or use Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf59e-189">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="bf59e-189">-SrcFilePath</span></span>
<span data-ttu-id="bf59e-190">Kaynak dizinin veya kaynak paylaşımın kaynak dosyası göreli yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf59e-190">Specifies the source file relative path of source directory or source share.</span></span>

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

### <span data-ttu-id="bf59e-191">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="bf59e-191">-SrcShare</span></span>
<span data-ttu-id="bf59e-192">Azure depolama Istemci kitaplığından bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf59e-192">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="bf59e-193">Bunu oluşturabilir veya Get-AzureStorageShare cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bf59e-193">You can create it or use Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf59e-194">-Srcpaylaşımadı</span><span class="sxs-lookup"><span data-stu-id="bf59e-194">-SrcShareName</span></span>
<span data-ttu-id="bf59e-195">Kaynak paylaşımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf59e-195">Specifies the source share name.</span></span>

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

### <span data-ttu-id="bf59e-196">-Onay</span><span class="sxs-lookup"><span data-stu-id="bf59e-196">-Confirm</span></span>
<span data-ttu-id="bf59e-197">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bf59e-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf59e-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf59e-198">-WhatIf</span></span>
<span data-ttu-id="bf59e-199">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bf59e-199">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf59e-200">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bf59e-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf59e-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf59e-201">CommonParameters</span></span>
<span data-ttu-id="bf59e-202">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf59e-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf59e-203">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf59e-203">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf59e-204">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf59e-204">INPUTS</span></span>

### <span data-ttu-id="bf59e-205">Microsoft. Windowsazde. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="bf59e-205">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="bf59e-206">Microsoft. Windowsazde. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="bf59e-206">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="bf59e-207">Microsoft. Windowsazde. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="bf59e-207">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="bf59e-208">Parametreler: SrcFile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bf59e-208">Parameters: SrcFile (ByValue)</span></span>

### <span data-ttu-id="bf59e-209">System. String</span><span class="sxs-lookup"><span data-stu-id="bf59e-209">System.String</span></span>

### <span data-ttu-id="bf59e-210">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="bf59e-210">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bf59e-211">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf59e-211">OUTPUTS</span></span>

### <span data-ttu-id="bf59e-212">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="bf59e-212">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="bf59e-213">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf59e-213">NOTES</span></span>

## <span data-ttu-id="bf59e-214">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf59e-214">RELATED LINKS</span></span>

[<span data-ttu-id="bf59e-215">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="bf59e-215">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)

[<span data-ttu-id="bf59e-216">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="bf59e-216">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)
