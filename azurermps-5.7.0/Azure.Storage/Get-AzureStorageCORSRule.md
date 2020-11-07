---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageCORSRule.md
ms.openlocfilehash: 38ad6f5631f816070e9d59ba7b78c2a39cff2b2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762672"
---
# <span data-ttu-id="f2005-101">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="f2005-101">Get-AzureStorageCORSRule</span></span>

## <span data-ttu-id="f2005-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2005-102">SYNOPSIS</span></span>
<span data-ttu-id="f2005-103">Depolama hizmeti türü için CORS kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="f2005-103">Gets CORS rules for a Storage service type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2005-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2005-104">SYNTAX</span></span>

```
Get-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2005-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2005-105">DESCRIPTION</span></span>
<span data-ttu-id="f2005-106">**Get-AzureStorageCORSRule** cmdlet 'ı bir Azure depolama hizmeti türü Için çapraz kaynak PAYLAŞıMı (CORS) kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="f2005-106">The **Get-AzureStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="f2005-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2005-107">EXAMPLES</span></span>

### <span data-ttu-id="f2005-108">Örnek 1: Blob hizmetinin CORS kurallarını alma</span><span class="sxs-lookup"><span data-stu-id="f2005-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="f2005-109">Bu komut, blob hizmet türü için CORS kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="f2005-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="f2005-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2005-110">PARAMETERS</span></span>

### <span data-ttu-id="f2005-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f2005-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f2005-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2005-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f2005-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="f2005-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f2005-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="f2005-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f2005-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f2005-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f2005-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2005-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f2005-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f2005-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f2005-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="f2005-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f2005-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="f2005-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f2005-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="f2005-120">The default value is 10.</span></span>

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

### <span data-ttu-id="f2005-121">-Context</span><span class="sxs-lookup"><span data-stu-id="f2005-121">-Context</span></span>
<span data-ttu-id="f2005-122">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2005-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="f2005-123">Bağlam almak için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f2005-123">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f2005-124">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f2005-124">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f2005-125">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2005-125">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f2005-126">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="f2005-126">-ServiceType</span></span>
<span data-ttu-id="f2005-127">Bu cmdlet 'in CORS kurallarını aldığı Azure depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2005-127">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="f2005-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f2005-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f2005-129">'Unu</span><span class="sxs-lookup"><span data-stu-id="f2005-129">Blob</span></span> 
- <span data-ttu-id="f2005-130">Tablo</span><span class="sxs-lookup"><span data-stu-id="f2005-130">Table</span></span> 
- <span data-ttu-id="f2005-131">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="f2005-131">Queue</span></span> 
- <span data-ttu-id="f2005-132">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="f2005-132">File</span></span>

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

### <span data-ttu-id="f2005-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2005-133">CommonParameters</span></span>
<span data-ttu-id="f2005-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2005-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2005-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2005-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2005-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2005-136">INPUTS</span></span>

### <span data-ttu-id="f2005-137">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="f2005-137">IStorageContext</span></span>

<span data-ttu-id="f2005-138">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f2005-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="f2005-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2005-139">OUTPUTS</span></span>

###  
<span data-ttu-id="f2005-140">Bu cmdlet, bir hizmette bulunan CORS kurallarını temsil eden bir **PSCORSRule** nesneleri dizisi döndürür.</span><span class="sxs-lookup"><span data-stu-id="f2005-140">This cmdlet returns an array of **PSCORSRule** objects which represent the CORS rules currently on a service.</span></span>

## <span data-ttu-id="f2005-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2005-141">NOTES</span></span>

## <span data-ttu-id="f2005-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2005-142">RELATED LINKS</span></span>

[<span data-ttu-id="f2005-143">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="f2005-143">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)

[<span data-ttu-id="f2005-144">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="f2005-144">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


