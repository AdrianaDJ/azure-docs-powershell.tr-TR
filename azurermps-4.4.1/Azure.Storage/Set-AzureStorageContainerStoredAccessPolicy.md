---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 63fd207c9d3348e17718f6d4ad8dbd53a09752af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764290"
---
# <span data-ttu-id="9d196-101">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9d196-101">Set-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="9d196-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d196-102">SYNOPSIS</span></span>
<span data-ttu-id="9d196-103">Azure depolama kapsayıcısı için depolanan bir erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9d196-103">Sets a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d196-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9d196-104">SYNTAX</span></span>

```
Set-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d196-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9d196-105">DESCRIPTION</span></span>
<span data-ttu-id="9d196-106">**Set-AzureStorageContainerStoredAccessPolicy** cmdlet 'i, bir Azure depolama kapsayıcısı için depolanan bir erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9d196-106">The **Set-AzureStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="9d196-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9d196-107">EXAMPLES</span></span>

### <span data-ttu-id="9d196-108">Örnek 1: tam izinli bir depolama kapsayıcısında depolanan erişim ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="9d196-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="9d196-109">Bu komut MyContainer adındaki depolama kapsayıcısı için Policy06 adlı bir erişim ilkesi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9d196-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="9d196-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9d196-110">PARAMETERS</span></span>

### <span data-ttu-id="9d196-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9d196-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9d196-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d196-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9d196-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="9d196-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9d196-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="9d196-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9d196-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9d196-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9d196-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d196-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9d196-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9d196-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9d196-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="9d196-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9d196-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="9d196-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9d196-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="9d196-120">The default value is 10.</span></span>

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

### <span data-ttu-id="9d196-121">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="9d196-121">-Container</span></span>
<span data-ttu-id="9d196-122">Azure depolama kapsayıcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d196-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="9d196-123">-Context</span><span class="sxs-lookup"><span data-stu-id="9d196-123">-Context</span></span>
<span data-ttu-id="9d196-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d196-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9d196-125">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9d196-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9d196-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="9d196-126">-ExpiryTime</span></span>
<span data-ttu-id="9d196-127">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d196-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="9d196-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="9d196-128">-NoExpiryTime</span></span>
<span data-ttu-id="9d196-129">Erişim ilkesinde son kullanma tarihi olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9d196-129">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d196-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="9d196-130">-NoStartTime</span></span>
<span data-ttu-id="9d196-131">Başlangıç saatini $Null olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9d196-131">Sets the start time to be $Null.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d196-132">-İzin</span><span class="sxs-lookup"><span data-stu-id="9d196-132">-Permission</span></span>
<span data-ttu-id="9d196-133">Depolanan erişim ilkesinde depolama kapsayıcısına erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d196-133">Specifies permissions in the stored access policy to access the storage container.</span></span>

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

### <span data-ttu-id="9d196-134">-İlke</span><span class="sxs-lookup"><span data-stu-id="9d196-134">-Policy</span></span>
<span data-ttu-id="9d196-135">Depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d196-135">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="9d196-136">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9d196-136">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9d196-137">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d196-137">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9d196-138">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="9d196-138">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9d196-139">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="9d196-139">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9d196-140">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="9d196-140">-StartTime</span></span>
<span data-ttu-id="9d196-141">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d196-141">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="9d196-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="9d196-142">-Confirm</span></span>
<span data-ttu-id="9d196-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9d196-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d196-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d196-144">-WhatIf</span></span>
<span data-ttu-id="9d196-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9d196-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d196-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9d196-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d196-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d196-147">CommonParameters</span></span>
<span data-ttu-id="9d196-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9d196-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d196-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d196-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d196-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9d196-150">INPUTS</span></span>

### <span data-ttu-id="9d196-151">Dizisi</span><span class="sxs-lookup"><span data-stu-id="9d196-151">String</span></span>

<span data-ttu-id="9d196-152">Parametre ' Container ', ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="9d196-152">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="9d196-153">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="9d196-153">IStorageContext</span></span>

<span data-ttu-id="9d196-154">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="9d196-154">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="9d196-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9d196-155">OUTPUTS</span></span>

### <span data-ttu-id="9d196-156">System. String</span><span class="sxs-lookup"><span data-stu-id="9d196-156">System.String</span></span>

## <span data-ttu-id="9d196-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9d196-157">NOTES</span></span>

## <span data-ttu-id="9d196-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9d196-158">RELATED LINKS</span></span>

[<span data-ttu-id="9d196-159">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9d196-159">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="9d196-160">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="9d196-160">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="9d196-161">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9d196-161">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="9d196-162">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9d196-162">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)
