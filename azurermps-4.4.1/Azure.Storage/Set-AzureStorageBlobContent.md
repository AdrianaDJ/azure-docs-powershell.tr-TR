---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
gitcommit: https://github.com/Azure/azure-powershell/blob/a2772c13c7cb665d7485636044c46f8c9222fc68
ms.openlocfilehash: c7acda834cda53a86073692dc6c888ce2803d859
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593878"
---
# <span data-ttu-id="61757-101">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="61757-101">Set-AzureStorageBlobContent</span></span>

## <span data-ttu-id="61757-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61757-102">SYNOPSIS</span></span>
<span data-ttu-id="61757-103">Bir Azure depolama blobir yerel dosyayı karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="61757-103">Uploads a local file to an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61757-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61757-104">SYNTAX</span></span>

### <span data-ttu-id="61757-105">SendManual (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="61757-105">SendManual (Default)</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61757-106">Kapsayıcı boru hattı</span><span class="sxs-lookup"><span data-stu-id="61757-106">ContainerPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61757-107">Blobboru hattı</span><span class="sxs-lookup"><span data-stu-id="61757-107">BlobPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61757-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="61757-108">DESCRIPTION</span></span>
<span data-ttu-id="61757-109">**Set-AzureStorageBlobContent** cmdlet 'i bir yerel dosyayı Azure depolama blob blob 'una yükler.</span><span class="sxs-lookup"><span data-stu-id="61757-109">The **Set-AzureStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="61757-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61757-110">EXAMPLES</span></span>

### <span data-ttu-id="61757-111">Örnek 1: adlandırılmış bir dosyayı karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="61757-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="61757-112">Bu komut, Planlıkverileri adındaki dosyayı Planning2015 adlı bir blob 'a yükler.</span><span class="sxs-lookup"><span data-stu-id="61757-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="61757-113">Örnek 2: geçerli klasörün altındaki tüm dosyaları karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="61757-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="61757-114">Bu komut, geçerli klasördeki ve alt klasörlerdeki tüm dosyaları almak için Get-ChildItem çekirdek Windows PowerShell cmdlet 'ini kullanır ve ardından bunları geçerli cmdlet 'e, ardışık düzen işlecini kullanarak geçirir.</span><span class="sxs-lookup"><span data-stu-id="61757-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="61757-115">**Set-AzureStorageBlobContent** cmdlet 'i, dosyaları contosocontosoadındaki kapsayıcıya yükler.</span><span class="sxs-lookup"><span data-stu-id="61757-115">The **Set-AzureStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="61757-116">Örnek 3: var olan bir bloonun üzerine yazma</span><span class="sxs-lookup"><span data-stu-id="61757-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="61757-117">Bu komut, Get-AzureStorageBlob cmdlet 'ini kullanarak Contosoyüklemelerini kapsayıcısında Planning2015 adındaki blob 'u alır ve bu blobu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="61757-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzureStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="61757-118">Komut, ContosoPlanning adındaki dosyayı Planning2015 olarak yükler.</span><span class="sxs-lookup"><span data-stu-id="61757-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="61757-119">Bu komut *Force* parametresini belirtmez.</span><span class="sxs-lookup"><span data-stu-id="61757-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="61757-120">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="61757-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="61757-121">Komutu onaylamıyorsanız cmdlet var olan bloonun üzerine yazar.</span><span class="sxs-lookup"><span data-stu-id="61757-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="61757-122">Örnek 4: ardışık düzeni kullanarak bir dosyayı kapsayıcıya yükleme</span><span class="sxs-lookup"><span data-stu-id="61757-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="61757-123">Bu komut, **contoso-AzureStorageContainer** cmdlet 'ini kullanarak, contosoupload dizesiyle başlayan kapsayıcıyı alır ve o blob 'u geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="61757-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzureStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="61757-124">Komut, ContosoPlanning adındaki dosyayı Planning2015 olarak yükler.</span><span class="sxs-lookup"><span data-stu-id="61757-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="61757-125">Örnek 5: PremiumPageBlobTier as</span><span class="sxs-lookup"><span data-stu-id="61757-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="61757-126">İlk komut, blob için meta veriler içeren bir karma tablo oluşturur ve bu karma tabloyu $Metadata değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="61757-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>

<span data-ttu-id="61757-127">İkinci komut, ContosoPlanning adlı dosyayı Contosoyüklemeler adlı kapsayıcıya yükler.</span><span class="sxs-lookup"><span data-stu-id="61757-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="61757-128">Blob, $Metadata depolanan meta verileri içerir ve PremiumPageBlobTier olarak.</span><span class="sxs-lookup"><span data-stu-id="61757-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

## <span data-ttu-id="61757-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61757-129">PARAMETERS</span></span>

### <span data-ttu-id="61757-130">-Blob</span><span class="sxs-lookup"><span data-stu-id="61757-130">-Blob</span></span>
<span data-ttu-id="61757-131">Blob 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61757-131">Specifies the name of a blob.</span></span>
<span data-ttu-id="61757-132">Bu cmdlet, bu parametrenin belirttiği Azure depolama blob blob 'ine bir dosya yükler.</span><span class="sxs-lookup"><span data-stu-id="61757-132">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="61757-133">-BlobType</span><span class="sxs-lookup"><span data-stu-id="61757-133">-BlobType</span></span>
<span data-ttu-id="61757-134">Bu cmdlet 'in karşıya yükleolduğu blob 'un türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="61757-134">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="61757-135">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="61757-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="61757-136">Engellenebilir</span><span class="sxs-lookup"><span data-stu-id="61757-136">Block</span></span>
- <span data-ttu-id="61757-137">Sayfa</span><span class="sxs-lookup"><span data-stu-id="61757-137">Page</span></span>

<span data-ttu-id="61757-138">Varsayılan değer engelle değeridir.</span><span class="sxs-lookup"><span data-stu-id="61757-138">The default value is Block.</span></span>

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

### <span data-ttu-id="61757-139">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="61757-139">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="61757-140">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="61757-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="61757-141">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="61757-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="61757-142">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="61757-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="61757-143">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="61757-143">-CloudBlob</span></span>
<span data-ttu-id="61757-144">**Cloudblob** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="61757-144">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="61757-145">**Cloudblob** nesnesi edinmek için Get-AzureStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="61757-145">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="61757-146">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="61757-146">-CloudBlobContainer</span></span>
<span data-ttu-id="61757-147">Azure depolama Istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="61757-147">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="61757-148">Bu cmdlet, bu parametrenin belirttiği kapsayıcıdaki bir blob 'a içerik yükler.</span><span class="sxs-lookup"><span data-stu-id="61757-148">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="61757-149">**Cloudblobcontainer** nesnesi edinmek için Get-AzureStorageContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="61757-149">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="61757-150">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="61757-150">-ConcurrentTaskCount</span></span>
<span data-ttu-id="61757-151">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61757-151">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="61757-152">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="61757-152">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="61757-153">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="61757-153">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="61757-154">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="61757-154">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="61757-155">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="61757-155">The default value is 10.</span></span>

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

### <span data-ttu-id="61757-156">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="61757-156">-Container</span></span>
<span data-ttu-id="61757-157">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61757-157">Specifies the name of a container.</span></span>
<span data-ttu-id="61757-158">Bu cmdlet, bu parametrenin belirttiği kapsayıcıdaki bir blob 'a dosya yükler.</span><span class="sxs-lookup"><span data-stu-id="61757-158">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="61757-159">-Context</span><span class="sxs-lookup"><span data-stu-id="61757-159">-Context</span></span>
<span data-ttu-id="61757-160">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61757-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="61757-161">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="61757-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="61757-162">-Dosya</span><span class="sxs-lookup"><span data-stu-id="61757-162">-File</span></span>
<span data-ttu-id="61757-163">Dosya BLOB içeriği olarak yüklenecek bir dosya yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="61757-163">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="61757-164">-Force</span><span class="sxs-lookup"><span data-stu-id="61757-164">-Force</span></span>
<span data-ttu-id="61757-165">Bu cmdlet 'in var olan bir bloonun onay istemeden üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="61757-165">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="61757-166">-Metadata</span><span class="sxs-lookup"><span data-stu-id="61757-166">-Metadata</span></span>
<span data-ttu-id="61757-167">Karşıya yüklenen blob için meta verileri belirtir.</span><span class="sxs-lookup"><span data-stu-id="61757-167">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="61757-168">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="61757-168">-PremiumPageBlobTier</span></span>
<span data-ttu-id="61757-169">Sayfa blob katmanı</span><span class="sxs-lookup"><span data-stu-id="61757-169">Page Blob Tier</span></span>

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

### <span data-ttu-id="61757-170">-Özellikler</span><span class="sxs-lookup"><span data-stu-id="61757-170">-Properties</span></span>
<span data-ttu-id="61757-171">Karşıya yüklenen blob 'un özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="61757-171">Specifies properties for the uploaded blob.</span></span>

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

### <span data-ttu-id="61757-172">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="61757-172">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="61757-173">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61757-173">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="61757-174">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="61757-174">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="61757-175">-Onay</span><span class="sxs-lookup"><span data-stu-id="61757-175">-Confirm</span></span>
<span data-ttu-id="61757-176">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="61757-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61757-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61757-177">-WhatIf</span></span>
<span data-ttu-id="61757-178">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61757-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61757-179">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="61757-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61757-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61757-180">CommonParameters</span></span>
<span data-ttu-id="61757-181">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61757-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61757-182">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61757-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61757-183">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61757-183">INPUTS</span></span>

### <span data-ttu-id="61757-184">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="61757-184">IStorageContext</span></span>

<span data-ttu-id="61757-185">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="61757-185">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="61757-186">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61757-186">OUTPUTS</span></span>

### <span data-ttu-id="61757-187">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="61757-187">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="61757-188">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61757-188">NOTES</span></span>

## <span data-ttu-id="61757-189">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61757-189">RELATED LINKS</span></span>

[<span data-ttu-id="61757-190">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="61757-190">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="61757-191">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="61757-191">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="61757-192">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="61757-192">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
