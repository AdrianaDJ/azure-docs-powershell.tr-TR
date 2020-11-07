---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragesharestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 5e4a6c5ad69ae8f31564335a410a67ec58181f3d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939004"
---
# <span data-ttu-id="1a419-101">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1a419-101">Get-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="1a419-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a419-102">SYNOPSIS</span></span>
<span data-ttu-id="1a419-103">Depolama paylaşımı için depolanan erişim ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="1a419-103">Gets stored access policies for a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a419-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a419-104">SYNTAX</span></span>

```
Get-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="1a419-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a419-105">DESCRIPTION</span></span>
<span data-ttu-id="1a419-106">**Get-AzureStorageShareStoredAccessPolicy** cmdlet 'ı bir Azure depolama paylaşımı için depolanan erişim ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="1a419-106">The **Get-AzureStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="1a419-107">Belirli bir ilkeyi almak için adını adıyla belirtin.</span><span class="sxs-lookup"><span data-stu-id="1a419-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="1a419-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a419-108">EXAMPLES</span></span>

### <span data-ttu-id="1a419-109">Örnek 1: paylaşımda depolanan bir Access ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="1a419-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="1a419-110">Bu komut, ContosoShare 'daki GeneralPolicy adlı saklı bir erişim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="1a419-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="1a419-111">Örnek 2: tüm depolanan erişim ilkelerini paylaşımda edinme</span><span class="sxs-lookup"><span data-stu-id="1a419-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="1a419-112">Bu komut, ContosoShare 'daki tüm depolanmış erişim ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="1a419-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="1a419-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a419-113">PARAMETERS</span></span>

### <span data-ttu-id="1a419-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1a419-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1a419-115">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a419-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1a419-116">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="1a419-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1a419-117">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="1a419-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1a419-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1a419-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1a419-119">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a419-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1a419-120">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1a419-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1a419-121">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="1a419-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1a419-122">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="1a419-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1a419-123">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="1a419-123">The default value is 10.</span></span>

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

### <span data-ttu-id="1a419-124">-Context</span><span class="sxs-lookup"><span data-stu-id="1a419-124">-Context</span></span>
<span data-ttu-id="1a419-125">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a419-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="1a419-126">Bağlam almak için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1a419-126">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="1a419-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a419-127">-DefaultProfile</span></span>
<span data-ttu-id="1a419-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1a419-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a419-129">-İlke</span><span class="sxs-lookup"><span data-stu-id="1a419-129">-Policy</span></span>
<span data-ttu-id="1a419-130">Bu cmdlet 'in aldığı depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a419-130">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1a419-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1a419-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1a419-132">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a419-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="1a419-133">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="1a419-133">-ShareName</span></span>
<span data-ttu-id="1a419-134">Bu cmdlet 'in ilkeleri aldığı depolama paylaşımı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a419-134">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="1a419-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a419-135">CommonParameters</span></span>
<span data-ttu-id="1a419-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a419-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a419-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a419-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a419-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a419-138">INPUTS</span></span>

### <span data-ttu-id="1a419-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1a419-139">System.String</span></span>

### <span data-ttu-id="1a419-140">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="1a419-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1a419-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a419-141">OUTPUTS</span></span>

### <span data-ttu-id="1a419-142">Microsoft. Windowsazde. Storage. File. SharedAccessFilePolicy</span><span class="sxs-lookup"><span data-stu-id="1a419-142">Microsoft.WindowsAzure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="1a419-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a419-143">NOTES</span></span>

## <span data-ttu-id="1a419-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a419-144">RELATED LINKS</span></span>

[<span data-ttu-id="1a419-145">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1a419-145">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="1a419-146">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1a419-146">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="1a419-147">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1a419-147">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="1a419-148">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1a419-148">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
