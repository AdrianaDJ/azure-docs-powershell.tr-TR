---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: 55a41e03d07cccc30f2cf8193749fcf4096c5179
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936259"
---
# <span data-ttu-id="72252-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="72252-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="72252-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72252-102">SYNOPSIS</span></span>
<span data-ttu-id="72252-103">Kopyalama işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="72252-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="72252-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72252-104">SYNTAX</span></span>

### <span data-ttu-id="72252-105">PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="72252-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="72252-106">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="72252-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="72252-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="72252-107">DESCRIPTION</span></span>
<span data-ttu-id="72252-108">**Get-AzStorageFileCopyState** cmdlet 'i, bir Azure depolama dosya kopyalama işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="72252-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="72252-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72252-109">EXAMPLES</span></span>

### <span data-ttu-id="72252-110">Örnek 1: dosya adına göre kopyalama durumunu alma</span><span class="sxs-lookup"><span data-stu-id="72252-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="72252-111">Bu komut, belirtilen ada sahip bir dosya için kopyalama işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="72252-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="72252-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72252-112">PARAMETERS</span></span>

### <span data-ttu-id="72252-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="72252-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="72252-114">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="72252-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="72252-115">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="72252-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="72252-116">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="72252-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="72252-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="72252-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="72252-118">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72252-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="72252-119">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72252-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="72252-120">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="72252-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="72252-121">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="72252-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="72252-122">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="72252-122">The default value is 10.</span></span>

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

### <span data-ttu-id="72252-123">-Context</span><span class="sxs-lookup"><span data-stu-id="72252-123">-Context</span></span>
<span data-ttu-id="72252-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72252-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="72252-125">Bağlam almak için, [New-AzStorageContext](./New-AzStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="72252-125">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="72252-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72252-126">-DefaultProfile</span></span>
<span data-ttu-id="72252-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="72252-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72252-128">-Dosya</span><span class="sxs-lookup"><span data-stu-id="72252-128">-File</span></span>
<span data-ttu-id="72252-129">Bir **Cloudfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="72252-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="72252-130">Get-AzStorageFile cmdlet 'ini kullanarak bir bulut dosyası oluşturabilir veya bir tane edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72252-130">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="72252-131">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="72252-131">-FilePath</span></span>
<span data-ttu-id="72252-132">Bir Azure depolama paylaşımına göre dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="72252-132">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="72252-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="72252-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="72252-134">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="72252-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="72252-135">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="72252-135">-ShareName</span></span>
<span data-ttu-id="72252-136">Bir paylaşımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72252-136">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="72252-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="72252-137">-WaitForComplete</span></span>
<span data-ttu-id="72252-138">Bu cmdlet 'in kopyanın bitmesini beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="72252-138">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="72252-139">Bu parametreyi belirtmezseniz, bu cmdlet hemen bir sonuç döndürür.</span><span class="sxs-lookup"><span data-stu-id="72252-139">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="72252-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72252-140">CommonParameters</span></span>
<span data-ttu-id="72252-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72252-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72252-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="72252-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72252-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72252-143">INPUTS</span></span>

### <span data-ttu-id="72252-144">Microsoft. WindowsAz. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="72252-144">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>
<span data-ttu-id="72252-145">Parametreler: FILE (ByValue)</span><span class="sxs-lookup"><span data-stu-id="72252-145">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="72252-146">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="72252-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="72252-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72252-147">OUTPUTS</span></span>

### <span data-ttu-id="72252-148">Microsoft. WindowsAz. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="72252-148">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>

## <span data-ttu-id="72252-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72252-149">NOTES</span></span>

## <span data-ttu-id="72252-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72252-150">RELATED LINKS</span></span>

[<span data-ttu-id="72252-151">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="72252-151">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="72252-152">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="72252-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="72252-153">Başlangıç-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="72252-153">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="72252-154">Dur-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="72252-154">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)