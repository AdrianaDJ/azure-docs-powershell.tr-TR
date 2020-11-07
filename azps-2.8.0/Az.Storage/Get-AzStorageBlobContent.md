---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: 320de9e1dab757265d626b1df34e5049c691b7bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934012"
---
# <span data-ttu-id="253c1-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="253c1-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="253c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="253c1-102">SYNOPSIS</span></span>
<span data-ttu-id="253c1-103">Bir Depolama Blobu yükler.</span><span class="sxs-lookup"><span data-stu-id="253c1-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="253c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="253c1-104">SYNTAX</span></span>

### <span data-ttu-id="253c1-105">ReceiveManual (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="253c1-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="253c1-106">Blobboru hattı</span><span class="sxs-lookup"><span data-stu-id="253c1-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="253c1-107">Kapsayıcı boru hattı</span><span class="sxs-lookup"><span data-stu-id="253c1-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="253c1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="253c1-108">DESCRIPTION</span></span>
<span data-ttu-id="253c1-109">**Get-AzStorageBlobContent** cmdlet 'i belirtilen depolama blobundan indirir.</span><span class="sxs-lookup"><span data-stu-id="253c1-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="253c1-110">Blob adı yerel bilgisayar için geçerli değilse, bu cmdlet mümkünse otomatik olarak çözer.</span><span class="sxs-lookup"><span data-stu-id="253c1-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="253c1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="253c1-111">EXAMPLES</span></span>

### <span data-ttu-id="253c1-112">Örnek 1: blob içeriğini ada göre Indirme</span><span class="sxs-lookup"><span data-stu-id="253c1-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="253c1-113">Bu komut, bir blob 'u adla indirir.</span><span class="sxs-lookup"><span data-stu-id="253c1-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="253c1-114">Örnek 2: ardışık düzeni kullanarak blob içeriğini Indirme</span><span class="sxs-lookup"><span data-stu-id="253c1-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="253c1-115">Bu komut, blob içeriğini bulmak ve indirmek için ardışık düzeni kullanır.</span><span class="sxs-lookup"><span data-stu-id="253c1-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="253c1-116">Örnek 3: ardışık düzen ve joker karakter kullanarak blob içeriği Indirin</span><span class="sxs-lookup"><span data-stu-id="253c1-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="253c1-117">Bu örnekte, blob içeriğini bulmak ve indirmek için joker karakter ve ardışık düzen kullanılır.</span><span class="sxs-lookup"><span data-stu-id="253c1-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="253c1-118">Örnek 4: blob nesnesi alma ve bir değişkene kaydetme, ardından blob nesnesini blob nesnesiyle indirme</span><span class="sxs-lookup"><span data-stu-id="253c1-118">Example 4: Get a blob object and save it in a variable, then download blob content with the blob object</span></span>
```
PS C:\>$blob = Get-AzStorageBlob -Container containername -Blob blobname 
PS C:\>Get-AzStorageBlobContent -CloudBlob $blob.ICloudBlob -Destination "C:\test"
```

<span data-ttu-id="253c1-119">Bu örnekte, önce bir blob nesnesi alın ve bir değişkene kaydedin, ardından blob nesnesini blob nesnesiyle indirin.</span><span class="sxs-lookup"><span data-stu-id="253c1-119">This example first get a blob object and save it in a variable, then download blob content with the blob object.</span></span> 

## <span data-ttu-id="253c1-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="253c1-120">PARAMETERS</span></span>

### <span data-ttu-id="253c1-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="253c1-121">-AsJob</span></span>
<span data-ttu-id="253c1-122">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="253c1-122">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="253c1-123">-Blob</span><span class="sxs-lookup"><span data-stu-id="253c1-123">-Blob</span></span>
<span data-ttu-id="253c1-124">İndirilecek olan blob 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="253c1-124">Specifies the name of the blob to be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="253c1-125">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="253c1-125">-CheckMd5</span></span>
<span data-ttu-id="253c1-126">İndirilen dosyanın MD5 toplamının olup olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="253c1-126">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="253c1-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="253c1-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="253c1-128">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="253c1-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="253c1-129">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="253c1-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="253c1-130">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="253c1-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="253c1-131">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="253c1-131">-CloudBlob</span></span>
<span data-ttu-id="253c1-132">Bulut blob 'unu belirtir.</span><span class="sxs-lookup"><span data-stu-id="253c1-132">Specifies a cloud blob.</span></span>
<span data-ttu-id="253c1-133">**Cloudblob** nesnesi edinmek için Get-AzStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="253c1-133">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="253c1-134">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="253c1-134">-CloudBlobContainer</span></span>
<span data-ttu-id="253c1-135">Azure depolama istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="253c1-135">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="253c1-136">Bunu oluşturabilir veya Get-AzStorageContainer cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="253c1-136">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="253c1-137">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="253c1-137">-ConcurrentTaskCount</span></span>
<span data-ttu-id="253c1-138">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="253c1-138">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="253c1-139">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="253c1-139">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="253c1-140">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="253c1-140">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="253c1-141">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="253c1-141">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="253c1-142">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="253c1-142">The default value is 10.</span></span>

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

### <span data-ttu-id="253c1-143">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="253c1-143">-Container</span></span>
<span data-ttu-id="253c1-144">Yüklemek istediğiniz blob 'u içeren kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="253c1-144">Specifies the name of container that has the blob you want to download.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="253c1-145">-Context</span><span class="sxs-lookup"><span data-stu-id="253c1-145">-Context</span></span>
<span data-ttu-id="253c1-146">Blob içeriğini indirmek istediğiniz Azure Depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="253c1-146">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="253c1-147">Depolama bağlamı oluşturmak için New-AzStorageContext cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="253c1-147">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="253c1-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="253c1-148">-DefaultProfile</span></span>
<span data-ttu-id="253c1-149">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="253c1-149">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="253c1-150">-Hedef</span><span class="sxs-lookup"><span data-stu-id="253c1-150">-Destination</span></span>
<span data-ttu-id="253c1-151">İndirilen dosyanın depolanacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="253c1-151">Specifies the location to store the downloaded file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="253c1-152">-Force</span><span class="sxs-lookup"><span data-stu-id="253c1-152">-Force</span></span>
<span data-ttu-id="253c1-153">Mevcut bir dosyanın üzerine onay olmadan yazar.</span><span class="sxs-lookup"><span data-stu-id="253c1-153">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="253c1-154">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="253c1-154">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="253c1-155">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="253c1-155">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="253c1-156">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="253c1-156">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="253c1-157">-Onay</span><span class="sxs-lookup"><span data-stu-id="253c1-157">-Confirm</span></span>
<span data-ttu-id="253c1-158">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="253c1-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="253c1-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="253c1-159">-WhatIf</span></span>
<span data-ttu-id="253c1-160">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="253c1-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="253c1-161">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="253c1-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="253c1-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="253c1-162">CommonParameters</span></span>
<span data-ttu-id="253c1-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="253c1-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="253c1-164">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="253c1-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="253c1-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="253c1-165">INPUTS</span></span>

### <span data-ttu-id="253c1-166">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="253c1-166">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="253c1-167">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="253c1-167">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="253c1-168">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="253c1-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="253c1-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="253c1-169">OUTPUTS</span></span>

### <span data-ttu-id="253c1-170">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="253c1-170">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="253c1-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="253c1-171">NOTES</span></span>
* <span data-ttu-id="253c1-172">Blob adı yerel bilgisayar için geçersizse, bu cmdlet mümkünse otomatik olarak çözülür.</span><span class="sxs-lookup"><span data-stu-id="253c1-172">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="253c1-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="253c1-173">RELATED LINKS</span></span>

[<span data-ttu-id="253c1-174">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="253c1-174">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="253c1-175">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="253c1-175">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="253c1-176">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="253c1-176">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
