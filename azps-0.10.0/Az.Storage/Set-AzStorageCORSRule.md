---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
ms.openlocfilehash: d57b5b2c7c91e56c56d5674edbb5b412a221cd56
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936164"
---
# <span data-ttu-id="06e83-101">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="06e83-101">Set-AzStorageCORSRule</span></span>

## <span data-ttu-id="06e83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06e83-102">SYNOPSIS</span></span>
<span data-ttu-id="06e83-103">Bir depolama hizmeti türü için CORS kurallarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="06e83-103">Sets the CORS rules for a type of Storage service.</span></span>

## <span data-ttu-id="06e83-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06e83-104">SYNTAX</span></span>

```
Set-AzStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="06e83-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="06e83-105">DESCRIPTION</span></span>
<span data-ttu-id="06e83-106">**Set-AzStorageCORSRule** cmdlet 'i, bir Azure depolama hizmeti türünün çapraz kaynak PAYLAŞıMı (CORS) kurallarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="06e83-106">The **Set-AzStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="06e83-107">Bu cmdlet için depolama hizmetleri türleri blob, tablo, kuyruk ve dosyadır.</span><span class="sxs-lookup"><span data-stu-id="06e83-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="06e83-108">Bu cmdlet var olan kuralların üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="06e83-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="06e83-109">Geçerli kuralları görmek için Get-AzStorageCORSRule cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="06e83-109">To see the current rules, use the Get-AzStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="06e83-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06e83-110">EXAMPLES</span></span>

### <span data-ttu-id="06e83-111">Örnek 1: blob hizmetine CORS kuralları atama</span><span class="sxs-lookup"><span data-stu-id="06e83-111">Example 1: Assign CORS rules to the blob service</span></span>
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
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="06e83-112">İlk komut $CorsRules değişkenine bir dizi kural atar.</span><span class="sxs-lookup"><span data-stu-id="06e83-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="06e83-113">Bu komut, bu kod bloğundaki birkaç satırın yerine standart extends kullanır.</span><span class="sxs-lookup"><span data-stu-id="06e83-113">This command uses standard extends over several lines in this code block.</span></span>
<span data-ttu-id="06e83-114">İkinci komut $CorsRules kuralları blob hizmet türüne atar.</span><span class="sxs-lookup"><span data-stu-id="06e83-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="06e83-115">Örnek 2: blob hizmeti için CORS kuralının özelliklerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="06e83-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="06e83-116">İlk komut, **Get-AzStorageCORSRule** cmdlet 'Ini kullanarak blob türünün geçerli CORS kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="06e83-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="06e83-117">Komut, kuralları $CorsRules dizi değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="06e83-117">The command stores the rules in the $CorsRules array variable.</span></span>
<span data-ttu-id="06e83-118">İkinci ve üçüncü komutlar $CorsRules ilk kuralı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="06e83-118">The second and third commands modify the first rule in $CorsRules.</span></span>
<span data-ttu-id="06e83-119">Son komut $CorsRules kuralları blob hizmet türüne atar.</span><span class="sxs-lookup"><span data-stu-id="06e83-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="06e83-120">Gözden geçirilmiş kurallar geçerli CORS kurallarının üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="06e83-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="06e83-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06e83-121">PARAMETERS</span></span>

### <span data-ttu-id="06e83-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="06e83-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="06e83-123">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="06e83-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="06e83-124">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="06e83-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="06e83-125">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="06e83-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="06e83-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="06e83-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="06e83-127">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="06e83-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="06e83-128">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06e83-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="06e83-129">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="06e83-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="06e83-130">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="06e83-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="06e83-131">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="06e83-131">The default value is 10.</span></span>

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

### <span data-ttu-id="06e83-132">-Context</span><span class="sxs-lookup"><span data-stu-id="06e83-132">-Context</span></span>
<span data-ttu-id="06e83-133">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="06e83-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="06e83-134">Bağlam almak için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="06e83-134">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="06e83-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="06e83-135">-CorsRules</span></span>
<span data-ttu-id="06e83-136">CORS kuralları dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="06e83-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="06e83-137">Get-AzStorageCORSRule cmdlet 'ini kullanarak var olan kuralları alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06e83-137">You can retrieve the existing rules using the Get-AzStorageCORSRule cmdlet.</span></span>

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

### <span data-ttu-id="06e83-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e83-138">-DefaultProfile</span></span>
<span data-ttu-id="06e83-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="06e83-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06e83-140">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="06e83-140">-PassThru</span></span>
<span data-ttu-id="06e83-141">Bu cmdlet 'in işlemin başarısını yansıtan bir Boole değeri döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="06e83-141">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="06e83-142">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="06e83-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="06e83-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="06e83-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="06e83-144">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="06e83-144">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="06e83-145">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="06e83-145">-ServiceType</span></span>
<span data-ttu-id="06e83-146">Bu cmdlet 'in kuralları atadığı Azure depolama hizmeti türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="06e83-146">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="06e83-147">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="06e83-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="06e83-148">'Unu</span><span class="sxs-lookup"><span data-stu-id="06e83-148">Blob</span></span> 
- <span data-ttu-id="06e83-149">Tablo</span><span class="sxs-lookup"><span data-stu-id="06e83-149">Table</span></span> 
- <span data-ttu-id="06e83-150">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="06e83-150">Queue</span></span> 
- <span data-ttu-id="06e83-151">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="06e83-151">File</span></span>

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

### <span data-ttu-id="06e83-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e83-152">CommonParameters</span></span>
<span data-ttu-id="06e83-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06e83-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e83-154">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06e83-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e83-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06e83-155">INPUTS</span></span>

### <span data-ttu-id="06e83-156">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="06e83-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="06e83-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06e83-157">OUTPUTS</span></span>

### <span data-ttu-id="06e83-158">Microsoft. Windowsazme. Commands. Storage. model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="06e83-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="06e83-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06e83-159">NOTES</span></span>

## <span data-ttu-id="06e83-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06e83-160">RELATED LINKS</span></span>

[<span data-ttu-id="06e83-161">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="06e83-161">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="06e83-162">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="06e83-162">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="06e83-163">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="06e83-163">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)

