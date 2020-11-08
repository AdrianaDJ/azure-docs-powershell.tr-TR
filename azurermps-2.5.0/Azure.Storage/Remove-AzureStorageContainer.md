---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragecontainer
schema: 2.0.0
ms.openlocfilehash: 24eba8b6aeedb2f240fbd7da16b1b7a76ee9d759
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939970"
---
# <span data-ttu-id="2a082-101">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2a082-101">Remove-AzureStorageContainer</span></span>

## <span data-ttu-id="2a082-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a082-102">SYNOPSIS</span></span>
<span data-ttu-id="2a082-103">Belirtilen depolama kapsayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2a082-103">Removes the specified storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a082-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a082-104">SYNTAX</span></span>

```
Remove-AzureStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a082-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a082-105">DESCRIPTION</span></span>
<span data-ttu-id="2a082-106">**Remove-AzureStorageContainer** cmdlet 'i Azure 'da belirtilen depolama kapsayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2a082-106">The **Remove-AzureStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="2a082-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a082-107">EXAMPLES</span></span>

### <span data-ttu-id="2a082-108">Örnek 1: kapsayıcıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="2a082-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzureStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="2a082-109">Bu örnek MyTestContainer adlı kapsayıcıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2a082-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="2a082-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a082-110">PARAMETERS</span></span>

### <span data-ttu-id="2a082-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2a082-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2a082-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a082-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2a082-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="2a082-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2a082-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="2a082-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2a082-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2a082-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2a082-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a082-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2a082-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2a082-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2a082-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="2a082-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2a082-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="2a082-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2a082-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="2a082-120">The default value is 10.</span></span>

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

### <span data-ttu-id="2a082-121">-Context</span><span class="sxs-lookup"><span data-stu-id="2a082-121">-Context</span></span>
<span data-ttu-id="2a082-122">Kaldırmak istediğiniz kapsayıcının bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a082-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="2a082-123">New-AzureStorageContext cmdlet 'ini oluşturmak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2a082-123">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="2a082-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a082-124">-DefaultProfile</span></span>
<span data-ttu-id="2a082-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2a082-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a082-126">-Force</span><span class="sxs-lookup"><span data-stu-id="2a082-126">-Force</span></span>
<span data-ttu-id="2a082-127">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="2a082-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2a082-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="2a082-128">-Name</span></span>
<span data-ttu-id="2a082-129">Kaldırılacak kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a082-129">Specifies the name of the container to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a082-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2a082-130">-PassThru</span></span>
<span data-ttu-id="2a082-131">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="2a082-131">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="2a082-132">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="2a082-132">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="2a082-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2a082-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2a082-134">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a082-134">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="2a082-135">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="2a082-135">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="2a082-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="2a082-136">-Confirm</span></span>
<span data-ttu-id="2a082-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2a082-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a082-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a082-138">-WhatIf</span></span>
<span data-ttu-id="2a082-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2a082-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a082-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2a082-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a082-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a082-141">CommonParameters</span></span>
<span data-ttu-id="2a082-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a082-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a082-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a082-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a082-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a082-144">INPUTS</span></span>

### <span data-ttu-id="2a082-145">System. String</span><span class="sxs-lookup"><span data-stu-id="2a082-145">System.String</span></span>

### <span data-ttu-id="2a082-146">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="2a082-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2a082-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a082-147">OUTPUTS</span></span>

### <span data-ttu-id="2a082-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2a082-148">System.Boolean</span></span>

## <span data-ttu-id="2a082-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a082-149">NOTES</span></span>

## <span data-ttu-id="2a082-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a082-150">RELATED LINKS</span></span>

[<span data-ttu-id="2a082-151">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2a082-151">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="2a082-152">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2a082-152">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)