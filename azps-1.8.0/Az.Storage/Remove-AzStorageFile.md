---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
ms.openlocfilehash: cfe3a924f9ce1d911c4e6e01fc7b35adc54537a8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758566"
---
# <span data-ttu-id="95c2c-101">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="95c2c-101">Remove-AzStorageFile</span></span>

## <span data-ttu-id="95c2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95c2c-102">SYNOPSIS</span></span>
<span data-ttu-id="95c2c-103">Dosyayı siler.</span><span class="sxs-lookup"><span data-stu-id="95c2c-103">Deletes a file.</span></span>

## <span data-ttu-id="95c2c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95c2c-104">SYNTAX</span></span>

### <span data-ttu-id="95c2c-105">PaylaşımAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="95c2c-105">ShareName (Default)</span></span>
```
Remove-AzStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95c2c-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="95c2c-106">Share</span></span>
```
Remove-AzStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95c2c-107">Directory</span><span class="sxs-lookup"><span data-stu-id="95c2c-107">Directory</span></span>
```
Remove-AzStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95c2c-108">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="95c2c-108">File</span></span>
```
Remove-AzStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95c2c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="95c2c-109">DESCRIPTION</span></span>
<span data-ttu-id="95c2c-110">**Remove-AzStorageFile** cmdlet 'i dosyayı siler.</span><span class="sxs-lookup"><span data-stu-id="95c2c-110">The **Remove-AzStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="95c2c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95c2c-111">EXAMPLES</span></span>

### <span data-ttu-id="95c2c-112">Örnek 1: dosya paylaşımından dosya silme</span><span class="sxs-lookup"><span data-stu-id="95c2c-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="95c2c-113">Bu komut, ContosoShare06 adındaki dosya paylaşımından ContosoFile22 adlı dosyayı siler.</span><span class="sxs-lookup"><span data-stu-id="95c2c-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="95c2c-114">Örnek 2: dosya paylaşımı nesnesi kullanarak dosya paylaşımından dosya alma</span><span class="sxs-lookup"><span data-stu-id="95c2c-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | Remove-AzStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="95c2c-115">Bu komut, ContosoShare06 adlı dosya paylaşımını almak için **Get-Azstoragesshare** cmdlet 'ini kullanır ve ardından bu nesneyi ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="95c2c-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="95c2c-116">Current komutu, ContosoFile22 adındaki dosyayı ContosoShare06 'dan siler.</span><span class="sxs-lookup"><span data-stu-id="95c2c-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="95c2c-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95c2c-117">PARAMETERS</span></span>

### <span data-ttu-id="95c2c-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="95c2c-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="95c2c-119">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="95c2c-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="95c2c-120">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="95c2c-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="95c2c-121">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="95c2c-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="95c2c-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="95c2c-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="95c2c-123">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="95c2c-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="95c2c-124">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95c2c-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="95c2c-125">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="95c2c-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="95c2c-126">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="95c2c-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="95c2c-127">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="95c2c-127">The default value is 10.</span></span>

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

### <span data-ttu-id="95c2c-128">-Context</span><span class="sxs-lookup"><span data-stu-id="95c2c-128">-Context</span></span>
<span data-ttu-id="95c2c-129">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="95c2c-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="95c2c-130">Depolama bağlamı edinmek için, [New-AzStorageContext](./New-AzStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="95c2c-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="95c2c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95c2c-131">-DefaultProfile</span></span>
<span data-ttu-id="95c2c-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="95c2c-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95c2c-133">-Dizin</span><span class="sxs-lookup"><span data-stu-id="95c2c-133">-Directory</span></span>
<span data-ttu-id="95c2c-134">Bir klasörü **Cloudfiledirectory** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="95c2c-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="95c2c-135">Bu cmdlet, bu parametrenin belirttiği klasördeki dosyayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="95c2c-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="95c2c-136">-Dosya</span><span class="sxs-lookup"><span data-stu-id="95c2c-136">-File</span></span>
<span data-ttu-id="95c2c-137">Bir dosyayı **cloudfile** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="95c2c-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="95c2c-138">Bu cmdlet, bu parametrenin belirttiği dosyayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="95c2c-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="95c2c-139">**Cloudfile** nesnesi edinmek için Get-AzStorageFile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="95c2c-139">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="95c2c-140">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="95c2c-140">-PassThru</span></span>
<span data-ttu-id="95c2c-141">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="95c2c-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="95c2c-142">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="95c2c-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="95c2c-143">-Yol</span><span class="sxs-lookup"><span data-stu-id="95c2c-143">-Path</span></span>
<span data-ttu-id="95c2c-144">Dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="95c2c-144">Specifies the path of a file.</span></span>
<span data-ttu-id="95c2c-145">Bu cmdlet, bu parametrenin belirttiği dosyayı siler.</span><span class="sxs-lookup"><span data-stu-id="95c2c-145">This cmdlet deletes the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="95c2c-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="95c2c-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="95c2c-147">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="95c2c-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="95c2c-148">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="95c2c-148">-Share</span></span>
<span data-ttu-id="95c2c-149">Bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="95c2c-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="95c2c-150">Bu cmdlet, bu parametrenin belirttiği paylaşımdaki dosyayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="95c2c-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="95c2c-151">**Cloudfileshare** nesnesi edinmek için Get-AzStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="95c2c-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="95c2c-152">Bu nesne depolama bağlamını içerir.</span><span class="sxs-lookup"><span data-stu-id="95c2c-152">This object contains the storage context.</span></span>
<span data-ttu-id="95c2c-153">Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="95c2c-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="95c2c-154">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="95c2c-154">-ShareName</span></span>
<span data-ttu-id="95c2c-155">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="95c2c-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="95c2c-156">Bu cmdlet, bu parametrenin belirttiği paylaşımdaki dosyayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="95c2c-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="95c2c-157">-Onay</span><span class="sxs-lookup"><span data-stu-id="95c2c-157">-Confirm</span></span>
<span data-ttu-id="95c2c-158">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="95c2c-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95c2c-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95c2c-159">-WhatIf</span></span>
<span data-ttu-id="95c2c-160">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="95c2c-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95c2c-161">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="95c2c-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95c2c-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95c2c-162">CommonParameters</span></span>
<span data-ttu-id="95c2c-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95c2c-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95c2c-164">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95c2c-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95c2c-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95c2c-165">INPUTS</span></span>

### <span data-ttu-id="95c2c-166">Microsoft. Windowsazde. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="95c2c-166">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="95c2c-167">Microsoft. Windowsazde. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="95c2c-167">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="95c2c-168">Microsoft. Windowsazde. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="95c2c-168">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="95c2c-169">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="95c2c-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="95c2c-170">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95c2c-170">OUTPUTS</span></span>

### <span data-ttu-id="95c2c-171">Microsoft. Windowsazde. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="95c2c-171">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="95c2c-172">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95c2c-172">NOTES</span></span>

## <span data-ttu-id="95c2c-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95c2c-173">RELATED LINKS</span></span>

[<span data-ttu-id="95c2c-174">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="95c2c-174">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="95c2c-175">Get-Azstorages,</span><span class="sxs-lookup"><span data-stu-id="95c2c-175">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="95c2c-176">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="95c2c-176">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
