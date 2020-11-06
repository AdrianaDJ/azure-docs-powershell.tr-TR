---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainer.md
ms.openlocfilehash: 23ea79879b7b194b9f761c585087a931f9373886
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589002"
---
# <span data-ttu-id="b8123-101">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b8123-101">Remove-AzureStorageContainer</span></span>

## <span data-ttu-id="b8123-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8123-102">SYNOPSIS</span></span>
<span data-ttu-id="b8123-103">Belirtilen depolama kapsayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b8123-103">Removes the specified storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8123-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b8123-104">SYNTAX</span></span>

```
Remove-AzureStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8123-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b8123-105">DESCRIPTION</span></span>
<span data-ttu-id="b8123-106">**Remove-AzureStorageContainer** cmdlet 'i Azure 'da belirtilen depolama kapsayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b8123-106">The **Remove-AzureStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="b8123-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b8123-107">EXAMPLES</span></span>

### <span data-ttu-id="b8123-108">Örnek 1: kapsayıcıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="b8123-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzureStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="b8123-109">Bu örnek MyTestContainer adlı kapsayıcıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b8123-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="b8123-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b8123-110">PARAMETERS</span></span>

### <span data-ttu-id="b8123-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b8123-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b8123-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8123-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b8123-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="b8123-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b8123-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="b8123-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b8123-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b8123-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b8123-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8123-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b8123-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b8123-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b8123-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="b8123-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b8123-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="b8123-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b8123-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="b8123-120">The default value is 10.</span></span>

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

### <span data-ttu-id="b8123-121">-Context</span><span class="sxs-lookup"><span data-stu-id="b8123-121">-Context</span></span>
<span data-ttu-id="b8123-122">Kaldırmak istediğiniz kapsayıcının bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8123-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="b8123-123">New-AzureStorageContext cmdlet 'ini oluşturmak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b8123-123">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="b8123-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b8123-124">-Force</span></span>
<span data-ttu-id="b8123-125">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b8123-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b8123-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="b8123-126">-Name</span></span>
<span data-ttu-id="b8123-127">Kaldırılacak kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8123-127">Specifies the name of the container to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8123-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b8123-128">-PassThru</span></span>
<span data-ttu-id="b8123-129">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="b8123-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="b8123-130">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="b8123-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="b8123-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b8123-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b8123-132">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8123-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="b8123-133">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="b8123-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="b8123-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="b8123-134">-Confirm</span></span>
<span data-ttu-id="b8123-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b8123-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8123-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8123-136">-WhatIf</span></span>
<span data-ttu-id="b8123-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b8123-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8123-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b8123-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8123-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8123-139">CommonParameters</span></span>
<span data-ttu-id="b8123-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b8123-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8123-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8123-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8123-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b8123-142">INPUTS</span></span>

### <span data-ttu-id="b8123-143">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="b8123-143">IStorageContext</span></span>

<span data-ttu-id="b8123-144">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b8123-144">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="b8123-145">Dizisi</span><span class="sxs-lookup"><span data-stu-id="b8123-145">String</span></span>

<span data-ttu-id="b8123-146">' Name ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b8123-146">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="b8123-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b8123-147">OUTPUTS</span></span>

### <span data-ttu-id="b8123-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b8123-148">System.Boolean</span></span>

## <span data-ttu-id="b8123-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b8123-149">NOTES</span></span>

## <span data-ttu-id="b8123-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b8123-150">RELATED LINKS</span></span>

[<span data-ttu-id="b8123-151">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b8123-151">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="b8123-152">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b8123-152">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)
