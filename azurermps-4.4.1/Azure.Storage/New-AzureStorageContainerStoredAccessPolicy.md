---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3429c142ce31f8cd08786e180b6725130501ac45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588340"
---
# <span data-ttu-id="34618-101">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="34618-101">New-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="34618-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34618-102">SYNOPSIS</span></span>
<span data-ttu-id="34618-103">Azure depolama kapsayıcısı için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34618-103">Creates a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34618-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34618-104">SYNTAX</span></span>

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="34618-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="34618-105">DESCRIPTION</span></span>
<span data-ttu-id="34618-106">**New-AzureStorageContainerStoredAccessPolicy** cmdlet 'ı bir Azure depolama kapsayıcısı için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34618-106">The **New-AzureStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="34618-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34618-107">EXAMPLES</span></span>

### <span data-ttu-id="34618-108">Örnek 1: depolama kapsayıcısında depolanan bir Access ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="34618-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="34618-109">Bu komut MyContainer adındaki depolama kapsayıcısında Policy01 adlı bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34618-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="34618-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34618-110">PARAMETERS</span></span>

### <span data-ttu-id="34618-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="34618-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="34618-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="34618-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="34618-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="34618-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="34618-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="34618-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="34618-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="34618-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="34618-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34618-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="34618-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34618-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="34618-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="34618-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="34618-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="34618-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="34618-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="34618-120">The default value is 10.</span></span>

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

### <span data-ttu-id="34618-121">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="34618-121">-Container</span></span>
<span data-ttu-id="34618-122">Azure depolama kapsayıcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34618-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="34618-123">-Context</span><span class="sxs-lookup"><span data-stu-id="34618-123">-Context</span></span>
<span data-ttu-id="34618-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34618-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="34618-125">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="34618-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="34618-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="34618-126">-ExpiryTime</span></span>
<span data-ttu-id="34618-127">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="34618-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34618-128">-İzin</span><span class="sxs-lookup"><span data-stu-id="34618-128">-Permission</span></span>
<span data-ttu-id="34618-129">Depolanan erişim ilkesindeki kapsayıcıya erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34618-129">Specifies permissions in the stored access policy to access the container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34618-130">-İlke</span><span class="sxs-lookup"><span data-stu-id="34618-130">-Policy</span></span>
<span data-ttu-id="34618-131">Bu SAS belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34618-131">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34618-132">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="34618-132">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="34618-133">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="34618-133">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="34618-134">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="34618-134">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="34618-135">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="34618-135">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="34618-136">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="34618-136">-StartTime</span></span>
<span data-ttu-id="34618-137">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="34618-137">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34618-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34618-138">CommonParameters</span></span>
<span data-ttu-id="34618-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34618-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34618-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34618-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34618-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34618-141">INPUTS</span></span>

### <span data-ttu-id="34618-142">Dizisi</span><span class="sxs-lookup"><span data-stu-id="34618-142">String</span></span>

<span data-ttu-id="34618-143">Parametre ' Container ', ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="34618-143">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="34618-144">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="34618-144">IStorageContext</span></span>

<span data-ttu-id="34618-145">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="34618-145">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="34618-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34618-146">OUTPUTS</span></span>

### <span data-ttu-id="34618-147">System. String</span><span class="sxs-lookup"><span data-stu-id="34618-147">System.String</span></span>

## <span data-ttu-id="34618-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34618-148">NOTES</span></span>

## <span data-ttu-id="34618-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34618-149">RELATED LINKS</span></span>

[<span data-ttu-id="34618-150">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="34618-150">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="34618-151">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="34618-151">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="34618-152">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="34618-152">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="34618-153">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="34618-153">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


