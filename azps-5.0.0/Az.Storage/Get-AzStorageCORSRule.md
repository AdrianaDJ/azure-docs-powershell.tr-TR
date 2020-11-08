---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
ms.openlocfilehash: 1eb5803c65739c2e202d042efbf6ba4dff815394
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276012"
---
# <span data-ttu-id="338e7-101">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="338e7-101">Get-AzStorageCORSRule</span></span>

## <span data-ttu-id="338e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="338e7-102">SYNOPSIS</span></span>
<span data-ttu-id="338e7-103">Depolama hizmeti türü için CORS kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="338e7-103">Gets CORS rules for a Storage service type.</span></span>

## <span data-ttu-id="338e7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="338e7-104">SYNTAX</span></span>

```
Get-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="338e7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="338e7-105">DESCRIPTION</span></span>
<span data-ttu-id="338e7-106">**Get-AzStorageCORSRule** cmdlet 'i, bir Azure depolama hizmeti türü Için çapraz kaynak PAYLAŞıMı (CORS) kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="338e7-106">The **Get-AzStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="338e7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="338e7-107">EXAMPLES</span></span>

### <span data-ttu-id="338e7-108">Örnek 1: Blob hizmetinin CORS kurallarını alma</span><span class="sxs-lookup"><span data-stu-id="338e7-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="338e7-109">Bu komut, blob hizmet türü için CORS kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="338e7-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="338e7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="338e7-110">PARAMETERS</span></span>

### <span data-ttu-id="338e7-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="338e7-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="338e7-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="338e7-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="338e7-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="338e7-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="338e7-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="338e7-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="338e7-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="338e7-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="338e7-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="338e7-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="338e7-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="338e7-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="338e7-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="338e7-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="338e7-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="338e7-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="338e7-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="338e7-120">The default value is 10.</span></span>

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

### <span data-ttu-id="338e7-121">-Context</span><span class="sxs-lookup"><span data-stu-id="338e7-121">-Context</span></span>
<span data-ttu-id="338e7-122">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="338e7-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="338e7-123">Bağlam almak için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="338e7-123">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="338e7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="338e7-124">-DefaultProfile</span></span>
<span data-ttu-id="338e7-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="338e7-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="338e7-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="338e7-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="338e7-127">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="338e7-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="338e7-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="338e7-128">-ServiceType</span></span>
<span data-ttu-id="338e7-129">Bu cmdlet 'in CORS kurallarını aldığı Azure depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="338e7-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="338e7-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="338e7-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="338e7-131">'Unu</span><span class="sxs-lookup"><span data-stu-id="338e7-131">Blob</span></span> 
- <span data-ttu-id="338e7-132">Tablo</span><span class="sxs-lookup"><span data-stu-id="338e7-132">Table</span></span> 
- <span data-ttu-id="338e7-133">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="338e7-133">Queue</span></span> 
- <span data-ttu-id="338e7-134">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="338e7-134">File</span></span>

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

### <span data-ttu-id="338e7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="338e7-135">CommonParameters</span></span>
<span data-ttu-id="338e7-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="338e7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="338e7-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="338e7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="338e7-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="338e7-138">INPUTS</span></span>

### <span data-ttu-id="338e7-139">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="338e7-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="338e7-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="338e7-140">OUTPUTS</span></span>

### <span data-ttu-id="338e7-141">Microsoft. Windowsazme. Commands. Storage. model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="338e7-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="338e7-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="338e7-142">NOTES</span></span>

## <span data-ttu-id="338e7-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="338e7-143">RELATED LINKS</span></span>

[<span data-ttu-id="338e7-144">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="338e7-144">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)

[<span data-ttu-id="338e7-145">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="338e7-145">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


