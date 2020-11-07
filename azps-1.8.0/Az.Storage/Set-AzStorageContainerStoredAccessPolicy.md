---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 0f56427fe576cec2aee573295fe57f0f71273ffa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758542"
---
# <span data-ttu-id="07f34-101">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="07f34-101">Set-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="07f34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07f34-102">SYNOPSIS</span></span>
<span data-ttu-id="07f34-103">Azure depolama kapsayıcısı için depolanan bir erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="07f34-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="07f34-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07f34-104">SYNTAX</span></span>

```
Set-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07f34-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="07f34-105">DESCRIPTION</span></span>
<span data-ttu-id="07f34-106">**Set-AzStorageContainerStoredAccessPolicy** cmdlet 'i, bir Azure depolama kapsayıcısı için depolanan bir erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="07f34-106">The **Set-AzStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="07f34-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07f34-107">EXAMPLES</span></span>

### <span data-ttu-id="07f34-108">Örnek 1: tam izinli bir depolama kapsayıcısında depolanan erişim ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="07f34-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="07f34-109">Bu komut MyContainer adındaki depolama kapsayıcısı için Policy06 adlı bir erişim ilkesi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="07f34-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="07f34-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07f34-110">PARAMETERS</span></span>

### <span data-ttu-id="07f34-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="07f34-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="07f34-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="07f34-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="07f34-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="07f34-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="07f34-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="07f34-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="07f34-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="07f34-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="07f34-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07f34-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="07f34-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="07f34-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="07f34-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="07f34-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="07f34-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="07f34-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="07f34-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="07f34-120">The default value is 10.</span></span>

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

### <span data-ttu-id="07f34-121">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="07f34-121">-Container</span></span>
<span data-ttu-id="07f34-122">Azure depolama kapsayıcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07f34-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07f34-123">-Context</span><span class="sxs-lookup"><span data-stu-id="07f34-123">-Context</span></span>
<span data-ttu-id="07f34-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07f34-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="07f34-125">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="07f34-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="07f34-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f34-126">-DefaultProfile</span></span>
<span data-ttu-id="07f34-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="07f34-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07f34-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="07f34-128">-ExpiryTime</span></span>
<span data-ttu-id="07f34-129">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="07f34-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07f34-130">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="07f34-130">-NoExpiryTime</span></span>
<span data-ttu-id="07f34-131">Erişim ilkesinde son kullanma tarihi olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="07f34-131">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="07f34-132">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="07f34-132">-NoStartTime</span></span>
<span data-ttu-id="07f34-133">Başlangıç saatini $Null olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="07f34-133">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="07f34-134">-İzin</span><span class="sxs-lookup"><span data-stu-id="07f34-134">-Permission</span></span>
<span data-ttu-id="07f34-135">Depolanan erişim ilkesinde depolama kapsayıcısına erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="07f34-135">Specifies permissions in the stored access policy to access the storage container.</span></span>
<span data-ttu-id="07f34-136">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="07f34-136">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07f34-137">-İlke</span><span class="sxs-lookup"><span data-stu-id="07f34-137">-Policy</span></span>
<span data-ttu-id="07f34-138">Depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07f34-138">Specifies the name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07f34-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="07f34-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="07f34-140">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="07f34-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="07f34-141">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="07f34-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="07f34-142">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="07f34-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="07f34-143">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="07f34-143">-StartTime</span></span>
<span data-ttu-id="07f34-144">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="07f34-144">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07f34-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="07f34-145">-Confirm</span></span>
<span data-ttu-id="07f34-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="07f34-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07f34-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07f34-147">-WhatIf</span></span>
<span data-ttu-id="07f34-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="07f34-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07f34-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="07f34-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07f34-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f34-150">CommonParameters</span></span>
<span data-ttu-id="07f34-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07f34-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f34-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07f34-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f34-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07f34-153">INPUTS</span></span>

### <span data-ttu-id="07f34-154">System. String</span><span class="sxs-lookup"><span data-stu-id="07f34-154">System.String</span></span>

### <span data-ttu-id="07f34-155">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="07f34-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="07f34-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07f34-156">OUTPUTS</span></span>

### <span data-ttu-id="07f34-157">System. String</span><span class="sxs-lookup"><span data-stu-id="07f34-157">System.String</span></span>

## <span data-ttu-id="07f34-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07f34-158">NOTES</span></span>

## <span data-ttu-id="07f34-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07f34-159">RELATED LINKS</span></span>

[<span data-ttu-id="07f34-160">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="07f34-160">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="07f34-161">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="07f34-161">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="07f34-162">Yeni-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="07f34-162">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="07f34-163">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="07f34-163">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)
