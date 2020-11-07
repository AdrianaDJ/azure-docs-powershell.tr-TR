---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: d9a602e3e946e28dd04b67c030aeec2aecc3ec93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758544"
---
# <span data-ttu-id="cd18c-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cd18c-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="cd18c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd18c-102">SYNOPSIS</span></span>
<span data-ttu-id="cd18c-103">Bir Azure depolama blobir yerel dosyayı karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="cd18c-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="cd18c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd18c-104">SYNTAX</span></span>

### <span data-ttu-id="cd18c-105">SendManual (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cd18c-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd18c-106">Kapsayıcı boru hattı</span><span class="sxs-lookup"><span data-stu-id="cd18c-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-AsJob] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd18c-107">Blobboru hattı</span><span class="sxs-lookup"><span data-stu-id="cd18c-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd18c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd18c-108">DESCRIPTION</span></span>
<span data-ttu-id="cd18c-109">**Set-AzStorageBlobContent** cmdlet 'i, yerel dosyayı bir Azure depolama blob blob 'una yükler.</span><span class="sxs-lookup"><span data-stu-id="cd18c-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="cd18c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd18c-110">EXAMPLES</span></span>

### <span data-ttu-id="cd18c-111">Örnek 1: adlandırılmış bir dosyayı karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="cd18c-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="cd18c-112">Bu komut, Planlıkverileri adındaki dosyayı Planning2015 adlı bir blob 'a yükler.</span><span class="sxs-lookup"><span data-stu-id="cd18c-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="cd18c-113">Örnek 2: geçerli klasörün altındaki tüm dosyaları karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="cd18c-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="cd18c-114">Bu komut, geçerli klasördeki ve alt klasörlerdeki tüm dosyaları almak için Get-ChildItem çekirdek Windows PowerShell cmdlet 'ini kullanır ve ardından bunları geçerli cmdlet 'e, ardışık düzen işlecini kullanarak geçirir.</span><span class="sxs-lookup"><span data-stu-id="cd18c-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cd18c-115">**Set-AzStorageBlobContent** cmdlet 'ı contosoyüklemeler adlı kapsayıcıya yükler.</span><span class="sxs-lookup"><span data-stu-id="cd18c-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="cd18c-116">Örnek 3: var olan bir bloonun üzerine yazma</span><span class="sxs-lookup"><span data-stu-id="cd18c-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="cd18c-117">Bu komut, Get-AzStorageBlob cmdlet 'ini kullanarak Contosoyüklemelerini kapsayıcısında Planning2015 adındaki blob 'u alır ve bu blobu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="cd18c-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="cd18c-118">Komut, ContosoPlanning adındaki dosyayı Planning2015 olarak yükler.</span><span class="sxs-lookup"><span data-stu-id="cd18c-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="cd18c-119">Bu komut *Force* parametresini belirtmez.</span><span class="sxs-lookup"><span data-stu-id="cd18c-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="cd18c-120">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cd18c-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="cd18c-121">Komutu onaylamıyorsanız cmdlet var olan bloonun üzerine yazar.</span><span class="sxs-lookup"><span data-stu-id="cd18c-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="cd18c-122">Örnek 4: ardışık düzeni kullanarak bir dosyayı kapsayıcıya yükleme</span><span class="sxs-lookup"><span data-stu-id="cd18c-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="cd18c-123">Bu komut **Get-AzStorageContainer** cmdlet 'Ini kullanarak contosoupload dizesiyle başlayan kapsayıcıyı alır ve o blob 'u geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="cd18c-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="cd18c-124">Komut, ContosoPlanning adındaki dosyayı Planning2015 olarak yükler.</span><span class="sxs-lookup"><span data-stu-id="cd18c-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="cd18c-125">Örnek 5: PremiumPageBlobTier as</span><span class="sxs-lookup"><span data-stu-id="cd18c-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="cd18c-126">İlk komut, blob için meta veriler içeren bir karma tablo oluşturur ve bu karma tabloyu $Metadata değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cd18c-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="cd18c-127">İkinci komut, ContosoPlanning adlı dosyayı Contosoyüklemeler adlı kapsayıcıya yükler.</span><span class="sxs-lookup"><span data-stu-id="cd18c-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="cd18c-128">Blob, $Metadata depolanan meta verileri içerir ve PremiumPageBlobTier olarak.</span><span class="sxs-lookup"><span data-stu-id="cd18c-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="cd18c-129">Örnek 6: belirtilen blob özellikleriyle blob 'a dosya yükleme</span><span class="sxs-lookup"><span data-stu-id="cd18c-129">Example 6: Upload a file to blob with specified blob properties</span></span>
```
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Properties @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="}
```

<span data-ttu-id="cd18c-130">Bu komut, ContosoPlanning adlı dosyayı, contoso, belirtilen blob özellikleriyle karşıya yüklemeler adlı kapsayıcıya yükler.</span><span class="sxs-lookup"><span data-stu-id="cd18c-130">This command  uploads the file that is named ContosoPlanning to the container named ContosoUploads with specified blob properties.</span></span>

## <span data-ttu-id="cd18c-131">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd18c-131">PARAMETERS</span></span>

### <span data-ttu-id="cd18c-132">-Iş</span><span class="sxs-lookup"><span data-stu-id="cd18c-132">-AsJob</span></span>
<span data-ttu-id="cd18c-133">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="cd18c-133">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="cd18c-134">-Blob</span><span class="sxs-lookup"><span data-stu-id="cd18c-134">-Blob</span></span>
<span data-ttu-id="cd18c-135">Blob 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd18c-135">Specifies the name of a blob.</span></span>
<span data-ttu-id="cd18c-136">Bu cmdlet, bu parametrenin belirttiği Azure depolama blob blob 'ine bir dosya yükler.</span><span class="sxs-lookup"><span data-stu-id="cd18c-136">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="cd18c-137">-BlobType</span><span class="sxs-lookup"><span data-stu-id="cd18c-137">-BlobType</span></span>
<span data-ttu-id="cd18c-138">Bu cmdlet 'in karşıya yükleolduğu blob 'un türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd18c-138">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="cd18c-139">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="cd18c-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cd18c-140">Engellenebilir</span><span class="sxs-lookup"><span data-stu-id="cd18c-140">Block</span></span>
- <span data-ttu-id="cd18c-141">Sayfa varsayılan değer engelle değeridir.</span><span class="sxs-lookup"><span data-stu-id="cd18c-141">Page The default value is Block.</span></span>

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

### <span data-ttu-id="cd18c-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cd18c-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cd18c-143">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd18c-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cd18c-144">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="cd18c-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cd18c-145">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="cd18c-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cd18c-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="cd18c-146">-CloudBlob</span></span>
<span data-ttu-id="cd18c-147">**Cloudblob** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd18c-147">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="cd18c-148">**Cloudblob** nesnesi edinmek için Get-AzStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cd18c-148">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="cd18c-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="cd18c-149">-CloudBlobContainer</span></span>
<span data-ttu-id="cd18c-150">Azure depolama Istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd18c-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="cd18c-151">Bu cmdlet, bu parametrenin belirttiği kapsayıcıdaki bir blob 'a içerik yükler.</span><span class="sxs-lookup"><span data-stu-id="cd18c-151">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="cd18c-152">**Cloudblobcontainer** nesnesi edinmek için Get-AzStorageContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cd18c-152">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="cd18c-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cd18c-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cd18c-154">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd18c-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cd18c-155">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd18c-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cd18c-156">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="cd18c-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cd18c-157">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="cd18c-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cd18c-158">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="cd18c-158">The default value is 10.</span></span>

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

### <span data-ttu-id="cd18c-159">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="cd18c-159">-Container</span></span>
<span data-ttu-id="cd18c-160">Kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd18c-160">Specifies the name of a container.</span></span>
<span data-ttu-id="cd18c-161">Bu cmdlet, bu parametrenin belirttiği kapsayıcıdaki bir blob 'a dosya yükler.</span><span class="sxs-lookup"><span data-stu-id="cd18c-161">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="cd18c-162">-Context</span><span class="sxs-lookup"><span data-stu-id="cd18c-162">-Context</span></span>
<span data-ttu-id="cd18c-163">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd18c-163">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cd18c-164">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cd18c-164">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="cd18c-165">Okuma izni olmadan SAS belirtecinden oluşturulan bir depolama bağlamını kullanmak için, Add-Force parametresine sahip Check blob 'unu atlayın.</span><span class="sxs-lookup"><span data-stu-id="cd18c-165">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existance.</span></span>

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

### <span data-ttu-id="cd18c-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd18c-166">-DefaultProfile</span></span>
<span data-ttu-id="cd18c-167">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cd18c-167">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd18c-168">-Dosya</span><span class="sxs-lookup"><span data-stu-id="cd18c-168">-File</span></span>
<span data-ttu-id="cd18c-169">Dosya BLOB içeriği olarak yüklenecek bir dosya yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd18c-169">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="cd18c-170">-Force</span><span class="sxs-lookup"><span data-stu-id="cd18c-170">-Force</span></span>
<span data-ttu-id="cd18c-171">Bu cmdlet 'in var olan bir bloonun onay istemeden üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd18c-171">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="cd18c-172">-Metadata</span><span class="sxs-lookup"><span data-stu-id="cd18c-172">-Metadata</span></span>
<span data-ttu-id="cd18c-173">Karşıya yüklenen blob için meta verileri belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd18c-173">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="cd18c-174">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="cd18c-174">-PremiumPageBlobTier</span></span>
<span data-ttu-id="cd18c-175">Sayfa blob katmanı</span><span class="sxs-lookup"><span data-stu-id="cd18c-175">Page Blob Tier</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd18c-176">-Özellikler</span><span class="sxs-lookup"><span data-stu-id="cd18c-176">-Properties</span></span>
<span data-ttu-id="cd18c-177">Karşıya yüklenen blob 'un özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd18c-177">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="cd18c-178">Desteklenen Özellikler: CacheControl, ContentDisposition, Contentenkodlama, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="cd18c-178">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="cd18c-179">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cd18c-179">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cd18c-180">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd18c-180">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="cd18c-181">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="cd18c-181">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="cd18c-182">-Onay</span><span class="sxs-lookup"><span data-stu-id="cd18c-182">-Confirm</span></span>
<span data-ttu-id="cd18c-183">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cd18c-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd18c-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd18c-184">-WhatIf</span></span>
<span data-ttu-id="cd18c-185">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd18c-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd18c-186">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cd18c-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd18c-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd18c-187">CommonParameters</span></span>
<span data-ttu-id="cd18c-188">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd18c-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd18c-189">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd18c-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd18c-190">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd18c-190">INPUTS</span></span>

### <span data-ttu-id="cd18c-191">System. String</span><span class="sxs-lookup"><span data-stu-id="cd18c-191">System.String</span></span>

### <span data-ttu-id="cd18c-192">Microsoft. Windowsazde. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="cd18c-192">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="cd18c-193">Microsoft. Windowsazde. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="cd18c-193">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="cd18c-194">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="cd18c-194">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cd18c-195">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd18c-195">OUTPUTS</span></span>

### <span data-ttu-id="cd18c-196">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cd18c-196">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="cd18c-197">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd18c-197">NOTES</span></span>

## <span data-ttu-id="cd18c-198">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd18c-198">RELATED LINKS</span></span>

[<span data-ttu-id="cd18c-199">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cd18c-199">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="cd18c-200">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cd18c-200">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="cd18c-201">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cd18c-201">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
