---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblobcontent
schema: 2.0.0
ms.openlocfilehash: 4b48e4c2e1184c26fd7b50a05e979fad1a61bf3b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939447"
---
# <span data-ttu-id="605cf-101">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="605cf-101">Get-AzureStorageBlobContent</span></span>

## <span data-ttu-id="605cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="605cf-102">SYNOPSIS</span></span>
<span data-ttu-id="605cf-103">Bir Depolama Blobu yükler.</span><span class="sxs-lookup"><span data-stu-id="605cf-103">Downloads a storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="605cf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="605cf-104">SYNTAX</span></span>

### <span data-ttu-id="605cf-105">ReceiveManual (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="605cf-105">ReceiveManual (Default)</span></span>
```
Get-AzureStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="605cf-106">Blobboru hattı</span><span class="sxs-lookup"><span data-stu-id="605cf-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="605cf-107">Kapsayıcı boru hattı</span><span class="sxs-lookup"><span data-stu-id="605cf-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="605cf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="605cf-108">DESCRIPTION</span></span>
<span data-ttu-id="605cf-109">**Get-AzureStorageBlobContent** cmdlet 'i belirtilen depolama blobundan indirir.</span><span class="sxs-lookup"><span data-stu-id="605cf-109">The **Get-AzureStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="605cf-110">Blob adı yerel bilgisayar için geçerli değilse, bu cmdlet mümkünse otomatik olarak çözer.</span><span class="sxs-lookup"><span data-stu-id="605cf-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="605cf-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="605cf-111">EXAMPLES</span></span>

### <span data-ttu-id="605cf-112">Örnek 1: blob içeriğini ada göre Indirme</span><span class="sxs-lookup"><span data-stu-id="605cf-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzureStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="605cf-113">Bu komut, bir blob 'u adla indirir.</span><span class="sxs-lookup"><span data-stu-id="605cf-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="605cf-114">Örnek 2: ardışık düzeni kullanarak blob içeriğini Indirme</span><span class="sxs-lookup"><span data-stu-id="605cf-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container containername -Blob blobname | Get-AzureStorageBlobContent
```

<span data-ttu-id="605cf-115">Bu komut, blob içeriğini bulmak ve indirmek için ardışık düzeni kullanır.</span><span class="sxs-lookup"><span data-stu-id="605cf-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="605cf-116">Örnek 3: ardışık düzen ve joker karakter kullanarak blob içeriği Indirin</span><span class="sxs-lookup"><span data-stu-id="605cf-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Get-AzureStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="605cf-117">Bu örnekte, blob içeriğini bulmak ve indirmek için joker karakter ve ardışık düzen kullanılır.</span><span class="sxs-lookup"><span data-stu-id="605cf-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

## <span data-ttu-id="605cf-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="605cf-118">PARAMETERS</span></span>

### <span data-ttu-id="605cf-119">-Blob</span><span class="sxs-lookup"><span data-stu-id="605cf-119">-Blob</span></span>
<span data-ttu-id="605cf-120">İndirilecek olan blob 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="605cf-120">Specifies the name of the blob to be downloaded.</span></span>

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

### <span data-ttu-id="605cf-121">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="605cf-121">-CheckMd5</span></span>
<span data-ttu-id="605cf-122">İndirilen dosyanın MD5 toplamının olup olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="605cf-122">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="605cf-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="605cf-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="605cf-124">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="605cf-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="605cf-125">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="605cf-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="605cf-126">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="605cf-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="605cf-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="605cf-127">-CloudBlob</span></span>
<span data-ttu-id="605cf-128">Bulut blob 'unu belirtir.</span><span class="sxs-lookup"><span data-stu-id="605cf-128">Specifies a cloud blob.</span></span>
<span data-ttu-id="605cf-129">**Cloudblob** nesnesi edinmek için Get-AzureStorageBlob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="605cf-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="605cf-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="605cf-130">-CloudBlobContainer</span></span>
<span data-ttu-id="605cf-131">Azure depolama istemci kitaplığından bir **Cloudblobcontainer** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="605cf-131">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="605cf-132">Bunu oluşturabilir veya Get-AzureStorageContainer cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="605cf-132">You can create it or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="605cf-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="605cf-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="605cf-134">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="605cf-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="605cf-135">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="605cf-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="605cf-136">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="605cf-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="605cf-137">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="605cf-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="605cf-138">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="605cf-138">The default value is 10.</span></span>
<span data-ttu-id="605cf-139">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="605cf-139">The default value is 10.</span></span>

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

### <span data-ttu-id="605cf-140">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="605cf-140">-Container</span></span>
<span data-ttu-id="605cf-141">Yüklemek istediğiniz blob 'u içeren kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="605cf-141">Specifies the name of container that has the blob you want to download.</span></span>

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

### <span data-ttu-id="605cf-142">-Context</span><span class="sxs-lookup"><span data-stu-id="605cf-142">-Context</span></span>
<span data-ttu-id="605cf-143">Blob içeriğini indirmek istediğiniz Azure Depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="605cf-143">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="605cf-144">Depolama bağlamı oluşturmak için New-AzureStorageContext cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="605cf-144">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="605cf-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="605cf-145">-DefaultProfile</span></span>
<span data-ttu-id="605cf-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="605cf-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="605cf-147">-Hedef</span><span class="sxs-lookup"><span data-stu-id="605cf-147">-Destination</span></span>
<span data-ttu-id="605cf-148">İndirilen dosyanın depolanacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="605cf-148">Specifies the location to store the downloaded file.</span></span>

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

### <span data-ttu-id="605cf-149">-Force</span><span class="sxs-lookup"><span data-stu-id="605cf-149">-Force</span></span>
<span data-ttu-id="605cf-150">Mevcut bir dosyanın üzerine onay olmadan yazar.</span><span class="sxs-lookup"><span data-stu-id="605cf-150">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="605cf-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="605cf-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="605cf-152">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="605cf-152">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="605cf-153">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="605cf-153">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="605cf-154">-Onay</span><span class="sxs-lookup"><span data-stu-id="605cf-154">-Confirm</span></span>
<span data-ttu-id="605cf-155">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="605cf-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="605cf-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="605cf-156">-WhatIf</span></span>
<span data-ttu-id="605cf-157">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="605cf-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="605cf-158">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="605cf-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="605cf-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="605cf-159">CommonParameters</span></span>
<span data-ttu-id="605cf-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="605cf-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="605cf-161">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="605cf-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="605cf-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="605cf-162">INPUTS</span></span>

### <span data-ttu-id="605cf-163">Microsoft. Windowsazde. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="605cf-163">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="605cf-164">Microsoft. Windowsazde. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="605cf-164">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="605cf-165">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="605cf-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="605cf-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="605cf-166">OUTPUTS</span></span>

### <span data-ttu-id="605cf-167">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="605cf-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="605cf-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="605cf-168">NOTES</span></span>
* <span data-ttu-id="605cf-169">Blob adı yerel bilgisayar için geçersizse, bu cmdlet mümkünse otomatik olarak çözülür.</span><span class="sxs-lookup"><span data-stu-id="605cf-169">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="605cf-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="605cf-170">RELATED LINKS</span></span>

[<span data-ttu-id="605cf-171">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="605cf-171">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)

[<span data-ttu-id="605cf-172">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="605cf-172">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="605cf-173">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="605cf-173">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)