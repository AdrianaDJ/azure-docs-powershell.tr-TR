---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: ''
schema: 2.0.0
ms.openlocfilehash: d80a8a75082503cf8cde9df7a779ca7f0d7d4b92
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572334"
---
# <span data-ttu-id="0be43-101">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0be43-101">New-AzureStorageContainer</span></span>

## <span data-ttu-id="0be43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0be43-102">SYNOPSIS</span></span>
<span data-ttu-id="0be43-103">Azure depolama kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0be43-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="0be43-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0be43-104">SYNTAX</span></span>

```
New-AzureStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="0be43-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0be43-105">DESCRIPTION</span></span>
<span data-ttu-id="0be43-106">**New-AzureStorageContainer** cmdlet 'ı bir Azure depolama kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0be43-106">The **New-AzureStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="0be43-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0be43-107">EXAMPLES</span></span>

### <span data-ttu-id="0be43-108">Örnek 1: Azure depolama kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="0be43-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzureStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="0be43-109">Bu komut bir depolama kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0be43-109">This command creates a storage container.</span></span>

### <span data-ttu-id="0be43-110">Örnek 2: birden çok Azure depolama konteyneri oluşturma</span><span class="sxs-lookup"><span data-stu-id="0be43-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzureStorageContainer -Permission Container
```

<span data-ttu-id="0be43-111">Bu örnek, birden çok depolama konteyneri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0be43-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="0be43-112">.NET **String** sınıfının **bölme** yöntemini kullanır ve sonra da ardışık düzene geçirir.</span><span class="sxs-lookup"><span data-stu-id="0be43-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="0be43-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0be43-113">PARAMETERS</span></span>

### <span data-ttu-id="0be43-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0be43-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0be43-115">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="0be43-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0be43-116">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="0be43-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0be43-117">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="0be43-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0be43-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0be43-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0be43-119">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0be43-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0be43-120">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0be43-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0be43-121">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="0be43-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0be43-122">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="0be43-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0be43-123">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="0be43-123">The default value is 10.</span></span>

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

### <span data-ttu-id="0be43-124">-Context</span><span class="sxs-lookup"><span data-stu-id="0be43-124">-Context</span></span>
<span data-ttu-id="0be43-125">Yeni kapsayıcı için bağlam belirtir.</span><span class="sxs-lookup"><span data-stu-id="0be43-125">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="0be43-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="0be43-126">-Name</span></span>
<span data-ttu-id="0be43-127">Yeni kapsayıcı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="0be43-127">Specifies a name for the new container.</span></span>

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

### <span data-ttu-id="0be43-128">-İzin</span><span class="sxs-lookup"><span data-stu-id="0be43-128">-Permission</span></span>
<span data-ttu-id="0be43-129">Bu kapsayıcıya genel erişim düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0be43-129">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="0be43-130">Varsayılan olarak, kapsayıcı ve içindeki blob 'lar yalnızca depolama hesabının sahibi tarafından erişilebilir.</span><span class="sxs-lookup"><span data-stu-id="0be43-130">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="0be43-131">Anonim kullanıcılara bir kapsayıcıya ve BLOB kullanıcılarına okuma izinleri vermek için, kapsayıcı izinlerini genel erişimi etkinleştirecek şekilde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0be43-131">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="0be43-132">Anonim kullanıcılar, isteği doğrulamadan, genel kullanıma yönelik kapsayıcıda blob okuyabilir.</span><span class="sxs-lookup"><span data-stu-id="0be43-132">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="0be43-133">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0be43-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0be43-134">Kapsayıcıdaki.</span><span class="sxs-lookup"><span data-stu-id="0be43-134">Container.</span></span>
<span data-ttu-id="0be43-135">Bir kapsayıcıya ve blobilerine tam okuma erişimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="0be43-135">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="0be43-136">İstemciler, anonim istek aracılığıyla kapsayıcıdaki blob 'ları numaralandırır, ancak depolama hesabındaki kapsayıcıları numaralandıramaz.</span><span class="sxs-lookup"><span data-stu-id="0be43-136">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="0be43-137">'Unu.</span><span class="sxs-lookup"><span data-stu-id="0be43-137">Blob.</span></span>
<span data-ttu-id="0be43-138">Anonim istek aracılığıyla kapsayıcı verilerine okuma erişimi sağlar, ancak kapsayıcı verilerine erişim sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="0be43-138">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="0be43-139">İstemciler anonim istek kullanılarak kapsayıcıdaki blob 'ları numaralandıramaz.</span><span class="sxs-lookup"><span data-stu-id="0be43-139">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="0be43-140">Kapatmayı.</span><span class="sxs-lookup"><span data-stu-id="0be43-140">Off.</span></span>
<span data-ttu-id="0be43-141">Yalnızca depolama hesabı sahibine erişimi kısıtlar.</span><span class="sxs-lookup"><span data-stu-id="0be43-141">Which restricts access to only the storage account owner.</span></span>

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

### <span data-ttu-id="0be43-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0be43-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0be43-143">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0be43-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="0be43-144">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="0be43-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="0be43-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0be43-145">CommonParameters</span></span>
<span data-ttu-id="0be43-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0be43-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0be43-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0be43-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0be43-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0be43-148">INPUTS</span></span>

## <span data-ttu-id="0be43-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0be43-149">OUTPUTS</span></span>

## <span data-ttu-id="0be43-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0be43-150">NOTES</span></span>

## <span data-ttu-id="0be43-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0be43-151">RELATED LINKS</span></span>

[<span data-ttu-id="0be43-152">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0be43-152">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="0be43-153">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0be43-153">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="0be43-154">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="0be43-154">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


