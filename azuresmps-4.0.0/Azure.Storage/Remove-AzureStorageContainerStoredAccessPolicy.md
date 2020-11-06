---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e2a6e00832ea57f3d5608b30791c37e5cde5be5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571362"
---
# <span data-ttu-id="ed18a-101">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ed18a-101">Remove-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="ed18a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed18a-102">SYNOPSIS</span></span>
<span data-ttu-id="ed18a-103">Depolanan bir Access ilkesini Azure depolama kapsayıcısından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ed18a-103">Removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="ed18a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed18a-104">SYNTAX</span></span>

```
Remove-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed18a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed18a-105">DESCRIPTION</span></span>
<span data-ttu-id="ed18a-106">**Remove-AzureStorageContainerStoredAccessPolicy** cmdlet 'i Azure depolama kapsayıcısından depolanan bir Access ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ed18a-106">The **Remove-AzureStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="ed18a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed18a-107">EXAMPLES</span></span>

### <span data-ttu-id="ed18a-108">Örnek 1: depolama kapsayıcısından depolanan bir erişim ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="ed18a-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="ed18a-109">Bu komut MyContainer adlı depolanan kapsayıcıdan Policy03 adındaki bir erişim ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ed18a-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="ed18a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed18a-110">PARAMETERS</span></span>

### <span data-ttu-id="ed18a-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ed18a-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ed18a-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed18a-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ed18a-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="ed18a-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ed18a-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="ed18a-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ed18a-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ed18a-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ed18a-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed18a-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ed18a-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ed18a-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ed18a-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="ed18a-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ed18a-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="ed18a-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ed18a-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="ed18a-120">The default value is 10.</span></span>

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

### <span data-ttu-id="ed18a-121">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="ed18a-121">-Container</span></span>
<span data-ttu-id="ed18a-122">Azure depolama kapsayıcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed18a-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed18a-123">-Context</span><span class="sxs-lookup"><span data-stu-id="ed18a-123">-Context</span></span>
<span data-ttu-id="ed18a-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed18a-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ed18a-125">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ed18a-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ed18a-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ed18a-126">-PassThru</span></span>
<span data-ttu-id="ed18a-127">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="ed18a-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ed18a-128">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="ed18a-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ed18a-129">-İlke</span><span class="sxs-lookup"><span data-stu-id="ed18a-129">-Policy</span></span>
<span data-ttu-id="ed18a-130">Bu SAS belirtecinin izinlerini içeren depolanan erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed18a-130">Specifies the stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed18a-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ed18a-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ed18a-132">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed18a-132">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ed18a-133">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="ed18a-133">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ed18a-134">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="ed18a-134">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ed18a-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="ed18a-135">-Confirm</span></span>
<span data-ttu-id="ed18a-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ed18a-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed18a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed18a-137">-WhatIf</span></span>
<span data-ttu-id="ed18a-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed18a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed18a-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ed18a-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed18a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed18a-140">CommonParameters</span></span>
<span data-ttu-id="ed18a-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed18a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed18a-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed18a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed18a-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed18a-143">INPUTS</span></span>

## <span data-ttu-id="ed18a-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed18a-144">OUTPUTS</span></span>

## <span data-ttu-id="ed18a-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed18a-145">NOTES</span></span>

## <span data-ttu-id="ed18a-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed18a-146">RELATED LINKS</span></span>

[<span data-ttu-id="ed18a-147">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ed18a-147">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="ed18a-148">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ed18a-148">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="ed18a-149">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ed18a-149">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="ed18a-150">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ed18a-150">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)
