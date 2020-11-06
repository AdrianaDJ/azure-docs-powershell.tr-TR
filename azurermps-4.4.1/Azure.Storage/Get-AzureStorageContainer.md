---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: c94c9b9d04745fe22c8836be1858c59c253d4b63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592704"
---
# <span data-ttu-id="31d24-101">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="31d24-101">Get-AzureStorageContainer</span></span>

## <span data-ttu-id="31d24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31d24-102">SYNOPSIS</span></span>
<span data-ttu-id="31d24-103">Depolama kapsayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="31d24-103">Lists the storage containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31d24-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31d24-104">SYNTAX</span></span>

### <span data-ttu-id="31d24-105">Kapsayıcıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="31d24-105">ContainerName (Default)</span></span>
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="31d24-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="31d24-106">ContainerPrefix</span></span>
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="31d24-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="31d24-107">DESCRIPTION</span></span>
<span data-ttu-id="31d24-108">**Get-AzureStorageContainer** cmdlet 'ı, Azure 'daki depolama hesabıyla ilişkilendirilmiş depolama kapsayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="31d24-108">The **Get-AzureStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="31d24-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31d24-109">EXAMPLES</span></span>

### <span data-ttu-id="31d24-110">Örnek 1: Azure depolama blob 'unu ada göre alma</span><span class="sxs-lookup"><span data-stu-id="31d24-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container*
```

<span data-ttu-id="31d24-111">Bu örnekte, kapsayıcıyla başlayan tüm kapsayıcıların listesini döndürmek için joker karakter kullanılır.</span><span class="sxs-lookup"><span data-stu-id="31d24-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="31d24-112">Örnek 2: kapsayıcı adı önekine göre Azure depolama kapsayıcısını alma</span><span class="sxs-lookup"><span data-stu-id="31d24-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

<span data-ttu-id="31d24-113">Bu örnek, konteynerle başlayan bir ada sahip tüm kapsayıcıların listesini döndürmek için *önek* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="31d24-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="31d24-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31d24-114">PARAMETERS</span></span>

### <span data-ttu-id="31d24-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="31d24-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="31d24-116">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="31d24-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="31d24-117">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="31d24-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="31d24-118">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="31d24-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="31d24-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="31d24-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="31d24-120">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31d24-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="31d24-121">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="31d24-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="31d24-122">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="31d24-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="31d24-123">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="31d24-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="31d24-124">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="31d24-124">The default value is 10.</span></span>

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

### <span data-ttu-id="31d24-125">-Context</span><span class="sxs-lookup"><span data-stu-id="31d24-125">-Context</span></span>
<span data-ttu-id="31d24-126">Depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31d24-126">Specifies the storage context.</span></span>
<span data-ttu-id="31d24-127">Bunu oluşturmak için New-AzureStorageContext cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="31d24-127">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="31d24-128">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="31d24-128">-ContinuationToken</span></span>
<span data-ttu-id="31d24-129">Blob listesi için bir devam belirteci belirtir.</span><span class="sxs-lookup"><span data-stu-id="31d24-129">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31d24-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="31d24-130">-MaxCount</span></span>
<span data-ttu-id="31d24-131">Bu cmdlet 'in döndürdüğü en fazla nesne sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31d24-131">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="31d24-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="31d24-132">-Name</span></span>
<span data-ttu-id="31d24-133">Kapsayıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31d24-133">Specifies the container name.</span></span>
<span data-ttu-id="31d24-134">Kapsayıcı adı boşsa, cmdlet tüm kapsayıcıları listeler.</span><span class="sxs-lookup"><span data-stu-id="31d24-134">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="31d24-135">Aksi halde, belirtilen ad veya normal Ad düzeniyle eşleşen tüm kapsayıcıları listeler.</span><span class="sxs-lookup"><span data-stu-id="31d24-135">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="31d24-136">-Önek</span><span class="sxs-lookup"><span data-stu-id="31d24-136">-Prefix</span></span>
<span data-ttu-id="31d24-137">Almak istediğiniz kapsayıcının veya kapsayıcıların adında kullanılan bir önek belirtir.</span><span class="sxs-lookup"><span data-stu-id="31d24-137">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="31d24-138">"My" veya "test" gibi aynı dizeyle başlayan tüm kapsayıcıları bulmak için bunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="31d24-138">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

```yaml
Type: String
Parameter Sets: ContainerPrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31d24-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="31d24-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="31d24-140">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31d24-140">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="31d24-141">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="31d24-141">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="31d24-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31d24-142">CommonParameters</span></span>
<span data-ttu-id="31d24-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31d24-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31d24-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31d24-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31d24-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31d24-145">INPUTS</span></span>

### <span data-ttu-id="31d24-146">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="31d24-146">IStorageContext</span></span>

<span data-ttu-id="31d24-147">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="31d24-147">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="31d24-148">Dizisi</span><span class="sxs-lookup"><span data-stu-id="31d24-148">String</span></span>

<span data-ttu-id="31d24-149">' Name ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="31d24-149">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="31d24-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31d24-150">OUTPUTS</span></span>

### <span data-ttu-id="31d24-151">Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="31d24-151">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="31d24-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31d24-152">NOTES</span></span>

## <span data-ttu-id="31d24-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31d24-153">RELATED LINKS</span></span>

[<span data-ttu-id="31d24-154">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="31d24-154">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="31d24-155">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="31d24-155">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="31d24-156">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="31d24-156">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


