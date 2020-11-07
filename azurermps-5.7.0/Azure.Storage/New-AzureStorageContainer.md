---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainer.md
ms.openlocfilehash: 27442311630bf57f9424d940397f4fc8ef0655fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763304"
---
# <span data-ttu-id="7d225-101">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7d225-101">New-AzureStorageContainer</span></span>

## <span data-ttu-id="7d225-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d225-102">SYNOPSIS</span></span>
<span data-ttu-id="7d225-103">Azure depolama kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7d225-103">Creates an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d225-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7d225-104">SYNTAX</span></span>

```
New-AzureStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="7d225-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7d225-105">DESCRIPTION</span></span>
<span data-ttu-id="7d225-106">**New-AzureStorageContainer** cmdlet 'ı bir Azure depolama kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7d225-106">The **New-AzureStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="7d225-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7d225-107">EXAMPLES</span></span>

### <span data-ttu-id="7d225-108">Örnek 1: Azure depolama kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="7d225-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzureStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="7d225-109">Bu komut bir depolama kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7d225-109">This command creates a storage container.</span></span>

### <span data-ttu-id="7d225-110">Örnek 2: birden çok Azure depolama konteyneri oluşturma</span><span class="sxs-lookup"><span data-stu-id="7d225-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzureStorageContainer -Permission Container
```

<span data-ttu-id="7d225-111">Bu örnek, birden çok depolama konteyneri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7d225-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="7d225-112">.NET **String** sınıfının **bölme** yöntemini kullanır ve sonra da ardışık düzene geçirir.</span><span class="sxs-lookup"><span data-stu-id="7d225-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="7d225-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7d225-113">PARAMETERS</span></span>

### <span data-ttu-id="7d225-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7d225-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7d225-115">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d225-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7d225-116">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="7d225-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7d225-117">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="7d225-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7d225-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7d225-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7d225-119">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d225-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7d225-120">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d225-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7d225-121">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="7d225-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7d225-122">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="7d225-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7d225-123">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="7d225-123">The default value is 10.</span></span>

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

### <span data-ttu-id="7d225-124">-Context</span><span class="sxs-lookup"><span data-stu-id="7d225-124">-Context</span></span>
<span data-ttu-id="7d225-125">Yeni kapsayıcı için bağlam belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d225-125">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="7d225-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="7d225-126">-Name</span></span>
<span data-ttu-id="7d225-127">Yeni kapsayıcı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d225-127">Specifies a name for the new container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d225-128">-İzin</span><span class="sxs-lookup"><span data-stu-id="7d225-128">-Permission</span></span>
<span data-ttu-id="7d225-129">Bu kapsayıcıya genel erişim düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d225-129">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="7d225-130">Varsayılan olarak, kapsayıcı ve içindeki blob 'lar yalnızca depolama hesabının sahibi tarafından erişilebilir.</span><span class="sxs-lookup"><span data-stu-id="7d225-130">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="7d225-131">Anonim kullanıcılara bir kapsayıcıya ve BLOB kullanıcılarına okuma izinleri vermek için, kapsayıcı izinlerini genel erişimi etkinleştirecek şekilde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d225-131">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="7d225-132">Anonim kullanıcılar, isteği doğrulamadan, genel kullanıma yönelik kapsayıcıda blob okuyabilir.</span><span class="sxs-lookup"><span data-stu-id="7d225-132">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="7d225-133">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7d225-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7d225-134">Kapsayıcıdaki.</span><span class="sxs-lookup"><span data-stu-id="7d225-134">Container.</span></span>
<span data-ttu-id="7d225-135">Bir kapsayıcıya ve blobilerine tam okuma erişimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="7d225-135">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="7d225-136">İstemciler, anonim istek aracılığıyla kapsayıcıdaki blob 'ları numaralandırır, ancak depolama hesabındaki kapsayıcıları numaralandıramaz.</span><span class="sxs-lookup"><span data-stu-id="7d225-136">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="7d225-137">'Unu.</span><span class="sxs-lookup"><span data-stu-id="7d225-137">Blob.</span></span>
<span data-ttu-id="7d225-138">Anonim istek aracılığıyla kapsayıcı verilerine okuma erişimi sağlar, ancak kapsayıcı verilerine erişim sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="7d225-138">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="7d225-139">İstemciler anonim istek kullanılarak kapsayıcıdaki blob 'ları numaralandıramaz.</span><span class="sxs-lookup"><span data-stu-id="7d225-139">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="7d225-140">Kapatmayı.</span><span class="sxs-lookup"><span data-stu-id="7d225-140">Off.</span></span>
<span data-ttu-id="7d225-141">Yalnızca depolama hesabı sahibine erişimi kısıtlar.</span><span class="sxs-lookup"><span data-stu-id="7d225-141">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d225-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7d225-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7d225-143">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d225-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="7d225-144">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="7d225-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="7d225-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d225-145">CommonParameters</span></span>
<span data-ttu-id="7d225-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7d225-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d225-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d225-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d225-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7d225-148">INPUTS</span></span>

### <span data-ttu-id="7d225-149">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="7d225-149">IStorageContext</span></span>

<span data-ttu-id="7d225-150">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7d225-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="7d225-151">Dizisi</span><span class="sxs-lookup"><span data-stu-id="7d225-151">String</span></span>

<span data-ttu-id="7d225-152">' Name ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7d225-152">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="7d225-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7d225-153">OUTPUTS</span></span>

### <span data-ttu-id="7d225-154">Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7d225-154">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="7d225-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7d225-155">NOTES</span></span>

## <span data-ttu-id="7d225-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7d225-156">RELATED LINKS</span></span>

[<span data-ttu-id="7d225-157">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7d225-157">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="7d225-158">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7d225-158">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="7d225-159">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="7d225-159">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)

