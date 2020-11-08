---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragefile
schema: 2.0.0
ms.openlocfilehash: cfb5a3255a91c7a7206ba0729c20e4d0c68c3ea2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939971"
---
# <span data-ttu-id="1a6ff-101">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="1a6ff-101">Remove-AzureStorageFile</span></span>

## <span data-ttu-id="1a6ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a6ff-102">SYNOPSIS</span></span>
<span data-ttu-id="1a6ff-103">Dosyayı siler.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-103">Deletes a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a6ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a6ff-104">SYNTAX</span></span>

### <span data-ttu-id="1a6ff-105">PaylaşımAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1a6ff-105">ShareName (Default)</span></span>
```
Remove-AzureStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a6ff-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="1a6ff-106">Share</span></span>
```
Remove-AzureStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a6ff-107">Directory</span><span class="sxs-lookup"><span data-stu-id="1a6ff-107">Directory</span></span>
```
Remove-AzureStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a6ff-108">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="1a6ff-108">File</span></span>
```
Remove-AzureStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a6ff-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a6ff-109">DESCRIPTION</span></span>
<span data-ttu-id="1a6ff-110">**Remove-AzureStorageFile** cmdlet 'i dosyayı siler.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-110">The **Remove-AzureStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="1a6ff-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a6ff-111">EXAMPLES</span></span>

### <span data-ttu-id="1a6ff-112">Örnek 1: dosya paylaşımından dosya silme</span><span class="sxs-lookup"><span data-stu-id="1a6ff-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="1a6ff-113">Bu komut, ContosoShare06 adındaki dosya paylaşımından ContosoFile22 adlı dosyayı siler.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="1a6ff-114">Örnek 2: dosya paylaşımı nesnesi kullanarak dosya paylaşımından dosya alma</span><span class="sxs-lookup"><span data-stu-id="1a6ff-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | Remove-AzureStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="1a6ff-115">Bu komut, ContosoShare06 adlı dosya paylaşımını almak için **Get-Azurestoragesshare** cmdlet 'ini kullanır ve ardından bu nesneyi ardışık düzen işlecini kullanarak geçerli cmdlet 'e iletir.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1a6ff-116">Current komutu, ContosoFile22 adındaki dosyayı ContosoShare06 'dan siler.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="1a6ff-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a6ff-117">PARAMETERS</span></span>

### <span data-ttu-id="1a6ff-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1a6ff-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1a6ff-119">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1a6ff-120">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1a6ff-121">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1a6ff-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1a6ff-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1a6ff-123">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1a6ff-124">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1a6ff-125">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1a6ff-126">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1a6ff-127">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-127">The default value is 10.</span></span>

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

### <span data-ttu-id="1a6ff-128">-Context</span><span class="sxs-lookup"><span data-stu-id="1a6ff-128">-Context</span></span>
<span data-ttu-id="1a6ff-129">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1a6ff-130">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="1a6ff-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a6ff-131">-DefaultProfile</span></span>
<span data-ttu-id="1a6ff-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a6ff-133">-Dizin</span><span class="sxs-lookup"><span data-stu-id="1a6ff-133">-Directory</span></span>
<span data-ttu-id="1a6ff-134">Bir klasörü **Cloudfiledirectory** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="1a6ff-135">Bu cmdlet, bu parametrenin belirttiği klasördeki dosyayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="1a6ff-136">-Dosya</span><span class="sxs-lookup"><span data-stu-id="1a6ff-136">-File</span></span>
<span data-ttu-id="1a6ff-137">Bir dosyayı **cloudfile** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="1a6ff-138">Bu cmdlet, bu parametrenin belirttiği dosyayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="1a6ff-139">**Cloudfile** nesnesi edinmek için Get-AzureStorageFile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-139">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="1a6ff-140">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1a6ff-140">-PassThru</span></span>
<span data-ttu-id="1a6ff-141">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="1a6ff-142">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="1a6ff-143">-Yol</span><span class="sxs-lookup"><span data-stu-id="1a6ff-143">-Path</span></span>
<span data-ttu-id="1a6ff-144">Dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-144">Specifies the path of a file.</span></span>
<span data-ttu-id="1a6ff-145">Bu cmdlet, bu parametrenin belirttiği dosyayı siler.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-145">This cmdlet deletes the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="1a6ff-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1a6ff-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1a6ff-147">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="1a6ff-148">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="1a6ff-148">-Share</span></span>
<span data-ttu-id="1a6ff-149">Bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="1a6ff-150">Bu cmdlet, bu parametrenin belirttiği paylaşımdaki dosyayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="1a6ff-151">**Cloudfileshare** nesnesi edinmek için Get-AzureStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-151">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="1a6ff-152">Bu nesne depolama bağlamını içerir.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-152">This object contains the storage context.</span></span>
<span data-ttu-id="1a6ff-153">Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="1a6ff-154">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="1a6ff-154">-ShareName</span></span>
<span data-ttu-id="1a6ff-155">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="1a6ff-156">Bu cmdlet, bu parametrenin belirttiği paylaşımdaki dosyayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="1a6ff-157">-Onay</span><span class="sxs-lookup"><span data-stu-id="1a6ff-157">-Confirm</span></span>
<span data-ttu-id="1a6ff-158">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a6ff-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a6ff-159">-WhatIf</span></span>
<span data-ttu-id="1a6ff-160">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a6ff-161">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a6ff-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a6ff-162">CommonParameters</span></span>
<span data-ttu-id="1a6ff-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a6ff-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a6ff-164">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a6ff-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a6ff-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a6ff-165">INPUTS</span></span>

### <span data-ttu-id="1a6ff-166">Microsoft. Windowsazde. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="1a6ff-166">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="1a6ff-167">Parametreler: paylaşma (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1a6ff-167">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="1a6ff-168">Microsoft. Windowsazde. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="1a6ff-168">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="1a6ff-169">Parametreler: Dizin (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1a6ff-169">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="1a6ff-170">Microsoft. Windowsazde. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="1a6ff-170">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="1a6ff-171">Parametreler: FILE (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1a6ff-171">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="1a6ff-172">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="1a6ff-172">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1a6ff-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a6ff-173">OUTPUTS</span></span>

### <span data-ttu-id="1a6ff-174">Microsoft. Windowsazde. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="1a6ff-174">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="1a6ff-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a6ff-175">NOTES</span></span>

## <span data-ttu-id="1a6ff-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a6ff-176">RELATED LINKS</span></span>

[<span data-ttu-id="1a6ff-177">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="1a6ff-177">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="1a6ff-178">Get-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="1a6ff-178">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="1a6ff-179">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1a6ff-179">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)