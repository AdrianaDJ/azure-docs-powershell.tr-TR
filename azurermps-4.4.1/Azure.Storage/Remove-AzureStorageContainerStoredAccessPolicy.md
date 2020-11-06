---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3dbc0f3c014290cb412751440590cbee1f6df685
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588335"
---
# <span data-ttu-id="64c9d-101">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="64c9d-101">Remove-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="64c9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64c9d-102">SYNOPSIS</span></span>
<span data-ttu-id="64c9d-103">Depolanan bir Access ilkesini Azure depolama kapsayıcısından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="64c9d-103">Removes a stored access policy from an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64c9d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="64c9d-104">SYNTAX</span></span>

```
Remove-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64c9d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="64c9d-105">DESCRIPTION</span></span>
<span data-ttu-id="64c9d-106">**Remove-AzureStorageContainerStoredAccessPolicy** cmdlet 'i Azure depolama kapsayıcısından depolanan bir Access ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="64c9d-106">The **Remove-AzureStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="64c9d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="64c9d-107">EXAMPLES</span></span>

### <span data-ttu-id="64c9d-108">Örnek 1: depolama kapsayıcısından depolanan bir erişim ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="64c9d-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="64c9d-109">Bu komut MyContainer adlı depolanan kapsayıcıdan Policy03 adındaki bir erişim ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="64c9d-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="64c9d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="64c9d-110">PARAMETERS</span></span>

### <span data-ttu-id="64c9d-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="64c9d-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="64c9d-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="64c9d-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="64c9d-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="64c9d-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="64c9d-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="64c9d-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="64c9d-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="64c9d-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="64c9d-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64c9d-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="64c9d-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64c9d-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="64c9d-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="64c9d-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="64c9d-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="64c9d-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="64c9d-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="64c9d-120">The default value is 10.</span></span>

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

### <span data-ttu-id="64c9d-121">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="64c9d-121">-Container</span></span>
<span data-ttu-id="64c9d-122">Azure depolama kapsayıcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64c9d-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="64c9d-123">-Context</span><span class="sxs-lookup"><span data-stu-id="64c9d-123">-Context</span></span>
<span data-ttu-id="64c9d-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64c9d-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="64c9d-125">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="64c9d-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="64c9d-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="64c9d-126">-PassThru</span></span>
<span data-ttu-id="64c9d-127">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="64c9d-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="64c9d-128">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="64c9d-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="64c9d-129">-İlke</span><span class="sxs-lookup"><span data-stu-id="64c9d-129">-Policy</span></span>
<span data-ttu-id="64c9d-130">Bu cmdlet 'in kaldırdığı depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64c9d-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="64c9d-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="64c9d-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="64c9d-132">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="64c9d-132">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="64c9d-133">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="64c9d-133">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="64c9d-134">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="64c9d-134">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="64c9d-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="64c9d-135">-Confirm</span></span>
<span data-ttu-id="64c9d-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="64c9d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64c9d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64c9d-137">-WhatIf</span></span>
<span data-ttu-id="64c9d-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="64c9d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64c9d-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="64c9d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64c9d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64c9d-140">CommonParameters</span></span>
<span data-ttu-id="64c9d-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="64c9d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64c9d-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64c9d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64c9d-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="64c9d-143">INPUTS</span></span>

### <span data-ttu-id="64c9d-144">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="64c9d-144">IStorageContext</span></span>

<span data-ttu-id="64c9d-145">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="64c9d-145">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="64c9d-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="64c9d-146">OUTPUTS</span></span>

### <span data-ttu-id="64c9d-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="64c9d-147">System.Boolean</span></span>

## <span data-ttu-id="64c9d-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="64c9d-148">NOTES</span></span>

## <span data-ttu-id="64c9d-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="64c9d-149">RELATED LINKS</span></span>

[<span data-ttu-id="64c9d-150">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="64c9d-150">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="64c9d-151">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="64c9d-151">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="64c9d-152">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="64c9d-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="64c9d-153">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="64c9d-153">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)
