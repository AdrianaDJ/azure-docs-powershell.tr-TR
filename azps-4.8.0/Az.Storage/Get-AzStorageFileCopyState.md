---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: b87c4169fb2a7d417f56051c4996cf0428ceafe7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266261"
---
# <span data-ttu-id="0c630-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="0c630-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="0c630-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c630-102">SYNOPSIS</span></span>
<span data-ttu-id="0c630-103">Kopyalama işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="0c630-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="0c630-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c630-104">SYNTAX</span></span>

### <span data-ttu-id="0c630-105">PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="0c630-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0c630-106">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="0c630-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c630-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c630-107">DESCRIPTION</span></span>
<span data-ttu-id="0c630-108">**Get-AzStorageFileCopyState** cmdlet 'i, bir Azure depolama dosya kopyalama işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="0c630-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>
<span data-ttu-id="0c630-109">Bu, hedef dosyayı Kopyala 'da çalışmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0c630-109">It should run on the copy destination file.</span></span>

## <span data-ttu-id="0c630-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c630-110">EXAMPLES</span></span>

### <span data-ttu-id="0c630-111">Örnek 1: dosya adına göre kopyalama durumunu alma</span><span class="sxs-lookup"><span data-stu-id="0c630-111">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="0c630-112">Bu komut, belirtilen ada sahip bir dosya için kopyalama işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="0c630-112">This command gets the state of the copy operation for a file that has the specified name.</span></span>

### <span data-ttu-id="0c630-113">Örnek 2: kopyalama durumunu almak için kopyalama ve ardışık düzeni başlatma</span><span class="sxs-lookup"><span data-stu-id="0c630-113">Example 2: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destfile = Start-AzStorageFileCopy -SrcShareName "contososhare" -SrcFilePath "contosofile" -DestShareName "contososhare2" -destfilepath "contosofile_copy"  

C:\PS> $destfile | Get-AzStorageFileCopyState
```

<span data-ttu-id="0c630-114">İlk komut "contosofile" dosyasını "contosofile_copy" olarak başlatır ve destiantion dosya nesnesinin çıkışını başlatır.</span><span class="sxs-lookup"><span data-stu-id="0c630-114">The first command starts copy file "contosofile" to "contosofile_copy", and output the destiantion file object.</span></span> <span data-ttu-id="0c630-115">İkinci komut ardışık düzeni, dosya kopyalama durumunu almak için Get-AzStorageFileCopyState için destiantion File nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="0c630-115">The second command pipeline the destiantion file object to Get-AzStorageFileCopyState, to get file copy state.</span></span>

## <span data-ttu-id="0c630-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c630-116">PARAMETERS</span></span>

### <span data-ttu-id="0c630-117">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0c630-117">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0c630-118">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c630-118">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0c630-119">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="0c630-119">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0c630-120">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="0c630-120">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0c630-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0c630-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0c630-122">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c630-122">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0c630-123">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0c630-123">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0c630-124">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="0c630-124">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0c630-125">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="0c630-125">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0c630-126">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="0c630-126">The default value is 10.</span></span>

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

### <span data-ttu-id="0c630-127">-Context</span><span class="sxs-lookup"><span data-stu-id="0c630-127">-Context</span></span>
<span data-ttu-id="0c630-128">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c630-128">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="0c630-129">Bağlam almak için, [New-AzStorageContext](./New-AzStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0c630-129">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="0c630-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c630-130">-DefaultProfile</span></span>
<span data-ttu-id="0c630-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c630-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c630-132">-Dosya</span><span class="sxs-lookup"><span data-stu-id="0c630-132">-File</span></span>
<span data-ttu-id="0c630-133">Bir **Cloudfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c630-133">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="0c630-134">Get-AzStorageFile cmdlet 'ini kullanarak bir bulut dosyası oluşturabilir veya bir tane edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0c630-134">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c630-135">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="0c630-135">-FilePath</span></span>
<span data-ttu-id="0c630-136">Bir Azure depolama paylaşımına göre dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c630-136">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="0c630-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0c630-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0c630-138">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c630-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="0c630-139">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="0c630-139">-ShareName</span></span>
<span data-ttu-id="0c630-140">Bir paylaşımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c630-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="0c630-141">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="0c630-141">-WaitForComplete</span></span>
<span data-ttu-id="0c630-142">Bu cmdlet 'in kopyanın bitmesini beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c630-142">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="0c630-143">Bu parametreyi belirtmezseniz, bu cmdlet hemen bir sonuç döndürür.</span><span class="sxs-lookup"><span data-stu-id="0c630-143">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="0c630-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c630-144">CommonParameters</span></span>
<span data-ttu-id="0c630-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c630-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c630-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c630-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c630-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c630-147">INPUTS</span></span>

### <span data-ttu-id="0c630-148">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="0c630-148">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="0c630-149">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="0c630-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0c630-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c630-150">OUTPUTS</span></span>

### <span data-ttu-id="0c630-151">Microsoft. Azure. Storage. File. CopyState</span><span class="sxs-lookup"><span data-stu-id="0c630-151">Microsoft.Azure.Storage.File.CopyState</span></span>

## <span data-ttu-id="0c630-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c630-152">NOTES</span></span>

## <span data-ttu-id="0c630-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c630-153">RELATED LINKS</span></span>

[<span data-ttu-id="0c630-154">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="0c630-154">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="0c630-155">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0c630-155">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="0c630-156">Başlangıç-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0c630-156">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="0c630-157">Dur-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0c630-157">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
