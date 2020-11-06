---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07ca74b29dad61c1cf909f13aefbf35b2048d4aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571897"
---
# <span data-ttu-id="5f070-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="5f070-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="5f070-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f070-102">SYNOPSIS</span></span>
<span data-ttu-id="5f070-103">Dosya paylaşımını siler.</span><span class="sxs-lookup"><span data-stu-id="5f070-103">Deletes a file share.</span></span>

## <span data-ttu-id="5f070-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f070-104">SYNTAX</span></span>

### <span data-ttu-id="5f070-105">PaylaşımAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5f070-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f070-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="5f070-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-Force] [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f070-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f070-107">DESCRIPTION</span></span>
<span data-ttu-id="5f070-108">**Remove-Azurestoragesshare** cmdlet 'i dosya paylaşımını siler.</span><span class="sxs-lookup"><span data-stu-id="5f070-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="5f070-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f070-109">EXAMPLES</span></span>

### <span data-ttu-id="5f070-110">Örnek 1: dosya paylaşımını kaldırma</span><span class="sxs-lookup"><span data-stu-id="5f070-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="5f070-111">Bu komut, ContosoShare06 adlı dosya paylaşımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5f070-111">This command removes the file share named ContosoShare06.</span></span>

## <span data-ttu-id="5f070-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f070-112">PARAMETERS</span></span>

### <span data-ttu-id="5f070-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5f070-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5f070-114">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f070-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5f070-115">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="5f070-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5f070-116">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="5f070-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5f070-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5f070-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5f070-118">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f070-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5f070-119">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5f070-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5f070-120">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="5f070-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5f070-121">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="5f070-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5f070-122">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="5f070-122">The default value is 10.</span></span>

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

### <span data-ttu-id="5f070-123">-Context</span><span class="sxs-lookup"><span data-stu-id="5f070-123">-Context</span></span>
<span data-ttu-id="5f070-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f070-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5f070-125">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5f070-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="5f070-126">-Force</span><span class="sxs-lookup"><span data-stu-id="5f070-126">-Force</span></span>
<span data-ttu-id="5f070-127">Paylaşımı ve içindeki tüm içeriği kaldırmaya zorla</span><span class="sxs-lookup"><span data-stu-id="5f070-127">Force to remove the share and all content in it</span></span>

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

### <span data-ttu-id="5f070-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="5f070-128">-Name</span></span>
<span data-ttu-id="5f070-129">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f070-129">Specifies the name of the file share.</span></span>
<span data-ttu-id="5f070-130">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımını siler.</span><span class="sxs-lookup"><span data-stu-id="5f070-130">This cmdlet deletes the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f070-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5f070-131">-PassThru</span></span>
<span data-ttu-id="5f070-132">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="5f070-132">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="5f070-133">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="5f070-133">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="5f070-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5f070-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5f070-135">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f070-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="5f070-136">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="5f070-136">-Share</span></span>
<span data-ttu-id="5f070-137">Bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f070-137">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="5f070-138">Bu cmdlet, bu parametrenin belirttiği nesneyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5f070-138">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="5f070-139">**Cloudfileshare** nesnesi edinmek için Get-AzureStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5f070-139">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="5f070-140">Bu nesne depolama bağlamını içerir.</span><span class="sxs-lookup"><span data-stu-id="5f070-140">This object contains the storage context.</span></span>
<span data-ttu-id="5f070-141">Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="5f070-141">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="5f070-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="5f070-142">-Confirm</span></span>
<span data-ttu-id="5f070-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5f070-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f070-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f070-144">-WhatIf</span></span>
<span data-ttu-id="5f070-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5f070-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f070-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5f070-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f070-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f070-147">CommonParameters</span></span>
<span data-ttu-id="5f070-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f070-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f070-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f070-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f070-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f070-150">INPUTS</span></span>

## <span data-ttu-id="5f070-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f070-151">OUTPUTS</span></span>

## <span data-ttu-id="5f070-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f070-152">NOTES</span></span>

## <span data-ttu-id="5f070-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f070-153">RELATED LINKS</span></span>

[<span data-ttu-id="5f070-154">Get-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="5f070-154">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="5f070-155">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5f070-155">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="5f070-156">New-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="5f070-156">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
