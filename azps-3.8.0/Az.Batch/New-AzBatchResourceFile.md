---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097917"
---
# <span data-ttu-id="90650-101">New-AzBatchResourceFile</span><span class="sxs-lookup"><span data-stu-id="90650-101">New-AzBatchResourceFile</span></span>

## <span data-ttu-id="90650-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90650-102">SYNOPSIS</span></span>
<span data-ttu-id="90650-103">Tarafından kullanım için bir kaynak dosyası oluşturur `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="90650-103">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="90650-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90650-104">SYNTAX</span></span>

### <span data-ttu-id="90650-105">HttpUrl (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="90650-105">HttpUrl (Default)</span></span>
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90650-106">StorageContainerUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="90650-106">StorageContainerUrl</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90650-107">AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="90650-107">AutoStorageContainerName</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90650-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="90650-108">DESCRIPTION</span></span>
<span data-ttu-id="90650-109">Tarafından kullanım için bir kaynak dosyası oluşturur `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="90650-109">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="90650-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90650-110">EXAMPLES</span></span>

### <span data-ttu-id="90650-111">Örnek 1: tek bir dosyaya işaret eden bir HTTP URL 'sinden kaynak dosyası oluşturma</span><span class="sxs-lookup"><span data-stu-id="90650-111">Example 1: Create a resource file from an HTTP URL pointing at a single file</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="90650-112">`PSResourceFile`Http url 'sine başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="90650-112">Creates a `PSResourceFile` referencing an HTTP url.</span></span>

### <span data-ttu-id="90650-113">Örnek 2: Azure depolama kapsayıcısı URL 'sinden kaynak dosyası oluşturma</span><span class="sxs-lookup"><span data-stu-id="90650-113">Example 2: Create a resource file from an Azure Storage container URL</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="90650-114">`PSResourceFile`Azure depolama kapsayıcısı URL 'sine başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="90650-114">Creates a `PSResourceFile` referencing an Azure Storage container URL.</span></span> <span data-ttu-id="90650-115">Kapsayıcıdaki tüm dosyalar belirtilen klasöre indirilir.</span><span class="sxs-lookup"><span data-stu-id="90650-115">All files in the container will be downloaded to the specified folder.</span></span>

### <span data-ttu-id="90650-116">Örnek 3: otomatik depolama kapsayıcısı adından kaynak dosyası oluşturma</span><span class="sxs-lookup"><span data-stu-id="90650-116">Example 3: Create a resource file from an Auto Storage container name</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="90650-117">Bir `PSResourceFile` Otomatik depolama kapsayıcısı adına başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="90650-117">Creates a `PSResourceFile` referencing an Auto Storage container name.</span></span> <span data-ttu-id="90650-118">Kapsayıcıdaki tüm dosyalar belirtilen klasöre indirilir.</span><span class="sxs-lookup"><span data-stu-id="90650-118">All files in the container will be downloaded to the specified folder.</span></span>

## <span data-ttu-id="90650-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90650-119">PARAMETERS</span></span>

### <span data-ttu-id="90650-120">-AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="90650-120">-AutoStorageContainerName</span></span>
<span data-ttu-id="90650-121">Otomatik depolama hesabındaki depolama kapsayıcısı adı.</span><span class="sxs-lookup"><span data-stu-id="90650-121">The storage container name in the auto storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AutoStorageContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90650-122">-BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="90650-122">-BlobPrefix</span></span>
<span data-ttu-id="90650-123">Bir Azure depolama kapsayıcısından blob indirme sırasında kullanılacak blob önekini alır.</span><span class="sxs-lookup"><span data-stu-id="90650-123">Gets the blob prefix to use when downloading blobs from an Azure Storage container.</span></span>
<span data-ttu-id="90650-124">Yalnızca adları belirtilen önekle başlayan blob indirilir.</span><span class="sxs-lookup"><span data-stu-id="90650-124">Only the blobs whose names begin with the specified prefix will be downloaded.</span></span>
<span data-ttu-id="90650-125">Bu önek bir kısmi dosya adı veya alt dizin olabilir.</span><span class="sxs-lookup"><span data-stu-id="90650-125">This prefix can be a partial filename or a subdirectory.</span></span>
<span data-ttu-id="90650-126">Bir önek belirtilmemişse, kapsayıcıdaki tüm dosyalar indirilir.</span><span class="sxs-lookup"><span data-stu-id="90650-126">If a prefix is not specified, all the files in the container will be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90650-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90650-127">-DefaultProfile</span></span>
<span data-ttu-id="90650-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="90650-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90650-129">-FileMode</span><span class="sxs-lookup"><span data-stu-id="90650-129">-FileMode</span></span>
<span data-ttu-id="90650-130">Dosya izin modu özniteliğini sekizlik biçimde alır.</span><span class="sxs-lookup"><span data-stu-id="90650-130">Gets the file permission mode attribute in octal format.</span></span>
<span data-ttu-id="90650-131">Bu özellik yalnızca kaynak dosyası bir Linux düğümüne indirildiğinde uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="90650-131">This property is applicable only if the resource file is downloaded to a Linux node.</span></span>
<span data-ttu-id="90650-132">Linux düğümü için bu özellik belirtilmemişse, varsayılan değer 0770 olur.</span><span class="sxs-lookup"><span data-stu-id="90650-132">If this property is not specified for a Linux node, then the default value is 0770.</span></span>

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

### <span data-ttu-id="90650-133">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="90650-133">-FilePath</span></span>
<span data-ttu-id="90650-134">Görevin çalışma diziniyle göreli olarak dosyaların indirileceği işlem düğümündeki konum.</span><span class="sxs-lookup"><span data-stu-id="90650-134">The location on the compute node to which to download the file(s), relative to the task's working directory.</span></span> <span data-ttu-id="90650-135">HttpUrl parametresi belirtilmişse, DosyaYolu gereklidir ve dosya adı da içinde olmak üzere dosyanın indirileceği yolu açıklar.</span><span class="sxs-lookup"><span data-stu-id="90650-135">If the HttpUrl parameter is specified, the FilePath is required and describes the path which the file will be downloaded to, including the filename.</span></span> <span data-ttu-id="90650-136">Aksi takdirde, AutoStorageContainerName veya StorageContainerUrl parametreleri belirtilmişse, DosyaYolu isteğe bağlıdır ve dosyaların indirileceği dizindir.</span><span class="sxs-lookup"><span data-stu-id="90650-136">Otherwise, if the AutoStorageContainerName or StorageContainerUrl parameters are specified, FilePath is optional and is the directory to download the files to.</span></span> <span data-ttu-id="90650-137">DosyaYolu 'nin bir dizin olarak kullanıldığı durumlarda, giriş verileriyle ilişkilendirilmiş olan tüm dizin yapısı tam olarak korunur ve belirtilen FilePath dizinine eklenir.</span><span class="sxs-lookup"><span data-stu-id="90650-137">In the case where FilePath is used as a directory, any directory structure already associated with the input data will be retained in full and appended to the specified FilePath directory.</span></span> <span data-ttu-id="90650-138">Belirtilen göreli yol görevin çalışma dizinini kesemezsiniz (örneğin, '.. ' kullanarak).</span><span class="sxs-lookup"><span data-stu-id="90650-138">The specified relative path cannot break out of the task's working directory (for example by using '..').</span></span>

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90650-139">-HttpUrl</span><span class="sxs-lookup"><span data-stu-id="90650-139">-HttpUrl</span></span>
<span data-ttu-id="90650-140">İndirilecek dosyanın URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="90650-140">The URL of the file to download.</span></span>
<span data-ttu-id="90650-141">URL, Azure Blob depolama ise, anonim erişim kullanılarak okunabilir olmalıdır; Yani, toplu Iş hizmeti, blob indirilirken herhangi bir kimlik bilgisi sunmaz.</span><span class="sxs-lookup"><span data-stu-id="90650-141">If the URL is Azure Blob Storage, it must be readable using anonymous access; that is, the Batch service does not present any credentials when downloading the blob.</span></span>
<span data-ttu-id="90650-142">Azure Storage 'da blob için böyle bir URL almanın iki yolu vardır: blob 'a okuma izinleri veren paylaşılan erişim Imzasını (SAS) ekleme veya blob veya kapsayıcısının ACL 'sini genel erişime izin verecek şekilde ayarlama.</span><span class="sxs-lookup"><span data-stu-id="90650-142">There are two ways to get such a URL for a blob in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the blob, or set the ACL for the blob or its container to allow public access.</span></span>

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90650-143">-StorageContainerUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="90650-143">-StorageContainerUrl</span></span>
<span data-ttu-id="90650-144">Azure Blob depolama içindeki blob kapsayıcısının URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="90650-144">The URL of the blob container within Azure Blob Storage.</span></span>
<span data-ttu-id="90650-145">Anonim erişim kullanılarak bu URL okunabilir ve kararlı olmalıdır; Yani, toplu Iş hizmeti kapsayıcıdan blob 'ları indirirken herhangi bir kimlik bilgisi sunmaz.</span><span class="sxs-lookup"><span data-stu-id="90650-145">This URL must be readable and listable using anonymous access; that is, the Batch service does not present any credentials when downloading blobs from the container.</span></span>
<span data-ttu-id="90650-146">Azure Storage 'daki bir kapsayıcının URL 'sini almanın iki yolu vardır: kapsayıcıya bir paylaşılan erişim Imzası (SAS) ekleme veya kapsayıcının ACL 'sini genel erişime izin verecek şekilde ayarlama.</span><span class="sxs-lookup"><span data-stu-id="90650-146">There are two ways to get such a URL for a container in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the container, or set the ACL for the container to allow public access.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90650-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90650-147">CommonParameters</span></span>
<span data-ttu-id="90650-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="90650-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90650-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="90650-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90650-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90650-150">INPUTS</span></span>

### <span data-ttu-id="90650-151">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="90650-151">None</span></span>

## <span data-ttu-id="90650-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90650-152">OUTPUTS</span></span>

### <span data-ttu-id="90650-153">Microsoft.Azure.Commands.Batch. Modeller. PSResourceFile</span><span class="sxs-lookup"><span data-stu-id="90650-153">Microsoft.Azure.Commands.Batch.Models.PSResourceFile</span></span>

## <span data-ttu-id="90650-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90650-154">NOTES</span></span>

## <span data-ttu-id="90650-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90650-155">RELATED LINKS</span></span>

[<span data-ttu-id="90650-156">Yeni-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="90650-156">New-AzBatchTask</span></span>](./New-AzBatchTask.md)