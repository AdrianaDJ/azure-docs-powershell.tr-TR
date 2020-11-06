---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
ms.openlocfilehash: 6df60027ff2c25a8f2c1c948d04213cfc6d6158e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587359"
---
# <span data-ttu-id="4870e-101">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="4870e-101">Remove-AzureStorageDirectory</span></span>

## <span data-ttu-id="4870e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4870e-102">SYNOPSIS</span></span>
<span data-ttu-id="4870e-103">Dizin siler.</span><span class="sxs-lookup"><span data-stu-id="4870e-103">Deletes a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4870e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4870e-104">SYNTAX</span></span>

### <span data-ttu-id="4870e-105">PaylaşımAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4870e-105">ShareName (Default)</span></span>
```
Remove-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4870e-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="4870e-106">Share</span></span>
```
Remove-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4870e-107">Directory</span><span class="sxs-lookup"><span data-stu-id="4870e-107">Directory</span></span>
```
Remove-AzureStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4870e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4870e-108">DESCRIPTION</span></span>
<span data-ttu-id="4870e-109">**Remove-AzureStorageDirectory** cmdlet 'i bir dizini siler.</span><span class="sxs-lookup"><span data-stu-id="4870e-109">The **Remove-AzureStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="4870e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4870e-110">EXAMPLES</span></span>

### <span data-ttu-id="4870e-111">Örnek 1: klasör silme</span><span class="sxs-lookup"><span data-stu-id="4870e-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="4870e-112">Bu komut, ContosoShare06 adlı dosya paylaşımından Contosoworkingklasörünün adını siler.</span><span class="sxs-lookup"><span data-stu-id="4870e-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="4870e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4870e-113">PARAMETERS</span></span>

### <span data-ttu-id="4870e-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4870e-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4870e-115">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="4870e-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4870e-116">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="4870e-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4870e-117">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="4870e-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4870e-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4870e-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4870e-119">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4870e-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4870e-120">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4870e-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4870e-121">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="4870e-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4870e-122">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="4870e-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4870e-123">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="4870e-123">The default value is 10.</span></span>

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

### <span data-ttu-id="4870e-124">-Context</span><span class="sxs-lookup"><span data-stu-id="4870e-124">-Context</span></span>
<span data-ttu-id="4870e-125">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4870e-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4870e-126">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4870e-126">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4870e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4870e-127">-DefaultProfile</span></span>
<span data-ttu-id="4870e-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4870e-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4870e-129">-Dizin</span><span class="sxs-lookup"><span data-stu-id="4870e-129">-Directory</span></span>
<span data-ttu-id="4870e-130">Bir klasörü **Cloudfiledirectory** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="4870e-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="4870e-131">Bu cmdlet, bu parametrenin belirttiği klasörü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4870e-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="4870e-132">Dizin edinmek için New-AzureStorageDirectory cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4870e-132">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="4870e-133">Bir dizin edinmek için **Get-Azurestoragefıle** cmdlet 'ini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4870e-133">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4870e-134">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4870e-134">-PassThru</span></span>
<span data-ttu-id="4870e-135">Bu cmdlet başarılı olursa, $True değerini döndüren anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="4870e-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="4870e-136">Bu parametreyi belirtirseniz ve cmdlet _yol_ parametresi için uygun olmayan bir değer nedeniyle başarısız olursa cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="4870e-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="4870e-137">Bu parametreyi belirtmezseniz, bu cmdlet bir değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="4870e-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4870e-138">-Yol</span><span class="sxs-lookup"><span data-stu-id="4870e-138">-Path</span></span>
<span data-ttu-id="4870e-139">Klasörün yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4870e-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="4870e-140">Bu parametrenin belirttiği klasör boşsa, bu cmdlet bu klasörü siler.</span><span class="sxs-lookup"><span data-stu-id="4870e-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="4870e-141">Klasör boşsa, bu cmdlet değişiklik yapmaz ve hata verir.</span><span class="sxs-lookup"><span data-stu-id="4870e-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4870e-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4870e-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4870e-143">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4870e-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4870e-144">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="4870e-144">-Share</span></span>
<span data-ttu-id="4870e-145">Bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4870e-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="4870e-146">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımının altındaki klasörü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4870e-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="4870e-147">**Cloudfileshare** nesnesi edinmek için Get-AzureStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4870e-147">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="4870e-148">Bu nesne depolama bağlamını içerir.</span><span class="sxs-lookup"><span data-stu-id="4870e-148">This object contains the storage context.</span></span>
<span data-ttu-id="4870e-149">Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="4870e-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4870e-150">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="4870e-150">-ShareName</span></span>
<span data-ttu-id="4870e-151">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4870e-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="4870e-152">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımının altındaki klasörü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4870e-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4870e-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="4870e-153">-Confirm</span></span>
<span data-ttu-id="4870e-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4870e-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4870e-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4870e-155">-WhatIf</span></span>
<span data-ttu-id="4870e-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4870e-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4870e-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4870e-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4870e-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4870e-158">CommonParameters</span></span>
<span data-ttu-id="4870e-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4870e-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4870e-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4870e-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4870e-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4870e-161">INPUTS</span></span>

### <span data-ttu-id="4870e-162">Microsoft. Windowsazde. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="4870e-162">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="4870e-163">Parametreler: paylaşma (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4870e-163">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="4870e-164">Microsoft. Windowsazde. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="4870e-164">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="4870e-165">Parametreler: Dizin (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4870e-165">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="4870e-166">System. String</span><span class="sxs-lookup"><span data-stu-id="4870e-166">System.String</span></span>

### <span data-ttu-id="4870e-167">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="4870e-167">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4870e-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4870e-168">OUTPUTS</span></span>

### <span data-ttu-id="4870e-169">Microsoft. Windowsazde. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="4870e-169">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="4870e-170">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4870e-170">NOTES</span></span>

## <span data-ttu-id="4870e-171">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4870e-171">RELATED LINKS</span></span>

[<span data-ttu-id="4870e-172">Get-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="4870e-172">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="4870e-173">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="4870e-173">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="4870e-174">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="4870e-174">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)
