---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobIncrementalCopy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/e87bc1c9e534808427b7dc77aa06eacc46663253
ms.openlocfilehash: b327db4c7054e3c841dca3310887b1d1f1201d23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591853"
---
# <span data-ttu-id="57816-101">Start-AzureStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="57816-101">Start-AzureStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="57816-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57816-102">SYNOPSIS</span></span>
<span data-ttu-id="57816-103">Sayfa blob anlık görüntüsünden belirtilen hedef sayfa blob 'una artımlı kopyalama işlemi başlatın.</span><span class="sxs-lookup"><span data-stu-id="57816-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57816-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57816-104">SYNTAX</span></span>

### <span data-ttu-id="57816-105">Containerınstance (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="57816-105">ContainerInstance (Default)</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57816-106">Blobörneği</span><span class="sxs-lookup"><span data-stu-id="57816-106">BlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57816-107">Blobınstancetoblobınstance</span><span class="sxs-lookup"><span data-stu-id="57816-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57816-108">Öğesini</span><span class="sxs-lookup"><span data-stu-id="57816-108">ContainerName</span></span>
```
Start-AzureStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57816-109">Uripipda</span><span class="sxs-lookup"><span data-stu-id="57816-109">UriPipeline</span></span>
```
Start-AzureStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57816-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="57816-110">DESCRIPTION</span></span>
<span data-ttu-id="57816-111">Sayfa blob anlık görüntüsünden belirtilen hedef sayfa blob 'una artımlı kopyalama işlemi başlatın.</span><span class="sxs-lookup"><span data-stu-id="57816-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="57816-112">Uygulamasındaki özelliğin diğer ayrıntılarını görün https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="57816-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="57816-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57816-113">EXAMPLES</span></span>

### <span data-ttu-id="57816-114">Örnek 1: blob adı ve anlık görüntü zamanına göre artımlı kopyalama Işlemi başlatma</span><span class="sxs-lookup"><span data-stu-id="57816-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="57816-115">Bu komut artımlı kopyalama Işlemini blob adı ve anlık görüntü zamanına göre Başlat</span><span class="sxs-lookup"><span data-stu-id="57816-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="57816-116">Örnek 2: Kaynak URI kullanarak artımlı kopyalama işlemini başlatma</span><span class="sxs-lookup"><span data-stu-id="57816-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="57816-117">Bu komut kaynak URI kullanarak artımlı kopyalama Işlemi başlatır</span><span class="sxs-lookup"><span data-stu-id="57816-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="57816-118">Örnek 3: GetAzureStorageContainer 'den kapsayıcı ardışık düzeni kullanarak artımlı kopyalama işlemi başlatın</span><span class="sxs-lookup"><span data-stu-id="57816-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container1 | Start-AzureStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="57816-119">Bu komut GetAzureStorageContainer 'den kapsayıcı ardışık düzeni kullanarak artımlı kopyalama Işlemi başlatır</span><span class="sxs-lookup"><span data-stu-id="57816-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="57816-120">Örnek 4: CloudPageBlob nesnesinden, blob adıyla hedef blob 'a artımlı kopyalama işlemi başlatma</span><span class="sxs-lookup"><span data-stu-id="57816-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzureStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzureStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="57816-121">Bu komut CloudPageBlob nesnesinden, blob adıyla hedef blob 'a artımlı kopyalama Işlemi başlatır</span><span class="sxs-lookup"><span data-stu-id="57816-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="57816-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57816-122">PARAMETERS</span></span>

### <span data-ttu-id="57816-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="57816-123">-AbsoluteUri</span></span>
<span data-ttu-id="57816-124">Kaynağın mutlak Uri 'Si.</span><span class="sxs-lookup"><span data-stu-id="57816-124">Absolute Uri to the source.</span></span> <span data-ttu-id="57816-125">Kaynak gerektiriyorsa, kimlik bilgisinin URI 'de sağlanması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="57816-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57816-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="57816-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="57816-127">Her isteğin saniye cinsinden istemci tarafı maksimum yürütme süresi.</span><span class="sxs-lookup"><span data-stu-id="57816-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="57816-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="57816-128">-CloudBlob</span></span>
<span data-ttu-id="57816-129">Azure depolama Istemci kitaplığından CloudBlob nesnesi.</span><span class="sxs-lookup"><span data-stu-id="57816-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="57816-130">Bunu oluşturabilir veya Get-AzureStorageBlob cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57816-130">You can create it or use Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57816-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="57816-131">-CloudBlobContainer</span></span>
<span data-ttu-id="57816-132">Azure depolama Istemci kitaplığından CloudBlobContainer nesnesi.</span><span class="sxs-lookup"><span data-stu-id="57816-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="57816-133">Bunu oluşturabilir veya Get-AzureStorageContainer cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57816-133">You can create it or use Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57816-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="57816-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="57816-135">Eşzamanlı eşzamansız görevlerin toplam miktarı.</span><span class="sxs-lookup"><span data-stu-id="57816-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="57816-136">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="57816-136">The default value is 10.</span></span>

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

### <span data-ttu-id="57816-137">-Context</span><span class="sxs-lookup"><span data-stu-id="57816-137">-Context</span></span>
<span data-ttu-id="57816-138">Kaynak Azure depolama bağlamı.</span><span class="sxs-lookup"><span data-stu-id="57816-138">Source Azure Storage Context.</span></span> <span data-ttu-id="57816-139">Bunu New-AzureStorageContext cmdlet ile oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57816-139">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerInstance, BlobInstance, BlobInstanceToBlobInstance, ContainerName
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57816-140">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="57816-140">-DestBlob</span></span>
<span data-ttu-id="57816-141">Hedef blob adı</span><span class="sxs-lookup"><span data-stu-id="57816-141">Destination blob name</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57816-142">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="57816-142">-DestCloudBlob</span></span>
<span data-ttu-id="57816-143">Hedef CloudBlob nesnesi</span><span class="sxs-lookup"><span data-stu-id="57816-143">Destination CloudBlob object</span></span>

```yaml
Type: CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57816-144">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="57816-144">-DestContainer</span></span>
<span data-ttu-id="57816-145">Hedef kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="57816-145">Destination container name</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57816-146">-DestContext</span><span class="sxs-lookup"><span data-stu-id="57816-146">-DestContext</span></span>
<span data-ttu-id="57816-147">Hedef Azure depolama bağlamı.</span><span class="sxs-lookup"><span data-stu-id="57816-147">Destination Azure Storage Context.</span></span> <span data-ttu-id="57816-148">Bunu New-AzureStorageContext cmdlet ile oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57816-148">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57816-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="57816-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="57816-150">Her isteğin saniye cinsinden zaman aşımı.</span><span class="sxs-lookup"><span data-stu-id="57816-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="57816-151">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="57816-151">-SrcBlob</span></span>
<span data-ttu-id="57816-152">Kaynak sayfası blob adı.</span><span class="sxs-lookup"><span data-stu-id="57816-152">Source page blob name.</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57816-153">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="57816-153">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="57816-154">Kaynak Sayfa blob anlık görüntü süresi.</span><span class="sxs-lookup"><span data-stu-id="57816-154">Source page blob snapshot time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlobSnapshotTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57816-155">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="57816-155">-SrcContainer</span></span>
<span data-ttu-id="57816-156">Kaynak kapsayıcı adı</span><span class="sxs-lookup"><span data-stu-id="57816-156">Source Container name</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57816-157">-Onay</span><span class="sxs-lookup"><span data-stu-id="57816-157">-Confirm</span></span>
<span data-ttu-id="57816-158">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="57816-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57816-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57816-159">-WhatIf</span></span>
<span data-ttu-id="57816-160">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="57816-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57816-161">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="57816-161">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57816-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57816-162">CommonParameters</span></span>
<span data-ttu-id="57816-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57816-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57816-164">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57816-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57816-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57816-165">INPUTS</span></span>

### <span data-ttu-id="57816-166">Microsoft. Windowsazde. Storage. blob. CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="57816-166">Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob</span></span>
<span data-ttu-id="57816-167">Microsoft. Windowsazde. Storage. blob. CloudBlobContainer System. String Microsoft. Windowsazme. Commands. Common. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="57816-167">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer System.String Microsoft.WindowsAzure.Commands.Common.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="57816-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57816-168">OUTPUTS</span></span>

### <span data-ttu-id="57816-169">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="57816-169">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="57816-170">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57816-170">NOTES</span></span>

## <span data-ttu-id="57816-171">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57816-171">RELATED LINKS</span></span>

