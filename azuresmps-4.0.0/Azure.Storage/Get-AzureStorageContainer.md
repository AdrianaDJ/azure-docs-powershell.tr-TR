---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66845678619a7777bbda9257aa208393b0fa178c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572386"
---
# <span data-ttu-id="44ea8-101">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="44ea8-101">Get-AzureStorageContainer</span></span>

## <span data-ttu-id="44ea8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="44ea8-103">Depolama kapsayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="44ea8-103">Lists the storage containers.</span></span>

## <span data-ttu-id="44ea8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="44ea8-104">SYNTAX</span></span>

### <span data-ttu-id="44ea8-105">Kapsayıcıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="44ea8-105">ContainerName (Default)</span></span>
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="44ea8-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="44ea8-106">ContainerPrefix</span></span>
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="44ea8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="44ea8-107">DESCRIPTION</span></span>
<span data-ttu-id="44ea8-108">**Get-AzureStorageContainer** cmdlet 'ı, Azure 'daki depolama hesabıyla ilişkilendirilmiş depolama kapsayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="44ea8-108">The **Get-AzureStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="44ea8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="44ea8-109">EXAMPLES</span></span>

### <span data-ttu-id="44ea8-110">Örnek 1: Azure depolama blob 'unu ada göre alma</span><span class="sxs-lookup"><span data-stu-id="44ea8-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container*
```

<span data-ttu-id="44ea8-111">Bu örnekte, kapsayıcıyla başlayan tüm kapsayıcıların listesini döndürmek için joker karakter kullanılır.</span><span class="sxs-lookup"><span data-stu-id="44ea8-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="44ea8-112">Örnek 2: kapsayıcı adı önekine göre Azure depolama kapsayıcısını alma</span><span class="sxs-lookup"><span data-stu-id="44ea8-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

<span data-ttu-id="44ea8-113">Bu örnek, konteynerle başlayan bir ada sahip tüm kapsayıcıların listesini döndürmek için *önek* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="44ea8-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="44ea8-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="44ea8-114">PARAMETERS</span></span>

### <span data-ttu-id="44ea8-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="44ea8-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="44ea8-116">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="44ea8-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="44ea8-117">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="44ea8-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="44ea8-118">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="44ea8-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="44ea8-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="44ea8-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="44ea8-120">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="44ea8-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="44ea8-121">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="44ea8-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="44ea8-122">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="44ea8-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="44ea8-123">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="44ea8-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="44ea8-124">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="44ea8-124">The default value is 10.</span></span>

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

### <span data-ttu-id="44ea8-125">-Context</span><span class="sxs-lookup"><span data-stu-id="44ea8-125">-Context</span></span>
<span data-ttu-id="44ea8-126">Depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="44ea8-126">Specifies the storage context.</span></span>
<span data-ttu-id="44ea8-127">Bunu oluşturmak için New-AzureStorageContext cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="44ea8-127">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="44ea8-128">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="44ea8-128">-ContinuationToken</span></span>
<span data-ttu-id="44ea8-129">Blob listesi için bir devam belirteci belirtir.</span><span class="sxs-lookup"><span data-stu-id="44ea8-129">Specifies a continuation token for the blob list.</span></span>

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

### <span data-ttu-id="44ea8-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="44ea8-130">-MaxCount</span></span>
<span data-ttu-id="44ea8-131">Bu cmdlet 'in döndürdüğü en fazla nesne sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="44ea8-131">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="44ea8-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="44ea8-132">-Name</span></span>
<span data-ttu-id="44ea8-133">Kapsayıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="44ea8-133">Specifies the container name.</span></span>
<span data-ttu-id="44ea8-134">Kapsayıcı adı boşsa, cmdlet tüm kapsayıcıları listeler.</span><span class="sxs-lookup"><span data-stu-id="44ea8-134">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="44ea8-135">Aksi halde, belirtilen ad veya normal Ad düzeniyle eşleşen tüm kapsayıcıları listeler.</span><span class="sxs-lookup"><span data-stu-id="44ea8-135">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44ea8-136">-Önek</span><span class="sxs-lookup"><span data-stu-id="44ea8-136">-Prefix</span></span>
<span data-ttu-id="44ea8-137">Almak istediğiniz kapsayıcının veya kapsayıcıların adında kullanılan bir önek belirtir.</span><span class="sxs-lookup"><span data-stu-id="44ea8-137">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="44ea8-138">"My" veya "test" gibi aynı dizeyle başlayan tüm kapsayıcıları bulmak için bunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="44ea8-138">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

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

### <span data-ttu-id="44ea8-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="44ea8-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="44ea8-140">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="44ea8-140">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="44ea8-141">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="44ea8-141">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="44ea8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ea8-142">CommonParameters</span></span>
<span data-ttu-id="44ea8-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="44ea8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ea8-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44ea8-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ea8-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="44ea8-145">INPUTS</span></span>

## <span data-ttu-id="44ea8-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="44ea8-146">OUTPUTS</span></span>

## <span data-ttu-id="44ea8-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="44ea8-147">NOTES</span></span>

## <span data-ttu-id="44ea8-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="44ea8-148">RELATED LINKS</span></span>

[<span data-ttu-id="44ea8-149">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="44ea8-149">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="44ea8-150">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="44ea8-150">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="44ea8-151">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="44ea8-151">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


