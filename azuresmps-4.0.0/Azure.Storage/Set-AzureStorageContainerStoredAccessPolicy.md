---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1bdded3834806e33f4605f626b78fe06bc370bf6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572482"
---
# <span data-ttu-id="5b3ee-101">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5b3ee-101">Set-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="5b3ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b3ee-102">SYNOPSIS</span></span>
<span data-ttu-id="5b3ee-103">Azure depolama kapsayıcısı için depolanan bir erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="5b3ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b3ee-104">SYNTAX</span></span>

```
Set-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b3ee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b3ee-105">DESCRIPTION</span></span>
<span data-ttu-id="5b3ee-106">**Set-AzureStorageContainerStoredAccessPolicy** cmdlet 'i, bir Azure depolama kapsayıcısı için depolanan bir erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-106">The **Set-AzureStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="5b3ee-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b3ee-107">EXAMPLES</span></span>

### <span data-ttu-id="5b3ee-108">Örnek 1: depolama kapsayıcısında depolanan bir erişim ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="5b3ee-108">Example 1: Set a stored access policy in a storage container</span></span>
```
PS C:\>Set-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06"
```

<span data-ttu-id="5b3ee-109">Bu komut MyContainer adındaki depolama kapsayıcısı için Policy06 adlı bir erişim ilkesi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="5b3ee-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b3ee-110">PARAMETERS</span></span>

### <span data-ttu-id="5b3ee-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5b3ee-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5b3ee-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5b3ee-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5b3ee-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5b3ee-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5b3ee-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5b3ee-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5b3ee-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5b3ee-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5b3ee-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5b3ee-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-120">The default value is 10.</span></span>

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

### <span data-ttu-id="5b3ee-121">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="5b3ee-121">-Container</span></span>
<span data-ttu-id="5b3ee-122">Azure depolama kapsayıcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="5b3ee-123">-Context</span><span class="sxs-lookup"><span data-stu-id="5b3ee-123">-Context</span></span>
<span data-ttu-id="5b3ee-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5b3ee-125">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5b3ee-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5b3ee-126">-ExpiryTime</span></span>
<span data-ttu-id="5b3ee-127">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="5b3ee-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5b3ee-128">-NoExpiryTime</span></span>
<span data-ttu-id="5b3ee-129">Erişim ilkesinde son kullanma tarihi olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-129">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="5b3ee-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="5b3ee-130">-NoStartTime</span></span>
<span data-ttu-id="5b3ee-131">Başlangıç saatini $Null olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-131">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="5b3ee-132">-İzin</span><span class="sxs-lookup"><span data-stu-id="5b3ee-132">-Permission</span></span>
<span data-ttu-id="5b3ee-133">Bu kapsayıcıya genel erişim düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-133">Specifies the level of public access to this container.</span></span>

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

### <span data-ttu-id="5b3ee-134">-İlke</span><span class="sxs-lookup"><span data-stu-id="5b3ee-134">-Policy</span></span>
<span data-ttu-id="5b3ee-135">Bu paylaşılan erişim Imzası (SAS) belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-135">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="5b3ee-136">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5b3ee-136">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5b3ee-137">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-137">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5b3ee-138">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-138">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5b3ee-139">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-139">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5b3ee-140">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="5b3ee-140">-StartTime</span></span>
<span data-ttu-id="5b3ee-141">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-141">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="5b3ee-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="5b3ee-142">-Confirm</span></span>
<span data-ttu-id="5b3ee-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b3ee-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b3ee-144">-WhatIf</span></span>
<span data-ttu-id="5b3ee-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b3ee-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b3ee-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b3ee-147">CommonParameters</span></span>
<span data-ttu-id="5b3ee-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b3ee-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b3ee-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b3ee-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b3ee-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b3ee-150">INPUTS</span></span>

## <span data-ttu-id="5b3ee-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b3ee-151">OUTPUTS</span></span>

## <span data-ttu-id="5b3ee-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b3ee-152">NOTES</span></span>

## <span data-ttu-id="5b3ee-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b3ee-153">RELATED LINKS</span></span>

[<span data-ttu-id="5b3ee-154">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5b3ee-154">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="5b3ee-155">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5b3ee-155">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="5b3ee-156">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5b3ee-156">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="5b3ee-157">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5b3ee-157">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)
