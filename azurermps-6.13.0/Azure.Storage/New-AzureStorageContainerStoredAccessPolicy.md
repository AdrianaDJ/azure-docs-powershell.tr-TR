---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 6dadd92955c325120b67d8faae99c7f8ae90dc5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591519"
---
# <span data-ttu-id="755ca-101">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="755ca-101">New-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="755ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="755ca-102">SYNOPSIS</span></span>
<span data-ttu-id="755ca-103">Azure depolama kapsayıcısı için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="755ca-103">Creates a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="755ca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="755ca-104">SYNTAX</span></span>

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="755ca-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="755ca-105">DESCRIPTION</span></span>
<span data-ttu-id="755ca-106">**New-AzureStorageContainerStoredAccessPolicy** cmdlet 'ı bir Azure depolama kapsayıcısı için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="755ca-106">The **New-AzureStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="755ca-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="755ca-107">EXAMPLES</span></span>

### <span data-ttu-id="755ca-108">Örnek 1: depolama kapsayıcısında depolanan bir Access ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="755ca-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="755ca-109">Bu komut MyContainer adındaki depolama kapsayıcısında Policy01 adlı bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="755ca-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="755ca-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="755ca-110">PARAMETERS</span></span>

### <span data-ttu-id="755ca-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="755ca-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="755ca-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="755ca-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="755ca-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="755ca-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="755ca-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="755ca-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="755ca-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="755ca-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="755ca-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="755ca-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="755ca-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="755ca-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="755ca-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="755ca-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="755ca-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="755ca-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="755ca-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="755ca-120">The default value is 10.</span></span>

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

### <span data-ttu-id="755ca-121">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="755ca-121">-Container</span></span>
<span data-ttu-id="755ca-122">Azure depolama kapsayıcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="755ca-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="755ca-123">-Context</span><span class="sxs-lookup"><span data-stu-id="755ca-123">-Context</span></span>
<span data-ttu-id="755ca-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="755ca-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="755ca-125">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="755ca-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="755ca-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="755ca-126">-DefaultProfile</span></span>
<span data-ttu-id="755ca-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="755ca-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="755ca-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="755ca-128">-ExpiryTime</span></span>
<span data-ttu-id="755ca-129">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="755ca-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="755ca-130">-İzin</span><span class="sxs-lookup"><span data-stu-id="755ca-130">-Permission</span></span>
<span data-ttu-id="755ca-131">Depolanan erişim ilkesindeki kapsayıcıya erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="755ca-131">Specifies permissions in the stored access policy to access the container.</span></span>
<span data-ttu-id="755ca-132">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="755ca-132">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="755ca-133">-İlke</span><span class="sxs-lookup"><span data-stu-id="755ca-133">-Policy</span></span>
<span data-ttu-id="755ca-134">Bu SAS belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="755ca-134">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="755ca-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="755ca-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="755ca-136">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="755ca-136">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="755ca-137">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="755ca-137">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="755ca-138">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="755ca-138">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="755ca-139">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="755ca-139">-StartTime</span></span>
<span data-ttu-id="755ca-140">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="755ca-140">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="755ca-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="755ca-141">CommonParameters</span></span>
<span data-ttu-id="755ca-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="755ca-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="755ca-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="755ca-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="755ca-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="755ca-144">INPUTS</span></span>

### <span data-ttu-id="755ca-145">System. String</span><span class="sxs-lookup"><span data-stu-id="755ca-145">System.String</span></span>

### <span data-ttu-id="755ca-146">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="755ca-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="755ca-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="755ca-147">OUTPUTS</span></span>

### <span data-ttu-id="755ca-148">System. String</span><span class="sxs-lookup"><span data-stu-id="755ca-148">System.String</span></span>

## <span data-ttu-id="755ca-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="755ca-149">NOTES</span></span>

## <span data-ttu-id="755ca-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="755ca-150">RELATED LINKS</span></span>

[<span data-ttu-id="755ca-151">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="755ca-151">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="755ca-152">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="755ca-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="755ca-153">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="755ca-153">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="755ca-154">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="755ca-154">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


