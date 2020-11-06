---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/stop-azurestoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageFileCopy.md
ms.openlocfilehash: ea9902b9bf678ad8f914104022a5ce5a7d04eb07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592139"
---
# <span data-ttu-id="d5673-101">Stop-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d5673-101">Stop-AzureStorageFileCopy</span></span>

## <span data-ttu-id="d5673-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5673-102">SYNOPSIS</span></span>
<span data-ttu-id="d5673-103">Belirtilen hedef dosyaya kopyalama işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="d5673-103">Stops a copy operation to the specified destination file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5673-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5673-104">SYNTAX</span></span>

### <span data-ttu-id="d5673-105">PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="d5673-105">ShareName</span></span>
```
Stop-AzureStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5673-106">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="d5673-106">File</span></span>
```
Stop-AzureStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5673-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5673-107">DESCRIPTION</span></span>
<span data-ttu-id="d5673-108">**Stop-AzureStorageFileCopy** cmdlet 'i dosyayı hedef dosyaya kopyalamayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="d5673-108">The **Stop-AzureStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="d5673-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5673-109">EXAMPLES</span></span>

### <span data-ttu-id="d5673-110">Örnek 1: kopyalama işlemini durdurma</span><span class="sxs-lookup"><span data-stu-id="d5673-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzureStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="d5673-111">Bu komut, belirtilen ada sahip bir dosyayı kopyalamayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="d5673-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="d5673-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5673-112">PARAMETERS</span></span>

### <span data-ttu-id="d5673-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d5673-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d5673-114">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5673-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d5673-115">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="d5673-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d5673-116">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="d5673-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d5673-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d5673-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d5673-118">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5673-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d5673-119">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d5673-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d5673-120">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="d5673-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d5673-121">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="d5673-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d5673-122">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="d5673-122">The default value is 10.</span></span>

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

### <span data-ttu-id="d5673-123">-Context</span><span class="sxs-lookup"><span data-stu-id="d5673-123">-Context</span></span>
<span data-ttu-id="d5673-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5673-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d5673-125">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d5673-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="d5673-126">-Copyıd</span><span class="sxs-lookup"><span data-stu-id="d5673-126">-CopyId</span></span>
<span data-ttu-id="d5673-127">Kopyalama işleminin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5673-127">Specifies the ID of the copy operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5673-128">-Dosya</span><span class="sxs-lookup"><span data-stu-id="d5673-128">-File</span></span>
<span data-ttu-id="d5673-129">Bir **Cloudfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5673-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="d5673-130">Get-AzureStorageFile cmdlet 'ini kullanarak bir bulut dosyası oluşturabilir veya bir tane edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d5673-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5673-131">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="d5673-131">-FilePath</span></span>
<span data-ttu-id="d5673-132">Dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5673-132">Specifies the path of a file.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5673-133">-Force</span><span class="sxs-lookup"><span data-stu-id="d5673-133">-Force</span></span>
<span data-ttu-id="d5673-134">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="d5673-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d5673-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d5673-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d5673-136">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5673-136">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="d5673-137">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="d5673-137">-ShareName</span></span>
<span data-ttu-id="d5673-138">Bir paylaşımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5673-138">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="d5673-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="d5673-139">-Confirm</span></span>
<span data-ttu-id="d5673-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d5673-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5673-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5673-141">-WhatIf</span></span>
<span data-ttu-id="d5673-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d5673-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5673-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d5673-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5673-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5673-144">CommonParameters</span></span>
<span data-ttu-id="d5673-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5673-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5673-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5673-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5673-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5673-147">INPUTS</span></span>

### <span data-ttu-id="d5673-148">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="d5673-148">IStorageContext</span></span>

<span data-ttu-id="d5673-149">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d5673-149">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="d5673-150">CloudFile</span><span class="sxs-lookup"><span data-stu-id="d5673-150">CloudFile</span></span>

<span data-ttu-id="d5673-151">' File ' parametresi ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="d5673-151">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

## <span data-ttu-id="d5673-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5673-152">OUTPUTS</span></span>

## <span data-ttu-id="d5673-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5673-153">NOTES</span></span>

## <span data-ttu-id="d5673-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5673-154">RELATED LINKS</span></span>

[<span data-ttu-id="d5673-155">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="d5673-155">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="d5673-156">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="d5673-156">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="d5673-157">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d5673-157">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="d5673-158">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d5673-158">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)
