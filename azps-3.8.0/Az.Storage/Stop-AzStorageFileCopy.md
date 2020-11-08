---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/stop-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
ms.openlocfilehash: 7d015a9f3255672e0de0c85a5ff8390bc3cde68e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096978"
---
# <span data-ttu-id="f0a00-101">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f0a00-101">Stop-AzStorageFileCopy</span></span>

## <span data-ttu-id="f0a00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0a00-102">SYNOPSIS</span></span>
<span data-ttu-id="f0a00-103">Belirtilen hedef dosyaya kopyalama işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="f0a00-103">Stops a copy operation to the specified destination file.</span></span>

## <span data-ttu-id="f0a00-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0a00-104">SYNTAX</span></span>

### <span data-ttu-id="f0a00-105">PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="f0a00-105">ShareName</span></span>
```
Stop-AzStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0a00-106">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="f0a00-106">File</span></span>
```
Stop-AzStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0a00-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0a00-107">DESCRIPTION</span></span>
<span data-ttu-id="f0a00-108">**Stop-AzStorageFileCopy** cmdlet 'i bir dosyayı hedef dosyaya kopyalamayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="f0a00-108">The **Stop-AzStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="f0a00-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0a00-109">EXAMPLES</span></span>

### <span data-ttu-id="f0a00-110">Örnek 1: kopyalama işlemini durdurma</span><span class="sxs-lookup"><span data-stu-id="f0a00-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="f0a00-111">Bu komut, belirtilen ada sahip bir dosyayı kopyalamayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="f0a00-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="f0a00-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0a00-112">PARAMETERS</span></span>

### <span data-ttu-id="f0a00-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f0a00-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f0a00-114">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0a00-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f0a00-115">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="f0a00-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f0a00-116">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="f0a00-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a00-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f0a00-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f0a00-118">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0a00-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f0a00-119">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0a00-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f0a00-120">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="f0a00-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f0a00-121">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="f0a00-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f0a00-122">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="f0a00-122">The default value is 10.</span></span>

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

### <span data-ttu-id="f0a00-123">-Context</span><span class="sxs-lookup"><span data-stu-id="f0a00-123">-Context</span></span>
<span data-ttu-id="f0a00-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0a00-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f0a00-125">Depolama bağlamı edinmek için, [New-AzStorageContext](./New-AzStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f0a00-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="f0a00-126">-Copyıd</span><span class="sxs-lookup"><span data-stu-id="f0a00-126">-CopyId</span></span>
<span data-ttu-id="f0a00-127">Kopyalama işleminin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0a00-127">Specifies the ID of the copy operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a00-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0a00-128">-DefaultProfile</span></span>
<span data-ttu-id="f0a00-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f0a00-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0a00-130">-Dosya</span><span class="sxs-lookup"><span data-stu-id="f0a00-130">-File</span></span>
<span data-ttu-id="f0a00-131">Bir **Cloudfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0a00-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="f0a00-132">Get-AzStorageFile cmdlet 'ini kullanarak bir bulut dosyası oluşturabilir veya bir tane edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0a00-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a00-133">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="f0a00-133">-FilePath</span></span>
<span data-ttu-id="f0a00-134">Dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0a00-134">Specifies the path of a file.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a00-135">-Force</span><span class="sxs-lookup"><span data-stu-id="f0a00-135">-Force</span></span>
<span data-ttu-id="f0a00-136">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f0a00-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f0a00-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f0a00-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f0a00-138">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0a00-138">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a00-139">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="f0a00-139">-ShareName</span></span>
<span data-ttu-id="f0a00-140">Bir paylaşımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0a00-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="f0a00-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="f0a00-141">-Confirm</span></span>
<span data-ttu-id="f0a00-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f0a00-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0a00-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0a00-143">-WhatIf</span></span>
<span data-ttu-id="f0a00-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f0a00-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0a00-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f0a00-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0a00-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0a00-146">CommonParameters</span></span>
<span data-ttu-id="f0a00-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0a00-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0a00-148">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0a00-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0a00-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0a00-149">INPUTS</span></span>

### <span data-ttu-id="f0a00-150">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="f0a00-150">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="f0a00-151">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="f0a00-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f0a00-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0a00-152">OUTPUTS</span></span>

### <span data-ttu-id="f0a00-153">System. void</span><span class="sxs-lookup"><span data-stu-id="f0a00-153">System.Void</span></span>

## <span data-ttu-id="f0a00-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0a00-154">NOTES</span></span>

## <span data-ttu-id="f0a00-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0a00-155">RELATED LINKS</span></span>

[<span data-ttu-id="f0a00-156">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="f0a00-156">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="f0a00-157">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="f0a00-157">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="f0a00-158">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f0a00-158">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="f0a00-159">Başlangıç-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f0a00-159">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)
