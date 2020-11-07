---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragesharestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 6a00bbe0a80218dfdd29666fffaf6ec314c41f01
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939968"
---
# <span data-ttu-id="28bd6-101">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="28bd6-101">Remove-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="28bd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28bd6-102">SYNOPSIS</span></span>
<span data-ttu-id="28bd6-103">Depolanan bir Access ilkesini depolama paylaşımından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="28bd6-103">Removes a stored access policy from a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28bd6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="28bd6-104">SYNTAX</span></span>

```
Remove-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28bd6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="28bd6-105">DESCRIPTION</span></span>
<span data-ttu-id="28bd6-106">**Remove-AzureStorageShareStoredAccessPolicy** cmdlet 'ı Azure depolama paylaşımından depolanan bir Access ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="28bd6-106">The **Remove-AzureStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="28bd6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="28bd6-107">EXAMPLES</span></span>

### <span data-ttu-id="28bd6-108">Örnek 1: Azure depolama paylaşımından depolanan bir Access ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="28bd6-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="28bd6-109">Bu komut, ContosoShare adlı bir depolanmış erişim ilkesini ContosoShare 'tan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="28bd6-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="28bd6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="28bd6-110">PARAMETERS</span></span>

### <span data-ttu-id="28bd6-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="28bd6-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="28bd6-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="28bd6-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="28bd6-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="28bd6-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="28bd6-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="28bd6-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="28bd6-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="28bd6-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="28bd6-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="28bd6-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="28bd6-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="28bd6-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="28bd6-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="28bd6-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="28bd6-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="28bd6-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="28bd6-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="28bd6-120">The default value is 10.</span></span>

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

### <span data-ttu-id="28bd6-121">-Context</span><span class="sxs-lookup"><span data-stu-id="28bd6-121">-Context</span></span>
<span data-ttu-id="28bd6-122">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="28bd6-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="28bd6-123">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="28bd6-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="28bd6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28bd6-124">-DefaultProfile</span></span>
<span data-ttu-id="28bd6-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="28bd6-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28bd6-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="28bd6-126">-PassThru</span></span>
<span data-ttu-id="28bd6-127">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="28bd6-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="28bd6-128">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="28bd6-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="28bd6-129">-İlke</span><span class="sxs-lookup"><span data-stu-id="28bd6-129">-Policy</span></span>
<span data-ttu-id="28bd6-130">Bu cmdlet 'in kaldırdığı depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="28bd6-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="28bd6-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="28bd6-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="28bd6-132">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="28bd6-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="28bd6-133">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="28bd6-133">-ShareName</span></span>
<span data-ttu-id="28bd6-134">Bu cmdlet 'in ilkeyi kaldırdığı depolama paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="28bd6-134">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

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

### <span data-ttu-id="28bd6-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="28bd6-135">-Confirm</span></span>
<span data-ttu-id="28bd6-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="28bd6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28bd6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28bd6-137">-WhatIf</span></span>
<span data-ttu-id="28bd6-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="28bd6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28bd6-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="28bd6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28bd6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28bd6-140">CommonParameters</span></span>
<span data-ttu-id="28bd6-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="28bd6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28bd6-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28bd6-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28bd6-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="28bd6-143">INPUTS</span></span>

### <span data-ttu-id="28bd6-144">System. String</span><span class="sxs-lookup"><span data-stu-id="28bd6-144">System.String</span></span>

### <span data-ttu-id="28bd6-145">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="28bd6-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="28bd6-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="28bd6-146">OUTPUTS</span></span>

### <span data-ttu-id="28bd6-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="28bd6-147">System.Boolean</span></span>

## <span data-ttu-id="28bd6-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="28bd6-148">NOTES</span></span>

## <span data-ttu-id="28bd6-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="28bd6-149">RELATED LINKS</span></span>

[<span data-ttu-id="28bd6-150">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="28bd6-150">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="28bd6-151">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="28bd6-151">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="28bd6-152">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="28bd6-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="28bd6-153">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="28bd6-153">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
