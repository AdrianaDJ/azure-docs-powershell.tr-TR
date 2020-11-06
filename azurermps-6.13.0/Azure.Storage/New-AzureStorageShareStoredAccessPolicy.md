---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 823ae6183021e368933af8d2e01a61f0b582323e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588661"
---
# <span data-ttu-id="109f9-101">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="109f9-101">New-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="109f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="109f9-102">SYNOPSIS</span></span>
<span data-ttu-id="109f9-103">Depolama paylaşımında depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="109f9-103">Creates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="109f9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="109f9-104">SYNTAX</span></span>

```
New-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="109f9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="109f9-105">DESCRIPTION</span></span>
<span data-ttu-id="109f9-106">**New-AzureStorageShareStoredAccessPolicy** cmdlet 'ı Azure depolama paylaşımında depolanan bir Access ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="109f9-106">The **New-AzureStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="109f9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="109f9-107">EXAMPLES</span></span>

### <span data-ttu-id="109f9-108">Örnek 1: paylaşımda depolanan bir Access ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="109f9-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="109f9-109">Bu komut, paylaşımda tam izni olan bir depolanmış erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="109f9-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="109f9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="109f9-110">PARAMETERS</span></span>

### <span data-ttu-id="109f9-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="109f9-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="109f9-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="109f9-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="109f9-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="109f9-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="109f9-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="109f9-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="109f9-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="109f9-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="109f9-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="109f9-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="109f9-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="109f9-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="109f9-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="109f9-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="109f9-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="109f9-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="109f9-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="109f9-120">The default value is 10.</span></span>

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

### <span data-ttu-id="109f9-121">-Context</span><span class="sxs-lookup"><span data-stu-id="109f9-121">-Context</span></span>
<span data-ttu-id="109f9-122">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="109f9-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="109f9-123">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="109f9-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="109f9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="109f9-124">-DefaultProfile</span></span>
<span data-ttu-id="109f9-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="109f9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="109f9-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="109f9-126">-ExpiryTime</span></span>
<span data-ttu-id="109f9-127">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="109f9-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="109f9-128">-İzin</span><span class="sxs-lookup"><span data-stu-id="109f9-128">-Permission</span></span>
<span data-ttu-id="109f9-129">Depolanan erişim ilkesindeki depolama paylaşımına veya bu dosyaların altındaki dosyalara erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="109f9-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="109f9-130">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="109f9-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="109f9-131">-İlke</span><span class="sxs-lookup"><span data-stu-id="109f9-131">-Policy</span></span>
<span data-ttu-id="109f9-132">Depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="109f9-132">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="109f9-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="109f9-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="109f9-134">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="109f9-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="109f9-135">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="109f9-135">-ShareName</span></span>
<span data-ttu-id="109f9-136">Depolama paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="109f9-136">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="109f9-137">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="109f9-137">-StartTime</span></span>
<span data-ttu-id="109f9-138">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="109f9-138">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="109f9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="109f9-139">CommonParameters</span></span>
<span data-ttu-id="109f9-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="109f9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="109f9-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="109f9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="109f9-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="109f9-142">INPUTS</span></span>

### <span data-ttu-id="109f9-143">System. String</span><span class="sxs-lookup"><span data-stu-id="109f9-143">System.String</span></span>

### <span data-ttu-id="109f9-144">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="109f9-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="109f9-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="109f9-145">OUTPUTS</span></span>

### <span data-ttu-id="109f9-146">System. String</span><span class="sxs-lookup"><span data-stu-id="109f9-146">System.String</span></span>

## <span data-ttu-id="109f9-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="109f9-147">NOTES</span></span>

## <span data-ttu-id="109f9-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="109f9-148">RELATED LINKS</span></span>

[<span data-ttu-id="109f9-149">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="109f9-149">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="109f9-150">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="109f9-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="109f9-151">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="109f9-151">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="109f9-152">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="109f9-152">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
