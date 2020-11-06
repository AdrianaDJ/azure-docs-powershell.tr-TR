---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
ms.openlocfilehash: eddc442dd442fbb64f7b075f49a3c638ea6920e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592149"
---
# <span data-ttu-id="2ae01-101">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2ae01-101">Set-AzureStorageBlobContent</span></span>

## <span data-ttu-id="2ae01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ae01-102">SYNOPSIS</span></span>
<span data-ttu-id="2ae01-103">Bir Azure depolama blobir yerel dosyayı karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="2ae01-103">Uploads a local file to an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ae01-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ae01-104">SYNTAX</span></span>

### <span data-ttu-id="2ae01-105">SendManual (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2ae01-105">SendManual (Default)</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ae01-106">Kapsayıcı boru hattı</span><span class="sxs-lookup"><span data-stu-id="2ae01-106">ContainerPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ae01-107">Blobboru hattı</span><span class="sxs-lookup"><span data-stu-id="2ae01-107">BlobPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ae01-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ae01-108">DESCRIPTION</span></span>
<span data-ttu-id="2ae01-109">**Set-AzureStorageBlobContent** cmdlet 'i bir yerel dosyayı Azure depolama blob blob 'una yükler.</span><span class="sxs-lookup"><span data-stu-id="2ae01-109">The **Set-AzureStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="2ae01-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ae01-110">EXAMPLES</span></span>

### <span data-ttu-id="2ae01-111">Örnek 1: adlandırılmış bir dosyayı karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="2ae01-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="2ae01-112">Bu komut, Planlıkverileri adındaki dosyayı Planning2015 adlı bir blob 'a yükler.</span><span class="sxs-lookup"><span data-stu-id="2ae01-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="2ae01-113">Örnek 2: geçerli klasörün altındaki tüm dosyaları karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="2ae01-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="2ae01-114">Bu komut, geçerli klasördeki ve alt klasörlerdeki tüm dosyaları almak için Get-ChildItem çekirdek Windows PowerShell cmdlet 'ini kullanır ve ardından bunları geçerli cmdlet 'e, ardışık düzen işlecini kullanarak geçirir.</span><span class="sxs-lookup"><span data-stu-id="2ae01-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2ae01-115">**Set-AzureStorageBlobContent** cmdlet 'i, dosyaları contosocontosoadındaki kapsayıcıya yükler.</span><span class="sxs-lookup"><span data-stu-id="2ae01-115">The **Set-AzureStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="2ae01-116">Örnek 3: var olan bir bloonun üzerine yazma</span><span class="sxs-lookup"><span data-stu-id="2ae01-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="2ae01-117">Bu komut, Get-AzureStorageBlob cmdlet 'ini kullanarak Contosoyüklemelerini kapsayıcısında Planning2015 adındaki blob 'u alır ve bu blobu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="2ae01-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzureStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="2ae01-118">Komut, ContosoPlanning adındaki dosyayı Planning2015 olarak yükler.</span><span class="sxs-lookup"><span data-stu-id="2ae01-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="2ae01-119">Bu komut *Force* parametresini belirtmez.</span><span class="sxs-lookup"><span data-stu-id="2ae01-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="2ae01-120">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2ae01-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="2ae01-121">Komutu onaylamıyorsanız cmdlet var olan bloonun üzerine yazar.</span><span class="sxs-lookup"><span data-stu-id="2ae01-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="2ae01-122">Örnek 4: ardışık düzeni kullanarak bir dosyayı kapsayıcıya yükleme</span><span class="sxs-lookup"><span data-stu-id="2ae01-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="2ae01-123">Bu komut, **contoso-AzureStorageContainer** cmdlet 'ini kullanarak, contosoupload dizesiyle başlayan kapsayıcıyı alır ve o blob 'u geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="2ae01-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzureStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="2ae01-124">Komut, ContosoPlanning adındaki dosyayı Planning2015 olarak yükler.</span><span class="sxs-lookup"><span data-stu-id="2ae01-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="2ae01-125">Örnek 5: PremiumPageBlobTier as</span><span class="sxs-lookup"><span data-stu-id="2ae01-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="2ae01-126">İlk komut, blob için meta veriler içeren bir karma tablo oluşturur ve bu karma tabloyu $Metadata değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2ae01-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>

<span data-ttu-id="2ae01-127">İkinci komut, ContosoPlanning adlı dosyayı Contosoyüklemeler adlı kapsayıcıya yükler.</span><span class="sxs-lookup"><span data-stu-id="2ae01-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="2ae01-128">Blob, $Metadata depolanan meta verileri içerir ve PremiumPageBlobTier olarak.</span><span class="sxs-lookup"><span data-stu-id="2ae01-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="2ae01-129">Örnek 6: belirtilen blob özellikleriyle blob 'a dosya yükleme</span><span class="sxs-lookup"><span data-stu-id="2ae01-129">Example 6: Upload a file to blob with specified blob properties</span></span>
```
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Properties @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="}
```

<span data-ttu-id="2ae01-130">Bu komut, ContosoPlanning adlı dosyayı, contoso, belirtilen blob özellikleriyle karşıya yüklemeler adlı kapsayıcıya yükler.</span><span class="sxs-lookup"><span data-stu-id="2ae01-130">This command  uploads the file that is named ContosoPlanning to the container named ContosoUploads with specified blob properties.</span></span>

## <span data-ttu-id="2ae01-131">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ae01-131">PARAMETERS</span></span>

### <span data-ttu-id="2ae01-132">-Blob</span><span class="sxs-lookup"><span data-stu-id="2ae01-132">-Blob</span></span>
<span data-ttu-id="2ae01-133">Blob 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ae01-133">Specifies the name of a blob.</span></span>
<span data-ttu-id="2ae01-134">Bu cmdlet, bu parametrenin belirttiği Azure depolama blob blob 'ine bir dosya yükler.</span><span class="sxs-lookup"><span data-stu-id="2ae01-134">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: SendManual, ContainerPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ae01-135">-BlobType</span><span class="sxs-lookup"><span data-stu-id="2ae01-135">-BlobType</span></span>
<span data-ttu-id="2ae01-136">Bu cmdlet 'in karşıya yükleolduğu blob 'un türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ae01-136">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="2ae01-137">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2ae01-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2ae01-138">Engellenebilir</span><span class="sxs-lookup"><span data-stu-id="2ae01-138">Block</span></span>
- <span data-ttu-id="2ae01-139">Sayfa</span><span class="sxs-lookup"><span data-stu-id="2ae01-139">Page</span></span>

<span data-ttu-id="2ae01-140">Varsayılan değer engelle değeridir.</span><span class="sxs-lookup"><span data-stu-id="2ae01-140">The default value is Block.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ae01-141">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2ae01-141">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2ae01-142">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ae01-142">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2ae01-143">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="2ae01-143">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2ae01-144">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="2ae01-144">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2ae01-145">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="2ae01-145">-CloudBlob</span></span>
<span data-ttu-id="2ae01-146">**Cloudblob** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ae01-146">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="2ae01-147">**Cloudblob** nesnesi edinmek için Get-AzureStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2ae01-147">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="2ae01-148">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="2ae01-148">-CloudBlobContainer</span></span>
<span data-ttu-id="2ae01-149">Azure depolama Istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ae01-149">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="2ae01-150">Bu cmdlet, bu parametrenin belirttiği kapsayıcıdaki bir blob 'a içerik yükler.</span><span class="sxs-lookup"><span data-stu-id="2ae01-150">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="2ae01-151">**Cloudblobcontainer** nesnesi edinmek için Get-AzureStorageContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2ae01-151">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="2ae01-152">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2ae01-152">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2ae01-153">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ae01-153">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2ae01-154">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ae01-154">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2ae01-155">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="2ae01-155">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2ae01-156">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="2ae01-156">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2ae01-157">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="2ae01-157">The default value is 10.</span></span>

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

### <span data-ttu-id="2ae01-158">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="2ae01-158">-Container</span></span>
<span data-ttu-id="2ae01-159">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ae01-159">Specifies the name of a container.</span></span>
<span data-ttu-id="2ae01-160">Bu cmdlet, bu parametrenin belirttiği kapsayıcıdaki bir blob 'a dosya yükler.</span><span class="sxs-lookup"><span data-stu-id="2ae01-160">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: SendManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ae01-161">-Context</span><span class="sxs-lookup"><span data-stu-id="2ae01-161">-Context</span></span>
<span data-ttu-id="2ae01-162">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ae01-162">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2ae01-163">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2ae01-163">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2ae01-164">-Dosya</span><span class="sxs-lookup"><span data-stu-id="2ae01-164">-File</span></span>
<span data-ttu-id="2ae01-165">Dosya BLOB içeriği olarak yüklenecek bir dosya yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ae01-165">Specifies a local file path for a file to upload as blob content.</span></span>

```yaml
Type: String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ae01-166">-Force</span><span class="sxs-lookup"><span data-stu-id="2ae01-166">-Force</span></span>
<span data-ttu-id="2ae01-167">Bu cmdlet 'in var olan bir bloonun onay istemeden üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ae01-167">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="2ae01-168">-Metadata</span><span class="sxs-lookup"><span data-stu-id="2ae01-168">-Metadata</span></span>
<span data-ttu-id="2ae01-169">Karşıya yüklenen blob için meta verileri belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ae01-169">Specifies metadata for the uploaded blob.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ae01-170">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="2ae01-170">-PremiumPageBlobTier</span></span>
<span data-ttu-id="2ae01-171">Sayfa blob katmanı</span><span class="sxs-lookup"><span data-stu-id="2ae01-171">Page Blob Tier</span></span>

```yaml
Type: PremiumPageBlobTier
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ae01-172">-Özellikler</span><span class="sxs-lookup"><span data-stu-id="2ae01-172">-Properties</span></span>
<span data-ttu-id="2ae01-173">Karşıya yüklenen blob 'un özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ae01-173">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="2ae01-174">Desteklenen Özellikler: CacheControl, ContentDisposition, Contentenkodlama, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="2ae01-174">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ae01-175">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2ae01-175">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2ae01-176">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ae01-176">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="2ae01-177">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="2ae01-177">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="2ae01-178">-Onay</span><span class="sxs-lookup"><span data-stu-id="2ae01-178">-Confirm</span></span>
<span data-ttu-id="2ae01-179">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2ae01-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ae01-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ae01-180">-WhatIf</span></span>
<span data-ttu-id="2ae01-181">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ae01-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ae01-182">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2ae01-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ae01-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ae01-183">CommonParameters</span></span>
<span data-ttu-id="2ae01-184">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ae01-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ae01-185">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ae01-185">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ae01-186">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ae01-186">INPUTS</span></span>

### <span data-ttu-id="2ae01-187">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="2ae01-187">IStorageContext</span></span>

<span data-ttu-id="2ae01-188">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="2ae01-188">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="2ae01-189">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ae01-189">OUTPUTS</span></span>

### <span data-ttu-id="2ae01-190">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2ae01-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="2ae01-191">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ae01-191">NOTES</span></span>

## <span data-ttu-id="2ae01-192">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ae01-192">RELATED LINKS</span></span>

[<span data-ttu-id="2ae01-193">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2ae01-193">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="2ae01-194">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2ae01-194">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="2ae01-195">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2ae01-195">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
