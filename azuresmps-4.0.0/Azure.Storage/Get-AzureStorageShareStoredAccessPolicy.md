---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc7268d3d7d233f6a3fafeb92540e23ae3eaa6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572346"
---
# <span data-ttu-id="4270b-101">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4270b-101">Get-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="4270b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4270b-102">SYNOPSIS</span></span>
<span data-ttu-id="4270b-103">Depolama paylaşımı için depolanan erişim ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="4270b-103">Gets stored access policies for a Storage share.</span></span>

## <span data-ttu-id="4270b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4270b-104">SYNTAX</span></span>

```
Get-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="4270b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4270b-105">DESCRIPTION</span></span>
<span data-ttu-id="4270b-106">**Get-AzureStorageShareStoredAccessPolicy** cmdlet 'ı bir Azure depolama paylaşımı için depolanan erişim ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="4270b-106">The **Get-AzureStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="4270b-107">Belirli bir ilkeyi almak için adını adıyla belirtin.</span><span class="sxs-lookup"><span data-stu-id="4270b-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="4270b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4270b-108">EXAMPLES</span></span>

### <span data-ttu-id="4270b-109">Örnek 1: paylaşımda depolanan bir Access ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="4270b-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="4270b-110">Bu komut, ContosoShare 'daki GeneralPolicy adlı saklı bir erişim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="4270b-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="4270b-111">Örnek 2: tüm depolanan erişim ilkelerini paylaşımda edinme</span><span class="sxs-lookup"><span data-stu-id="4270b-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="4270b-112">Bu komut, ContosoShare 'daki tüm depolanmış erişim ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="4270b-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="4270b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4270b-113">PARAMETERS</span></span>

### <span data-ttu-id="4270b-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4270b-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4270b-115">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="4270b-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4270b-116">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="4270b-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4270b-117">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="4270b-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4270b-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4270b-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4270b-119">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4270b-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4270b-120">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4270b-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4270b-121">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="4270b-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4270b-122">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="4270b-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4270b-123">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="4270b-123">The default value is 10.</span></span>

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

### <span data-ttu-id="4270b-124">-Context</span><span class="sxs-lookup"><span data-stu-id="4270b-124">-Context</span></span>
<span data-ttu-id="4270b-125">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4270b-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="4270b-126">Bağlam almak için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4270b-126">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4270b-127">-İlke</span><span class="sxs-lookup"><span data-stu-id="4270b-127">-Policy</span></span>
<span data-ttu-id="4270b-128">Bu cmdlet 'in aldığı depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4270b-128">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4270b-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4270b-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4270b-130">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4270b-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4270b-131">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="4270b-131">-ShareName</span></span>
<span data-ttu-id="4270b-132">Bu cmdlet 'in ilkeleri aldığı depolama paylaşımı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4270b-132">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="4270b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4270b-133">CommonParameters</span></span>
<span data-ttu-id="4270b-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4270b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4270b-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4270b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4270b-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4270b-136">INPUTS</span></span>

## <span data-ttu-id="4270b-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4270b-137">OUTPUTS</span></span>

## <span data-ttu-id="4270b-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4270b-138">NOTES</span></span>

## <span data-ttu-id="4270b-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4270b-139">RELATED LINKS</span></span>

[<span data-ttu-id="4270b-140">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="4270b-140">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="4270b-141">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4270b-141">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="4270b-142">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4270b-142">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="4270b-143">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4270b-143">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
