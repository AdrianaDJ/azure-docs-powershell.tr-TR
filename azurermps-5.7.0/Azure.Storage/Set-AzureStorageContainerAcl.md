---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerAcl.md
ms.openlocfilehash: 5cfd42ebbdae85d59bf6715f41ffbe99911ec35c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592144"
---
# <span data-ttu-id="24e09-101">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="24e09-101">Set-AzureStorageContainerAcl</span></span>

## <span data-ttu-id="24e09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24e09-102">SYNOPSIS</span></span>
<span data-ttu-id="24e09-103">Bir depolama kapsayıcısına genel erişim iznini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="24e09-103">Sets the public access permission to a storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24e09-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24e09-104">SYNTAX</span></span>

```
Set-AzureStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="24e09-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="24e09-105">DESCRIPTION</span></span>
<span data-ttu-id="24e09-106">**Set-AzureStorageContainerAcl** cmdlet 'i, genel erişim iznini Azure 'da belirtilen depolama kapsayıcısına ayarlar.</span><span class="sxs-lookup"><span data-stu-id="24e09-106">The **Set-AzureStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="24e09-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24e09-107">EXAMPLES</span></span>

### <span data-ttu-id="24e09-108">Örnek 1: Azure depolama kapsayıcısı ACL 'sini ada göre ayarlama</span><span class="sxs-lookup"><span data-stu-id="24e09-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzureStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="24e09-109">Bu komut, genel erişimi olmayan bir kapsayıcı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="24e09-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="24e09-110">Örnek 2: ardışık düzeni kullanarak Azure depolama kapsayıcısı ACL 'sini ayarlama</span><span class="sxs-lookup"><span data-stu-id="24e09-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Set-AzureStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="24e09-111">Bu komut, adı konteynerle başlayan tüm depolama kapsayıcılarını alır ve ardından tüm bunları blob erişimine izin verecek şekilde sonucu ardışık düzene geçirir.</span><span class="sxs-lookup"><span data-stu-id="24e09-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="24e09-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24e09-112">PARAMETERS</span></span>

### <span data-ttu-id="24e09-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="24e09-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="24e09-114">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="24e09-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="24e09-115">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="24e09-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="24e09-116">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="24e09-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="24e09-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="24e09-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="24e09-118">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24e09-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="24e09-119">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="24e09-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="24e09-120">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="24e09-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="24e09-121">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="24e09-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="24e09-122">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="24e09-122">The default value is 10.</span></span>

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

### <span data-ttu-id="24e09-123">-Context</span><span class="sxs-lookup"><span data-stu-id="24e09-123">-Context</span></span>
<span data-ttu-id="24e09-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24e09-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="24e09-125">Bunu, New-AzureStorageContext cmdlet 'ini kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="24e09-125">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="24e09-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="24e09-126">-Name</span></span>
<span data-ttu-id="24e09-127">Kapsayıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24e09-127">Specifies a container name.</span></span>

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

### <span data-ttu-id="24e09-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="24e09-128">-PassThru</span></span>
<span data-ttu-id="24e09-129">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="24e09-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="24e09-130">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="24e09-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="24e09-131">-İzin</span><span class="sxs-lookup"><span data-stu-id="24e09-131">-Permission</span></span>
<span data-ttu-id="24e09-132">Bu kapsayıcıya genel erişim düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="24e09-132">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="24e09-133">Varsayılan olarak, kapsayıcı ve içindeki blob 'lar yalnızca depolama hesabının sahibi tarafından erişilebilir.</span><span class="sxs-lookup"><span data-stu-id="24e09-133">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="24e09-134">Anonim kullanıcılara bir kapsayıcıya ve BLOB kullanıcılarına okuma izinleri vermek için, kapsayıcı izinlerini genel erişimi etkinleştirecek şekilde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="24e09-134">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="24e09-135">Anonim kullanıcılar, isteği doğrulamadan, genel kullanıma yönelik kapsayıcıda blob okuyabilir.</span><span class="sxs-lookup"><span data-stu-id="24e09-135">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="24e09-136">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="24e09-136">The acceptable values for this parameter are:</span></span>

<span data-ttu-id="24e09-137">--Container.</span><span class="sxs-lookup"><span data-stu-id="24e09-137">--Container.</span></span>
<span data-ttu-id="24e09-138">Bir kapsayıcıya ve blobilerine tam okuma erişimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="24e09-138">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="24e09-139">İstemciler, anonim istek aracılığıyla kapsayıcıdaki blob 'ları numaralandırır, ancak depolama hesabındaki kapsayıcıları numaralandıramaz.</span><span class="sxs-lookup"><span data-stu-id="24e09-139">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="24e09-140">--BLOB.</span><span class="sxs-lookup"><span data-stu-id="24e09-140">--Blob.</span></span>
<span data-ttu-id="24e09-141">Anonim istek aracılığıyla kapsayıcıda blob verilerine okuma erişimi sağlar, ancak kapsayıcı verilerine erişim sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="24e09-141">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="24e09-142">İstemciler anonim istek kullanılarak kapsayıcıdaki blob 'ları numaralandıramaz.</span><span class="sxs-lookup"><span data-stu-id="24e09-142">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="24e09-143">--Off.</span><span class="sxs-lookup"><span data-stu-id="24e09-143">--Off.</span></span>
<span data-ttu-id="24e09-144">Erişimi yalnızca depolama hesabı sahibine kısıtlar.</span><span class="sxs-lookup"><span data-stu-id="24e09-144">Restricts access to only the storage account owner.</span></span>

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

### <span data-ttu-id="24e09-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="24e09-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="24e09-146">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24e09-146">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="24e09-147">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="24e09-147">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="24e09-148">Her istek için sunucu tarafı zaman aşımı.</span><span class="sxs-lookup"><span data-stu-id="24e09-148">Server side time out for each request.</span></span>

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

### <span data-ttu-id="24e09-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24e09-149">CommonParameters</span></span>
<span data-ttu-id="24e09-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24e09-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24e09-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24e09-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24e09-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24e09-152">INPUTS</span></span>

### <span data-ttu-id="24e09-153">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="24e09-153">IStorageContext</span></span>

<span data-ttu-id="24e09-154">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="24e09-154">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="24e09-155">Dizisi</span><span class="sxs-lookup"><span data-stu-id="24e09-155">String</span></span>

<span data-ttu-id="24e09-156">' Name ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="24e09-156">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="24e09-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24e09-157">OUTPUTS</span></span>

### <span data-ttu-id="24e09-158">Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="24e09-158">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="24e09-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24e09-159">NOTES</span></span>

## <span data-ttu-id="24e09-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24e09-160">RELATED LINKS</span></span>

[<span data-ttu-id="24e09-161">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="24e09-161">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="24e09-162">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="24e09-162">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="24e09-163">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="24e09-163">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)


