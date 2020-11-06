---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageCORSRule.md
ms.openlocfilehash: 6b5d7fa889810563964aa66a34b567f482781ac6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589636"
---
# <span data-ttu-id="51c3e-101">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="51c3e-101">Get-AzureStorageCORSRule</span></span>

## <span data-ttu-id="51c3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51c3e-102">SYNOPSIS</span></span>
<span data-ttu-id="51c3e-103">Depolama hizmeti türü için CORS kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="51c3e-103">Gets CORS rules for a Storage service type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51c3e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51c3e-104">SYNTAX</span></span>

```
Get-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="51c3e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="51c3e-105">DESCRIPTION</span></span>
<span data-ttu-id="51c3e-106">**Get-AzureStorageCORSRule** cmdlet 'ı bir Azure depolama hizmeti türü Için çapraz kaynak PAYLAŞıMı (CORS) kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="51c3e-106">The **Get-AzureStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="51c3e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51c3e-107">EXAMPLES</span></span>

### <span data-ttu-id="51c3e-108">Örnek 1: Blob hizmetinin CORS kurallarını alma</span><span class="sxs-lookup"><span data-stu-id="51c3e-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="51c3e-109">Bu komut, blob hizmet türü için CORS kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="51c3e-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="51c3e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51c3e-110">PARAMETERS</span></span>

### <span data-ttu-id="51c3e-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="51c3e-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="51c3e-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="51c3e-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="51c3e-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="51c3e-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="51c3e-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="51c3e-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="51c3e-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="51c3e-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="51c3e-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51c3e-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="51c3e-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="51c3e-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="51c3e-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="51c3e-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="51c3e-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="51c3e-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="51c3e-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="51c3e-120">The default value is 10.</span></span>

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

### <span data-ttu-id="51c3e-121">-Context</span><span class="sxs-lookup"><span data-stu-id="51c3e-121">-Context</span></span>
<span data-ttu-id="51c3e-122">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51c3e-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="51c3e-123">Bağlam almak için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="51c3e-123">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="51c3e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51c3e-124">-DefaultProfile</span></span>
<span data-ttu-id="51c3e-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="51c3e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51c3e-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="51c3e-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="51c3e-127">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="51c3e-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="51c3e-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="51c3e-128">-ServiceType</span></span>
<span data-ttu-id="51c3e-129">Bu cmdlet 'in CORS kurallarını aldığı Azure depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="51c3e-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="51c3e-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="51c3e-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="51c3e-131">'Unu</span><span class="sxs-lookup"><span data-stu-id="51c3e-131">Blob</span></span> 
- <span data-ttu-id="51c3e-132">Tablo</span><span class="sxs-lookup"><span data-stu-id="51c3e-132">Table</span></span> 
- <span data-ttu-id="51c3e-133">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="51c3e-133">Queue</span></span> 
- <span data-ttu-id="51c3e-134">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="51c3e-134">File</span></span>

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

### <span data-ttu-id="51c3e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51c3e-135">CommonParameters</span></span>
<span data-ttu-id="51c3e-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51c3e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51c3e-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51c3e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51c3e-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51c3e-138">INPUTS</span></span>

### <span data-ttu-id="51c3e-139">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="51c3e-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="51c3e-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51c3e-140">OUTPUTS</span></span>

### <span data-ttu-id="51c3e-141">Microsoft. Windowsazme. Commands. Storage. model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="51c3e-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="51c3e-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51c3e-142">NOTES</span></span>

## <span data-ttu-id="51c3e-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51c3e-143">RELATED LINKS</span></span>

[<span data-ttu-id="51c3e-144">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="51c3e-144">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)

[<span data-ttu-id="51c3e-145">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="51c3e-145">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


