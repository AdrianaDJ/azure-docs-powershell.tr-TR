---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
ms.openlocfilehash: c929a7e3e685fd870c57ff942262a0c5ac4a9966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587722"
---
# <span data-ttu-id="2527d-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="2527d-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="2527d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2527d-102">SYNOPSIS</span></span>
<span data-ttu-id="2527d-103">Dosya paylaşımını siler.</span><span class="sxs-lookup"><span data-stu-id="2527d-103">Deletes a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2527d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2527d-104">SYNTAX</span></span>

### <span data-ttu-id="2527d-105">PaylaşımAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2527d-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2527d-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="2527d-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2527d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2527d-107">DESCRIPTION</span></span>
<span data-ttu-id="2527d-108">**Remove-Azurestoragesshare** cmdlet 'i dosya paylaşımını siler.</span><span class="sxs-lookup"><span data-stu-id="2527d-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="2527d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2527d-109">EXAMPLES</span></span>

### <span data-ttu-id="2527d-110">Örnek 1: dosya paylaşımını kaldırma</span><span class="sxs-lookup"><span data-stu-id="2527d-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="2527d-111">Bu komut, ContosoShare06 adlı dosya paylaşımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2527d-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="2527d-112">Örnek 2: dosya paylaşımını ve tüm anlık görüntülerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="2527d-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="2527d-113">Bu komut, ContosoShare06 adlı dosya paylaşımını ve tüm anlık görüntülerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2527d-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="2527d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2527d-114">PARAMETERS</span></span>

### <span data-ttu-id="2527d-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2527d-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2527d-116">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="2527d-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2527d-117">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="2527d-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2527d-118">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="2527d-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2527d-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2527d-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2527d-120">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2527d-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2527d-121">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2527d-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2527d-122">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="2527d-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2527d-123">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="2527d-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2527d-124">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="2527d-124">The default value is 10.</span></span>

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

### <span data-ttu-id="2527d-125">-Context</span><span class="sxs-lookup"><span data-stu-id="2527d-125">-Context</span></span>
<span data-ttu-id="2527d-126">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2527d-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2527d-127">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2527d-127">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="2527d-128">-Force</span><span class="sxs-lookup"><span data-stu-id="2527d-128">-Force</span></span>
<span data-ttu-id="2527d-129">Paylaşımı tüm anlık görüntülerle ve tüm içeriklerle kaldırmaya zorlayın.</span><span class="sxs-lookup"><span data-stu-id="2527d-129">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="2527d-130">-Includeallsnapshot</span><span class="sxs-lookup"><span data-stu-id="2527d-130">-IncludeAllSnapshot</span></span>
<span data-ttu-id="2527d-131">Dosya paylaşımını tüm anlık görüntüleriyle kaldırma</span><span class="sxs-lookup"><span data-stu-id="2527d-131">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="2527d-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="2527d-132">-Name</span></span>
<span data-ttu-id="2527d-133">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2527d-133">Specifies the name of the file share.</span></span>
<span data-ttu-id="2527d-134">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımını siler.</span><span class="sxs-lookup"><span data-stu-id="2527d-134">This cmdlet deletes the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="2527d-135">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2527d-135">-PassThru</span></span>
<span data-ttu-id="2527d-136">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="2527d-136">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="2527d-137">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="2527d-137">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="2527d-138">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2527d-138">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2527d-139">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2527d-139">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="2527d-140">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="2527d-140">-Share</span></span>
<span data-ttu-id="2527d-141">Bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2527d-141">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="2527d-142">Bu cmdlet, bu parametrenin belirttiği nesneyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2527d-142">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="2527d-143">**Cloudfileshare** nesnesi edinmek için Get-AzureStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2527d-143">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="2527d-144">Bu nesne depolama bağlamını içerir.</span><span class="sxs-lookup"><span data-stu-id="2527d-144">This object contains the storage context.</span></span>
<span data-ttu-id="2527d-145">Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="2527d-145">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="2527d-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="2527d-146">-Confirm</span></span>
<span data-ttu-id="2527d-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2527d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2527d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2527d-148">-WhatIf</span></span>
<span data-ttu-id="2527d-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2527d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2527d-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2527d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2527d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2527d-151">CommonParameters</span></span>
<span data-ttu-id="2527d-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2527d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2527d-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2527d-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2527d-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2527d-154">INPUTS</span></span>

### <span data-ttu-id="2527d-155">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="2527d-155">IStorageContext</span></span>

<span data-ttu-id="2527d-156">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="2527d-156">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="2527d-157">Dizisi</span><span class="sxs-lookup"><span data-stu-id="2527d-157">String</span></span>

<span data-ttu-id="2527d-158">' Name ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="2527d-158">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="2527d-159">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="2527d-159">CloudFileShare</span></span>

<span data-ttu-id="2527d-160">' Share ' parametresi ardışık düzenin ' CloudFileShare ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="2527d-160">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="2527d-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2527d-161">OUTPUTS</span></span>

## <span data-ttu-id="2527d-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2527d-162">NOTES</span></span>

## <span data-ttu-id="2527d-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2527d-163">RELATED LINKS</span></span>

[<span data-ttu-id="2527d-164">Get-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="2527d-164">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="2527d-165">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="2527d-165">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="2527d-166">New-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="2527d-166">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
