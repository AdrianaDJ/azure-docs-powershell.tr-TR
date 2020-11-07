---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: 0730d509ddf207d7541e854b15f34c30b44093e0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936168"
---
# <span data-ttu-id="93e99-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="93e99-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="93e99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93e99-102">SYNOPSIS</span></span>
<span data-ttu-id="93e99-103">Bir Azure depolama blobir yerel dosyayı karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="93e99-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="93e99-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="93e99-104">SYNTAX</span></span>

### <span data-ttu-id="93e99-105">SendManual (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="93e99-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93e99-106">Kapsayıcı boru hattı</span><span class="sxs-lookup"><span data-stu-id="93e99-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93e99-107">Blobboru hattı</span><span class="sxs-lookup"><span data-stu-id="93e99-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93e99-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="93e99-108">DESCRIPTION</span></span>
<span data-ttu-id="93e99-109">**Set-AzStorageBlobContent** cmdlet 'i, yerel dosyayı bir Azure depolama blob blob 'una yükler.</span><span class="sxs-lookup"><span data-stu-id="93e99-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="93e99-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="93e99-110">EXAMPLES</span></span>

### <span data-ttu-id="93e99-111">Örnek 1: adlandırılmış bir dosyayı karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="93e99-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="93e99-112">Bu komut, Planlıkverileri adındaki dosyayı Planning2015 adlı bir blob 'a yükler.</span><span class="sxs-lookup"><span data-stu-id="93e99-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="93e99-113">Örnek 2: geçerli klasörün altındaki tüm dosyaları karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="93e99-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="93e99-114">Bu komut, geçerli klasördeki ve alt klasörlerdeki tüm dosyaları almak için Get-ChildItem çekirdek Windows PowerShell cmdlet 'ini kullanır ve ardından bunları geçerli cmdlet 'e, ardışık düzen işlecini kullanarak geçirir.</span><span class="sxs-lookup"><span data-stu-id="93e99-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="93e99-115">**Set-AzStorageBlobContent** cmdlet 'ı contosoyüklemeler adlı kapsayıcıya yükler.</span><span class="sxs-lookup"><span data-stu-id="93e99-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="93e99-116">Örnek 3: var olan bir bloonun üzerine yazma</span><span class="sxs-lookup"><span data-stu-id="93e99-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="93e99-117">Bu komut, Get-AzStorageBlob cmdlet 'ini kullanarak Contosoyüklemelerini kapsayıcısında Planning2015 adındaki blob 'u alır ve bu blobu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="93e99-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="93e99-118">Komut, ContosoPlanning adındaki dosyayı Planning2015 olarak yükler.</span><span class="sxs-lookup"><span data-stu-id="93e99-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="93e99-119">Bu komut *Force* parametresini belirtmez.</span><span class="sxs-lookup"><span data-stu-id="93e99-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="93e99-120">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="93e99-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="93e99-121">Komutu onaylamıyorsanız cmdlet var olan bloonun üzerine yazar.</span><span class="sxs-lookup"><span data-stu-id="93e99-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="93e99-122">Örnek 4: ardışık düzeni kullanarak bir dosyayı kapsayıcıya yükleme</span><span class="sxs-lookup"><span data-stu-id="93e99-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="93e99-123">Bu komut **Get-AzStorageContainer** cmdlet 'Ini kullanarak contosoupload dizesiyle başlayan kapsayıcıyı alır ve o blob 'u geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="93e99-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="93e99-124">Komut, ContosoPlanning adındaki dosyayı Planning2015 olarak yükler.</span><span class="sxs-lookup"><span data-stu-id="93e99-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="93e99-125">Örnek 5: PremiumPageBlobTier as</span><span class="sxs-lookup"><span data-stu-id="93e99-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="93e99-126">İlk komut, blob için meta veriler içeren bir karma tablo oluşturur ve bu karma tabloyu $Metadata değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="93e99-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="93e99-127">İkinci komut, ContosoPlanning adlı dosyayı Contosoyüklemeler adlı kapsayıcıya yükler.</span><span class="sxs-lookup"><span data-stu-id="93e99-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="93e99-128">Blob, $Metadata depolanan meta verileri içerir ve PremiumPageBlobTier olarak.</span><span class="sxs-lookup"><span data-stu-id="93e99-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="93e99-129">Örnek 6: belirtilen blob özellikleriyle blob 'a dosya yükleme</span><span class="sxs-lookup"><span data-stu-id="93e99-129">Example 6: Upload a file to blob with specified blob properties</span></span>
```
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Properties @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="}
```

<span data-ttu-id="93e99-130">Bu komut, ContosoPlanning adlı dosyayı, contoso, belirtilen blob özellikleriyle karşıya yüklemeler adlı kapsayıcıya yükler.</span><span class="sxs-lookup"><span data-stu-id="93e99-130">This command  uploads the file that is named ContosoPlanning to the container named ContosoUploads with specified blob properties.</span></span>

## <span data-ttu-id="93e99-131">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="93e99-131">PARAMETERS</span></span>

### <span data-ttu-id="93e99-132">-Blob</span><span class="sxs-lookup"><span data-stu-id="93e99-132">-Blob</span></span>
<span data-ttu-id="93e99-133">Blob 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93e99-133">Specifies the name of a blob.</span></span>
<span data-ttu-id="93e99-134">Bu cmdlet, bu parametrenin belirttiği Azure depolama blob blob 'ine bir dosya yükler.</span><span class="sxs-lookup"><span data-stu-id="93e99-134">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93e99-135">-BlobType</span><span class="sxs-lookup"><span data-stu-id="93e99-135">-BlobType</span></span>
<span data-ttu-id="93e99-136">Bu cmdlet 'in karşıya yükleolduğu blob 'un türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="93e99-136">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="93e99-137">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="93e99-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="93e99-138">Engellenebilir</span><span class="sxs-lookup"><span data-stu-id="93e99-138">Block</span></span>
- <span data-ttu-id="93e99-139">Sayfa varsayılan değer engelle değeridir.</span><span class="sxs-lookup"><span data-stu-id="93e99-139">Page The default value is Block.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93e99-140">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="93e99-140">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="93e99-141">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="93e99-141">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="93e99-142">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="93e99-142">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="93e99-143">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="93e99-143">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="93e99-144">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="93e99-144">-CloudBlob</span></span>
<span data-ttu-id="93e99-145">**Cloudblob** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="93e99-145">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="93e99-146">**Cloudblob** nesnesi edinmek için Get-AzStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="93e99-146">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93e99-147">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="93e99-147">-CloudBlobContainer</span></span>
<span data-ttu-id="93e99-148">Azure depolama Istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="93e99-148">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="93e99-149">Bu cmdlet, bu parametrenin belirttiği kapsayıcıdaki bir blob 'a içerik yükler.</span><span class="sxs-lookup"><span data-stu-id="93e99-149">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="93e99-150">**Cloudblobcontainer** nesnesi edinmek için Get-AzStorageContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="93e99-150">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93e99-151">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="93e99-151">-ConcurrentTaskCount</span></span>
<span data-ttu-id="93e99-152">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93e99-152">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="93e99-153">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="93e99-153">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="93e99-154">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="93e99-154">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="93e99-155">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="93e99-155">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="93e99-156">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="93e99-156">The default value is 10.</span></span>

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

### <span data-ttu-id="93e99-157">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="93e99-157">-Container</span></span>
<span data-ttu-id="93e99-158">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93e99-158">Specifies the name of a container.</span></span>
<span data-ttu-id="93e99-159">Bu cmdlet, bu parametrenin belirttiği kapsayıcıdaki bir blob 'a dosya yükler.</span><span class="sxs-lookup"><span data-stu-id="93e99-159">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93e99-160">-Context</span><span class="sxs-lookup"><span data-stu-id="93e99-160">-Context</span></span>
<span data-ttu-id="93e99-161">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93e99-161">Specifies an Azure storage context.</span></span>
<span data-ttu-id="93e99-162">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="93e99-162">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="93e99-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e99-163">-DefaultProfile</span></span>
<span data-ttu-id="93e99-164">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="93e99-164">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93e99-165">-Dosya</span><span class="sxs-lookup"><span data-stu-id="93e99-165">-File</span></span>
<span data-ttu-id="93e99-166">Dosya BLOB içeriği olarak yüklenecek bir dosya yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="93e99-166">Specifies a local file path for a file to upload as blob content.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93e99-167">-Force</span><span class="sxs-lookup"><span data-stu-id="93e99-167">-Force</span></span>
<span data-ttu-id="93e99-168">Bu cmdlet 'in var olan bir bloonun onay istemeden üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="93e99-168">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="93e99-169">-Metadata</span><span class="sxs-lookup"><span data-stu-id="93e99-169">-Metadata</span></span>
<span data-ttu-id="93e99-170">Karşıya yüklenen blob için meta verileri belirtir.</span><span class="sxs-lookup"><span data-stu-id="93e99-170">Specifies metadata for the uploaded blob.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93e99-171">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="93e99-171">-PremiumPageBlobTier</span></span>
<span data-ttu-id="93e99-172">Sayfa blob katmanı</span><span class="sxs-lookup"><span data-stu-id="93e99-172">Page Blob Tier</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93e99-173">-Özellikler</span><span class="sxs-lookup"><span data-stu-id="93e99-173">-Properties</span></span>
<span data-ttu-id="93e99-174">Karşıya yüklenen blob 'un özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="93e99-174">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="93e99-175">Desteklenen Özellikler: CacheControl, ContentDisposition, Contentenkodlama, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="93e99-175">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93e99-176">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="93e99-176">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="93e99-177">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93e99-177">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="93e99-178">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="93e99-178">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="93e99-179">-Onay</span><span class="sxs-lookup"><span data-stu-id="93e99-179">-Confirm</span></span>
<span data-ttu-id="93e99-180">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="93e99-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93e99-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93e99-181">-WhatIf</span></span>
<span data-ttu-id="93e99-182">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="93e99-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93e99-183">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="93e99-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93e99-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e99-184">CommonParameters</span></span>
<span data-ttu-id="93e99-185">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="93e99-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e99-186">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93e99-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e99-187">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="93e99-187">INPUTS</span></span>

### <span data-ttu-id="93e99-188">System. String</span><span class="sxs-lookup"><span data-stu-id="93e99-188">System.String</span></span>

### <span data-ttu-id="93e99-189">Microsoft. WindowsAz. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="93e99-189">Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="93e99-190">Microsoft. WindowsAz. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="93e99-190">Microsoft.WindowsAz.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="93e99-191">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="93e99-191">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="93e99-192">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="93e99-192">OUTPUTS</span></span>

### <span data-ttu-id="93e99-193">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="93e99-193">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="93e99-194">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="93e99-194">NOTES</span></span>

## <span data-ttu-id="93e99-195">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="93e99-195">RELATED LINKS</span></span>

[<span data-ttu-id="93e99-196">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="93e99-196">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="93e99-197">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="93e99-197">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="93e99-198">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="93e99-198">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
