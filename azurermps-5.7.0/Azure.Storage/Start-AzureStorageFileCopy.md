---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/start-azurestoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageFileCopy.md
ms.openlocfilehash: 47129dfd409ad72aa250ed78ce4b61d1463b9390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595136"
---
# <span data-ttu-id="1c683-101">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1c683-101">Start-AzureStorageFileCopy</span></span>

## <span data-ttu-id="1c683-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c683-102">SYNOPSIS</span></span>
<span data-ttu-id="1c683-103">Kaynak dosyayı kopyalamaya başlar.</span><span class="sxs-lookup"><span data-stu-id="1c683-103">Starts to copy a source file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c683-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1c683-104">SYNTAX</span></span>

### <span data-ttu-id="1c683-105">Öğesini</span><span class="sxs-lookup"><span data-stu-id="1c683-105">ContainerName</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c683-106">Containerınstance</span><span class="sxs-lookup"><span data-stu-id="1c683-106">ContainerInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c683-107">Blobınstancefilepath</span><span class="sxs-lookup"><span data-stu-id="1c683-107">BlobInstanceFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c683-108">Blobınstancefileınstance</span><span class="sxs-lookup"><span data-stu-id="1c683-108">BlobInstanceFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c683-109">PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="1c683-109">ShareName</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c683-110">Shareınstance</span><span class="sxs-lookup"><span data-stu-id="1c683-110">ShareInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c683-111">Fileınstancetofilepath</span><span class="sxs-lookup"><span data-stu-id="1c683-111">FileInstanceToFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c683-112">Fileınstancetofileınstance</span><span class="sxs-lookup"><span data-stu-id="1c683-112">FileInstanceToFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c683-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="1c683-113">UriToFilePath</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c683-114">Uritofileınstance</span><span class="sxs-lookup"><span data-stu-id="1c683-114">UriToFileInstance</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c683-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="1c683-115">DESCRIPTION</span></span>
<span data-ttu-id="1c683-116">**Start-AzureStorageFileCopy** cmdlet 'i kaynak dosyayı hedef dosyaya kopyalamaya başlar.</span><span class="sxs-lookup"><span data-stu-id="1c683-116">The **Start-AzureStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="1c683-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1c683-117">EXAMPLES</span></span>

### <span data-ttu-id="1c683-118">Örnek 1: paylaşım adını ve dosya adını kullanarak dosyadan dosyaya kopyalama işlemi başlatın</span><span class="sxs-lookup"><span data-stu-id="1c683-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="1c683-119">Bu komut dosyadan dosyaya kopyalama işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="1c683-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="1c683-120">Komut, paylaşım adını ve dosya adını belirtir</span><span class="sxs-lookup"><span data-stu-id="1c683-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="1c683-121">Örnek 2: kapsayıcı adını ve BLOB adını kullanarak blob 'dan dosyaya kopyalama işlemini Başlat</span><span class="sxs-lookup"><span data-stu-id="1c683-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="1c683-122">Bu komut blob 'dan dosyaya kopyalama işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="1c683-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="1c683-123">Komut kapsayıcı adını ve BLOB adını belirtir</span><span class="sxs-lookup"><span data-stu-id="1c683-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="1c683-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1c683-124">PARAMETERS</span></span>

### <span data-ttu-id="1c683-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="1c683-125">-AbsoluteUri</span></span>
<span data-ttu-id="1c683-126">Kaynak dosyanın URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c683-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="1c683-127">Kaynak konumu kimlik bilgisi gerektiriyorsa, bir tane sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1c683-127">If the source location requires a credential, you must provide one.</span></span>

```yaml
Type: String
Parameter Sets: UriToFilePath, UriToFileInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c683-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1c683-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1c683-129">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c683-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1c683-130">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="1c683-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1c683-131">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="1c683-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1c683-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1c683-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1c683-133">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c683-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1c683-134">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1c683-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1c683-135">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="1c683-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1c683-136">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="1c683-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1c683-137">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="1c683-137">The default value is 10.</span></span>

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

### <span data-ttu-id="1c683-138">-Context</span><span class="sxs-lookup"><span data-stu-id="1c683-138">-Context</span></span>
<span data-ttu-id="1c683-139">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c683-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="1c683-140">Bağlam almak için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1c683-140">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerName, ShareName
Aliases: SrcContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c683-141">-DestContext</span><span class="sxs-lookup"><span data-stu-id="1c683-141">-DestContext</span></span>
<span data-ttu-id="1c683-142">Hedefin Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c683-142">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="1c683-143">Bağlam almak için, **New-AzureStorageContext** kullanın.</span><span class="sxs-lookup"><span data-stu-id="1c683-143">To obtain a context, use **New-AzureStorageContext**.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c683-144">-DestFile</span><span class="sxs-lookup"><span data-stu-id="1c683-144">-DestFile</span></span>
<span data-ttu-id="1c683-145">Bir **Cloudfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c683-145">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="1c683-146">Get-AzureStorageFile cmdlet 'ini kullanarak bir bulut dosyası oluşturabilir veya bir tane edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1c683-146">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c683-147">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="1c683-147">-DestFilePath</span></span>
<span data-ttu-id="1c683-148">Hedef paylaşım ile ilgili hedef dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c683-148">Specifies the path of the destination file relative to the destination share.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c683-149">-Destpaylaşımadı</span><span class="sxs-lookup"><span data-stu-id="1c683-149">-DestShareName</span></span>
<span data-ttu-id="1c683-150">Hedef paylaşımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c683-150">Specifies the name of the destination share.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c683-151">-Force</span><span class="sxs-lookup"><span data-stu-id="1c683-151">-Force</span></span>
<span data-ttu-id="1c683-152">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="1c683-152">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1c683-153">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1c683-153">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1c683-154">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c683-154">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="1c683-155">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="1c683-155">-SrcBlob</span></span>
<span data-ttu-id="1c683-156">**Cloudblob** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c683-156">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="1c683-157">Get-AzureStorageBlob cmdlet 'ini kullanarak bir bulut blob oluşturabilir veya bir tane edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1c683-157">You can create a cloud blob or obtain one by using the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c683-158">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="1c683-158">-SrcBlobName</span></span>
<span data-ttu-id="1c683-159">Kaynak bloonun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c683-159">Specifies the name of the source blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, ContainerInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c683-160">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="1c683-160">-SrcContainer</span></span>
<span data-ttu-id="1c683-161">Bulut blob kapsayıcı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c683-161">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="1c683-162">Bulut blob kapsayıcı nesnesi oluşturabilir veya Get-AzureStorageContainer cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1c683-162">You can create cloud blob container object or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c683-163">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="1c683-163">-SrcContainerName</span></span>
<span data-ttu-id="1c683-164">Kaynak kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c683-164">Specifies the name of the source container.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c683-165">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="1c683-165">-SrcFile</span></span>
<span data-ttu-id="1c683-166">Bir **Cloudfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c683-166">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="1c683-167">**Get-AzureStorageFile** kullanarak bir bulut dosyası oluşturabilir veya bir tane edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1c683-167">You can create a cloud file or obtain one by using **Get-AzureStorageFile**.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c683-168">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="1c683-168">-SrcFilePath</span></span>
<span data-ttu-id="1c683-169">Kaynak dosyanın veya kaynak paylaşımın göreli yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c683-169">Specifies the path of the source file relative to the source directory or source share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, ShareInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c683-170">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="1c683-170">-SrcShare</span></span>
<span data-ttu-id="1c683-171">Bulut dosya paylaşımı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c683-171">Specifies a cloud file share object.</span></span>
<span data-ttu-id="1c683-172">Get-AzureStorageShare cmdlet 'ini kullanarak bir bulut dosya paylaşımı oluşturabilir veya bir tane edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1c683-172">You can create a cloud file share or obtain one by using the Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: ShareInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c683-173">-Srcpaylaşımadı</span><span class="sxs-lookup"><span data-stu-id="1c683-173">-SrcShareName</span></span>
<span data-ttu-id="1c683-174">Kaynak paylaşımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c683-174">Specifies the name of the source share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c683-175">-Onay</span><span class="sxs-lookup"><span data-stu-id="1c683-175">-Confirm</span></span>
<span data-ttu-id="1c683-176">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1c683-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c683-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c683-177">-WhatIf</span></span>
<span data-ttu-id="1c683-178">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c683-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c683-179">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1c683-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c683-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c683-180">CommonParameters</span></span>
<span data-ttu-id="1c683-181">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1c683-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c683-182">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c683-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c683-183">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1c683-183">INPUTS</span></span>

### <span data-ttu-id="1c683-184">CloudBlob</span><span class="sxs-lookup"><span data-stu-id="1c683-184">CloudBlob</span></span>

<span data-ttu-id="1c683-185">' SrcBlob ' parametresi ardışık düzenin ' CloudBlob ' türünün değerini kabul ediyor</span><span class="sxs-lookup"><span data-stu-id="1c683-185">Parameter 'SrcBlob' accepts value of type 'CloudBlob' from the pipeline</span></span>

### <span data-ttu-id="1c683-186">CloudFile</span><span class="sxs-lookup"><span data-stu-id="1c683-186">CloudFile</span></span>

<span data-ttu-id="1c683-187">' SrcFile ' parametresi ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="1c683-187">Parameter 'SrcFile' accepts value of type 'CloudFile' from the pipeline</span></span>

## <span data-ttu-id="1c683-188">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1c683-188">OUTPUTS</span></span>

## <span data-ttu-id="1c683-189">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1c683-189">NOTES</span></span>

## <span data-ttu-id="1c683-190">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1c683-190">RELATED LINKS</span></span>

[<span data-ttu-id="1c683-191">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="1c683-191">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="1c683-192">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1c683-192">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="1c683-193">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="1c683-193">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="1c683-194">Get-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="1c683-194">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="1c683-195">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="1c683-195">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="1c683-196">Stop-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1c683-196">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)