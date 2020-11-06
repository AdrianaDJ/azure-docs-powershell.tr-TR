---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: ''
schema: 2.0.0
ms.openlocfilehash: fa33f6ba457ad51504cc9005f70f0e4c8f529359
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572481"
---
# <span data-ttu-id="1487d-101">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="1487d-101">Set-AzureStorageContainerAcl</span></span>

## <span data-ttu-id="1487d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1487d-102">SYNOPSIS</span></span>
<span data-ttu-id="1487d-103">Bir depolama kapsayıcısına genel erişim iznini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1487d-103">Sets the public access permission to a storage container.</span></span>

## <span data-ttu-id="1487d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1487d-104">SYNTAX</span></span>

```
Set-AzureStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="1487d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1487d-105">DESCRIPTION</span></span>
<span data-ttu-id="1487d-106">**Set-AzureStorageContainerAcl** cmdlet 'i, genel erişim iznini Azure 'da belirtilen depolama kapsayıcısına ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1487d-106">The **Set-AzureStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="1487d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1487d-107">EXAMPLES</span></span>

### <span data-ttu-id="1487d-108">Örnek 1: Azure depolama kapsayıcısı ACL 'sini ada göre ayarlama</span><span class="sxs-lookup"><span data-stu-id="1487d-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzureStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="1487d-109">Bu komut, genel erişimi olmayan bir kapsayıcı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1487d-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="1487d-110">Örnek 2: ardışık düzeni kullanarak Azure depolama kapsayıcısı ACL 'sini ayarlama</span><span class="sxs-lookup"><span data-stu-id="1487d-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Set-AzureStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="1487d-111">Bu komut, adı konteynerle başlayan tüm depolama kapsayıcılarını alır ve ardından tüm bunları blob erişimine izin verecek şekilde sonucu ardışık düzene geçirir.</span><span class="sxs-lookup"><span data-stu-id="1487d-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="1487d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1487d-112">PARAMETERS</span></span>

### <span data-ttu-id="1487d-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1487d-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1487d-114">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="1487d-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1487d-115">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="1487d-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1487d-116">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="1487d-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1487d-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1487d-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1487d-118">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1487d-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1487d-119">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1487d-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1487d-120">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="1487d-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1487d-121">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="1487d-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1487d-122">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="1487d-122">The default value is 10.</span></span>

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

### <span data-ttu-id="1487d-123">-Context</span><span class="sxs-lookup"><span data-stu-id="1487d-123">-Context</span></span>
<span data-ttu-id="1487d-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1487d-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="1487d-125">Bunu, New-AzureStorageContext cmdlet 'ini kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1487d-125">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1487d-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="1487d-126">-Name</span></span>
<span data-ttu-id="1487d-127">Kapsayıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1487d-127">Specifies a container name.</span></span>

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

### <span data-ttu-id="1487d-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1487d-128">-PassThru</span></span>
<span data-ttu-id="1487d-129">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="1487d-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1487d-130">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="1487d-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1487d-131">-İzin</span><span class="sxs-lookup"><span data-stu-id="1487d-131">-Permission</span></span>
<span data-ttu-id="1487d-132">Bu kapsayıcıya genel erişim düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1487d-132">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="1487d-133">Varsayılan olarak, kapsayıcı ve içindeki blob 'lar yalnızca depolama hesabının sahibi tarafından erişilebilir.</span><span class="sxs-lookup"><span data-stu-id="1487d-133">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="1487d-134">Anonim kullanıcılara bir kapsayıcıya ve BLOB kullanıcılarına okuma izinleri vermek için, kapsayıcı izinlerini genel erişimi etkinleştirecek şekilde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1487d-134">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="1487d-135">Anonim kullanıcılar, isteği doğrulamadan, genel kullanıma yönelik kapsayıcıda blob okuyabilir.</span><span class="sxs-lookup"><span data-stu-id="1487d-135">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="1487d-136">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1487d-136">The acceptable values for this parameter are:</span></span>

<span data-ttu-id="1487d-137">--Container.</span><span class="sxs-lookup"><span data-stu-id="1487d-137">--Container.</span></span>
<span data-ttu-id="1487d-138">Bir kapsayıcıya ve blobilerine tam okuma erişimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="1487d-138">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="1487d-139">İstemciler, anonim istek aracılığıyla kapsayıcıdaki blob 'ları numaralandırır, ancak depolama hesabındaki kapsayıcıları numaralandıramaz.</span><span class="sxs-lookup"><span data-stu-id="1487d-139">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="1487d-140">--BLOB.</span><span class="sxs-lookup"><span data-stu-id="1487d-140">--Blob.</span></span>
<span data-ttu-id="1487d-141">Anonim istek aracılığıyla kapsayıcıda blob verilerine okuma erişimi sağlar, ancak kapsayıcı verilerine erişim sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="1487d-141">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="1487d-142">İstemciler anonim istek kullanılarak kapsayıcıdaki blob 'ları numaralandıramaz.</span><span class="sxs-lookup"><span data-stu-id="1487d-142">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="1487d-143">--Off.</span><span class="sxs-lookup"><span data-stu-id="1487d-143">--Off.</span></span>
<span data-ttu-id="1487d-144">Erişimi yalnızca depolama hesabı sahibine kısıtlar.</span><span class="sxs-lookup"><span data-stu-id="1487d-144">Restricts access to only the storage account owner.</span></span>

```yaml
Type: BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1487d-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1487d-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1487d-146">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1487d-146">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="1487d-147">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="1487d-147">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="1487d-148">Her istek için sunucu tarafı zaman aşımı.</span><span class="sxs-lookup"><span data-stu-id="1487d-148">Server side time out for each request.</span></span>

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

### <span data-ttu-id="1487d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1487d-149">CommonParameters</span></span>
<span data-ttu-id="1487d-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1487d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1487d-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1487d-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1487d-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1487d-152">INPUTS</span></span>

## <span data-ttu-id="1487d-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1487d-153">OUTPUTS</span></span>

## <span data-ttu-id="1487d-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1487d-154">NOTES</span></span>

## <span data-ttu-id="1487d-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1487d-155">RELATED LINKS</span></span>

[<span data-ttu-id="1487d-156">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1487d-156">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="1487d-157">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1487d-157">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="1487d-158">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1487d-158">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)


