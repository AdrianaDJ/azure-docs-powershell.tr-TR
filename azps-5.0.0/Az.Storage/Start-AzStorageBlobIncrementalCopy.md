---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobincrementalcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
ms.openlocfilehash: 126d89ca600c9696a1300054c2dc82cb1d9f5d2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324985"
---
# <span data-ttu-id="0712b-101">Start-AzStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="0712b-101">Start-AzStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="0712b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0712b-102">SYNOPSIS</span></span>
<span data-ttu-id="0712b-103">Sayfa blob anlık görüntüsünden belirtilen hedef sayfa blob 'una artımlı kopyalama işlemi başlatın.</span><span class="sxs-lookup"><span data-stu-id="0712b-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="0712b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0712b-104">SYNTAX</span></span>

### <span data-ttu-id="0712b-105">Containerınstance (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0712b-105">ContainerInstance (Default)</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0712b-106">Blobörneği</span><span class="sxs-lookup"><span data-stu-id="0712b-106">BlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0712b-107">Blobınstancetoblobınstance</span><span class="sxs-lookup"><span data-stu-id="0712b-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0712b-108">Öğesini</span><span class="sxs-lookup"><span data-stu-id="0712b-108">ContainerName</span></span>
```
Start-AzStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0712b-109">Uripipda</span><span class="sxs-lookup"><span data-stu-id="0712b-109">UriPipeline</span></span>
```
Start-AzStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0712b-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="0712b-110">DESCRIPTION</span></span>
<span data-ttu-id="0712b-111">Sayfa blob anlık görüntüsünden belirtilen hedef sayfa blob 'una artımlı kopyalama işlemi başlatın.</span><span class="sxs-lookup"><span data-stu-id="0712b-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="0712b-112">Uygulamasındaki özelliğin diğer ayrıntılarını görün https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="0712b-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="0712b-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0712b-113">EXAMPLES</span></span>

### <span data-ttu-id="0712b-114">Örnek 1: blob adı ve anlık görüntü zamanına göre artımlı kopyalama Işlemi başlatma</span><span class="sxs-lookup"><span data-stu-id="0712b-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="0712b-115">Bu komut artımlı kopyalama Işlemini blob adı ve anlık görüntü zamanına göre Başlat</span><span class="sxs-lookup"><span data-stu-id="0712b-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="0712b-116">Örnek 2: Kaynak URI kullanarak artımlı kopyalama işlemini başlatma</span><span class="sxs-lookup"><span data-stu-id="0712b-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="0712b-117">Bu komut kaynak URI kullanarak artımlı kopyalama Işlemi başlatır</span><span class="sxs-lookup"><span data-stu-id="0712b-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="0712b-118">Örnek 3: GetAzureStorageContainer 'den kapsayıcı ardışık düzeni kullanarak artımlı kopyalama işlemi başlatın</span><span class="sxs-lookup"><span data-stu-id="0712b-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzStorageContainer -Container container1 | Start-AzStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="0712b-119">Bu komut GetAzureStorageContainer 'den kapsayıcı ardışık düzeni kullanarak artımlı kopyalama Işlemi başlatır</span><span class="sxs-lookup"><span data-stu-id="0712b-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="0712b-120">Örnek 4: CloudPageBlob nesnesinden, blob adıyla hedef blob 'a artımlı kopyalama işlemi başlatma</span><span class="sxs-lookup"><span data-stu-id="0712b-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="0712b-121">Bu komut CloudPageBlob nesnesinden, blob adıyla hedef blob 'a artımlı kopyalama Işlemi başlatır</span><span class="sxs-lookup"><span data-stu-id="0712b-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="0712b-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0712b-122">PARAMETERS</span></span>

### <span data-ttu-id="0712b-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="0712b-123">-AbsoluteUri</span></span>
<span data-ttu-id="0712b-124">Kaynağın mutlak Uri 'Si.</span><span class="sxs-lookup"><span data-stu-id="0712b-124">Absolute Uri to the source.</span></span> <span data-ttu-id="0712b-125">Kaynak gerektiriyorsa, kimlik bilgisinin URI 'de sağlanması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="0712b-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0712b-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0712b-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0712b-127">Her isteğin saniye cinsinden istemci tarafı maksimum yürütme süresi.</span><span class="sxs-lookup"><span data-stu-id="0712b-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="0712b-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="0712b-128">-CloudBlob</span></span>
<span data-ttu-id="0712b-129">Azure depolama Istemci kitaplığından CloudBlob nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0712b-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="0712b-130">Bunu oluşturabilir veya Get-AzStorageBlob cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0712b-130">You can create it or use Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0712b-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="0712b-131">-CloudBlobContainer</span></span>
<span data-ttu-id="0712b-132">Azure depolama Istemci kitaplığından CloudBlobContainer nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0712b-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="0712b-133">Bunu oluşturabilir veya Get-AzStorageContainer cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0712b-133">You can create it or use Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0712b-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0712b-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0712b-135">Eşzamanlı eşzamansız görevlerin toplam miktarı.</span><span class="sxs-lookup"><span data-stu-id="0712b-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="0712b-136">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="0712b-136">The default value is 10.</span></span>

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

### <span data-ttu-id="0712b-137">-Context</span><span class="sxs-lookup"><span data-stu-id="0712b-137">-Context</span></span>
<span data-ttu-id="0712b-138">Kaynak Azure depolama bağlamı.</span><span class="sxs-lookup"><span data-stu-id="0712b-138">Source Azure Storage Context.</span></span> <span data-ttu-id="0712b-139">Bunu New-AzStorageContext cmdlet ile oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0712b-139">You can create it by New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerInstance, BlobInstance, BlobInstanceToBlobInstance, ContainerName
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0712b-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0712b-140">-DefaultProfile</span></span>
<span data-ttu-id="0712b-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0712b-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0712b-142">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="0712b-142">-DestBlob</span></span>
<span data-ttu-id="0712b-143">Hedef blob adı</span><span class="sxs-lookup"><span data-stu-id="0712b-143">Destination blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0712b-144">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="0712b-144">-DestCloudBlob</span></span>
<span data-ttu-id="0712b-145">Hedef CloudBlob nesnesi</span><span class="sxs-lookup"><span data-stu-id="0712b-145">Destination CloudBlob object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0712b-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="0712b-146">-DestContainer</span></span>
<span data-ttu-id="0712b-147">Hedef kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="0712b-147">Destination container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0712b-148">-DestContext</span><span class="sxs-lookup"><span data-stu-id="0712b-148">-DestContext</span></span>
<span data-ttu-id="0712b-149">Hedef Azure depolama bağlamı.</span><span class="sxs-lookup"><span data-stu-id="0712b-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="0712b-150">Bunu New-AzStorageContext cmdlet ile oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0712b-150">You can create it by New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0712b-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0712b-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0712b-152">Her isteğin saniye cinsinden zaman aşımı.</span><span class="sxs-lookup"><span data-stu-id="0712b-152">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="0712b-153">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="0712b-153">-SrcBlob</span></span>
<span data-ttu-id="0712b-154">Kaynak sayfası blob adı.</span><span class="sxs-lookup"><span data-stu-id="0712b-154">Source page blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0712b-155">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="0712b-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="0712b-156">Kaynak Sayfa blob anlık görüntü süresi.</span><span class="sxs-lookup"><span data-stu-id="0712b-156">Source page blob snapshot time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlobSnapshotTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0712b-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="0712b-157">-SrcContainer</span></span>
<span data-ttu-id="0712b-158">Kaynak kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="0712b-158">Source Container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0712b-159">-Onay</span><span class="sxs-lookup"><span data-stu-id="0712b-159">-Confirm</span></span>
<span data-ttu-id="0712b-160">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0712b-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0712b-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0712b-161">-WhatIf</span></span>
<span data-ttu-id="0712b-162">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0712b-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0712b-163">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0712b-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0712b-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0712b-164">CommonParameters</span></span>
<span data-ttu-id="0712b-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0712b-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0712b-166">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0712b-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0712b-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0712b-167">INPUTS</span></span>

### <span data-ttu-id="0712b-168">Microsoft. Azure. Storage. blob. CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="0712b-168">Microsoft.Azure.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="0712b-169">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="0712b-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="0712b-170">System. String</span><span class="sxs-lookup"><span data-stu-id="0712b-170">System.String</span></span>

### <span data-ttu-id="0712b-171">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="0712b-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0712b-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0712b-172">OUTPUTS</span></span>

### <span data-ttu-id="0712b-173">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="0712b-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="0712b-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0712b-174">NOTES</span></span>

## <span data-ttu-id="0712b-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0712b-175">RELATED LINKS</span></span>
