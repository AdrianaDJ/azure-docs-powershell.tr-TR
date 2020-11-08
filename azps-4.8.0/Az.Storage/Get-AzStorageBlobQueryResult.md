---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-azstorageblobqueryresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
ms.openlocfilehash: fbb1c8e4e2a5421ea7714a0d7a82b1f1cc2567f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107530"
---
# <span data-ttu-id="e7274-101">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="e7274-101">Get-AzStorageBlobQueryResult</span></span>

## <span data-ttu-id="e7274-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7274-102">SYNOPSIS</span></span>
<span data-ttu-id="e7274-103">Blob içeriğinde basit bir yapılandırılmış sorgu dili (SQL) deyimi uygular ve verilerin yalnızca sorgulanan alt kümesini bir yerel dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="e7274-103">Applies a simple Structured Query Language (SQL) statement on a blob's contents and save only the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="e7274-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7274-104">SYNTAX</span></span>

### <span data-ttu-id="e7274-105">Ad boru hattı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e7274-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobQueryResult [-Blob] <String> [-Container] <String> [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7274-106">Blobboru hattı</span><span class="sxs-lookup"><span data-stu-id="e7274-106">BlobPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobBaseClient <BlobBaseClient> -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7274-107">Kapsayıcı boru hattı</span><span class="sxs-lookup"><span data-stu-id="e7274-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobContainerClient <BlobContainerClient> [-Blob] <String>
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7274-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7274-108">DESCRIPTION</span></span>
<span data-ttu-id="e7274-109">**Get-AzStorageBlobQueryResult** cmdlet 'i, blob içeriğinde basit bir yapılandırılmış sorgu DILI (SQL) deyimi uygular ve verilerin sorgulanan alt kümesini bir yerel dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="e7274-109">The **Get-AzStorageBlobQueryResult** cmdlet applies a simple Structured Query Language (SQL) statement on a blob's contents and save the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="e7274-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7274-110">EXAMPLES</span></span>

### <span data-ttu-id="e7274-111">Örnek 1: bir blob sorgulama</span><span class="sxs-lookup"><span data-stu-id="e7274-111">Example 1: Query a blob</span></span>
```powershell
PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE Name = 'a'"

PS C:\> $result = Get-AzStorageBlobQueryResult -Container $containerName -Blob $blobName -QueryString $queryString -ResultFile "c:\resultfile.json" -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig -Context $ctx

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
         449            0
```

<span data-ttu-id="e7274-112">Bu komut, giriş yapılandırmasını CSV olarak ve çıkış yapılandırması 'nı c:\resultfile.jsJSON olarak içeren bir blob succsssfully</span><span class="sxs-lookup"><span data-stu-id="e7274-112">This command querys a blob succsssfully with input config as csv, and output config as json, and save the output to local file "c:\resultfile.json".</span></span>

### <span data-ttu-id="e7274-113">Örnek 2: bir blob anlık görüntüsünü sorgulama</span><span class="sxs-lookup"><span data-stu-id="e7274-113">Example 2: Query a blob snapshot</span></span>
```powershell
PS C:\> $blob = Get-AzStorageBlob -Container $containerName -Blob $blobName -SnapshotTime "2020-07-29T11:08:21.1097874Z" -Context $ctx

PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -ColumnSeparator "," -QuotationCharacter """" -EscapeCharacter "\" -RecordSeparator "`n" -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson -RecordSeparator "`n" 

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE _1 LIKE '1%%'"

PS C:\> $result = $blob | Get-AzStorageBlobQueryResult -QueryString $queryString -ResultFile $localFilePath -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
   187064971            1 {ParseError}  



PS C:\> $result.BlobQueryError

Name       Description                                                   IsFatal Position
----       -----------                                                   ------- --------
ParseError Unexpected token '1' at [byte: 3077737]. Expecting token ','.    True  7270632
```

<span data-ttu-id="e7274-114">Bu komut öncelikle blob anlık görüntüsünün blob nesnesini alır, ardından blob anlık görüntüsünü sorgular ve sonucu sorgu hatasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7274-114">This command first gets a blob object for blob snapshot, then queries the blob snapshot and show the result include query error.</span></span>

## <span data-ttu-id="e7274-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7274-115">PARAMETERS</span></span>

### <span data-ttu-id="e7274-116">-Blob</span><span class="sxs-lookup"><span data-stu-id="e7274-116">-Blob</span></span>
<span data-ttu-id="e7274-117">Blob adı</span><span class="sxs-lookup"><span data-stu-id="e7274-117">Blob name</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7274-118">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="e7274-118">-BlobBaseClient</span></span>
<span data-ttu-id="e7274-119">BlobBaseClient nesnesi</span><span class="sxs-lookup"><span data-stu-id="e7274-119">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7274-120">-BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="e7274-120">-BlobContainerClient</span></span>
<span data-ttu-id="e7274-121">BlobContainerClient nesnesi</span><span class="sxs-lookup"><span data-stu-id="e7274-121">BlobContainerClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.BlobContainerClient
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7274-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e7274-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e7274-123">Her isteğin saniye cinsinden istemci tarafı maksimum yürütme süresi.</span><span class="sxs-lookup"><span data-stu-id="e7274-123">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="e7274-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e7274-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e7274-125">Eşzamanlı eşzamansız görevlerin toplam miktarı.</span><span class="sxs-lookup"><span data-stu-id="e7274-125">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="e7274-126">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="e7274-126">The default value is 10.</span></span>

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

### <span data-ttu-id="e7274-127">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="e7274-127">-Container</span></span>
<span data-ttu-id="e7274-128">Kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="e7274-128">Container name</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7274-129">-Context</span><span class="sxs-lookup"><span data-stu-id="e7274-129">-Context</span></span>
<span data-ttu-id="e7274-130">Azure depolama bağlamı nesnesi</span><span class="sxs-lookup"><span data-stu-id="e7274-130">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="e7274-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7274-131">-DefaultProfile</span></span>
<span data-ttu-id="e7274-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e7274-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7274-133">-Force</span><span class="sxs-lookup"><span data-stu-id="e7274-133">-Force</span></span>
<span data-ttu-id="e7274-134">Var olan dosyanın üzerine yazmayı zorlayın.</span><span class="sxs-lookup"><span data-stu-id="e7274-134">Force to overwrite the existing file.</span></span>

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

### <span data-ttu-id="e7274-135">-Inputtextconfiguration</span><span class="sxs-lookup"><span data-stu-id="e7274-135">-InputTextConfiguration</span></span>
<span data-ttu-id="e7274-136">Sorgu giriş metnini işlenmiş olarak yapılandırma.</span><span class="sxs-lookup"><span data-stu-id="e7274-136">The configuration used to handled the query input text.</span></span> <span data-ttu-id="e7274-137">Yeni-AzStorageBlobQueryConfig ile yapılandırma nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e7274-137">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7274-138">-OutputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7274-138">-OutputTextConfiguration</span></span>
<span data-ttu-id="e7274-139">Sorgu çıktı metnini işlenmiş yapılandırma.</span><span class="sxs-lookup"><span data-stu-id="e7274-139">The configuration used to handled the query output text.</span></span> <span data-ttu-id="e7274-140">Yeni-AzStorageBlobQueryConfig ile yapılandırma nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e7274-140">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7274-141">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e7274-141">-PassThru</span></span>
<span data-ttu-id="e7274-142">Belirtilen Blobun başarıyla sorgulanmış olup olmadığını döndürme.</span><span class="sxs-lookup"><span data-stu-id="e7274-142">Return whether the specified blob is successfully queried.</span></span>

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

### <span data-ttu-id="e7274-143">-QueryString</span><span class="sxs-lookup"><span data-stu-id="e7274-143">-QueryString</span></span>
<span data-ttu-id="e7274-144">Sorgu dizesi, şu konuda diğer ayrıntılara bakın: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span><span class="sxs-lookup"><span data-stu-id="e7274-144">Query string, see more details in: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7274-145">-ResultFile</span><span class="sxs-lookup"><span data-stu-id="e7274-145">-ResultFile</span></span>
<span data-ttu-id="e7274-146">Sorgu sonucunu kaydetmek için yerel dosya yolu.</span><span class="sxs-lookup"><span data-stu-id="e7274-146">Local file path to save the query result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7274-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e7274-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e7274-148">Her isteğin saniye cinsinden zaman aşımı.</span><span class="sxs-lookup"><span data-stu-id="e7274-148">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="e7274-149">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="e7274-149">-SnapshotTime</span></span>
<span data-ttu-id="e7274-150">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="e7274-150">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7274-151">-VersionId</span><span class="sxs-lookup"><span data-stu-id="e7274-151">-VersionId</span></span>
<span data-ttu-id="e7274-152">Blob VersionId 'Si</span><span class="sxs-lookup"><span data-stu-id="e7274-152">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7274-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="e7274-153">-Confirm</span></span>
<span data-ttu-id="e7274-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e7274-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7274-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7274-155">-WhatIf</span></span>
<span data-ttu-id="e7274-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7274-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7274-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e7274-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7274-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7274-158">CommonParameters</span></span>
<span data-ttu-id="e7274-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7274-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7274-160">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7274-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7274-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7274-161">INPUTS</span></span>

### <span data-ttu-id="e7274-162">Azure. Storage. blob. özelleştirilmiş. BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="e7274-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="e7274-163">Azure. Storage. blob. BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="e7274-163">Azure.Storage.Blobs.BlobContainerClient</span></span>

### <span data-ttu-id="e7274-164">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="e7274-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e7274-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7274-165">OUTPUTS</span></span>

### <span data-ttu-id="e7274-166">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e7274-166">System.Boolean</span></span>

## <span data-ttu-id="e7274-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7274-167">NOTES</span></span>

## <span data-ttu-id="e7274-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7274-168">RELATED LINKS</span></span>
