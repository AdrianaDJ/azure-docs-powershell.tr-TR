---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: ''
schema: 2.0.0
ms.openlocfilehash: 27237a00866c42d5e7eb587267ad6573cbd6cac7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571369"
---
# <span data-ttu-id="bada6-101">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="bada6-101">Remove-AzureStorageCORSRule</span></span>

## <span data-ttu-id="bada6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bada6-102">SYNOPSIS</span></span>
<span data-ttu-id="bada6-103">Bir depolama hizmeti için CORS 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bada6-103">Removes CORS for a Storage service.</span></span>

## <span data-ttu-id="bada6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bada6-104">SYNTAX</span></span>

```
Remove-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="bada6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bada6-105">DESCRIPTION</span></span>
<span data-ttu-id="bada6-106">**Remove-AzureStorageCORSRule** cmdlet 'ı bir Azure depolama hizmeti için çapraz kaynak PAYLAŞıMıNı (CORS) kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bada6-106">The **Remove-AzureStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="bada6-107">Bu cmdlet, bir depolama hizmeti türündeki tüm CORS kurallarını siler.</span><span class="sxs-lookup"><span data-stu-id="bada6-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="bada6-108">Bu cmdlet için depolama hizmetleri türleri blob, tablo, kuyruk ve dosyadır.</span><span class="sxs-lookup"><span data-stu-id="bada6-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="bada6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bada6-109">EXAMPLES</span></span>

### <span data-ttu-id="bada6-110">Örnek 1: blob hizmeti için CORS kurallarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="bada6-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="bada6-111">Bu komut, blob hizmet türü için CORS kurallarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bada6-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="bada6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bada6-112">PARAMETERS</span></span>

### <span data-ttu-id="bada6-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bada6-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bada6-114">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="bada6-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bada6-115">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="bada6-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bada6-116">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="bada6-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bada6-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bada6-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bada6-118">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bada6-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bada6-119">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bada6-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bada6-120">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="bada6-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bada6-121">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="bada6-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bada6-122">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="bada6-122">The default value is 10.</span></span>

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

### <span data-ttu-id="bada6-123">-Context</span><span class="sxs-lookup"><span data-stu-id="bada6-123">-Context</span></span>
<span data-ttu-id="bada6-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bada6-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="bada6-125">Depolama bağlamını edinmek için New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bada6-125">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bada6-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bada6-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bada6-127">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bada6-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="bada6-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="bada6-128">-ServiceType</span></span>
<span data-ttu-id="bada6-129">Bu cmdlet 'in kuralları kaldırdığı Azure depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="bada6-129">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="bada6-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bada6-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bada6-131">'Unu</span><span class="sxs-lookup"><span data-stu-id="bada6-131">Blob</span></span> 
- <span data-ttu-id="bada6-132">Tablo</span><span class="sxs-lookup"><span data-stu-id="bada6-132">Table</span></span> 
- <span data-ttu-id="bada6-133">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="bada6-133">Queue</span></span> 
- <span data-ttu-id="bada6-134">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="bada6-134">File</span></span>

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

### <span data-ttu-id="bada6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bada6-135">CommonParameters</span></span>
<span data-ttu-id="bada6-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bada6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bada6-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bada6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bada6-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bada6-138">INPUTS</span></span>

## <span data-ttu-id="bada6-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bada6-139">OUTPUTS</span></span>

## <span data-ttu-id="bada6-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bada6-140">NOTES</span></span>

## <span data-ttu-id="bada6-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bada6-141">RELATED LINKS</span></span>

[<span data-ttu-id="bada6-142">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="bada6-142">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="bada6-143">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="bada6-143">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


