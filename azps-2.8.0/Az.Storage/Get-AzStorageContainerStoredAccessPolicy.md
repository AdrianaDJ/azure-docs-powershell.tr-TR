---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 71f00e9e1842eef237a7128d5e20e2ac2116e8a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934090"
---
# <span data-ttu-id="43127-101">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="43127-101">Get-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="43127-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43127-102">SYNOPSIS</span></span>
<span data-ttu-id="43127-103">Azure depolama kapsayıcısı için depolanan erişim ilkesini veya ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="43127-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="43127-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="43127-104">SYNTAX</span></span>

```
Get-AzStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="43127-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="43127-105">DESCRIPTION</span></span>
<span data-ttu-id="43127-106">**Get-AzStorageContainerStoredAccessPolicy** cmdlet 'ı, Azure depolama kapsayıcısı için depolanan erişim ilkesini veya ilkelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="43127-106">The **Get-AzStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="43127-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="43127-107">EXAMPLES</span></span>

### <span data-ttu-id="43127-108">Örnek 1: depolama kapsayıcısında depolanan bir erişim ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="43127-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="43127-109">Bu komut, Container07 adındaki depolama kapsayıcısında Policy22 adındaki erişim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="43127-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="43127-110">Örnek 2: depolama kapsayıcısındaki tüm depolanan erişim ilkelerini alma</span><span class="sxs-lookup"><span data-stu-id="43127-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="43127-111">Bu komut, Container07 adlı depolama kapsayıcısındaki tüm erişim ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="43127-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="43127-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="43127-112">PARAMETERS</span></span>

### <span data-ttu-id="43127-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="43127-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="43127-114">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="43127-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="43127-115">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="43127-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="43127-116">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="43127-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="43127-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="43127-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="43127-118">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43127-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="43127-119">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="43127-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="43127-120">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="43127-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="43127-121">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="43127-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="43127-122">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="43127-122">The default value is 10.</span></span>

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

### <span data-ttu-id="43127-123">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="43127-123">-Container</span></span>
<span data-ttu-id="43127-124">Azure depolama kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43127-124">Specifies the name of your Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43127-125">-Context</span><span class="sxs-lookup"><span data-stu-id="43127-125">-Context</span></span>
<span data-ttu-id="43127-126">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43127-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="43127-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43127-127">-DefaultProfile</span></span>
<span data-ttu-id="43127-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="43127-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43127-129">-İlke</span><span class="sxs-lookup"><span data-stu-id="43127-129">-Policy</span></span>
<span data-ttu-id="43127-130">Azure depolanan erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="43127-130">Specifies the Azure stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43127-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="43127-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="43127-132">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43127-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="43127-133">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="43127-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="43127-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43127-134">CommonParameters</span></span>
<span data-ttu-id="43127-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="43127-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43127-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43127-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43127-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="43127-137">INPUTS</span></span>

### <span data-ttu-id="43127-138">System. String</span><span class="sxs-lookup"><span data-stu-id="43127-138">System.String</span></span>

### <span data-ttu-id="43127-139">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="43127-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="43127-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="43127-140">OUTPUTS</span></span>

### <span data-ttu-id="43127-141">Microsoft. Azure. Storage. blob. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="43127-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="43127-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="43127-142">NOTES</span></span>

## <span data-ttu-id="43127-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="43127-143">RELATED LINKS</span></span>

[<span data-ttu-id="43127-144">Yeni-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="43127-144">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="43127-145">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="43127-145">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="43127-146">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="43127-146">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)

