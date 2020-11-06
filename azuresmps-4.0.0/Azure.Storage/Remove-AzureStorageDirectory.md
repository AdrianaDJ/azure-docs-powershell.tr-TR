---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd885e79fb4daf1eec9dd8958283be28e52f920f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571497"
---
# <span data-ttu-id="34371-101">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="34371-101">Remove-AzureStorageDirectory</span></span>

## <span data-ttu-id="34371-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34371-102">SYNOPSIS</span></span>
<span data-ttu-id="34371-103">Dizin siler.</span><span class="sxs-lookup"><span data-stu-id="34371-103">Deletes a directory.</span></span>

## <span data-ttu-id="34371-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34371-104">SYNTAX</span></span>

### <span data-ttu-id="34371-105">PaylaşımAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="34371-105">ShareName (Default)</span></span>
```
Remove-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34371-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="34371-106">Share</span></span>
```
Remove-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34371-107">Directory</span><span class="sxs-lookup"><span data-stu-id="34371-107">Directory</span></span>
```
Remove-AzureStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34371-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="34371-108">DESCRIPTION</span></span>
<span data-ttu-id="34371-109">**Remove-AzureStorageDirectory** cmdlet 'i bir dizini siler.</span><span class="sxs-lookup"><span data-stu-id="34371-109">The **Remove-AzureStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="34371-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34371-110">EXAMPLES</span></span>

### <span data-ttu-id="34371-111">Örnek 1: klasör silme</span><span class="sxs-lookup"><span data-stu-id="34371-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="34371-112">Bu komut, ContosoShare06 adlı dosya paylaşımından Contosoworkingklasörünün adını siler.</span><span class="sxs-lookup"><span data-stu-id="34371-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="34371-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34371-113">PARAMETERS</span></span>

### <span data-ttu-id="34371-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="34371-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="34371-115">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="34371-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="34371-116">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="34371-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="34371-117">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="34371-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="34371-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="34371-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="34371-119">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34371-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="34371-120">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34371-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="34371-121">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="34371-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="34371-122">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="34371-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="34371-123">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="34371-123">The default value is 10.</span></span>

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

### <span data-ttu-id="34371-124">-Context</span><span class="sxs-lookup"><span data-stu-id="34371-124">-Context</span></span>
<span data-ttu-id="34371-125">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34371-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="34371-126">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="34371-126">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="34371-127">-Dizin</span><span class="sxs-lookup"><span data-stu-id="34371-127">-Directory</span></span>
<span data-ttu-id="34371-128">Bir klasörü **Cloudfiledirectory** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="34371-128">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="34371-129">Bu cmdlet, bu parametrenin belirttiği klasörü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="34371-129">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="34371-130">Dizin edinmek için New-AzureStorageDirectory cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="34371-130">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="34371-131">Bir dizin edinmek için **Get-Azurestoragefıle** cmdlet 'ini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34371-131">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="34371-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="34371-132">-PassThru</span></span>
<span data-ttu-id="34371-133">Bu cmdlet başarılı olursa, $True değerini döndüren anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="34371-133">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="34371-134">Bu parametreyi belirtirseniz ve cmdlet _yol_ parametresi için uygun olmayan bir değer nedeniyle başarısız olursa cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="34371-134">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="34371-135">Bu parametreyi belirtmezseniz, bu cmdlet bir değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="34371-135">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="34371-136">-Yol</span><span class="sxs-lookup"><span data-stu-id="34371-136">-Path</span></span>
<span data-ttu-id="34371-137">Klasörün yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="34371-137">Specifies the path of a folder.</span></span>
<span data-ttu-id="34371-138">Bu parametrenin belirttiği klasör boşsa, bu cmdlet bu klasörü siler.</span><span class="sxs-lookup"><span data-stu-id="34371-138">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="34371-139">Klasör boşsa, bu cmdlet değişiklik yapmaz ve hata verir.</span><span class="sxs-lookup"><span data-stu-id="34371-139">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="34371-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="34371-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="34371-141">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="34371-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="34371-142">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="34371-142">-Share</span></span>
<span data-ttu-id="34371-143">Bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="34371-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="34371-144">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımının altındaki klasörü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="34371-144">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="34371-145">**Cloudfileshare** nesnesi edinmek için Get-AzureStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="34371-145">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="34371-146">Bu nesne depolama bağlamını içerir.</span><span class="sxs-lookup"><span data-stu-id="34371-146">This object contains the storage context.</span></span>
<span data-ttu-id="34371-147">Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="34371-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="34371-148">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="34371-148">-ShareName</span></span>
<span data-ttu-id="34371-149">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34371-149">Specifies the name of the file share.</span></span>
<span data-ttu-id="34371-150">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımının altındaki klasörü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="34371-150">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="34371-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="34371-151">-Confirm</span></span>
<span data-ttu-id="34371-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34371-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34371-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34371-153">-WhatIf</span></span>
<span data-ttu-id="34371-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34371-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34371-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34371-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34371-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34371-156">CommonParameters</span></span>
<span data-ttu-id="34371-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34371-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34371-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34371-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34371-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34371-159">INPUTS</span></span>

## <span data-ttu-id="34371-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34371-160">OUTPUTS</span></span>

## <span data-ttu-id="34371-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34371-161">NOTES</span></span>

## <span data-ttu-id="34371-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34371-162">RELATED LINKS</span></span>

[<span data-ttu-id="34371-163">Get-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="34371-163">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="34371-164">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="34371-164">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="34371-165">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="34371-165">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)
