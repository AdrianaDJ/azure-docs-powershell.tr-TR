---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 0b734acb6d1a0d491a0b9e6397f7ae9af2645b35
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939015"
---
# <span data-ttu-id="a9337-101">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a9337-101">Get-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="a9337-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9337-102">SYNOPSIS</span></span>
<span data-ttu-id="a9337-103">Azure depolama kapsayıcısı için depolanan erişim ilkesini veya ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="a9337-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9337-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9337-104">SYNTAX</span></span>

```
Get-AzureStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a9337-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9337-105">DESCRIPTION</span></span>
<span data-ttu-id="a9337-106">**Get-AzureStorageContainerStoredAccessPolicy** cmdlet 'ı, Azure depolama kapsayıcısı için depolanan erişim ilkesini veya ilkelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="a9337-106">The **Get-AzureStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="a9337-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9337-107">EXAMPLES</span></span>

### <span data-ttu-id="a9337-108">Örnek 1: depolama kapsayıcısında depolanan bir erişim ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="a9337-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="a9337-109">Bu komut, Container07 adındaki depolama kapsayıcısında Policy22 adındaki erişim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="a9337-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="a9337-110">Örnek 2: depolama kapsayıcısındaki tüm depolanan erişim ilkelerini alma</span><span class="sxs-lookup"><span data-stu-id="a9337-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="a9337-111">Bu komut, Container07 adlı depolama kapsayıcısındaki tüm erişim ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="a9337-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="a9337-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9337-112">PARAMETERS</span></span>

### <span data-ttu-id="a9337-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a9337-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a9337-114">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9337-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a9337-115">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="a9337-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a9337-116">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="a9337-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a9337-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a9337-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a9337-118">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9337-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a9337-119">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9337-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a9337-120">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="a9337-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a9337-121">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="a9337-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a9337-122">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="a9337-122">The default value is 10.</span></span>

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

### <span data-ttu-id="a9337-123">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="a9337-123">-Container</span></span>
<span data-ttu-id="a9337-124">Azure depolama kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9337-124">Specifies the name of your Azure storage container.</span></span>

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

### <span data-ttu-id="a9337-125">-Context</span><span class="sxs-lookup"><span data-stu-id="a9337-125">-Context</span></span>
<span data-ttu-id="a9337-126">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9337-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="a9337-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9337-127">-DefaultProfile</span></span>
<span data-ttu-id="a9337-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9337-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9337-129">-İlke</span><span class="sxs-lookup"><span data-stu-id="a9337-129">-Policy</span></span>
<span data-ttu-id="a9337-130">Azure depolanan erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9337-130">Specifies the Azure stored access policy.</span></span>

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

### <span data-ttu-id="a9337-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a9337-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a9337-132">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9337-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="a9337-133">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="a9337-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a9337-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9337-134">CommonParameters</span></span>
<span data-ttu-id="a9337-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9337-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9337-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9337-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9337-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9337-137">INPUTS</span></span>

### <span data-ttu-id="a9337-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a9337-138">System.String</span></span>

### <span data-ttu-id="a9337-139">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="a9337-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a9337-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9337-140">OUTPUTS</span></span>

### <span data-ttu-id="a9337-141">Microsoft. Windowsazde. Storage. blob. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="a9337-141">Microsoft.WindowsAzure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="a9337-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9337-142">NOTES</span></span>

## <span data-ttu-id="a9337-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9337-143">RELATED LINKS</span></span>

[<span data-ttu-id="a9337-144">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a9337-144">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="a9337-145">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a9337-145">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="a9337-146">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a9337-146">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)

