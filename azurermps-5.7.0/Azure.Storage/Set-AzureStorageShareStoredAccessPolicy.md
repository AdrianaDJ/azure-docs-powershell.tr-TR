---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 0c77d2dedadd205a659bf296e02c09b98342dcc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765010"
---
# <span data-ttu-id="913b9-101">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="913b9-101">Set-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="913b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="913b9-102">SYNOPSIS</span></span>
<span data-ttu-id="913b9-103">Depolanan bir erişim ilkesini depolama paylaşımında güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="913b9-103">Updates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="913b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="913b9-104">SYNTAX</span></span>

```
Set-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="913b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="913b9-105">DESCRIPTION</span></span>
<span data-ttu-id="913b9-106">**Set-AzureStorageShareStoredAccessPolicy** cmdlet 'ı bir Azure depolama paylaşımında depolanan erişim ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="913b9-106">The **Set-AzureStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="913b9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="913b9-107">EXAMPLES</span></span>

### <span data-ttu-id="913b9-108">Örnek 1: depolama paylaşımında depolanan bir erişim ilkesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="913b9-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="913b9-109">Bu komut, paylaşımda tam izni olan bir depolanmış erişim ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="913b9-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="913b9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="913b9-110">PARAMETERS</span></span>

### <span data-ttu-id="913b9-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="913b9-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="913b9-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="913b9-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="913b9-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="913b9-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="913b9-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="913b9-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="913b9-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="913b9-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="913b9-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="913b9-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="913b9-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="913b9-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="913b9-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="913b9-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="913b9-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="913b9-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="913b9-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="913b9-120">The default value is 10.</span></span>

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

### <span data-ttu-id="913b9-121">-Context</span><span class="sxs-lookup"><span data-stu-id="913b9-121">-Context</span></span>
<span data-ttu-id="913b9-122">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="913b9-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="913b9-123">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="913b9-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="913b9-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="913b9-124">-ExpiryTime</span></span>
<span data-ttu-id="913b9-125">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="913b9-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="913b9-126">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="913b9-126">-NoExpiryTime</span></span>
<span data-ttu-id="913b9-127">Bu cmdlet 'in depolanan erişim ilkesinde **Expirytime** özelliğini temizdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="913b9-127">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="913b9-128">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="913b9-128">-NoStartTime</span></span>
<span data-ttu-id="913b9-129">Bu cmdlet 'in depolanan erişim ilkesindeki **StartTime** özelliğini temizdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="913b9-129">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="913b9-130">-İzin</span><span class="sxs-lookup"><span data-stu-id="913b9-130">-Permission</span></span>
<span data-ttu-id="913b9-131">Depolanan erişim ilkesindeki paylaşım veya dosyaların altındaki dosyalara erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="913b9-131">Specifies permissions in the stored access policy to access the share or files under it.</span></span>

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

### <span data-ttu-id="913b9-132">-İlke</span><span class="sxs-lookup"><span data-stu-id="913b9-132">-Policy</span></span>
<span data-ttu-id="913b9-133">Depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="913b9-133">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="913b9-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="913b9-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="913b9-135">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="913b9-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="913b9-136">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="913b9-136">-ShareName</span></span>
<span data-ttu-id="913b9-137">Depolama paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="913b9-137">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="913b9-138">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="913b9-138">-StartTime</span></span>
<span data-ttu-id="913b9-139">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="913b9-139">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="913b9-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="913b9-140">-Confirm</span></span>
<span data-ttu-id="913b9-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="913b9-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="913b9-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="913b9-142">-WhatIf</span></span>
<span data-ttu-id="913b9-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="913b9-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="913b9-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="913b9-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="913b9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="913b9-145">CommonParameters</span></span>
<span data-ttu-id="913b9-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="913b9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="913b9-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="913b9-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="913b9-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="913b9-148">INPUTS</span></span>

### <span data-ttu-id="913b9-149">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="913b9-149">IStorageContext</span></span>

<span data-ttu-id="913b9-150">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="913b9-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="913b9-151">Dizisi</span><span class="sxs-lookup"><span data-stu-id="913b9-151">String</span></span>

<span data-ttu-id="913b9-152">' PaylaşımAdı ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="913b9-152">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="913b9-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="913b9-153">OUTPUTS</span></span>

### <span data-ttu-id="913b9-154">System. String</span><span class="sxs-lookup"><span data-stu-id="913b9-154">System.String</span></span>

## <span data-ttu-id="913b9-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="913b9-155">NOTES</span></span>

## <span data-ttu-id="913b9-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="913b9-156">RELATED LINKS</span></span>

[<span data-ttu-id="913b9-157">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="913b9-157">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="913b9-158">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="913b9-158">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="913b9-159">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="913b9-159">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="913b9-160">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="913b9-160">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)
