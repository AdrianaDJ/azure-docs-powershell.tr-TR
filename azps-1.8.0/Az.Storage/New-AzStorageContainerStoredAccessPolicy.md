---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 439000d73f2671b6f7c789e4f690a649b57f027b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758613"
---
# <span data-ttu-id="8bde2-101">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8bde2-101">New-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="8bde2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bde2-102">SYNOPSIS</span></span>
<span data-ttu-id="8bde2-103">Azure depolama kapsayıcısı için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8bde2-103">Creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="8bde2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8bde2-104">SYNTAX</span></span>

```
New-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="8bde2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8bde2-105">DESCRIPTION</span></span>
<span data-ttu-id="8bde2-106">**New-AzStorageContainerStoredAccessPolicy** cmdlet 'ı bir Azure depolama kapsayıcısı için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8bde2-106">The **New-AzStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="8bde2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8bde2-107">EXAMPLES</span></span>

### <span data-ttu-id="8bde2-108">Örnek 1: depolama kapsayıcısında depolanan bir Access ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8bde2-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="8bde2-109">Bu komut MyContainer adındaki depolama kapsayıcısında Policy01 adlı bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8bde2-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="8bde2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8bde2-110">PARAMETERS</span></span>

### <span data-ttu-id="8bde2-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8bde2-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8bde2-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bde2-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8bde2-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="8bde2-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8bde2-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="8bde2-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8bde2-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8bde2-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8bde2-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bde2-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8bde2-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8bde2-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8bde2-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="8bde2-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8bde2-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="8bde2-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8bde2-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="8bde2-120">The default value is 10.</span></span>

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

### <span data-ttu-id="8bde2-121">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="8bde2-121">-Container</span></span>
<span data-ttu-id="8bde2-122">Azure depolama kapsayıcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bde2-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="8bde2-123">-Context</span><span class="sxs-lookup"><span data-stu-id="8bde2-123">-Context</span></span>
<span data-ttu-id="8bde2-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bde2-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8bde2-125">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8bde2-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8bde2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bde2-126">-DefaultProfile</span></span>
<span data-ttu-id="8bde2-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8bde2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bde2-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8bde2-128">-ExpiryTime</span></span>
<span data-ttu-id="8bde2-129">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bde2-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="8bde2-130">-İzin</span><span class="sxs-lookup"><span data-stu-id="8bde2-130">-Permission</span></span>
<span data-ttu-id="8bde2-131">Depolanan erişim ilkesindeki kapsayıcıya erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bde2-131">Specifies permissions in the stored access policy to access the container.</span></span>
<span data-ttu-id="8bde2-132">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="8bde2-132">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="8bde2-133">-İlke</span><span class="sxs-lookup"><span data-stu-id="8bde2-133">-Policy</span></span>
<span data-ttu-id="8bde2-134">Bu SAS belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bde2-134">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="8bde2-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8bde2-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8bde2-136">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bde2-136">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8bde2-137">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="8bde2-137">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8bde2-138">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="8bde2-138">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8bde2-139">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="8bde2-139">-StartTime</span></span>
<span data-ttu-id="8bde2-140">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bde2-140">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="8bde2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bde2-141">CommonParameters</span></span>
<span data-ttu-id="8bde2-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8bde2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bde2-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bde2-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bde2-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8bde2-144">INPUTS</span></span>

### <span data-ttu-id="8bde2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="8bde2-145">System.String</span></span>

### <span data-ttu-id="8bde2-146">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="8bde2-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8bde2-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8bde2-147">OUTPUTS</span></span>

### <span data-ttu-id="8bde2-148">System. String</span><span class="sxs-lookup"><span data-stu-id="8bde2-148">System.String</span></span>

## <span data-ttu-id="8bde2-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8bde2-149">NOTES</span></span>

## <span data-ttu-id="8bde2-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8bde2-150">RELATED LINKS</span></span>

[<span data-ttu-id="8bde2-151">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8bde2-151">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="8bde2-152">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8bde2-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="8bde2-153">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8bde2-153">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="8bde2-154">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8bde2-154">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


