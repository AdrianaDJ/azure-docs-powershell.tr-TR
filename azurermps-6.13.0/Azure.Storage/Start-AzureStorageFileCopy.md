---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/start-azurestoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageFileCopy.md
ms.openlocfilehash: c5e071ddb5316f223260d3e6f239df4e75612332
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591489"
---
# <span data-ttu-id="9ebdd-101">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="9ebdd-101">Start-AzureStorageFileCopy</span></span>

## <span data-ttu-id="9ebdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ebdd-102">SYNOPSIS</span></span>
<span data-ttu-id="9ebdd-103">Kaynak dosyayı kopyalamaya başlar.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-103">Starts to copy a source file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ebdd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ebdd-104">SYNTAX</span></span>

### <span data-ttu-id="9ebdd-105">Öğesini</span><span class="sxs-lookup"><span data-stu-id="9ebdd-105">ContainerName</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ebdd-106">Containerınstance</span><span class="sxs-lookup"><span data-stu-id="9ebdd-106">ContainerInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ebdd-107">Blobınstancefilepath</span><span class="sxs-lookup"><span data-stu-id="9ebdd-107">BlobInstanceFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ebdd-108">Blobınstancefileınstance</span><span class="sxs-lookup"><span data-stu-id="9ebdd-108">BlobInstanceFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ebdd-109">PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="9ebdd-109">ShareName</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ebdd-110">Shareınstance</span><span class="sxs-lookup"><span data-stu-id="9ebdd-110">ShareInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ebdd-111">Fileınstancetofilepath</span><span class="sxs-lookup"><span data-stu-id="9ebdd-111">FileInstanceToFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ebdd-112">Fileınstancetofileınstance</span><span class="sxs-lookup"><span data-stu-id="9ebdd-112">FileInstanceToFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ebdd-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="9ebdd-113">UriToFilePath</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ebdd-114">Uritofileınstance</span><span class="sxs-lookup"><span data-stu-id="9ebdd-114">UriToFileInstance</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ebdd-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ebdd-115">DESCRIPTION</span></span>
<span data-ttu-id="9ebdd-116">**Start-AzureStorageFileCopy** cmdlet 'i kaynak dosyayı hedef dosyaya kopyalamaya başlar.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-116">The **Start-AzureStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="9ebdd-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ebdd-117">EXAMPLES</span></span>

### <span data-ttu-id="9ebdd-118">Örnek 1: paylaşım adını ve dosya adını kullanarak dosyadan dosyaya kopyalama işlemi başlatın</span><span class="sxs-lookup"><span data-stu-id="9ebdd-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="9ebdd-119">Bu komut dosyadan dosyaya kopyalama işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="9ebdd-120">Komut, paylaşım adını ve dosya adını belirtir</span><span class="sxs-lookup"><span data-stu-id="9ebdd-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="9ebdd-121">Örnek 2: kapsayıcı adını ve BLOB adını kullanarak blob 'dan dosyaya kopyalama işlemini Başlat</span><span class="sxs-lookup"><span data-stu-id="9ebdd-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="9ebdd-122">Bu komut blob 'dan dosyaya kopyalama işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="9ebdd-123">Komut kapsayıcı adını ve BLOB adını belirtir</span><span class="sxs-lookup"><span data-stu-id="9ebdd-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="9ebdd-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ebdd-124">PARAMETERS</span></span>

### <span data-ttu-id="9ebdd-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="9ebdd-125">-AbsoluteUri</span></span>
<span data-ttu-id="9ebdd-126">Kaynak dosyanın URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="9ebdd-127">Kaynak konumu kimlik bilgisi gerektiriyorsa, bir tane sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-127">If the source location requires a credential, you must provide one.</span></span>

```yaml
Type: System.String
Parameter Sets: UriToFilePath, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ebdd-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9ebdd-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9ebdd-129">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9ebdd-130">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9ebdd-131">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9ebdd-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9ebdd-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9ebdd-133">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9ebdd-134">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9ebdd-135">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9ebdd-136">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9ebdd-137">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-137">The default value is 10.</span></span>

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

### <span data-ttu-id="9ebdd-138">-Context</span><span class="sxs-lookup"><span data-stu-id="9ebdd-138">-Context</span></span>
<span data-ttu-id="9ebdd-139">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="9ebdd-140">Bağlam almak için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-140">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, ShareName
Aliases: SrcContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ebdd-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ebdd-141">-DefaultProfile</span></span>
<span data-ttu-id="9ebdd-142">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ebdd-143">-DestContext</span><span class="sxs-lookup"><span data-stu-id="9ebdd-143">-DestContext</span></span>
<span data-ttu-id="9ebdd-144">Hedefin Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="9ebdd-145">Bağlam almak için, **New-AzureStorageContext** kullanın.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-145">To obtain a context, use **New-AzureStorageContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ebdd-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="9ebdd-146">-DestFile</span></span>
<span data-ttu-id="9ebdd-147">Bir **Cloudfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="9ebdd-148">Get-AzureStorageFile cmdlet 'ini kullanarak bir bulut dosyası oluşturabilir veya bir tane edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-148">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ebdd-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="9ebdd-149">-DestFilePath</span></span>
<span data-ttu-id="9ebdd-150">Hedef paylaşım ile ilgili hedef dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-150">Specifies the path of the destination file relative to the destination share.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ebdd-151">-Destpaylaşımadı</span><span class="sxs-lookup"><span data-stu-id="9ebdd-151">-DestShareName</span></span>
<span data-ttu-id="9ebdd-152">Hedef paylaşımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-152">Specifies the name of the destination share.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ebdd-153">-Force</span><span class="sxs-lookup"><span data-stu-id="9ebdd-153">-Force</span></span>
<span data-ttu-id="9ebdd-154">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9ebdd-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9ebdd-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9ebdd-156">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="9ebdd-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="9ebdd-157">-SrcBlob</span></span>
<span data-ttu-id="9ebdd-158">**Cloudblob** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="9ebdd-159">Get-AzureStorageBlob cmdlet 'ini kullanarak bir bulut blob oluşturabilir veya bir tane edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-159">You can create a cloud blob or obtain one by using the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ebdd-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="9ebdd-160">-SrcBlobName</span></span>
<span data-ttu-id="9ebdd-161">Kaynak bloonun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-161">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ebdd-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="9ebdd-162">-SrcContainer</span></span>
<span data-ttu-id="9ebdd-163">Bulut blob kapsayıcı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="9ebdd-164">Bulut blob kapsayıcı nesnesi oluşturabilir veya Get-AzureStorageContainer cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-164">You can create cloud blob container object or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ebdd-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="9ebdd-165">-SrcContainerName</span></span>
<span data-ttu-id="9ebdd-166">Kaynak kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-166">Specifies the name of the source container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ebdd-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="9ebdd-167">-SrcFile</span></span>
<span data-ttu-id="9ebdd-168">Bir **Cloudfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="9ebdd-169">**Get-AzureStorageFile** kullanarak bir bulut dosyası oluşturabilir veya bir tane edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-169">You can create a cloud file or obtain one by using **Get-AzureStorageFile**.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ebdd-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="9ebdd-170">-SrcFilePath</span></span>
<span data-ttu-id="9ebdd-171">Kaynak dosyanın veya kaynak paylaşımın göreli yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ebdd-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="9ebdd-172">-SrcShare</span></span>
<span data-ttu-id="9ebdd-173">Bulut dosya paylaşımı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="9ebdd-174">Get-AzureStorageShare cmdlet 'ini kullanarak bir bulut dosya paylaşımı oluşturabilir veya bir tane edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-174">You can create a cloud file share or obtain one by using the Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ebdd-175">-Srcpaylaşımadı</span><span class="sxs-lookup"><span data-stu-id="9ebdd-175">-SrcShareName</span></span>
<span data-ttu-id="9ebdd-176">Kaynak paylaşımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-176">Specifies the name of the source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ebdd-177">-Onay</span><span class="sxs-lookup"><span data-stu-id="9ebdd-177">-Confirm</span></span>
<span data-ttu-id="9ebdd-178">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ebdd-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ebdd-179">-WhatIf</span></span>
<span data-ttu-id="9ebdd-180">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ebdd-181">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ebdd-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ebdd-182">CommonParameters</span></span>
<span data-ttu-id="9ebdd-183">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ebdd-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ebdd-184">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ebdd-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ebdd-185">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ebdd-185">INPUTS</span></span>

### <span data-ttu-id="9ebdd-186">Microsoft. Windowsazde. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="9ebdd-186">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="9ebdd-187">Microsoft. Windowsazde. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="9ebdd-187">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="9ebdd-188">Parametreler: SrcFile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9ebdd-188">Parameters: SrcFile (ByValue)</span></span>

### <span data-ttu-id="9ebdd-189">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="9ebdd-189">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9ebdd-190">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ebdd-190">OUTPUTS</span></span>

### <span data-ttu-id="9ebdd-191">System. void</span><span class="sxs-lookup"><span data-stu-id="9ebdd-191">System.Void</span></span>

## <span data-ttu-id="9ebdd-192">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ebdd-192">NOTES</span></span>

## <span data-ttu-id="9ebdd-193">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ebdd-193">RELATED LINKS</span></span>

[<span data-ttu-id="9ebdd-194">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9ebdd-194">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="9ebdd-195">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9ebdd-195">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="9ebdd-196">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="9ebdd-196">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="9ebdd-197">Get-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="9ebdd-197">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="9ebdd-198">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="9ebdd-198">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="9ebdd-199">Stop-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="9ebdd-199">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)