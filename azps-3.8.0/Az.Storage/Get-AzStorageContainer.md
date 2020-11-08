---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
ms.openlocfilehash: 0c26899b772fd21772b625cb057e141071767002
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096717"
---
# <span data-ttu-id="fb94b-101">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fb94b-101">Get-AzStorageContainer</span></span>

## <span data-ttu-id="fb94b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb94b-102">SYNOPSIS</span></span>
<span data-ttu-id="fb94b-103">Depolama kapsayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="fb94b-103">Lists the storage containers.</span></span>

## <span data-ttu-id="fb94b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb94b-104">SYNTAX</span></span>

### <span data-ttu-id="fb94b-105">Kapsayıcıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fb94b-105">ContainerName (Default)</span></span>
```
Get-AzStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="fb94b-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="fb94b-106">ContainerPrefix</span></span>
```
Get-AzStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="fb94b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb94b-107">DESCRIPTION</span></span>
<span data-ttu-id="fb94b-108">**Get-AzStorageContainer** cmdlet 'ı, Azure 'daki depolama hesabıyla ilişkilendirilmiş depolama kapsayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="fb94b-108">The **Get-AzStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="fb94b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb94b-109">EXAMPLES</span></span>

### <span data-ttu-id="fb94b-110">Örnek 1: Azure depolama blob 'unu ada göre alma</span><span class="sxs-lookup"><span data-stu-id="fb94b-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzStorageContainer -Name container*
```

<span data-ttu-id="fb94b-111">Bu örnekte, kapsayıcıyla başlayan tüm kapsayıcıların listesini döndürmek için joker karakter kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fb94b-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="fb94b-112">Örnek 2: kapsayıcı adı önekine göre Azure depolama kapsayıcısını alma</span><span class="sxs-lookup"><span data-stu-id="fb94b-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzStorageContainer -Prefix "container"
```

<span data-ttu-id="fb94b-113">Bu örnek, konteynerle başlayan bir ada sahip tüm kapsayıcıların listesini döndürmek için *önek* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="fb94b-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="fb94b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb94b-114">PARAMETERS</span></span>

### <span data-ttu-id="fb94b-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fb94b-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fb94b-116">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb94b-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fb94b-117">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="fb94b-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fb94b-118">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="fb94b-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fb94b-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fb94b-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fb94b-120">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb94b-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fb94b-121">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb94b-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fb94b-122">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="fb94b-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fb94b-123">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="fb94b-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fb94b-124">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="fb94b-124">The default value is 10.</span></span>

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

### <span data-ttu-id="fb94b-125">-Context</span><span class="sxs-lookup"><span data-stu-id="fb94b-125">-Context</span></span>
<span data-ttu-id="fb94b-126">Depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb94b-126">Specifies the storage context.</span></span>
<span data-ttu-id="fb94b-127">Bunu oluşturmak için New-AzStorageContext cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb94b-127">To create it, you can use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="fb94b-128">Erişim kapsayıcısı izinleri depolama hesabı anahtarı izni gerektirdiğinden, SAS belirtecinden oluşturulan bir depolama bağlamını kullandığınızda kapsayıcı izinleri alınmaz.</span><span class="sxs-lookup"><span data-stu-id="fb94b-128">The container permissions won't be retrieved when you use a storage context created from SAS Token, because query container permissions requires Storage account key permission.</span></span>

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

### <span data-ttu-id="fb94b-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="fb94b-129">-ContinuationToken</span></span>
<span data-ttu-id="fb94b-130">Blob listesi için bir devam belirteci belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb94b-130">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb94b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb94b-131">-DefaultProfile</span></span>
<span data-ttu-id="fb94b-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb94b-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb94b-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="fb94b-133">-MaxCount</span></span>
<span data-ttu-id="fb94b-134">Bu cmdlet 'in döndürdüğü en fazla nesne sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb94b-134">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="fb94b-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="fb94b-135">-Name</span></span>
<span data-ttu-id="fb94b-136">Kapsayıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb94b-136">Specifies the container name.</span></span>
<span data-ttu-id="fb94b-137">Kapsayıcı adı boşsa, cmdlet tüm kapsayıcıları listeler.</span><span class="sxs-lookup"><span data-stu-id="fb94b-137">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="fb94b-138">Aksi halde, belirtilen ad veya normal Ad düzeniyle eşleşen tüm kapsayıcıları listeler.</span><span class="sxs-lookup"><span data-stu-id="fb94b-138">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb94b-139">-Önek</span><span class="sxs-lookup"><span data-stu-id="fb94b-139">-Prefix</span></span>
<span data-ttu-id="fb94b-140">Almak istediğiniz kapsayıcının veya kapsayıcıların adında kullanılan bir önek belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb94b-140">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="fb94b-141">"My" veya "test" gibi aynı dizeyle başlayan tüm kapsayıcıları bulmak için bunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb94b-141">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb94b-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fb94b-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fb94b-143">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb94b-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="fb94b-144">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="fb94b-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="fb94b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb94b-145">CommonParameters</span></span>
<span data-ttu-id="fb94b-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb94b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb94b-147">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb94b-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb94b-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb94b-148">INPUTS</span></span>

### <span data-ttu-id="fb94b-149">System. String</span><span class="sxs-lookup"><span data-stu-id="fb94b-149">System.String</span></span>

### <span data-ttu-id="fb94b-150">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="fb94b-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fb94b-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb94b-151">OUTPUTS</span></span>

### <span data-ttu-id="fb94b-152">Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fb94b-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="fb94b-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb94b-153">NOTES</span></span>

## <span data-ttu-id="fb94b-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb94b-154">RELATED LINKS</span></span>

[<span data-ttu-id="fb94b-155">Yeni-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fb94b-155">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="fb94b-156">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fb94b-156">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="fb94b-157">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="fb94b-157">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)

