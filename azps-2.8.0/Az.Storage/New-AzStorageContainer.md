---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: c4e3ba53ccb583b72001bfdfcc08c15025eda0da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934198"
---
# <span data-ttu-id="9ebe6-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9ebe6-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="9ebe6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ebe6-102">SYNOPSIS</span></span>
<span data-ttu-id="9ebe6-103">Azure depolama kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="9ebe6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ebe6-104">SYNTAX</span></span>

```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="9ebe6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ebe6-105">DESCRIPTION</span></span>
<span data-ttu-id="9ebe6-106">**New-AzStorageContainer** cmdlet 'ı bir Azure depolama kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-106">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="9ebe6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ebe6-107">EXAMPLES</span></span>

### <span data-ttu-id="9ebe6-108">Örnek 1: Azure depolama kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="9ebe6-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="9ebe6-109">Bu komut bir depolama kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-109">This command creates a storage container.</span></span>

### <span data-ttu-id="9ebe6-110">Örnek 2: birden çok Azure depolama konteyneri oluşturma</span><span class="sxs-lookup"><span data-stu-id="9ebe6-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="9ebe6-111">Bu örnek, birden çok depolama konteyneri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="9ebe6-112">.NET **String** sınıfının **bölme** yöntemini kullanır ve sonra da ardışık düzene geçirir.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="9ebe6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ebe6-113">PARAMETERS</span></span>

### <span data-ttu-id="9ebe6-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9ebe6-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9ebe6-115">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9ebe6-116">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9ebe6-117">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9ebe6-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9ebe6-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9ebe6-119">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9ebe6-120">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9ebe6-121">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9ebe6-122">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9ebe6-123">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-123">The default value is 10.</span></span>

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

### <span data-ttu-id="9ebe6-124">-Context</span><span class="sxs-lookup"><span data-stu-id="9ebe6-124">-Context</span></span>
<span data-ttu-id="9ebe6-125">Yeni kapsayıcı için bağlam belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-125">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="9ebe6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ebe6-126">-DefaultProfile</span></span>
<span data-ttu-id="9ebe6-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ebe6-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="9ebe6-128">-Name</span></span>
<span data-ttu-id="9ebe6-129">Yeni kapsayıcı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-129">Specifies a name for the new container.</span></span>

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

### <span data-ttu-id="9ebe6-130">-İzin</span><span class="sxs-lookup"><span data-stu-id="9ebe6-130">-Permission</span></span>
<span data-ttu-id="9ebe6-131">Bu kapsayıcıya genel erişim düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-131">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="9ebe6-132">Varsayılan olarak, kapsayıcı ve içindeki blob 'lar yalnızca depolama hesabının sahibi tarafından erişilebilir.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-132">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="9ebe6-133">Anonim kullanıcılara bir kapsayıcıya ve BLOB kullanıcılarına okuma izinleri vermek için, kapsayıcı izinlerini genel erişimi etkinleştirecek şekilde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-133">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="9ebe6-134">Anonim kullanıcılar, isteği doğrulamadan, genel kullanıma yönelik kapsayıcıda blob okuyabilir.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-134">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="9ebe6-135">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9ebe6-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9ebe6-136">Kapsayıcıdaki.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-136">Container.</span></span>
<span data-ttu-id="9ebe6-137">Bir kapsayıcıya ve blobilerine tam okuma erişimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-137">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="9ebe6-138">İstemciler, anonim istek aracılığıyla kapsayıcıdaki blob 'ları numaralandırır, ancak depolama hesabındaki kapsayıcıları numaralandıramaz.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-138">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="9ebe6-139">'Unu.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-139">Blob.</span></span>
<span data-ttu-id="9ebe6-140">Anonim istek aracılığıyla kapsayıcı verilerine okuma erişimi sağlar, ancak kapsayıcı verilerine erişim sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-140">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="9ebe6-141">İstemciler anonim istek kullanılarak kapsayıcıdaki blob 'ları numaralandıramaz.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-141">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="9ebe6-142">Kapatmayı.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-142">Off.</span></span>
<span data-ttu-id="9ebe6-143">Yalnızca depolama hesabı sahibine erişimi kısıtlar.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-143">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType]
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ebe6-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9ebe6-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9ebe6-145">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-145">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="9ebe6-146">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-146">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="9ebe6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ebe6-147">CommonParameters</span></span>
<span data-ttu-id="9ebe6-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ebe6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ebe6-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ebe6-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ebe6-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ebe6-150">INPUTS</span></span>

### <span data-ttu-id="9ebe6-151">System. String</span><span class="sxs-lookup"><span data-stu-id="9ebe6-151">System.String</span></span>

### <span data-ttu-id="9ebe6-152">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="9ebe6-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9ebe6-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ebe6-153">OUTPUTS</span></span>

### <span data-ttu-id="9ebe6-154">Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9ebe6-154">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="9ebe6-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ebe6-155">NOTES</span></span>

## <span data-ttu-id="9ebe6-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ebe6-156">RELATED LINKS</span></span>

[<span data-ttu-id="9ebe6-157">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9ebe6-157">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="9ebe6-158">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9ebe6-158">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="9ebe6-159">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="9ebe6-159">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)

