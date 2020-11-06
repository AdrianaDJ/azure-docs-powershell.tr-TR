---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShareStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: b88a03f38ff3e88b6fbbe7b966498e547f8cc026
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588327"
---
# <span data-ttu-id="b936c-101">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b936c-101">Remove-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="b936c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b936c-102">SYNOPSIS</span></span>
<span data-ttu-id="b936c-103">Depolanan bir Access ilkesini depolama paylaşımından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b936c-103">Removes a stored access policy from a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b936c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b936c-104">SYNTAX</span></span>

```
Remove-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b936c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b936c-105">DESCRIPTION</span></span>
<span data-ttu-id="b936c-106">**Remove-AzureStorageShareStoredAccessPolicy** cmdlet 'ı Azure depolama paylaşımından depolanan bir Access ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b936c-106">The **Remove-AzureStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="b936c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b936c-107">EXAMPLES</span></span>

### <span data-ttu-id="b936c-108">Örnek 1: Azure depolama paylaşımından depolanan bir Access ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="b936c-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="b936c-109">Bu komut, ContosoShare adlı bir depolanmış erişim ilkesini ContosoShare 'tan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b936c-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="b936c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b936c-110">PARAMETERS</span></span>

### <span data-ttu-id="b936c-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b936c-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b936c-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="b936c-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b936c-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="b936c-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b936c-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="b936c-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b936c-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b936c-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b936c-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b936c-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b936c-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b936c-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b936c-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="b936c-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b936c-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="b936c-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b936c-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="b936c-120">The default value is 10.</span></span>

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

### <span data-ttu-id="b936c-121">-Context</span><span class="sxs-lookup"><span data-stu-id="b936c-121">-Context</span></span>
<span data-ttu-id="b936c-122">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b936c-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b936c-123">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b936c-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="b936c-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b936c-124">-PassThru</span></span>
<span data-ttu-id="b936c-125">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="b936c-125">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="b936c-126">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="b936c-126">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="b936c-127">-İlke</span><span class="sxs-lookup"><span data-stu-id="b936c-127">-Policy</span></span>
<span data-ttu-id="b936c-128">Bu cmdlet 'in kaldırdığı depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b936c-128">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b936c-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b936c-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b936c-130">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b936c-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="b936c-131">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="b936c-131">-ShareName</span></span>
<span data-ttu-id="b936c-132">Bu cmdlet 'in ilkeyi kaldırdığı depolama paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b936c-132">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

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

### <span data-ttu-id="b936c-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="b936c-133">-Confirm</span></span>
<span data-ttu-id="b936c-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b936c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b936c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b936c-135">-WhatIf</span></span>
<span data-ttu-id="b936c-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b936c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b936c-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b936c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b936c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b936c-138">CommonParameters</span></span>
<span data-ttu-id="b936c-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b936c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b936c-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b936c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b936c-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b936c-141">INPUTS</span></span>

### <span data-ttu-id="b936c-142">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="b936c-142">IStorageContext</span></span>

<span data-ttu-id="b936c-143">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b936c-143">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="b936c-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b936c-144">OUTPUTS</span></span>

### <span data-ttu-id="b936c-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b936c-145">System.Boolean</span></span>

## <span data-ttu-id="b936c-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b936c-146">NOTES</span></span>

## <span data-ttu-id="b936c-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b936c-147">RELATED LINKS</span></span>

[<span data-ttu-id="b936c-148">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b936c-148">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="b936c-149">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b936c-149">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="b936c-150">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b936c-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="b936c-151">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b936c-151">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
