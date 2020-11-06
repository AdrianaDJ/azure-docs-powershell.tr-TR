---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 66662899694f7b1fb93dd109e1dccefee5e00182
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593880"
---
# <span data-ttu-id="7040f-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="7040f-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="7040f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7040f-102">SYNOPSIS</span></span>
<span data-ttu-id="7040f-103">Dosya paylaşımını siler.</span><span class="sxs-lookup"><span data-stu-id="7040f-103">Deletes a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7040f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7040f-104">SYNTAX</span></span>

### <span data-ttu-id="7040f-105">PaylaşımAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7040f-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7040f-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="7040f-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-Force] [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7040f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7040f-107">DESCRIPTION</span></span>
<span data-ttu-id="7040f-108">**Remove-Azurestoragesshare** cmdlet 'i dosya paylaşımını siler.</span><span class="sxs-lookup"><span data-stu-id="7040f-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="7040f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7040f-109">EXAMPLES</span></span>

### <span data-ttu-id="7040f-110">Örnek 1: dosya paylaşımını kaldırma</span><span class="sxs-lookup"><span data-stu-id="7040f-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="7040f-111">Bu komut, ContosoShare06 adlı dosya paylaşımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7040f-111">This command removes the file share named ContosoShare06.</span></span>

## <span data-ttu-id="7040f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7040f-112">PARAMETERS</span></span>

### <span data-ttu-id="7040f-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7040f-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7040f-114">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="7040f-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7040f-115">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="7040f-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7040f-116">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="7040f-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7040f-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7040f-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7040f-118">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7040f-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7040f-119">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7040f-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7040f-120">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="7040f-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7040f-121">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="7040f-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7040f-122">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="7040f-122">The default value is 10.</span></span>

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

### <span data-ttu-id="7040f-123">-Context</span><span class="sxs-lookup"><span data-stu-id="7040f-123">-Context</span></span>
<span data-ttu-id="7040f-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7040f-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7040f-125">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7040f-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7040f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="7040f-126">-Force</span></span>
<span data-ttu-id="7040f-127">Paylaşımı ve içindeki tüm içeriği kaldırmaya zorla</span><span class="sxs-lookup"><span data-stu-id="7040f-127">Force to remove the share and all content in it</span></span>

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

### <span data-ttu-id="7040f-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="7040f-128">-Name</span></span>
<span data-ttu-id="7040f-129">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7040f-129">Specifies the name of the file share.</span></span>
<span data-ttu-id="7040f-130">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımını siler.</span><span class="sxs-lookup"><span data-stu-id="7040f-130">This cmdlet deletes the file share that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7040f-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7040f-131">-PassThru</span></span>
<span data-ttu-id="7040f-132">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="7040f-132">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="7040f-133">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="7040f-133">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="7040f-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7040f-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7040f-135">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7040f-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="7040f-136">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="7040f-136">-Share</span></span>
<span data-ttu-id="7040f-137">Bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7040f-137">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="7040f-138">Bu cmdlet, bu parametrenin belirttiği nesneyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7040f-138">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="7040f-139">**Cloudfileshare** nesnesi edinmek için Get-AzureStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7040f-139">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="7040f-140">Bu nesne depolama bağlamını içerir.</span><span class="sxs-lookup"><span data-stu-id="7040f-140">This object contains the storage context.</span></span>
<span data-ttu-id="7040f-141">Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="7040f-141">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7040f-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="7040f-142">-Confirm</span></span>
<span data-ttu-id="7040f-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7040f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7040f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7040f-144">-WhatIf</span></span>
<span data-ttu-id="7040f-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7040f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7040f-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7040f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7040f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7040f-147">CommonParameters</span></span>
<span data-ttu-id="7040f-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7040f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7040f-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7040f-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7040f-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7040f-150">INPUTS</span></span>

### <span data-ttu-id="7040f-151">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="7040f-151">IStorageContext</span></span>

<span data-ttu-id="7040f-152">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7040f-152">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="7040f-153">Dizisi</span><span class="sxs-lookup"><span data-stu-id="7040f-153">String</span></span>

<span data-ttu-id="7040f-154">' Name ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7040f-154">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="7040f-155">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="7040f-155">CloudFileShare</span></span>

<span data-ttu-id="7040f-156">' Share ' parametresi ardışık düzenin ' CloudFileShare ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7040f-156">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="7040f-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7040f-157">OUTPUTS</span></span>

## <span data-ttu-id="7040f-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7040f-158">NOTES</span></span>

## <span data-ttu-id="7040f-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7040f-159">RELATED LINKS</span></span>

[<span data-ttu-id="7040f-160">Get-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="7040f-160">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="7040f-161">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7040f-161">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="7040f-162">New-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="7040f-162">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
