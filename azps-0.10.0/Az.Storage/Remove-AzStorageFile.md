---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
ms.openlocfilehash: a4893e77c0ee8a161b589d5305d16d522305572b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936185"
---
# <span data-ttu-id="cb3d8-101">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="cb3d8-101">Remove-AzStorageFile</span></span>

## <span data-ttu-id="cb3d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb3d8-102">SYNOPSIS</span></span>
<span data-ttu-id="cb3d8-103">Dosyayı siler.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-103">Deletes a file.</span></span>

## <span data-ttu-id="cb3d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb3d8-104">SYNTAX</span></span>

### <span data-ttu-id="cb3d8-105">PaylaşımAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cb3d8-105">ShareName (Default)</span></span>
```
Remove-AzStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb3d8-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="cb3d8-106">Share</span></span>
```
Remove-AzStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb3d8-107">Directory</span><span class="sxs-lookup"><span data-stu-id="cb3d8-107">Directory</span></span>
```
Remove-AzStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb3d8-108">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="cb3d8-108">File</span></span>
```
Remove-AzStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb3d8-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb3d8-109">DESCRIPTION</span></span>
<span data-ttu-id="cb3d8-110">**Remove-AzStorageFile** cmdlet 'i dosyayı siler.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-110">The **Remove-AzStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="cb3d8-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb3d8-111">EXAMPLES</span></span>

### <span data-ttu-id="cb3d8-112">Örnek 1: dosya paylaşımından dosya silme</span><span class="sxs-lookup"><span data-stu-id="cb3d8-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="cb3d8-113">Bu komut, ContosoShare06 adındaki dosya paylaşımından ContosoFile22 adlı dosyayı siler.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="cb3d8-114">Örnek 2: dosya paylaşımı nesnesi kullanarak dosya paylaşımından dosya alma</span><span class="sxs-lookup"><span data-stu-id="cb3d8-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | Remove-AzStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="cb3d8-115">Bu komut, ContosoShare06 adlı dosya paylaşımını almak için **Get-Azstoragesshare** cmdlet 'ini kullanır ve ardından bu nesneyi ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cb3d8-116">Current komutu, ContosoFile22 adındaki dosyayı ContosoShare06 'dan siler.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="cb3d8-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb3d8-117">PARAMETERS</span></span>

### <span data-ttu-id="cb3d8-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cb3d8-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cb3d8-119">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cb3d8-120">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cb3d8-121">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cb3d8-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cb3d8-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cb3d8-123">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cb3d8-124">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cb3d8-125">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cb3d8-126">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cb3d8-127">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-127">The default value is 10.</span></span>

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

### <span data-ttu-id="cb3d8-128">-Context</span><span class="sxs-lookup"><span data-stu-id="cb3d8-128">-Context</span></span>
<span data-ttu-id="cb3d8-129">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cb3d8-130">Depolama bağlamı edinmek için, [New-AzStorageContext](./New-AzStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="cb3d8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb3d8-131">-DefaultProfile</span></span>
<span data-ttu-id="cb3d8-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb3d8-133">-Dizin</span><span class="sxs-lookup"><span data-stu-id="cb3d8-133">-Directory</span></span>
<span data-ttu-id="cb3d8-134">Bir klasörü **Cloudfiledirectory** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="cb3d8-135">Bu cmdlet, bu parametrenin belirttiği klasördeki dosyayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb3d8-136">-Dosya</span><span class="sxs-lookup"><span data-stu-id="cb3d8-136">-File</span></span>
<span data-ttu-id="cb3d8-137">Bir dosyayı **cloudfile** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="cb3d8-138">Bu cmdlet, bu parametrenin belirttiği dosyayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="cb3d8-139">**Cloudfile** nesnesi edinmek için Get-AzStorageFile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-139">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb3d8-140">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cb3d8-140">-PassThru</span></span>
<span data-ttu-id="cb3d8-141">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="cb3d8-142">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="cb3d8-143">-Yol</span><span class="sxs-lookup"><span data-stu-id="cb3d8-143">-Path</span></span>
<span data-ttu-id="cb3d8-144">Dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-144">Specifies the path of a file.</span></span>
<span data-ttu-id="cb3d8-145">Bu cmdlet, bu parametrenin belirttiği dosyayı siler.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-145">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb3d8-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cb3d8-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cb3d8-147">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="cb3d8-148">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="cb3d8-148">-Share</span></span>
<span data-ttu-id="cb3d8-149">Bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="cb3d8-150">Bu cmdlet, bu parametrenin belirttiği paylaşımdaki dosyayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="cb3d8-151">**Cloudfileshare** nesnesi edinmek için Get-AzStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="cb3d8-152">Bu nesne depolama bağlamını içerir.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-152">This object contains the storage context.</span></span>
<span data-ttu-id="cb3d8-153">Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="cb3d8-154">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="cb3d8-154">-ShareName</span></span>
<span data-ttu-id="cb3d8-155">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="cb3d8-156">Bu cmdlet, bu parametrenin belirttiği paylaşımdaki dosyayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="cb3d8-157">-Onay</span><span class="sxs-lookup"><span data-stu-id="cb3d8-157">-Confirm</span></span>
<span data-ttu-id="cb3d8-158">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb3d8-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb3d8-159">-WhatIf</span></span>
<span data-ttu-id="cb3d8-160">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb3d8-161">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb3d8-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb3d8-162">CommonParameters</span></span>
<span data-ttu-id="cb3d8-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb3d8-164">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cb3d8-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb3d8-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb3d8-165">INPUTS</span></span>

### <span data-ttu-id="cb3d8-166">Microsoft. WindowsAz. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="cb3d8-166">Microsoft.WindowsAz.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="cb3d8-167">Parametreler: paylaşma (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cb3d8-167">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="cb3d8-168">Microsoft. WindowsAz. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="cb3d8-168">Microsoft.WindowsAz.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="cb3d8-169">Parametreler: Dizin (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cb3d8-169">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="cb3d8-170">Microsoft. WindowsAz. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="cb3d8-170">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>
<span data-ttu-id="cb3d8-171">Parametreler: FILE (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cb3d8-171">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="cb3d8-172">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="cb3d8-172">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cb3d8-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb3d8-173">OUTPUTS</span></span>

### <span data-ttu-id="cb3d8-174">Microsoft. WindowsAz. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="cb3d8-174">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>

## <span data-ttu-id="cb3d8-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb3d8-175">NOTES</span></span>

## <span data-ttu-id="cb3d8-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb3d8-176">RELATED LINKS</span></span>

[<span data-ttu-id="cb3d8-177">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="cb3d8-177">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="cb3d8-178">Get-Azstorages,</span><span class="sxs-lookup"><span data-stu-id="cb3d8-178">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="cb3d8-179">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cb3d8-179">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
