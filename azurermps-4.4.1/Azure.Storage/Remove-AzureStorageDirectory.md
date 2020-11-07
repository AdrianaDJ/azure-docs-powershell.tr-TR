---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: cdd52b1e1bab28956605d70e1089d7804b8ccff7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762888"
---
# <span data-ttu-id="deaaf-101">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="deaaf-101">Remove-AzureStorageDirectory</span></span>

## <span data-ttu-id="deaaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="deaaf-102">SYNOPSIS</span></span>
<span data-ttu-id="deaaf-103">Dizin siler.</span><span class="sxs-lookup"><span data-stu-id="deaaf-103">Deletes a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="deaaf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="deaaf-104">SYNTAX</span></span>

### <span data-ttu-id="deaaf-105">PaylaşımAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="deaaf-105">ShareName (Default)</span></span>
```
Remove-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deaaf-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="deaaf-106">Share</span></span>
```
Remove-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deaaf-107">Directory</span><span class="sxs-lookup"><span data-stu-id="deaaf-107">Directory</span></span>
```
Remove-AzureStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deaaf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="deaaf-108">DESCRIPTION</span></span>
<span data-ttu-id="deaaf-109">**Remove-AzureStorageDirectory** cmdlet 'i bir dizini siler.</span><span class="sxs-lookup"><span data-stu-id="deaaf-109">The **Remove-AzureStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="deaaf-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="deaaf-110">EXAMPLES</span></span>

### <span data-ttu-id="deaaf-111">Örnek 1: klasör silme</span><span class="sxs-lookup"><span data-stu-id="deaaf-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="deaaf-112">Bu komut, ContosoShare06 adlı dosya paylaşımından Contosoworkingklasörünün adını siler.</span><span class="sxs-lookup"><span data-stu-id="deaaf-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="deaaf-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="deaaf-113">PARAMETERS</span></span>

### <span data-ttu-id="deaaf-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="deaaf-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="deaaf-115">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="deaaf-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="deaaf-116">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="deaaf-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="deaaf-117">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="deaaf-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="deaaf-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="deaaf-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="deaaf-119">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="deaaf-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="deaaf-120">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="deaaf-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="deaaf-121">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="deaaf-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="deaaf-122">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="deaaf-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="deaaf-123">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="deaaf-123">The default value is 10.</span></span>

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

### <span data-ttu-id="deaaf-124">-Context</span><span class="sxs-lookup"><span data-stu-id="deaaf-124">-Context</span></span>
<span data-ttu-id="deaaf-125">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="deaaf-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="deaaf-126">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="deaaf-126">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="deaaf-127">-Dizin</span><span class="sxs-lookup"><span data-stu-id="deaaf-127">-Directory</span></span>
<span data-ttu-id="deaaf-128">Bir klasörü **Cloudfiledirectory** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="deaaf-128">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="deaaf-129">Bu cmdlet, bu parametrenin belirttiği klasörü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="deaaf-129">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="deaaf-130">Dizin edinmek için New-AzureStorageDirectory cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="deaaf-130">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="deaaf-131">Bir dizin edinmek için **Get-Azurestoragefıle** cmdlet 'ini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="deaaf-131">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="deaaf-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="deaaf-132">-PassThru</span></span>
<span data-ttu-id="deaaf-133">Bu cmdlet başarılı olursa, $True değerini döndüren anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="deaaf-133">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="deaaf-134">Bu parametreyi belirtirseniz ve cmdlet _yol_ parametresi için uygun olmayan bir değer nedeniyle başarısız olursa cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="deaaf-134">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="deaaf-135">Bu parametreyi belirtmezseniz, bu cmdlet bir değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="deaaf-135">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="deaaf-136">-Yol</span><span class="sxs-lookup"><span data-stu-id="deaaf-136">-Path</span></span>
<span data-ttu-id="deaaf-137">Klasörün yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="deaaf-137">Specifies the path of a folder.</span></span>
<span data-ttu-id="deaaf-138">Bu parametrenin belirttiği klasör boşsa, bu cmdlet bu klasörü siler.</span><span class="sxs-lookup"><span data-stu-id="deaaf-138">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="deaaf-139">Klasör boşsa, bu cmdlet değişiklik yapmaz ve hata verir.</span><span class="sxs-lookup"><span data-stu-id="deaaf-139">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Directory
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deaaf-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="deaaf-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="deaaf-141">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="deaaf-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="deaaf-142">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="deaaf-142">-Share</span></span>
<span data-ttu-id="deaaf-143">Bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="deaaf-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="deaaf-144">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımının altındaki klasörü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="deaaf-144">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="deaaf-145">**Cloudfileshare** nesnesi edinmek için Get-AzureStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="deaaf-145">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="deaaf-146">Bu nesne depolama bağlamını içerir.</span><span class="sxs-lookup"><span data-stu-id="deaaf-146">This object contains the storage context.</span></span>
<span data-ttu-id="deaaf-147">Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="deaaf-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="deaaf-148">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="deaaf-148">-ShareName</span></span>
<span data-ttu-id="deaaf-149">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="deaaf-149">Specifies the name of the file share.</span></span>
<span data-ttu-id="deaaf-150">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımının altındaki klasörü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="deaaf-150">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deaaf-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="deaaf-151">-Confirm</span></span>
<span data-ttu-id="deaaf-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="deaaf-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deaaf-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deaaf-153">-WhatIf</span></span>
<span data-ttu-id="deaaf-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="deaaf-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deaaf-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="deaaf-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deaaf-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deaaf-156">CommonParameters</span></span>
<span data-ttu-id="deaaf-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="deaaf-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deaaf-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deaaf-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deaaf-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="deaaf-159">INPUTS</span></span>

### <span data-ttu-id="deaaf-160">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="deaaf-160">IStorageContext</span></span>

<span data-ttu-id="deaaf-161">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="deaaf-161">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="deaaf-162">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="deaaf-162">CloudFileDirectory</span></span>

<span data-ttu-id="deaaf-163">' Directory ' parametresi ardışık düzenin ' CloudFileDirectory ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="deaaf-163">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="deaaf-164">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="deaaf-164">CloudFileShare</span></span>

<span data-ttu-id="deaaf-165">' Share ' parametresi ardışık düzenin ' CloudFileShare ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="deaaf-165">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="deaaf-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="deaaf-166">OUTPUTS</span></span>

## <span data-ttu-id="deaaf-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="deaaf-167">NOTES</span></span>

## <span data-ttu-id="deaaf-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="deaaf-168">RELATED LINKS</span></span>

[<span data-ttu-id="deaaf-169">Get-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="deaaf-169">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="deaaf-170">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="deaaf-170">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="deaaf-171">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="deaaf-171">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)
