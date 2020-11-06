---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c65daf144708340649b9f7b1566c5e5f2dd81e45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572390"
---
# <span data-ttu-id="7eeed-101">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="7eeed-101">Get-AzureStorageCORSRule</span></span>

## <span data-ttu-id="7eeed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7eeed-102">SYNOPSIS</span></span>
<span data-ttu-id="7eeed-103">Depolama hizmeti türü için CORS kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="7eeed-103">Gets CORS rules for a Storage service type.</span></span>

## <span data-ttu-id="7eeed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7eeed-104">SYNTAX</span></span>

```
Get-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="7eeed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7eeed-105">DESCRIPTION</span></span>
<span data-ttu-id="7eeed-106">**Get-AzureStorageCORSRule** cmdlet 'ı bir Azure depolama hizmeti türü Için çapraz kaynak PAYLAŞıMı (CORS) kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="7eeed-106">The **Get-AzureStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="7eeed-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7eeed-107">EXAMPLES</span></span>

### <span data-ttu-id="7eeed-108">Örnek 1: Blob hizmetinin CORS kurallarını alma</span><span class="sxs-lookup"><span data-stu-id="7eeed-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="7eeed-109">Bu komut, blob hizmet türü için CORS kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="7eeed-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="7eeed-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7eeed-110">PARAMETERS</span></span>

### <span data-ttu-id="7eeed-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7eeed-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7eeed-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="7eeed-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7eeed-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="7eeed-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7eeed-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="7eeed-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7eeed-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7eeed-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7eeed-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7eeed-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7eeed-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7eeed-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7eeed-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="7eeed-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7eeed-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="7eeed-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7eeed-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="7eeed-120">The default value is 10.</span></span>

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

### <span data-ttu-id="7eeed-121">-Context</span><span class="sxs-lookup"><span data-stu-id="7eeed-121">-Context</span></span>
<span data-ttu-id="7eeed-122">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7eeed-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="7eeed-123">Bağlam almak için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7eeed-123">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7eeed-124">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7eeed-124">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7eeed-125">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7eeed-125">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="7eeed-126">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="7eeed-126">-ServiceType</span></span>
<span data-ttu-id="7eeed-127">Bu cmdlet 'in CORS kurallarını aldığı Azure depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7eeed-127">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="7eeed-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7eeed-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7eeed-129">'Unu</span><span class="sxs-lookup"><span data-stu-id="7eeed-129">Blob</span></span> 
- <span data-ttu-id="7eeed-130">Tablo</span><span class="sxs-lookup"><span data-stu-id="7eeed-130">Table</span></span> 
- <span data-ttu-id="7eeed-131">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="7eeed-131">Queue</span></span> 
- <span data-ttu-id="7eeed-132">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="7eeed-132">File</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eeed-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eeed-133">CommonParameters</span></span>
<span data-ttu-id="7eeed-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7eeed-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eeed-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eeed-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eeed-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7eeed-136">INPUTS</span></span>

## <span data-ttu-id="7eeed-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7eeed-137">OUTPUTS</span></span>

###  
<span data-ttu-id="7eeed-138">Bu cmdlet, bir hizmette bulunan CORS kurallarını temsil eden bir **PSCORSRule** nesneleri dizisi döndürür.</span><span class="sxs-lookup"><span data-stu-id="7eeed-138">This cmdlet returns an array of **PSCORSRule** objects which represent the CORS rules currently on a service.</span></span>

## <span data-ttu-id="7eeed-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7eeed-139">NOTES</span></span>

## <span data-ttu-id="7eeed-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7eeed-140">RELATED LINKS</span></span>

[<span data-ttu-id="7eeed-141">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="7eeed-141">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)

[<span data-ttu-id="7eeed-142">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="7eeed-142">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


