---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
ms.openlocfilehash: 578c32a27f53f586ec8a8013533e42928df48d30
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266731"
---
# <span data-ttu-id="ccaf3-101">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ccaf3-101">Start-AzStorageFileCopy</span></span>

## <span data-ttu-id="ccaf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccaf3-102">SYNOPSIS</span></span>
<span data-ttu-id="ccaf3-103">Kaynak dosyayı kopyalamaya başlar.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="ccaf3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ccaf3-104">SYNTAX</span></span>

### <span data-ttu-id="ccaf3-105">Öğesini</span><span class="sxs-lookup"><span data-stu-id="ccaf3-105">ContainerName</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ccaf3-106">Containerınstance</span><span class="sxs-lookup"><span data-stu-id="ccaf3-106">ContainerInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccaf3-107">Blobınstancefilepath</span><span class="sxs-lookup"><span data-stu-id="ccaf3-107">BlobInstanceFilePath</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccaf3-108">Blobınstancefileınstance</span><span class="sxs-lookup"><span data-stu-id="ccaf3-108">BlobInstanceFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccaf3-109">PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="ccaf3-109">ShareName</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ccaf3-110">Shareınstance</span><span class="sxs-lookup"><span data-stu-id="ccaf3-110">ShareInstance</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccaf3-111">Fileınstancetofilepath</span><span class="sxs-lookup"><span data-stu-id="ccaf3-111">FileInstanceToFilePath</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccaf3-112">Fileınstancetofileınstance</span><span class="sxs-lookup"><span data-stu-id="ccaf3-112">FileInstanceToFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccaf3-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="ccaf3-113">UriToFilePath</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccaf3-114">Uritofileınstance</span><span class="sxs-lookup"><span data-stu-id="ccaf3-114">UriToFileInstance</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccaf3-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="ccaf3-115">DESCRIPTION</span></span>
<span data-ttu-id="ccaf3-116">**Start-AzStorageFileCopy** cmdlet 'i kaynak dosyayı hedef dosyaya kopyalamaya başlar.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-116">The **Start-AzStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="ccaf3-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ccaf3-117">EXAMPLES</span></span>

### <span data-ttu-id="ccaf3-118">Örnek 1: paylaşım adını ve dosya adını kullanarak dosyadan dosyaya kopyalama işlemi başlatın</span><span class="sxs-lookup"><span data-stu-id="ccaf3-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="ccaf3-119">Bu komut dosyadan dosyaya kopyalama işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="ccaf3-120">Komut, paylaşım adını ve dosya adını belirtir</span><span class="sxs-lookup"><span data-stu-id="ccaf3-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="ccaf3-121">Örnek 2: kapsayıcı adını ve BLOB adını kullanarak blob 'dan dosyaya kopyalama işlemini Başlat</span><span class="sxs-lookup"><span data-stu-id="ccaf3-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="ccaf3-122">Bu komut blob 'dan dosyaya kopyalama işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="ccaf3-123">Komut kapsayıcı adını ve BLOB adını belirtir</span><span class="sxs-lookup"><span data-stu-id="ccaf3-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="ccaf3-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ccaf3-124">PARAMETERS</span></span>

### <span data-ttu-id="ccaf3-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="ccaf3-125">-AbsoluteUri</span></span>
<span data-ttu-id="ccaf3-126">Kaynak dosyanın URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="ccaf3-127">Kaynak konumu kimlik bilgisi gerektiriyorsa, bir tane sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-127">If the source location requires a credential, you must provide one.</span></span>

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

### <span data-ttu-id="ccaf3-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ccaf3-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ccaf3-129">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ccaf3-130">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ccaf3-131">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ccaf3-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ccaf3-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ccaf3-133">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ccaf3-134">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ccaf3-135">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ccaf3-136">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ccaf3-137">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-137">The default value is 10.</span></span>

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

### <span data-ttu-id="ccaf3-138">-Context</span><span class="sxs-lookup"><span data-stu-id="ccaf3-138">-Context</span></span>
<span data-ttu-id="ccaf3-139">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="ccaf3-140">Bağlam almak için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-140">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ccaf3-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccaf3-141">-DefaultProfile</span></span>
<span data-ttu-id="ccaf3-142">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccaf3-143">-DestContext</span><span class="sxs-lookup"><span data-stu-id="ccaf3-143">-DestContext</span></span>
<span data-ttu-id="ccaf3-144">Hedefin Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="ccaf3-145">Bağlam almak için, **New-AzStorageContext** kullanın.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-145">To obtain a context, use **New-AzStorageContext**.</span></span>

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

### <span data-ttu-id="ccaf3-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="ccaf3-146">-DestFile</span></span>
<span data-ttu-id="ccaf3-147">Bir **Cloudfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="ccaf3-148">Get-AzStorageFile cmdlet 'ini kullanarak bir bulut dosyası oluşturabilir veya bir tane edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-148">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaf3-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="ccaf3-149">-DestFilePath</span></span>
<span data-ttu-id="ccaf3-150">Hedef paylaşım ile ilgili hedef dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-150">Specifies the path of the destination file relative to the destination share.</span></span>

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

### <span data-ttu-id="ccaf3-151">-Destpaylaşımadı</span><span class="sxs-lookup"><span data-stu-id="ccaf3-151">-DestShareName</span></span>
<span data-ttu-id="ccaf3-152">Hedef paylaşımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-152">Specifies the name of the destination share.</span></span>

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

### <span data-ttu-id="ccaf3-153">-Force</span><span class="sxs-lookup"><span data-stu-id="ccaf3-153">-Force</span></span>
<span data-ttu-id="ccaf3-154">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ccaf3-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ccaf3-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ccaf3-156">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="ccaf3-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="ccaf3-157">-SrcBlob</span></span>
<span data-ttu-id="ccaf3-158">**Cloudblob** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="ccaf3-159">Get-AzStorageBlob cmdlet 'ini kullanarak bir bulut blob oluşturabilir veya bir tane edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-159">You can create a cloud blob or obtain one by using the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccaf3-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="ccaf3-160">-SrcBlobName</span></span>
<span data-ttu-id="ccaf3-161">Kaynak bloonun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-161">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="ccaf3-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="ccaf3-162">-SrcContainer</span></span>
<span data-ttu-id="ccaf3-163">Bulut blob kapsayıcı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="ccaf3-164">Bulut blob kapsayıcı nesnesi oluşturabilir veya Get-AzStorageContainer cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-164">You can create cloud blob container object or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaf3-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="ccaf3-165">-SrcContainerName</span></span>
<span data-ttu-id="ccaf3-166">Kaynak kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-166">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="ccaf3-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="ccaf3-167">-SrcFile</span></span>
<span data-ttu-id="ccaf3-168">Bir **Cloudfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="ccaf3-169">**Get-AzStorageFile** kullanarak bir bulut dosyası oluşturabilir veya bir tane edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-169">You can create a cloud file or obtain one by using **Get-AzStorageFile**.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases: CloudFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccaf3-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="ccaf3-170">-SrcFilePath</span></span>
<span data-ttu-id="ccaf3-171">Kaynak dosyanın veya kaynak paylaşımın göreli yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

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

### <span data-ttu-id="ccaf3-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="ccaf3-172">-SrcShare</span></span>
<span data-ttu-id="ccaf3-173">Bulut dosya paylaşımı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="ccaf3-174">Get-AzStorageShare cmdlet 'ini kullanarak bir bulut dosya paylaşımı oluşturabilir veya bir tane edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-174">You can create a cloud file share or obtain one by using the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: CloudFileShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccaf3-175">-Srcpaylaşımadı</span><span class="sxs-lookup"><span data-stu-id="ccaf3-175">-SrcShareName</span></span>
<span data-ttu-id="ccaf3-176">Kaynak paylaşımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-176">Specifies the name of the source share.</span></span>

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

### <span data-ttu-id="ccaf3-177">-Onay</span><span class="sxs-lookup"><span data-stu-id="ccaf3-177">-Confirm</span></span>
<span data-ttu-id="ccaf3-178">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccaf3-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccaf3-179">-WhatIf</span></span>
<span data-ttu-id="ccaf3-180">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccaf3-181">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccaf3-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccaf3-182">CommonParameters</span></span>
<span data-ttu-id="ccaf3-183">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccaf3-184">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccaf3-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccaf3-185">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ccaf3-185">INPUTS</span></span>

### <span data-ttu-id="ccaf3-186">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ccaf3-186">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="ccaf3-187">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="ccaf3-187">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="ccaf3-188">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="ccaf3-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ccaf3-189">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ccaf3-189">OUTPUTS</span></span>

### <span data-ttu-id="ccaf3-190">Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="ccaf3-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="ccaf3-191">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ccaf3-191">NOTES</span></span>

## <span data-ttu-id="ccaf3-192">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ccaf3-192">RELATED LINKS</span></span>

[<span data-ttu-id="ccaf3-193">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ccaf3-193">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="ccaf3-194">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ccaf3-194">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="ccaf3-195">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="ccaf3-195">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="ccaf3-196">Get-Azstorages,</span><span class="sxs-lookup"><span data-stu-id="ccaf3-196">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="ccaf3-197">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="ccaf3-197">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="ccaf3-198">Dur-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ccaf3-198">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
