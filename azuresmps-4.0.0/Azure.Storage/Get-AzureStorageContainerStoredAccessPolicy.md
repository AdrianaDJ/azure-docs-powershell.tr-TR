---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e9ea56c53d73b9c71d2eade4fec7025466ed82d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572382"
---
# <span data-ttu-id="f59fa-101">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f59fa-101">Get-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="f59fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f59fa-102">SYNOPSIS</span></span>
<span data-ttu-id="f59fa-103">Azure depolama kapsayıcısı için depolanan erişim ilkesini veya ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="f59fa-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="f59fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f59fa-104">SYNTAX</span></span>

```
Get-AzureStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="f59fa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f59fa-105">DESCRIPTION</span></span>
<span data-ttu-id="f59fa-106">**Get-AzureStorageContainerStoredAccessPolicy** cmdlet 'ı, Azure depolama kapsayıcısı için depolanan erişim ilkesini veya ilkelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="f59fa-106">The **Get-AzureStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="f59fa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f59fa-107">EXAMPLES</span></span>

### <span data-ttu-id="f59fa-108">Örnek 1: depolama kapsayıcısında depolanan bir erişim ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="f59fa-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="f59fa-109">Bu komut, Container07 adındaki depolama kapsayıcısında Policy22 adındaki erişim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="f59fa-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="f59fa-110">Örnek 2: depolama kapsayıcısındaki tüm depolanan erişim ilkelerini alma</span><span class="sxs-lookup"><span data-stu-id="f59fa-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="f59fa-111">Bu komut, Container07 adlı depolama kapsayıcısındaki tüm erişim ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="f59fa-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="f59fa-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f59fa-112">PARAMETERS</span></span>

### <span data-ttu-id="f59fa-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f59fa-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f59fa-114">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="f59fa-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f59fa-115">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="f59fa-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f59fa-116">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="f59fa-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f59fa-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f59fa-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f59fa-118">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f59fa-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f59fa-119">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f59fa-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f59fa-120">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="f59fa-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f59fa-121">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="f59fa-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f59fa-122">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="f59fa-122">The default value is 10.</span></span>

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

### <span data-ttu-id="f59fa-123">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="f59fa-123">-Container</span></span>
<span data-ttu-id="f59fa-124">Azure depolama kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f59fa-124">Specifies the name of your Azure storage container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f59fa-125">-Context</span><span class="sxs-lookup"><span data-stu-id="f59fa-125">-Context</span></span>
<span data-ttu-id="f59fa-126">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f59fa-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="f59fa-127">-İlke</span><span class="sxs-lookup"><span data-stu-id="f59fa-127">-Policy</span></span>
<span data-ttu-id="f59fa-128">Azure depolanan erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f59fa-128">Specifies the Azure stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f59fa-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f59fa-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f59fa-130">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f59fa-130">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="f59fa-131">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="f59fa-131">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="f59fa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f59fa-132">CommonParameters</span></span>
<span data-ttu-id="f59fa-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f59fa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f59fa-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f59fa-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f59fa-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f59fa-135">INPUTS</span></span>

## <span data-ttu-id="f59fa-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f59fa-136">OUTPUTS</span></span>

## <span data-ttu-id="f59fa-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f59fa-137">NOTES</span></span>

## <span data-ttu-id="f59fa-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f59fa-138">RELATED LINKS</span></span>

[<span data-ttu-id="f59fa-139">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f59fa-139">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="f59fa-140">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f59fa-140">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="f59fa-141">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f59fa-141">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


