---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: afae707fd66da5a54933d59bf63619145349e90b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758571"
---
# <span data-ttu-id="e3b63-101">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e3b63-101">Remove-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="e3b63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3b63-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b63-103">Depolanan bir Access ilkesini Azure depolama kapsayıcısından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e3b63-103">Removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="e3b63-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3b63-104">SYNTAX</span></span>

```
Remove-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3b63-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3b63-105">DESCRIPTION</span></span>
<span data-ttu-id="e3b63-106">**Remove-AzStorageContainerStoredAccessPolicy** cmdlet 'i Azure depolama kapsayıcısından depolanan bir Access ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e3b63-106">The **Remove-AzStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="e3b63-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3b63-107">EXAMPLES</span></span>

### <span data-ttu-id="e3b63-108">Örnek 1: depolama kapsayıcısından depolanan bir erişim ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="e3b63-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="e3b63-109">Bu komut MyContainer adlı depolanan kapsayıcıdan Policy03 adındaki bir erişim ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e3b63-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="e3b63-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3b63-110">PARAMETERS</span></span>

### <span data-ttu-id="e3b63-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e3b63-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e3b63-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3b63-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e3b63-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="e3b63-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e3b63-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="e3b63-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e3b63-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e3b63-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e3b63-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3b63-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e3b63-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e3b63-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e3b63-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="e3b63-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e3b63-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="e3b63-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e3b63-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="e3b63-120">The default value is 10.</span></span>

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

### <span data-ttu-id="e3b63-121">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="e3b63-121">-Container</span></span>
<span data-ttu-id="e3b63-122">Azure depolama kapsayıcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3b63-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b63-123">-Context</span><span class="sxs-lookup"><span data-stu-id="e3b63-123">-Context</span></span>
<span data-ttu-id="e3b63-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3b63-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e3b63-125">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e3b63-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e3b63-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b63-126">-DefaultProfile</span></span>
<span data-ttu-id="e3b63-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e3b63-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3b63-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e3b63-128">-PassThru</span></span>
<span data-ttu-id="e3b63-129">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="e3b63-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="e3b63-130">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="e3b63-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="e3b63-131">-İlke</span><span class="sxs-lookup"><span data-stu-id="e3b63-131">-Policy</span></span>
<span data-ttu-id="e3b63-132">Bu cmdlet 'in kaldırdığı depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3b63-132">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b63-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e3b63-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e3b63-134">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3b63-134">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e3b63-135">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="e3b63-135">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e3b63-136">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="e3b63-136">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e3b63-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="e3b63-137">-Confirm</span></span>
<span data-ttu-id="e3b63-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e3b63-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3b63-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3b63-139">-WhatIf</span></span>
<span data-ttu-id="e3b63-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3b63-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3b63-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e3b63-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3b63-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b63-142">CommonParameters</span></span>
<span data-ttu-id="e3b63-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3b63-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b63-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3b63-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b63-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3b63-145">INPUTS</span></span>

### <span data-ttu-id="e3b63-146">System. String</span><span class="sxs-lookup"><span data-stu-id="e3b63-146">System.String</span></span>

### <span data-ttu-id="e3b63-147">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="e3b63-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e3b63-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3b63-148">OUTPUTS</span></span>

### <span data-ttu-id="e3b63-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e3b63-149">System.Boolean</span></span>

## <span data-ttu-id="e3b63-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3b63-150">NOTES</span></span>

## <span data-ttu-id="e3b63-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3b63-151">RELATED LINKS</span></span>

[<span data-ttu-id="e3b63-152">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e3b63-152">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="e3b63-153">Yeni-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e3b63-153">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="e3b63-154">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e3b63-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="e3b63-155">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e3b63-155">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)
