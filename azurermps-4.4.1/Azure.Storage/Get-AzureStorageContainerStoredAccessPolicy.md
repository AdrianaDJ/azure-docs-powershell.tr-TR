---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 174353aacbfe939294f654a4f5f61548bfc672dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595063"
---
# <span data-ttu-id="fbbca-101">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fbbca-101">Get-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="fbbca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbbca-102">SYNOPSIS</span></span>
<span data-ttu-id="fbbca-103">Azure depolama kapsayıcısı için depolanan erişim ilkesini veya ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="fbbca-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbbca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fbbca-104">SYNTAX</span></span>

```
Get-AzureStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="fbbca-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fbbca-105">DESCRIPTION</span></span>
<span data-ttu-id="fbbca-106">**Get-AzureStorageContainerStoredAccessPolicy** cmdlet 'ı, Azure depolama kapsayıcısı için depolanan erişim ilkesini veya ilkelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="fbbca-106">The **Get-AzureStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="fbbca-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fbbca-107">EXAMPLES</span></span>

### <span data-ttu-id="fbbca-108">Örnek 1: depolama kapsayıcısında depolanan bir erişim ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="fbbca-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="fbbca-109">Bu komut, Container07 adındaki depolama kapsayıcısında Policy22 adındaki erişim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="fbbca-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="fbbca-110">Örnek 2: depolama kapsayıcısındaki tüm depolanan erişim ilkelerini alma</span><span class="sxs-lookup"><span data-stu-id="fbbca-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="fbbca-111">Bu komut, Container07 adlı depolama kapsayıcısındaki tüm erişim ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="fbbca-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="fbbca-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fbbca-112">PARAMETERS</span></span>

### <span data-ttu-id="fbbca-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fbbca-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fbbca-114">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbbca-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fbbca-115">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="fbbca-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fbbca-116">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="fbbca-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fbbca-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fbbca-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fbbca-118">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbbca-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fbbca-119">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbbca-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fbbca-120">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="fbbca-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fbbca-121">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="fbbca-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fbbca-122">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="fbbca-122">The default value is 10.</span></span>

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

### <span data-ttu-id="fbbca-123">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="fbbca-123">-Container</span></span>
<span data-ttu-id="fbbca-124">Azure depolama kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbbca-124">Specifies the name of your Azure storage container.</span></span>

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

### <span data-ttu-id="fbbca-125">-Context</span><span class="sxs-lookup"><span data-stu-id="fbbca-125">-Context</span></span>
<span data-ttu-id="fbbca-126">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbbca-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="fbbca-127">-İlke</span><span class="sxs-lookup"><span data-stu-id="fbbca-127">-Policy</span></span>
<span data-ttu-id="fbbca-128">Azure depolanan erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbbca-128">Specifies the Azure stored access policy.</span></span>

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

### <span data-ttu-id="fbbca-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fbbca-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fbbca-130">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbbca-130">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="fbbca-131">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="fbbca-131">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="fbbca-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbbca-132">CommonParameters</span></span>
<span data-ttu-id="fbbca-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fbbca-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbbca-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbbca-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbbca-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fbbca-135">INPUTS</span></span>

### <span data-ttu-id="fbbca-136">Dizisi</span><span class="sxs-lookup"><span data-stu-id="fbbca-136">String</span></span>

<span data-ttu-id="fbbca-137">Parametre ' Container ', ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="fbbca-137">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="fbbca-138">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="fbbca-138">IStorageContext</span></span>

<span data-ttu-id="fbbca-139">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="fbbca-139">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="fbbca-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fbbca-140">OUTPUTS</span></span>

### <span data-ttu-id="fbbca-141">Microsoft. Windowsazde. Storage. blob. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="fbbca-141">Microsoft.WindowsAzure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="fbbca-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fbbca-142">NOTES</span></span>

## <span data-ttu-id="fbbca-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fbbca-143">RELATED LINKS</span></span>

[<span data-ttu-id="fbbca-144">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fbbca-144">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="fbbca-145">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fbbca-145">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="fbbca-146">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fbbca-146">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


