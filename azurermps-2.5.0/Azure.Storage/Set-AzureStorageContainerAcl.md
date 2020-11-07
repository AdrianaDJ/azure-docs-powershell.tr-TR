---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragecontaineracl
schema: 2.0.0
ms.openlocfilehash: 95931b9aeb7c3b9f2869bc35115ab49a8aaf901f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938899"
---
# <span data-ttu-id="7bd3a-101">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="7bd3a-101">Set-AzureStorageContainerAcl</span></span>

## <span data-ttu-id="7bd3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bd3a-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd3a-103">Bir depolama kapsayıcısına genel erişim iznini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-103">Sets the public access permission to a storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bd3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7bd3a-104">SYNTAX</span></span>

```
Set-AzureStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="7bd3a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7bd3a-105">DESCRIPTION</span></span>
<span data-ttu-id="7bd3a-106">**Set-AzureStorageContainerAcl** cmdlet 'i, genel erişim iznini Azure 'da belirtilen depolama kapsayıcısına ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-106">The **Set-AzureStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="7bd3a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7bd3a-107">EXAMPLES</span></span>

### <span data-ttu-id="7bd3a-108">Örnek 1: Azure depolama kapsayıcısı ACL 'sini ada göre ayarlama</span><span class="sxs-lookup"><span data-stu-id="7bd3a-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzureStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="7bd3a-109">Bu komut, genel erişimi olmayan bir kapsayıcı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="7bd3a-110">Örnek 2: ardışık düzeni kullanarak Azure depolama kapsayıcısı ACL 'sini ayarlama</span><span class="sxs-lookup"><span data-stu-id="7bd3a-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Set-AzureStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="7bd3a-111">Bu komut, adı konteynerle başlayan tüm depolama kapsayıcılarını alır ve ardından tüm bunları blob erişimine izin verecek şekilde sonucu ardışık düzene geçirir.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="7bd3a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7bd3a-112">PARAMETERS</span></span>

### <span data-ttu-id="7bd3a-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7bd3a-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7bd3a-114">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7bd3a-115">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7bd3a-116">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7bd3a-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7bd3a-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7bd3a-118">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7bd3a-119">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7bd3a-120">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7bd3a-121">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7bd3a-122">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-122">The default value is 10.</span></span>

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

### <span data-ttu-id="7bd3a-123">-Context</span><span class="sxs-lookup"><span data-stu-id="7bd3a-123">-Context</span></span>
<span data-ttu-id="7bd3a-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="7bd3a-125">Bunu, New-AzureStorageContext cmdlet 'ini kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-125">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7bd3a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd3a-126">-DefaultProfile</span></span>
<span data-ttu-id="7bd3a-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bd3a-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="7bd3a-128">-Name</span></span>
<span data-ttu-id="7bd3a-129">Kapsayıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-129">Specifies a container name.</span></span>

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

### <span data-ttu-id="7bd3a-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7bd3a-130">-PassThru</span></span>
<span data-ttu-id="7bd3a-131">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7bd3a-132">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7bd3a-133">-İzin</span><span class="sxs-lookup"><span data-stu-id="7bd3a-133">-Permission</span></span>
<span data-ttu-id="7bd3a-134">Bu kapsayıcıya genel erişim düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-134">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="7bd3a-135">Varsayılan olarak, kapsayıcı ve içindeki blob 'lar yalnızca depolama hesabının sahibi tarafından erişilebilir.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-135">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="7bd3a-136">Anonim kullanıcılara bir kapsayıcıya ve BLOB kullanıcılarına okuma izinleri vermek için, kapsayıcı izinlerini genel erişimi etkinleştirecek şekilde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-136">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="7bd3a-137">Anonim kullanıcılar, isteği doğrulamadan, genel kullanıma yönelik kapsayıcıda blob okuyabilir.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-137">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="7bd3a-138">Bu parametre için kabul edilebilir değerler şunlardır:-Container.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-138">The acceptable values for this parameter are: --Container.</span></span>
<span data-ttu-id="7bd3a-139">Bir kapsayıcıya ve blobilerine tam okuma erişimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-139">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="7bd3a-140">İstemciler, anonim istek aracılığıyla kapsayıcıdaki blob 'ları numaralandırır, ancak depolama hesabındaki kapsayıcıları numaralandıramaz.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-140">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="7bd3a-141">--BLOB.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-141">--Blob.</span></span>
<span data-ttu-id="7bd3a-142">Anonim istek aracılığıyla kapsayıcıda blob verilerine okuma erişimi sağlar, ancak kapsayıcı verilerine erişim sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-142">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="7bd3a-143">İstemciler anonim istek kullanılarak kapsayıcıdaki blob 'ları numaralandıramaz.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-143">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="7bd3a-144">--Off.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-144">--Off.</span></span>
<span data-ttu-id="7bd3a-145">Erişimi yalnızca depolama hesabı sahibine kısıtlar.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-145">Restricts access to only the storage account owner.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd3a-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7bd3a-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7bd3a-147">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="7bd3a-148">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="7bd3a-149">Her istek için sunucu tarafı zaman aşımı.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-149">Server side time out for each request.</span></span>

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

### <span data-ttu-id="7bd3a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd3a-150">CommonParameters</span></span>
<span data-ttu-id="7bd3a-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd3a-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bd3a-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd3a-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7bd3a-153">INPUTS</span></span>

### <span data-ttu-id="7bd3a-154">System. String</span><span class="sxs-lookup"><span data-stu-id="7bd3a-154">System.String</span></span>

### <span data-ttu-id="7bd3a-155">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="7bd3a-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7bd3a-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7bd3a-156">OUTPUTS</span></span>

### <span data-ttu-id="7bd3a-157">Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7bd3a-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="7bd3a-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7bd3a-158">NOTES</span></span>

## <span data-ttu-id="7bd3a-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7bd3a-159">RELATED LINKS</span></span>

[<span data-ttu-id="7bd3a-160">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7bd3a-160">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="7bd3a-161">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7bd3a-161">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="7bd3a-162">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7bd3a-162">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)


