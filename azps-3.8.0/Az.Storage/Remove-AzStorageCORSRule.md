---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
ms.openlocfilehash: aeae25ab3a8ff0b1fa3eb91db90497b44555631f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104661"
---
# <span data-ttu-id="d04a1-101">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="d04a1-101">Remove-AzStorageCORSRule</span></span>

## <span data-ttu-id="d04a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d04a1-102">SYNOPSIS</span></span>
<span data-ttu-id="d04a1-103">Bir depolama hizmeti için CORS 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d04a1-103">Removes CORS for a Storage service.</span></span>

## <span data-ttu-id="d04a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d04a1-104">SYNTAX</span></span>

```
Remove-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="d04a1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d04a1-105">DESCRIPTION</span></span>
<span data-ttu-id="d04a1-106">**Remove-AzStorageCORSRule** cmdlet 'i, bir Azure depolama hizmeti için çapraz kaynak PAYLAŞıMıNı (CORS) kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d04a1-106">The **Remove-AzStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="d04a1-107">Bu cmdlet, bir depolama hizmeti türündeki tüm CORS kurallarını siler.</span><span class="sxs-lookup"><span data-stu-id="d04a1-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="d04a1-108">Bu cmdlet için depolama hizmetleri türleri blob, tablo, kuyruk ve dosyadır.</span><span class="sxs-lookup"><span data-stu-id="d04a1-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="d04a1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d04a1-109">EXAMPLES</span></span>

### <span data-ttu-id="d04a1-110">Örnek 1: blob hizmeti için CORS kurallarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d04a1-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="d04a1-111">Bu komut, blob hizmet türü için CORS kurallarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d04a1-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="d04a1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d04a1-112">PARAMETERS</span></span>

### <span data-ttu-id="d04a1-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d04a1-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d04a1-114">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="d04a1-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d04a1-115">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="d04a1-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d04a1-116">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="d04a1-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d04a1-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d04a1-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d04a1-118">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d04a1-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d04a1-119">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d04a1-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d04a1-120">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="d04a1-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d04a1-121">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="d04a1-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d04a1-122">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="d04a1-122">The default value is 10.</span></span>

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

### <span data-ttu-id="d04a1-123">-Context</span><span class="sxs-lookup"><span data-stu-id="d04a1-123">-Context</span></span>
<span data-ttu-id="d04a1-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d04a1-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="d04a1-125">Depolama bağlamını edinmek için New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d04a1-125">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d04a1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d04a1-126">-DefaultProfile</span></span>
<span data-ttu-id="d04a1-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d04a1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d04a1-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d04a1-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d04a1-129">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d04a1-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="d04a1-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="d04a1-130">-ServiceType</span></span>
<span data-ttu-id="d04a1-131">Bu cmdlet 'in kuralları kaldırdığı Azure depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d04a1-131">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="d04a1-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d04a1-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d04a1-133">'Unu</span><span class="sxs-lookup"><span data-stu-id="d04a1-133">Blob</span></span> 
- <span data-ttu-id="d04a1-134">Tablo</span><span class="sxs-lookup"><span data-stu-id="d04a1-134">Table</span></span> 
- <span data-ttu-id="d04a1-135">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="d04a1-135">Queue</span></span> 
- <span data-ttu-id="d04a1-136">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="d04a1-136">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d04a1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d04a1-137">CommonParameters</span></span>
<span data-ttu-id="d04a1-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d04a1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d04a1-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d04a1-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d04a1-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d04a1-140">INPUTS</span></span>

### <span data-ttu-id="d04a1-141">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="d04a1-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d04a1-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d04a1-142">OUTPUTS</span></span>

### <span data-ttu-id="d04a1-143">System. void</span><span class="sxs-lookup"><span data-stu-id="d04a1-143">System.Void</span></span>

## <span data-ttu-id="d04a1-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d04a1-144">NOTES</span></span>

## <span data-ttu-id="d04a1-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d04a1-145">RELATED LINKS</span></span>

[<span data-ttu-id="d04a1-146">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="d04a1-146">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="d04a1-147">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="d04a1-147">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


