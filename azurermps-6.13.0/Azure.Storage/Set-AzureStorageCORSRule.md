---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
ms.openlocfilehash: 21293b8262a10c5710ed132413658c3c1cfbd254
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587356"
---
# <span data-ttu-id="4f43c-101">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="4f43c-101">Set-AzureStorageCORSRule</span></span>

## <span data-ttu-id="4f43c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f43c-102">SYNOPSIS</span></span>
<span data-ttu-id="4f43c-103">Bir depolama hizmeti türü için CORS kurallarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4f43c-103">Sets the CORS rules for a type of Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f43c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f43c-104">SYNTAX</span></span>

```
Set-AzureStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4f43c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f43c-105">DESCRIPTION</span></span>
<span data-ttu-id="4f43c-106">**Set-AzureStorageCORSRule** cmdlet 'i, bir Azure depolama hizmeti türünün çapraz kaynak PAYLAŞıMı (CORS) kurallarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4f43c-106">The **Set-AzureStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="4f43c-107">Bu cmdlet için depolama hizmetleri türleri blob, tablo, kuyruk ve dosyadır.</span><span class="sxs-lookup"><span data-stu-id="4f43c-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="4f43c-108">Bu cmdlet var olan kuralların üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="4f43c-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="4f43c-109">Geçerli kuralları görmek için Get-AzureStorageCORSRule cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f43c-109">To see the current rules, use the Get-AzureStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="4f43c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f43c-110">EXAMPLES</span></span>

### <span data-ttu-id="4f43c-111">Örnek 1: blob hizmetine CORS kuralları atama</span><span class="sxs-lookup"><span data-stu-id="4f43c-111">Example 1: Assign CORS rules to the blob service</span></span>
```
PS C:\>$CorsRules = (@{
    AllowedHeaders=@("x-ms-blob-content-type","x-ms-blob-content-disposition");
    AllowedOrigins=@("*");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Get","Connect")},
    @{
    AllowedOrigins=@("http://www.fabrikam.com","http://www.contoso.com"); 
    ExposedHeaders=@("x-ms-meta-data*","x-ms-meta-customheader"); 
    AllowedHeaders=@("x-ms-meta-target*","x-ms-meta-customheader");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Put")})
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="4f43c-112">İlk komut $CorsRules değişkenine bir dizi kural atar.</span><span class="sxs-lookup"><span data-stu-id="4f43c-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="4f43c-113">Bu komut, bu kod bloğundaki birkaç satırın yerine standart extends kullanır.</span><span class="sxs-lookup"><span data-stu-id="4f43c-113">This command uses standard extends over several lines in this code block.</span></span>
<span data-ttu-id="4f43c-114">İkinci komut $CorsRules kuralları blob hizmet türüne atar.</span><span class="sxs-lookup"><span data-stu-id="4f43c-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="4f43c-115">Örnek 2: blob hizmeti için CORS kuralının özelliklerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="4f43c-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzureStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="4f43c-116">İlk komut, **Get-AzureStorageCORSRule** cmdlet 'Ini kullanarak blob türünün geçerli CORS kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="4f43c-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzureStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="4f43c-117">Komut, kuralları $CorsRules dizi değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4f43c-117">The command stores the rules in the $CorsRules array variable.</span></span>
<span data-ttu-id="4f43c-118">İkinci ve üçüncü komutlar $CorsRules ilk kuralı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4f43c-118">The second and third commands modify the first rule in $CorsRules.</span></span>
<span data-ttu-id="4f43c-119">Son komut $CorsRules kuralları blob hizmet türüne atar.</span><span class="sxs-lookup"><span data-stu-id="4f43c-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="4f43c-120">Gözden geçirilmiş kurallar geçerli CORS kurallarının üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="4f43c-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="4f43c-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f43c-121">PARAMETERS</span></span>

### <span data-ttu-id="4f43c-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4f43c-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4f43c-123">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f43c-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4f43c-124">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="4f43c-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4f43c-125">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="4f43c-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4f43c-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4f43c-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4f43c-127">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f43c-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4f43c-128">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f43c-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4f43c-129">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="4f43c-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4f43c-130">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="4f43c-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4f43c-131">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="4f43c-131">The default value is 10.</span></span>

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

### <span data-ttu-id="4f43c-132">-Context</span><span class="sxs-lookup"><span data-stu-id="4f43c-132">-Context</span></span>
<span data-ttu-id="4f43c-133">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f43c-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="4f43c-134">Bağlam almak için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f43c-134">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4f43c-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="4f43c-135">-CorsRules</span></span>
<span data-ttu-id="4f43c-136">CORS kuralları dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f43c-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="4f43c-137">Get-AzureStorageCORSRule cmdlet 'ini kullanarak var olan kuralları alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f43c-137">You can retrieve the existing rules using the Get-AzureStorageCORSRule cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f43c-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f43c-138">-DefaultProfile</span></span>
<span data-ttu-id="4f43c-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4f43c-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f43c-140">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4f43c-140">-PassThru</span></span>
<span data-ttu-id="4f43c-141">Bu cmdlet 'in işlemin başarısını yansıtan bir Boole değeri döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="4f43c-141">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="4f43c-142">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="4f43c-142">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f43c-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4f43c-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4f43c-144">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f43c-144">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4f43c-145">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="4f43c-145">-ServiceType</span></span>
<span data-ttu-id="4f43c-146">Bu cmdlet 'in kuralları atadığı Azure depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f43c-146">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="4f43c-147">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4f43c-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4f43c-148">'Unu</span><span class="sxs-lookup"><span data-stu-id="4f43c-148">Blob</span></span> 
- <span data-ttu-id="4f43c-149">Tablo</span><span class="sxs-lookup"><span data-stu-id="4f43c-149">Table</span></span> 
- <span data-ttu-id="4f43c-150">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="4f43c-150">Queue</span></span> 
- <span data-ttu-id="4f43c-151">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="4f43c-151">File</span></span>

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

### <span data-ttu-id="4f43c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f43c-152">CommonParameters</span></span>
<span data-ttu-id="4f43c-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f43c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f43c-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f43c-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f43c-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f43c-155">INPUTS</span></span>

### <span data-ttu-id="4f43c-156">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="4f43c-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4f43c-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f43c-157">OUTPUTS</span></span>

### <span data-ttu-id="4f43c-158">Microsoft. Windowsazme. Commands. Storage. model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="4f43c-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="4f43c-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f43c-159">NOTES</span></span>

## <span data-ttu-id="4f43c-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f43c-160">RELATED LINKS</span></span>

[<span data-ttu-id="4f43c-161">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="4f43c-161">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="4f43c-162">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="4f43c-162">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="4f43c-163">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="4f43c-163">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)


