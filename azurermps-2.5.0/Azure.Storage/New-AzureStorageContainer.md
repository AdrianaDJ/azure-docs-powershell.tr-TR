---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainer
schema: 2.0.0
ms.openlocfilehash: 87967dbaaa57bb8050191ee1b20ebb5a760bc045
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939443"
---
# <span data-ttu-id="89937-101">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="89937-101">New-AzureStorageContainer</span></span>

## <span data-ttu-id="89937-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89937-102">SYNOPSIS</span></span>
<span data-ttu-id="89937-103">Azure depolama kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="89937-103">Creates an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89937-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89937-104">SYNTAX</span></span>

```
New-AzureStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="89937-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="89937-105">DESCRIPTION</span></span>
<span data-ttu-id="89937-106">**New-AzureStorageContainer** cmdlet 'ı bir Azure depolama kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="89937-106">The **New-AzureStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="89937-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89937-107">EXAMPLES</span></span>

### <span data-ttu-id="89937-108">Örnek 1: Azure depolama kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="89937-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzureStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="89937-109">Bu komut bir depolama kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="89937-109">This command creates a storage container.</span></span>

### <span data-ttu-id="89937-110">Örnek 2: birden çok Azure depolama konteyneri oluşturma</span><span class="sxs-lookup"><span data-stu-id="89937-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzureStorageContainer -Permission Container
```

<span data-ttu-id="89937-111">Bu örnek, birden çok depolama konteyneri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="89937-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="89937-112">.NET **String** sınıfının **bölme** yöntemini kullanır ve sonra da ardışık düzene geçirir.</span><span class="sxs-lookup"><span data-stu-id="89937-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="89937-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89937-113">PARAMETERS</span></span>

### <span data-ttu-id="89937-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="89937-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="89937-115">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="89937-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="89937-116">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="89937-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="89937-117">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="89937-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="89937-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="89937-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="89937-119">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89937-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="89937-120">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="89937-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="89937-121">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="89937-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="89937-122">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="89937-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="89937-123">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="89937-123">The default value is 10.</span></span>

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

### <span data-ttu-id="89937-124">-Context</span><span class="sxs-lookup"><span data-stu-id="89937-124">-Context</span></span>
<span data-ttu-id="89937-125">Yeni kapsayıcı için bağlam belirtir.</span><span class="sxs-lookup"><span data-stu-id="89937-125">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="89937-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89937-126">-DefaultProfile</span></span>
<span data-ttu-id="89937-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89937-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89937-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="89937-128">-Name</span></span>
<span data-ttu-id="89937-129">Yeni kapsayıcı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="89937-129">Specifies a name for the new container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89937-130">-İzin</span><span class="sxs-lookup"><span data-stu-id="89937-130">-Permission</span></span>
<span data-ttu-id="89937-131">Bu kapsayıcıya genel erişim düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="89937-131">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="89937-132">Varsayılan olarak, kapsayıcı ve içindeki blob 'lar yalnızca depolama hesabının sahibi tarafından erişilebilir.</span><span class="sxs-lookup"><span data-stu-id="89937-132">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="89937-133">Anonim kullanıcılara bir kapsayıcıya ve BLOB kullanıcılarına okuma izinleri vermek için, kapsayıcı izinlerini genel erişimi etkinleştirecek şekilde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="89937-133">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="89937-134">Anonim kullanıcılar, isteği doğrulamadan, genel kullanıma yönelik kapsayıcıda blob okuyabilir.</span><span class="sxs-lookup"><span data-stu-id="89937-134">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="89937-135">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="89937-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="89937-136">Kapsayıcıdaki.</span><span class="sxs-lookup"><span data-stu-id="89937-136">Container.</span></span>
<span data-ttu-id="89937-137">Bir kapsayıcıya ve blobilerine tam okuma erişimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="89937-137">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="89937-138">İstemciler, anonim istek aracılığıyla kapsayıcıdaki blob 'ları numaralandırır, ancak depolama hesabındaki kapsayıcıları numaralandıramaz.</span><span class="sxs-lookup"><span data-stu-id="89937-138">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="89937-139">'Unu.</span><span class="sxs-lookup"><span data-stu-id="89937-139">Blob.</span></span>
<span data-ttu-id="89937-140">Anonim istek aracılığıyla kapsayıcı verilerine okuma erişimi sağlar, ancak kapsayıcı verilerine erişim sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="89937-140">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="89937-141">İstemciler anonim istek kullanılarak kapsayıcıdaki blob 'ları numaralandıramaz.</span><span class="sxs-lookup"><span data-stu-id="89937-141">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="89937-142">Kapatmayı.</span><span class="sxs-lookup"><span data-stu-id="89937-142">Off.</span></span>
<span data-ttu-id="89937-143">Yalnızca depolama hesabı sahibine erişimi kısıtlar.</span><span class="sxs-lookup"><span data-stu-id="89937-143">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.Blob.BlobContainerPublicAccessType]
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89937-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="89937-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="89937-145">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89937-145">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="89937-146">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="89937-146">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="89937-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89937-147">CommonParameters</span></span>
<span data-ttu-id="89937-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89937-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89937-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89937-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89937-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89937-150">INPUTS</span></span>

### <span data-ttu-id="89937-151">System. String</span><span class="sxs-lookup"><span data-stu-id="89937-151">System.String</span></span>

### <span data-ttu-id="89937-152">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="89937-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="89937-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89937-153">OUTPUTS</span></span>

### <span data-ttu-id="89937-154">Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="89937-154">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="89937-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89937-155">NOTES</span></span>

## <span data-ttu-id="89937-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89937-156">RELATED LINKS</span></span>

[<span data-ttu-id="89937-157">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="89937-157">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="89937-158">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="89937-158">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="89937-159">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="89937-159">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


