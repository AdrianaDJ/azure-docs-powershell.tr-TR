---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragesharestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: a1df300ab48a1de19b16b00c53379e05046b8588
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940205"
---
# <span data-ttu-id="e48a9-101">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e48a9-101">Set-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="e48a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e48a9-102">SYNOPSIS</span></span>
<span data-ttu-id="e48a9-103">Depolanan bir erişim ilkesini depolama paylaşımında güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e48a9-103">Updates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e48a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e48a9-104">SYNTAX</span></span>

```
Set-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e48a9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e48a9-105">DESCRIPTION</span></span>
<span data-ttu-id="e48a9-106">**Set-AzureStorageShareStoredAccessPolicy** cmdlet 'ı bir Azure depolama paylaşımında depolanan erişim ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e48a9-106">The **Set-AzureStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="e48a9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e48a9-107">EXAMPLES</span></span>

### <span data-ttu-id="e48a9-108">Örnek 1: depolama paylaşımında depolanan bir erişim ilkesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e48a9-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="e48a9-109">Bu komut, paylaşımda tam izni olan bir depolanmış erişim ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e48a9-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="e48a9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e48a9-110">PARAMETERS</span></span>

### <span data-ttu-id="e48a9-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e48a9-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e48a9-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="e48a9-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e48a9-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="e48a9-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e48a9-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="e48a9-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e48a9-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e48a9-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e48a9-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e48a9-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e48a9-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e48a9-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e48a9-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="e48a9-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e48a9-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="e48a9-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e48a9-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="e48a9-120">The default value is 10.</span></span>

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

### <span data-ttu-id="e48a9-121">-Context</span><span class="sxs-lookup"><span data-stu-id="e48a9-121">-Context</span></span>
<span data-ttu-id="e48a9-122">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e48a9-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e48a9-123">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e48a9-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="e48a9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e48a9-124">-DefaultProfile</span></span>
<span data-ttu-id="e48a9-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e48a9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e48a9-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e48a9-126">-ExpiryTime</span></span>
<span data-ttu-id="e48a9-127">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e48a9-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="e48a9-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e48a9-128">-NoExpiryTime</span></span>
<span data-ttu-id="e48a9-129">Bu cmdlet 'in depolanan erişim ilkesinde **Expirytime** özelliğini temizdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e48a9-129">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="e48a9-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="e48a9-130">-NoStartTime</span></span>
<span data-ttu-id="e48a9-131">Bu cmdlet 'in depolanan erişim ilkesindeki **StartTime** özelliğini temizdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e48a9-131">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="e48a9-132">-İzin</span><span class="sxs-lookup"><span data-stu-id="e48a9-132">-Permission</span></span>
<span data-ttu-id="e48a9-133">Depolanan erişim ilkesindeki paylaşım veya dosyaların altındaki dosyalara erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e48a9-133">Specifies permissions in the stored access policy to access the share or files under it.</span></span>
<span data-ttu-id="e48a9-134">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="e48a9-134">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="e48a9-135">-İlke</span><span class="sxs-lookup"><span data-stu-id="e48a9-135">-Policy</span></span>
<span data-ttu-id="e48a9-136">Depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e48a9-136">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="e48a9-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e48a9-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e48a9-138">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e48a9-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e48a9-139">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="e48a9-139">-ShareName</span></span>
<span data-ttu-id="e48a9-140">Depolama paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e48a9-140">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="e48a9-141">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="e48a9-141">-StartTime</span></span>
<span data-ttu-id="e48a9-142">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="e48a9-142">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="e48a9-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="e48a9-143">-Confirm</span></span>
<span data-ttu-id="e48a9-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e48a9-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e48a9-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e48a9-145">-WhatIf</span></span>
<span data-ttu-id="e48a9-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e48a9-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e48a9-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e48a9-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e48a9-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e48a9-148">CommonParameters</span></span>
<span data-ttu-id="e48a9-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e48a9-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e48a9-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e48a9-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e48a9-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e48a9-151">INPUTS</span></span>

### <span data-ttu-id="e48a9-152">System. String</span><span class="sxs-lookup"><span data-stu-id="e48a9-152">System.String</span></span>

### <span data-ttu-id="e48a9-153">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="e48a9-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e48a9-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e48a9-154">OUTPUTS</span></span>

### <span data-ttu-id="e48a9-155">System. String</span><span class="sxs-lookup"><span data-stu-id="e48a9-155">System.String</span></span>

## <span data-ttu-id="e48a9-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e48a9-156">NOTES</span></span>

## <span data-ttu-id="e48a9-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e48a9-157">RELATED LINKS</span></span>

[<span data-ttu-id="e48a9-158">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e48a9-158">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="e48a9-159">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e48a9-159">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e48a9-160">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e48a9-160">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="e48a9-161">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e48a9-161">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)
