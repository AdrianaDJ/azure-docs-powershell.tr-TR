---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/close-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
ms.openlocfilehash: 6f288a124d0a024fc4b961409a17f9e0fe736c4b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096742"
---
# <span data-ttu-id="9fb34-101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="9fb34-101">Close-AzStorageFileHandle</span></span>

## <span data-ttu-id="9fb34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fb34-102">SYNOPSIS</span></span>
<span data-ttu-id="9fb34-103">Dosya paylaşımının dosya tanıtıcılarını, dosya dizinini veya dosyayı kapatır.</span><span class="sxs-lookup"><span data-stu-id="9fb34-103">Closes file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="9fb34-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9fb34-104">SYNTAX</span></span>

### <span data-ttu-id="9fb34-105">ShareNameCloseAll (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9fb34-105">ShareNameCloseAll (Default)</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-Context <IStorageContext>] [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fb34-106">ShareNameCloseSingle</span><span class="sxs-lookup"><span data-stu-id="9fb34-106">ShareNameCloseSingle</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> -FileHandle <PSFileHandle> [-Context <IStorageContext>]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9fb34-107">ShareCloseAll</span><span class="sxs-lookup"><span data-stu-id="9fb34-107">ShareCloseAll</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive] [-CloseAll] [-PassThru]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9fb34-108">Paylaşım</span><span class="sxs-lookup"><span data-stu-id="9fb34-108">ShareCloseSingle</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> -FileHandle <PSFileHandle> [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9fb34-109">DirectoryCloseAll</span><span class="sxs-lookup"><span data-stu-id="9fb34-109">DirectoryCloseAll</span></span>
```
Close-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9fb34-110">FileCloseAll</span><span class="sxs-lookup"><span data-stu-id="9fb34-110">FileCloseAll</span></span>
```
Close-AzStorageFileHandle [-File] <CloudFile> [-CloseAll] [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9fb34-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="9fb34-111">DESCRIPTION</span></span>
<span data-ttu-id="9fb34-112">**Close-AzStorageFileHandle** cmdlet 'i dosya paylaşımının veya dosya dizininin veya dosyanın dosya tutamaçlarını kapatır.</span><span class="sxs-lookup"><span data-stu-id="9fb34-112">The **Close-AzStorageFileHandle** cmdlet closes file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="9fb34-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9fb34-113">EXAMPLES</span></span>

### <span data-ttu-id="9fb34-114">Örnek 1: geçerli depolama hesabının tüm dosya paylaşımlarını listeler ve dosya paylaşımlarının tüm dosya tanıtıcılarını yinelemeli olarak kapatın.</span><span class="sxs-lookup"><span data-stu-id="9fb34-114">Example 1: Lists all file shares of current Storage Account, and close all file handles of the file shares recursively.</span></span>
```
PS C:\>Get-AzStorageShare | Close-AzStorageFileHandle -CloseAll -Recursive
```

<span data-ttu-id="9fb34-115">Bu komut geçerli depolama hesabının tüm dosya paylaşımlarını listeler ve dosya paylaşımlarının tüm dosya tanıtıcılarını yinelemeli olarak kapatır.</span><span class="sxs-lookup"><span data-stu-id="9fb34-115">This command lists all file shares of current Storage Account, and close all file handles of the file shares recursively..</span></span>

### <span data-ttu-id="9fb34-116">Örnek 2: dosya dizinindeki tüm dosya tutamaçlarını özyinelemeli olarak kapatma ve kapalı dosya tanıtıcısı sayısını gösterme</span><span class="sxs-lookup"><span data-stu-id="9fb34-116">Example 2: Close all file handles on a file directory recursively and show the closed file handle count</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive -CloseAll -PassThru
10
```

<span data-ttu-id="9fb34-117">Bu komut, dosya dizinindeki tüm dosya tanıtıcılarını kapatır ve kapatılan dosya tanıtıcısı sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9fb34-117">This command closes all file handles on a file directory and show the closed file handle count.</span></span>

### <span data-ttu-id="9fb34-118">Örnek 3: dosya dizininde 1 gün önce açılan tüm dosya tutamaçlarını kapatın</span><span class="sxs-lookup"><span data-stu-id="9fb34-118">Example 3: Close all file handles which is opened 1 day ago on a file directory</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive | ? {$_.OpenTime.DateTime.AddDays(1) -lt (Get-Date)} | Close-AzStorageFileHandle -ShareName "mysharename"
```

<span data-ttu-id="9fb34-119">Bu komut, dosya dizinindeki tüm dosya tanıtıcılarını yinelemeli olarak listeler, 1 gün önce açılan tutamaçları filtreler ve sonra da kapatır.</span><span class="sxs-lookup"><span data-stu-id="9fb34-119">This command lists all file handles on a file directory recursively, filters out the handles which are opened 1 day ago, and then close them.</span></span>

### <span data-ttu-id="9fb34-120">Örnek 4: dosyadaki tüm dosya tutamaçlarını kapatma</span><span class="sxs-lookup"><span data-stu-id="9fb34-120">Example 4: Close all file handles on a file</span></span> 
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -CloseAll
```

<span data-ttu-id="9fb34-121">Bu komut, dosyadaki tüm dosya tanıtıcılarını kapatır.</span><span class="sxs-lookup"><span data-stu-id="9fb34-121">This command closes all file handles on a file.</span></span>

## <span data-ttu-id="9fb34-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9fb34-122">PARAMETERS</span></span>

### <span data-ttu-id="9fb34-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="9fb34-123">-AsJob</span></span>
<span data-ttu-id="9fb34-124">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9fb34-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9fb34-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9fb34-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9fb34-126">Her isteğin saniye cinsinden istemci tarafı maksimum yürütme süresi.</span><span class="sxs-lookup"><span data-stu-id="9fb34-126">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="9fb34-127">-CloseAll</span><span class="sxs-lookup"><span data-stu-id="9fb34-127">-CloseAll</span></span>
<span data-ttu-id="9fb34-128">Tüm dosya tutamaçlarını kapatmaya zorlayın.</span><span class="sxs-lookup"><span data-stu-id="9fb34-128">Force close all File handles.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll, FileCloseAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb34-129">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9fb34-129">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9fb34-130">Eşzamanlı eşzamansız görevlerin toplam miktarı.</span><span class="sxs-lookup"><span data-stu-id="9fb34-130">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="9fb34-131">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="9fb34-131">The default value is 10.</span></span>

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

### <span data-ttu-id="9fb34-132">-Context</span><span class="sxs-lookup"><span data-stu-id="9fb34-132">-Context</span></span>
<span data-ttu-id="9fb34-133">Azure depolama bağlamı nesnesi</span><span class="sxs-lookup"><span data-stu-id="9fb34-133">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb34-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fb34-134">-DefaultProfile</span></span>
<span data-ttu-id="9fb34-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9fb34-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fb34-136">-Dizin</span><span class="sxs-lookup"><span data-stu-id="9fb34-136">-Directory</span></span>
<span data-ttu-id="9fb34-137">CloudFileDirectory nesnesi, dosyaların/dizinlerin listelenmekte olduğu temel klasörü belirtti.</span><span class="sxs-lookup"><span data-stu-id="9fb34-137">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirectoryCloseAll
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb34-138">-Dosya</span><span class="sxs-lookup"><span data-stu-id="9fb34-138">-File</span></span>
<span data-ttu-id="9fb34-139">CloudFile nesnesi, kapatılacak dosyayı belirtti.</span><span class="sxs-lookup"><span data-stu-id="9fb34-139">CloudFile object indicated the file to close handle.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileCloseAll
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb34-140">-FileHandle</span><span class="sxs-lookup"><span data-stu-id="9fb34-140">-FileHandle</span></span>
<span data-ttu-id="9fb34-141">Kapatılacak dosya tutamacı.</span><span class="sxs-lookup"><span data-stu-id="9fb34-141">The File Handle to close.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSFileHandle
Parameter Sets: ShareNameCloseSingle, ShareCloseSingle
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb34-142">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9fb34-142">-PassThru</span></span>
<span data-ttu-id="9fb34-143">Kapatılan dosya tanıtıcılarının sayısını döndür.</span><span class="sxs-lookup"><span data-stu-id="9fb34-143">Return the count of closed file handles.</span></span>

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

### <span data-ttu-id="9fb34-144">-Yol</span><span class="sxs-lookup"><span data-stu-id="9fb34-144">-Path</span></span>
<span data-ttu-id="9fb34-145">Var olan bir dosyanın/dizinin yolu.</span><span class="sxs-lookup"><span data-stu-id="9fb34-145">Path to an existing file/directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb34-146">-Yinelemeli</span><span class="sxs-lookup"><span data-stu-id="9fb34-146">-Recursive</span></span>
<span data-ttu-id="9fb34-147">Liste tutamaçları yinelemeli olarak.</span><span class="sxs-lookup"><span data-stu-id="9fb34-147">List handles Recursively.</span></span>
<span data-ttu-id="9fb34-148">Yalnızca dosya dizininde çalışır.</span><span class="sxs-lookup"><span data-stu-id="9fb34-148">Only works on File Directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb34-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9fb34-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9fb34-150">Her isteğin saniye cinsinden zaman aşımı.</span><span class="sxs-lookup"><span data-stu-id="9fb34-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="9fb34-151">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="9fb34-151">-Share</span></span>
<span data-ttu-id="9fb34-152">CloudFileShare nesnesi, dosyaların/dizinlerin listelendiği paylaşımı belirtti.</span><span class="sxs-lookup"><span data-stu-id="9fb34-152">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareCloseAll, ShareCloseSingle
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb34-153">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="9fb34-153">-ShareName</span></span>
<span data-ttu-id="9fb34-154">Dosyaların/dizinlerin listelendiği dosya paylaşımının adı.</span><span class="sxs-lookup"><span data-stu-id="9fb34-154">Name of the file share where the files/directories would be listed.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb34-155">-Onay</span><span class="sxs-lookup"><span data-stu-id="9fb34-155">-Confirm</span></span>
<span data-ttu-id="9fb34-156">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9fb34-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb34-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fb34-157">-WhatIf</span></span>
<span data-ttu-id="9fb34-158">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9fb34-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fb34-159">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9fb34-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb34-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fb34-160">CommonParameters</span></span>
<span data-ttu-id="9fb34-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9fb34-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fb34-162">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fb34-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fb34-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9fb34-163">INPUTS</span></span>

### <span data-ttu-id="9fb34-164">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="9fb34-164">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="9fb34-165">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="9fb34-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="9fb34-166">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="9fb34-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9fb34-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9fb34-167">OUTPUTS</span></span>

### <span data-ttu-id="9fb34-168">Microsoft. Azure. Storage. File. CloseFileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="9fb34-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span></span>

## <span data-ttu-id="9fb34-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9fb34-169">NOTES</span></span>

## <span data-ttu-id="9fb34-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9fb34-170">RELATED LINKS</span></span>