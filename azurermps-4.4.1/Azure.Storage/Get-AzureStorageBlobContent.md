---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobContent.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 9eb7337ee39ed0e9c4d179a6a89401398a0d80f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592706"
---
# <span data-ttu-id="5cb83-101">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5cb83-101">Get-AzureStorageBlobContent</span></span>

## <span data-ttu-id="5cb83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cb83-102">SYNOPSIS</span></span>
<span data-ttu-id="5cb83-103">Bir Depolama Blobu yükler.</span><span class="sxs-lookup"><span data-stu-id="5cb83-103">Downloads a storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cb83-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5cb83-104">SYNTAX</span></span>

### <span data-ttu-id="5cb83-105">ReceiveManual (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5cb83-105">ReceiveManual (Default)</span></span>
```
Get-AzureStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cb83-106">Blobboru hattı</span><span class="sxs-lookup"><span data-stu-id="5cb83-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cb83-107">Kapsayıcı boru hattı</span><span class="sxs-lookup"><span data-stu-id="5cb83-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cb83-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5cb83-108">DESCRIPTION</span></span>
<span data-ttu-id="5cb83-109">**Get-AzureStorageBlobContent** cmdlet 'i belirtilen depolama blobundan indirir.</span><span class="sxs-lookup"><span data-stu-id="5cb83-109">The **Get-AzureStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="5cb83-110">Blob adı yerel bilgisayar için geçerli değilse, bu cmdlet mümkünse otomatik olarak çözer.</span><span class="sxs-lookup"><span data-stu-id="5cb83-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="5cb83-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5cb83-111">EXAMPLES</span></span>

### <span data-ttu-id="5cb83-112">Örnek 1: blob içeriğini ada göre Indirme</span><span class="sxs-lookup"><span data-stu-id="5cb83-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzureStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="5cb83-113">Bu komut, bir blob 'u adla indirir.</span><span class="sxs-lookup"><span data-stu-id="5cb83-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="5cb83-114">Örnek 2: ardışık düzeni kullanarak blob içeriğini Indirme</span><span class="sxs-lookup"><span data-stu-id="5cb83-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container containername -Blob blobname | Get-AzureStorageBlobContent
```

<span data-ttu-id="5cb83-115">Bu komut, blob içeriğini bulmak ve indirmek için ardışık düzeni kullanır.</span><span class="sxs-lookup"><span data-stu-id="5cb83-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="5cb83-116">Örnek 3: ardışık düzen ve joker karakter kullanarak blob içeriği Indirin</span><span class="sxs-lookup"><span data-stu-id="5cb83-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Get-AzureStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="5cb83-117">Bu örnekte, blob içeriğini bulmak ve indirmek için joker karakter ve ardışık düzen kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5cb83-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

## <span data-ttu-id="5cb83-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5cb83-118">PARAMETERS</span></span>

### <span data-ttu-id="5cb83-119">-Blob</span><span class="sxs-lookup"><span data-stu-id="5cb83-119">-Blob</span></span>
<span data-ttu-id="5cb83-120">İndirilecek olan blob 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cb83-120">Specifies the name of the blob to be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: ReceiveManual, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cb83-121">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="5cb83-121">-CheckMd5</span></span>
<span data-ttu-id="5cb83-122">İndirilen dosyanın MD5 toplamının olup olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cb83-122">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="5cb83-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5cb83-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5cb83-124">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cb83-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5cb83-125">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="5cb83-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5cb83-126">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="5cb83-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5cb83-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="5cb83-127">-CloudBlob</span></span>
<span data-ttu-id="5cb83-128">Bulut blob 'unu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cb83-128">Specifies a cloud blob.</span></span>
<span data-ttu-id="5cb83-129">**Cloudblob** nesnesi edinmek için Get-AzureStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5cb83-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cb83-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="5cb83-130">-CloudBlobContainer</span></span>
<span data-ttu-id="5cb83-131">Azure depolama istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cb83-131">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="5cb83-132">Bunu oluşturabilir veya Get-AzureStorageContainer cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5cb83-132">You can create it or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cb83-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5cb83-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5cb83-134">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cb83-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5cb83-135">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5cb83-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5cb83-136">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="5cb83-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5cb83-137">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="5cb83-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5cb83-138">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="5cb83-138">The default value is 10.</span></span>

<span data-ttu-id="5cb83-139">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="5cb83-139">The default value is 10.</span></span>

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

### <span data-ttu-id="5cb83-140">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="5cb83-140">-Container</span></span>
<span data-ttu-id="5cb83-141">Yüklemek istediğiniz blob 'u içeren kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cb83-141">Specifies the name of container that has the blob you want to download.</span></span>

```yaml
Type: String
Parameter Sets: ReceiveManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cb83-142">-Context</span><span class="sxs-lookup"><span data-stu-id="5cb83-142">-Context</span></span>
<span data-ttu-id="5cb83-143">Blob içeriğini indirmek istediğiniz Azure Depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cb83-143">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="5cb83-144">Depolama bağlamı oluşturmak için New-AzureStorageContext cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5cb83-144">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cb83-145">-Hedef</span><span class="sxs-lookup"><span data-stu-id="5cb83-145">-Destination</span></span>
<span data-ttu-id="5cb83-146">İndirilen dosyanın depolanacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cb83-146">Specifies the location to store the downloaded file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cb83-147">-Force</span><span class="sxs-lookup"><span data-stu-id="5cb83-147">-Force</span></span>
<span data-ttu-id="5cb83-148">Mevcut bir dosyanın üzerine onay olmadan yazar.</span><span class="sxs-lookup"><span data-stu-id="5cb83-148">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="5cb83-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5cb83-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5cb83-150">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cb83-150">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="5cb83-151">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="5cb83-151">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="5cb83-152">-Onay</span><span class="sxs-lookup"><span data-stu-id="5cb83-152">-Confirm</span></span>
<span data-ttu-id="5cb83-153">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5cb83-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cb83-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cb83-154">-WhatIf</span></span>
<span data-ttu-id="5cb83-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5cb83-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cb83-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5cb83-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cb83-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cb83-157">CommonParameters</span></span>
<span data-ttu-id="5cb83-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5cb83-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cb83-159">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cb83-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cb83-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5cb83-160">INPUTS</span></span>

### <span data-ttu-id="5cb83-161">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="5cb83-161">IStorageContext</span></span>

<span data-ttu-id="5cb83-162">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="5cb83-162">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="5cb83-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5cb83-163">OUTPUTS</span></span>

### <span data-ttu-id="5cb83-164">AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5cb83-164">AzureStorageContainer</span></span>

## <span data-ttu-id="5cb83-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5cb83-165">NOTES</span></span>
* <span data-ttu-id="5cb83-166">Blob adı yerel bilgisayar için geçersizse, bu cmdlet mümkünse otomatik olarak çözülür.</span><span class="sxs-lookup"><span data-stu-id="5cb83-166">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="5cb83-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5cb83-167">RELATED LINKS</span></span>

[<span data-ttu-id="5cb83-168">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5cb83-168">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)

[<span data-ttu-id="5cb83-169">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="5cb83-169">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="5cb83-170">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="5cb83-170">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
