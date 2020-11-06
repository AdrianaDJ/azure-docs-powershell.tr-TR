---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1caded810569225bfa269e7c0d29c60be87d4fb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572258"
---
# <span data-ttu-id="fd40b-101">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="fd40b-101">Set-AzureStorageBlobContent</span></span>

## <span data-ttu-id="fd40b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd40b-102">SYNOPSIS</span></span>
<span data-ttu-id="fd40b-103">Bir Azure depolama blobir yerel dosyayı karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="fd40b-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="fd40b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd40b-104">SYNTAX</span></span>

### <span data-ttu-id="fd40b-105">SendManual (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fd40b-105">SendManual (Default)</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd40b-106">Kapsayıcı boru hattı</span><span class="sxs-lookup"><span data-stu-id="fd40b-106">ContainerPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd40b-107">Blobboru hattı</span><span class="sxs-lookup"><span data-stu-id="fd40b-107">BlobPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd40b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd40b-108">DESCRIPTION</span></span>
<span data-ttu-id="fd40b-109">**Set-AzureStorageBlobContent** cmdlet 'i bir yerel dosyayı Azure depolama blob blob 'una yükler.</span><span class="sxs-lookup"><span data-stu-id="fd40b-109">The **Set-AzureStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="fd40b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd40b-110">EXAMPLES</span></span>

### <span data-ttu-id="fd40b-111">Örnek 1: adlandırılmış bir dosyayı karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="fd40b-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="fd40b-112">Bu komut, Planlıkverileri adındaki dosyayı Planning2015 adlı bir blob 'a yükler.</span><span class="sxs-lookup"><span data-stu-id="fd40b-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="fd40b-113">Örnek 2: geçerli klasörün altındaki tüm dosyaları karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="fd40b-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="fd40b-114">Bu komut, geçerli klasördeki ve alt klasörlerdeki tüm dosyaları almak için Get-ChildItem çekirdek Windows PowerShell cmdlet 'ini kullanır ve ardından bunları geçerli cmdlet 'e, ardışık düzen işlecini kullanarak geçirir.</span><span class="sxs-lookup"><span data-stu-id="fd40b-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fd40b-115">**Set-AzureStorageBlobContent** cmdlet 'i, dosyaları contosocontosoadındaki kapsayıcıya yükler.</span><span class="sxs-lookup"><span data-stu-id="fd40b-115">The **Set-AzureStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="fd40b-116">Örnek 3: var olan bir bloonun üzerine yazma</span><span class="sxs-lookup"><span data-stu-id="fd40b-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="fd40b-117">Bu komut, Get-AzureStorageBlob cmdlet 'ini kullanarak Contosoyüklemelerini kapsayıcısında Planning2015 adındaki blob 'u alır ve bu blobu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="fd40b-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzureStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="fd40b-118">Komut, ContosoPlanning adındaki dosyayı Planning2015 olarak yükler.</span><span class="sxs-lookup"><span data-stu-id="fd40b-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="fd40b-119">Bu komut *Force* parametresini belirtmez.</span><span class="sxs-lookup"><span data-stu-id="fd40b-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="fd40b-120">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fd40b-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="fd40b-121">Komutu onaylamıyorsanız cmdlet var olan bloonun üzerine yazar.</span><span class="sxs-lookup"><span data-stu-id="fd40b-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="fd40b-122">Örnek 4: ardışık düzeni kullanarak bir dosyayı kapsayıcıya yükleme</span><span class="sxs-lookup"><span data-stu-id="fd40b-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="fd40b-123">Bu komut, **contoso-AzureStorageContainer** cmdlet 'ini kullanarak, contosoupload dizesiyle başlayan kapsayıcıyı alır ve o blob 'u geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="fd40b-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzureStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="fd40b-124">Komut, ContosoPlanning adındaki dosyayı Planning2015 olarak yükler.</span><span class="sxs-lookup"><span data-stu-id="fd40b-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="fd40b-125">Örnek 5: dosya ve meta veri yükleme</span><span class="sxs-lookup"><span data-stu-id="fd40b-125">Example 5: Upload a file and metadata</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata
```

<span data-ttu-id="fd40b-126">İlk komut, blob için meta veriler içeren bir karma tablo oluşturur ve bu karma tabloyu $Metadata değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fd40b-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>

<span data-ttu-id="fd40b-127">İkinci komut, ContosoPlanning adlı dosyayı Contosoyüklemeler adlı kapsayıcıya yükler.</span><span class="sxs-lookup"><span data-stu-id="fd40b-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="fd40b-128">Blob, $Metadata depolanan meta verileri içerir.</span><span class="sxs-lookup"><span data-stu-id="fd40b-128">The blob includes the metadata stored in $Metadata.</span></span>

## <span data-ttu-id="fd40b-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd40b-129">PARAMETERS</span></span>

### <span data-ttu-id="fd40b-130">-Blob</span><span class="sxs-lookup"><span data-stu-id="fd40b-130">-Blob</span></span>
<span data-ttu-id="fd40b-131">Blob 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd40b-131">Specifies the name of a blob.</span></span>
<span data-ttu-id="fd40b-132">Bu cmdlet, bu parametrenin belirttiği Azure depolama blob blob 'ine bir dosya yükler.</span><span class="sxs-lookup"><span data-stu-id="fd40b-132">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="fd40b-133">-BlobType</span><span class="sxs-lookup"><span data-stu-id="fd40b-133">-BlobType</span></span>
<span data-ttu-id="fd40b-134">Bu cmdlet 'in karşıya yükleolduğu blob 'un türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd40b-134">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="fd40b-135">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fd40b-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fd40b-136">Engellenebilir</span><span class="sxs-lookup"><span data-stu-id="fd40b-136">Block</span></span>
- <span data-ttu-id="fd40b-137">Sayfa</span><span class="sxs-lookup"><span data-stu-id="fd40b-137">Page</span></span>

<span data-ttu-id="fd40b-138">Varsayılan değer engelle değeridir.</span><span class="sxs-lookup"><span data-stu-id="fd40b-138">The default value is Block.</span></span>

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

### <span data-ttu-id="fd40b-139">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fd40b-139">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fd40b-140">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd40b-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fd40b-141">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="fd40b-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fd40b-142">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="fd40b-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fd40b-143">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="fd40b-143">-CloudBlob</span></span>
<span data-ttu-id="fd40b-144">**Cloudblob** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd40b-144">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="fd40b-145">**Cloudblob** nesnesi edinmek için Get-AzureStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fd40b-145">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="fd40b-146">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="fd40b-146">-CloudBlobContainer</span></span>
<span data-ttu-id="fd40b-147">Azure depolama Istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd40b-147">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="fd40b-148">Bu cmdlet, bu parametrenin belirttiği kapsayıcıdaki bir blob 'a içerik yükler.</span><span class="sxs-lookup"><span data-stu-id="fd40b-148">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="fd40b-149">**Cloudblobcontainer** nesnesi edinmek için Get-AzureStorageContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fd40b-149">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="fd40b-150">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fd40b-150">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fd40b-151">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd40b-151">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fd40b-152">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fd40b-152">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fd40b-153">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="fd40b-153">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fd40b-154">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="fd40b-154">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fd40b-155">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="fd40b-155">The default value is 10.</span></span>

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

### <span data-ttu-id="fd40b-156">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="fd40b-156">-Container</span></span>
<span data-ttu-id="fd40b-157">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd40b-157">Specifies the name of a container.</span></span>
<span data-ttu-id="fd40b-158">Bu cmdlet, bu parametrenin belirttiği kapsayıcıdaki bir blob 'a dosya yükler.</span><span class="sxs-lookup"><span data-stu-id="fd40b-158">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="fd40b-159">-Context</span><span class="sxs-lookup"><span data-stu-id="fd40b-159">-Context</span></span>
<span data-ttu-id="fd40b-160">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd40b-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fd40b-161">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fd40b-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fd40b-162">-Dosya</span><span class="sxs-lookup"><span data-stu-id="fd40b-162">-File</span></span>
<span data-ttu-id="fd40b-163">Dosya BLOB içeriği olarak yüklenecek bir dosya yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd40b-163">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="fd40b-164">-Force</span><span class="sxs-lookup"><span data-stu-id="fd40b-164">-Force</span></span>
<span data-ttu-id="fd40b-165">Bu cmdlet 'in var olan bir bloonun onay istemeden üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd40b-165">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="fd40b-166">-Metadata</span><span class="sxs-lookup"><span data-stu-id="fd40b-166">-Metadata</span></span>
<span data-ttu-id="fd40b-167">Karşıya yüklenen blob için meta verileri belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd40b-167">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="fd40b-168">-Özellikler</span><span class="sxs-lookup"><span data-stu-id="fd40b-168">-Properties</span></span>
<span data-ttu-id="fd40b-169">Karşıya yüklenen blob 'un özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd40b-169">Specifies properties for the uploaded blob.</span></span>

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

### <span data-ttu-id="fd40b-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fd40b-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fd40b-171">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd40b-171">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="fd40b-172">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="fd40b-172">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="fd40b-173">-Onay</span><span class="sxs-lookup"><span data-stu-id="fd40b-173">-Confirm</span></span>
<span data-ttu-id="fd40b-174">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fd40b-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd40b-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd40b-175">-WhatIf</span></span>
<span data-ttu-id="fd40b-176">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd40b-176">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd40b-177">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fd40b-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd40b-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd40b-178">CommonParameters</span></span>
<span data-ttu-id="fd40b-179">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd40b-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd40b-180">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd40b-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd40b-181">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd40b-181">INPUTS</span></span>

## <span data-ttu-id="fd40b-182">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd40b-182">OUTPUTS</span></span>

## <span data-ttu-id="fd40b-183">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd40b-183">NOTES</span></span>

## <span data-ttu-id="fd40b-184">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd40b-184">RELATED LINKS</span></span>

[<span data-ttu-id="fd40b-185">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="fd40b-185">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="fd40b-186">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="fd40b-186">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="fd40b-187">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="fd40b-187">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
