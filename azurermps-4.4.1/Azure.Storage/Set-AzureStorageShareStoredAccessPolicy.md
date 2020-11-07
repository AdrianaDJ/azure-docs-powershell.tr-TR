---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 43e9ccca185a68d3c7b0e6cca118bb2cd63247bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593861"
---
# <span data-ttu-id="22c92-101">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="22c92-101">Set-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="22c92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22c92-102">SYNOPSIS</span></span>
<span data-ttu-id="22c92-103">Depolanan bir erişim ilkesini depolama paylaşımında güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="22c92-103">Updates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22c92-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22c92-104">SYNTAX</span></span>

```
Set-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22c92-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="22c92-105">DESCRIPTION</span></span>
<span data-ttu-id="22c92-106">**Set-AzureStorageShareStoredAccessPolicy** cmdlet 'ı bir Azure depolama paylaşımında depolanan erişim ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="22c92-106">The **Set-AzureStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="22c92-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22c92-107">EXAMPLES</span></span>

### <span data-ttu-id="22c92-108">Örnek 1: depolama paylaşımında depolanan bir erişim ilkesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="22c92-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="22c92-109">Bu komut, paylaşımda tam izni olan bir depolanmış erişim ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="22c92-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="22c92-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22c92-110">PARAMETERS</span></span>

### <span data-ttu-id="22c92-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="22c92-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="22c92-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c92-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="22c92-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="22c92-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="22c92-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="22c92-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="22c92-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="22c92-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="22c92-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c92-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="22c92-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="22c92-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="22c92-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="22c92-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="22c92-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="22c92-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="22c92-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="22c92-120">The default value is 10.</span></span>

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

### <span data-ttu-id="22c92-121">-Context</span><span class="sxs-lookup"><span data-stu-id="22c92-121">-Context</span></span>
<span data-ttu-id="22c92-122">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c92-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="22c92-123">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="22c92-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="22c92-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="22c92-124">-ExpiryTime</span></span>
<span data-ttu-id="22c92-125">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c92-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="22c92-126">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="22c92-126">-NoExpiryTime</span></span>
<span data-ttu-id="22c92-127">Bu cmdlet 'in depolanan erişim ilkesinde **Expirytime** özelliğini temizdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c92-127">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="22c92-128">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="22c92-128">-NoStartTime</span></span>
<span data-ttu-id="22c92-129">Bu cmdlet 'in depolanan erişim ilkesindeki **StartTime** özelliğini temizdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c92-129">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="22c92-130">-İzin</span><span class="sxs-lookup"><span data-stu-id="22c92-130">-Permission</span></span>
<span data-ttu-id="22c92-131">Depolanan erişim ilkesindeki paylaşım veya dosyaların altındaki dosyalara erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c92-131">Specifies permissions in the stored access policy to access the share or files under it.</span></span>

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

### <span data-ttu-id="22c92-132">-İlke</span><span class="sxs-lookup"><span data-stu-id="22c92-132">-Policy</span></span>
<span data-ttu-id="22c92-133">Depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c92-133">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="22c92-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="22c92-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="22c92-135">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c92-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="22c92-136">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="22c92-136">-ShareName</span></span>
<span data-ttu-id="22c92-137">Depolama paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c92-137">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="22c92-138">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="22c92-138">-StartTime</span></span>
<span data-ttu-id="22c92-139">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c92-139">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="22c92-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="22c92-140">-Confirm</span></span>
<span data-ttu-id="22c92-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="22c92-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22c92-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22c92-142">-WhatIf</span></span>
<span data-ttu-id="22c92-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="22c92-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22c92-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="22c92-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22c92-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22c92-145">CommonParameters</span></span>
<span data-ttu-id="22c92-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22c92-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22c92-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22c92-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22c92-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22c92-148">INPUTS</span></span>

### <span data-ttu-id="22c92-149">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="22c92-149">IStorageContext</span></span>

<span data-ttu-id="22c92-150">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="22c92-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="22c92-151">Dizisi</span><span class="sxs-lookup"><span data-stu-id="22c92-151">String</span></span>

<span data-ttu-id="22c92-152">' PaylaşımAdı ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="22c92-152">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="22c92-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22c92-153">OUTPUTS</span></span>

### <span data-ttu-id="22c92-154">System. String</span><span class="sxs-lookup"><span data-stu-id="22c92-154">System.String</span></span>

## <span data-ttu-id="22c92-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22c92-155">NOTES</span></span>

## <span data-ttu-id="22c92-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22c92-156">RELATED LINKS</span></span>

[<span data-ttu-id="22c92-157">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="22c92-157">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="22c92-158">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="22c92-158">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="22c92-159">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="22c92-159">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="22c92-160">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="22c92-160">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)