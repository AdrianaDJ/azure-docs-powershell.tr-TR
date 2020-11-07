---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageCORSRule.md
ms.openlocfilehash: 2b35f2ba556017d31754fd705bd78641b69e14bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763926"
---
# <span data-ttu-id="c7e31-101">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="c7e31-101">Remove-AzureStorageCORSRule</span></span>

## <span data-ttu-id="c7e31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7e31-102">SYNOPSIS</span></span>
<span data-ttu-id="c7e31-103">Bir depolama hizmeti için CORS 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c7e31-103">Removes CORS for a Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7e31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7e31-104">SYNTAX</span></span>

```
Remove-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c7e31-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7e31-105">DESCRIPTION</span></span>
<span data-ttu-id="c7e31-106">**Remove-AzureStorageCORSRule** cmdlet 'ı bir Azure depolama hizmeti için çapraz kaynak PAYLAŞıMıNı (CORS) kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c7e31-106">The **Remove-AzureStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="c7e31-107">Bu cmdlet, bir depolama hizmeti türündeki tüm CORS kurallarını siler.</span><span class="sxs-lookup"><span data-stu-id="c7e31-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="c7e31-108">Bu cmdlet için depolama hizmetleri türleri blob, tablo, kuyruk ve dosyadır.</span><span class="sxs-lookup"><span data-stu-id="c7e31-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="c7e31-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7e31-109">EXAMPLES</span></span>

### <span data-ttu-id="c7e31-110">Örnek 1: blob hizmeti için CORS kurallarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="c7e31-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="c7e31-111">Bu komut, blob hizmet türü için CORS kurallarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c7e31-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="c7e31-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7e31-112">PARAMETERS</span></span>

### <span data-ttu-id="c7e31-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c7e31-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c7e31-114">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7e31-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c7e31-115">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="c7e31-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c7e31-116">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="c7e31-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c7e31-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c7e31-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c7e31-118">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7e31-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c7e31-119">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7e31-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c7e31-120">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="c7e31-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c7e31-121">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="c7e31-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c7e31-122">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="c7e31-122">The default value is 10.</span></span>

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

### <span data-ttu-id="c7e31-123">-Context</span><span class="sxs-lookup"><span data-stu-id="c7e31-123">-Context</span></span>
<span data-ttu-id="c7e31-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7e31-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="c7e31-125">Depolama bağlamını edinmek için New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7e31-125">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c7e31-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7e31-126">-DefaultProfile</span></span>
<span data-ttu-id="c7e31-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c7e31-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7e31-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c7e31-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c7e31-129">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7e31-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c7e31-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="c7e31-130">-ServiceType</span></span>
<span data-ttu-id="c7e31-131">Bu cmdlet 'in kuralları kaldırdığı Azure depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7e31-131">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="c7e31-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c7e31-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c7e31-133">'Unu</span><span class="sxs-lookup"><span data-stu-id="c7e31-133">Blob</span></span> 
- <span data-ttu-id="c7e31-134">Tablo</span><span class="sxs-lookup"><span data-stu-id="c7e31-134">Table</span></span> 
- <span data-ttu-id="c7e31-135">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="c7e31-135">Queue</span></span> 
- <span data-ttu-id="c7e31-136">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="c7e31-136">File</span></span>

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

### <span data-ttu-id="c7e31-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7e31-137">CommonParameters</span></span>
<span data-ttu-id="c7e31-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7e31-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7e31-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7e31-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7e31-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7e31-140">INPUTS</span></span>

### <span data-ttu-id="c7e31-141">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="c7e31-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c7e31-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7e31-142">OUTPUTS</span></span>

### <span data-ttu-id="c7e31-143">System. void</span><span class="sxs-lookup"><span data-stu-id="c7e31-143">System.Void</span></span>

## <span data-ttu-id="c7e31-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7e31-144">NOTES</span></span>

## <span data-ttu-id="c7e31-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7e31-145">RELATED LINKS</span></span>

[<span data-ttu-id="c7e31-146">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="c7e31-146">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="c7e31-147">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="c7e31-147">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


