---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
ms.openlocfilehash: c2322b3044aa826f7f5163939e186181fe58a4d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758565"
---
# <span data-ttu-id="9b8cf-101">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="9b8cf-101">Remove-AzStorageShare</span></span>

## <span data-ttu-id="9b8cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b8cf-102">SYNOPSIS</span></span>
<span data-ttu-id="9b8cf-103">Dosya paylaşımını siler.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-103">Deletes a file share.</span></span>

## <span data-ttu-id="9b8cf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9b8cf-104">SYNTAX</span></span>

### <span data-ttu-id="9b8cf-105">PaylaşımAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9b8cf-105">ShareName (Default)</span></span>
```
Remove-AzStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b8cf-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="9b8cf-106">Share</span></span>
```
Remove-AzStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b8cf-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9b8cf-107">DESCRIPTION</span></span>
<span data-ttu-id="9b8cf-108">**Remove-Azstoragesshare** cmdlet 'i dosya paylaşımını siler.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-108">The **Remove-AzStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="9b8cf-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9b8cf-109">EXAMPLES</span></span>

### <span data-ttu-id="9b8cf-110">Örnek 1: dosya paylaşımını kaldırma</span><span class="sxs-lookup"><span data-stu-id="9b8cf-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="9b8cf-111">Bu komut, ContosoShare06 adlı dosya paylaşımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="9b8cf-112">Örnek 2: dosya paylaşımını ve tüm anlık görüntülerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="9b8cf-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="9b8cf-113">Bu komut, ContosoShare06 adlı dosya paylaşımını ve tüm anlık görüntülerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="9b8cf-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9b8cf-114">PARAMETERS</span></span>

### <span data-ttu-id="9b8cf-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9b8cf-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9b8cf-116">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9b8cf-117">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9b8cf-118">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9b8cf-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9b8cf-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9b8cf-120">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9b8cf-121">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9b8cf-122">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9b8cf-123">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9b8cf-124">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-124">The default value is 10.</span></span>

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

### <span data-ttu-id="9b8cf-125">-Context</span><span class="sxs-lookup"><span data-stu-id="9b8cf-125">-Context</span></span>
<span data-ttu-id="9b8cf-126">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9b8cf-127">Depolama bağlamı edinmek için, [New-AzStorageContext](./New-AzStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-127">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="9b8cf-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b8cf-128">-DefaultProfile</span></span>
<span data-ttu-id="9b8cf-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b8cf-130">-Force</span><span class="sxs-lookup"><span data-stu-id="9b8cf-130">-Force</span></span>
<span data-ttu-id="9b8cf-131">Paylaşımı tüm anlık görüntülerle ve tüm içeriklerle kaldırmaya zorlayın.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-131">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="9b8cf-132">-Includeallsnapshot</span><span class="sxs-lookup"><span data-stu-id="9b8cf-132">-IncludeAllSnapshot</span></span>
<span data-ttu-id="9b8cf-133">Dosya paylaşımını tüm anlık görüntüleriyle kaldırma</span><span class="sxs-lookup"><span data-stu-id="9b8cf-133">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="9b8cf-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="9b8cf-134">-Name</span></span>
<span data-ttu-id="9b8cf-135">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-135">Specifies the name of the file share.</span></span>
<span data-ttu-id="9b8cf-136">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımını siler.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-136">This cmdlet deletes the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b8cf-137">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9b8cf-137">-PassThru</span></span>
<span data-ttu-id="9b8cf-138">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-138">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="9b8cf-139">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-139">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="9b8cf-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9b8cf-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9b8cf-141">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="9b8cf-142">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="9b8cf-142">-Share</span></span>
<span data-ttu-id="9b8cf-143">Bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="9b8cf-144">Bu cmdlet, bu parametrenin belirttiği nesneyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-144">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="9b8cf-145">**Cloudfileshare** nesnesi edinmek için Get-AzStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-145">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="9b8cf-146">Bu nesne depolama bağlamını içerir.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-146">This object contains the storage context.</span></span>
<span data-ttu-id="9b8cf-147">Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="9b8cf-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="9b8cf-148">-Confirm</span></span>
<span data-ttu-id="9b8cf-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b8cf-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b8cf-150">-WhatIf</span></span>
<span data-ttu-id="9b8cf-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b8cf-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b8cf-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b8cf-153">CommonParameters</span></span>
<span data-ttu-id="9b8cf-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9b8cf-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b8cf-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b8cf-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b8cf-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9b8cf-156">INPUTS</span></span>

### <span data-ttu-id="9b8cf-157">System. String</span><span class="sxs-lookup"><span data-stu-id="9b8cf-157">System.String</span></span>

### <span data-ttu-id="9b8cf-158">Microsoft. Windowsazde. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="9b8cf-158">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="9b8cf-159">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="9b8cf-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9b8cf-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9b8cf-160">OUTPUTS</span></span>

### <span data-ttu-id="9b8cf-161">Microsoft. Windowsazde. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="9b8cf-161">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="9b8cf-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9b8cf-162">NOTES</span></span>

## <span data-ttu-id="9b8cf-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9b8cf-163">RELATED LINKS</span></span>

[<span data-ttu-id="9b8cf-164">Get-Azstorages,</span><span class="sxs-lookup"><span data-stu-id="9b8cf-164">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="9b8cf-165">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="9b8cf-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="9b8cf-166">Yeni-Azstoragesbir</span><span class="sxs-lookup"><span data-stu-id="9b8cf-166">New-AzStorageShare</span></span>](./New-AzStorageShare.md)
