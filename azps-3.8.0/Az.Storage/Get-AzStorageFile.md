---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: aadbbbaaefe1090b221e049d310bf262fdddf28c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096710"
---
# <span data-ttu-id="d58db-101">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="d58db-101">Get-AzStorageFile</span></span>

## <span data-ttu-id="d58db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d58db-102">SYNOPSIS</span></span>
<span data-ttu-id="d58db-103">Bir yolun dizinlerini ve dosyalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="d58db-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="d58db-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d58db-104">SYNTAX</span></span>

### <span data-ttu-id="d58db-105">PaylaşımAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d58db-105">ShareName (Default)</span></span>
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d58db-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="d58db-106">Share</span></span>
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="d58db-107">Directory</span><span class="sxs-lookup"><span data-stu-id="d58db-107">Directory</span></span>
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="d58db-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d58db-108">DESCRIPTION</span></span>
<span data-ttu-id="d58db-109">**Get-AzStorageFile** cmdlet 'i belirttiğiniz paylaşımın veya dizinin dizinlerini ve dosyalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="d58db-109">The **Get-AzStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="d58db-110">Belirtilen yoldaki bir dizinin veya dosyanın bir örneğinin alınacağı *yol* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="d58db-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="d58db-111">Bu cmdlet, **Azurestoragefile** ve **Azurestoragedirectory** nesnelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d58db-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="d58db-112">Dosya ve klasörleri birbirinden ayırt etmek için **IsDirectory** özelliğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d58db-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="d58db-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d58db-113">EXAMPLES</span></span>

### <span data-ttu-id="d58db-114">Örnek 1: paylaşımdaki dizinleri listeleme</span><span class="sxs-lookup"><span data-stu-id="d58db-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

<span data-ttu-id="d58db-115">Bu komut yalnızca paylaşım ContosoShare06 dizinleri listeler.</span><span class="sxs-lookup"><span data-stu-id="d58db-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="d58db-116">Önce hem dosyaları hem de dizinleri alır, ardışık düzen işlecini kullanarak bunları **WHERE** operatörüne geçirir ve sonra türü "CloudFileDirectory" olmayan tüm nesneleri atar.</span><span class="sxs-lookup"><span data-stu-id="d58db-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "CloudFileDirectory".</span></span>

### <span data-ttu-id="d58db-117">Örnek 2: dosya dizini listeleme</span><span class="sxs-lookup"><span data-stu-id="d58db-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

<span data-ttu-id="d58db-118">Bu komut, Share ContosoShare06 'in altındaki Contosoworkingklasöründeki dosya ve klasörleri listeler.</span><span class="sxs-lookup"><span data-stu-id="d58db-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="d58db-119">Önce dizin örneğini alır ve ardından dizini listelemek için **Get-AzStorageFile** cmdlet 'ine ardışık düzen.</span><span class="sxs-lookup"><span data-stu-id="d58db-119">It first gets the directory instance, and then pipelines it to the **Get-AzStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="d58db-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d58db-120">PARAMETERS</span></span>

### <span data-ttu-id="d58db-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d58db-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d58db-122">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="d58db-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d58db-123">Önceki çağrı belirtilen aralıkta başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="d58db-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d58db-124">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="d58db-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d58db-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d58db-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d58db-126">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d58db-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d58db-127">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d58db-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d58db-128">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="d58db-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d58db-129">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="d58db-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d58db-130">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="d58db-130">The default value is 10.</span></span>

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

### <span data-ttu-id="d58db-131">-Context</span><span class="sxs-lookup"><span data-stu-id="d58db-131">-Context</span></span>
<span data-ttu-id="d58db-132">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d58db-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="d58db-133">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d58db-133">To obtain a Storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d58db-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d58db-134">-DefaultProfile</span></span>
<span data-ttu-id="d58db-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d58db-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d58db-136">-Dizin</span><span class="sxs-lookup"><span data-stu-id="d58db-136">-Directory</span></span>
<span data-ttu-id="d58db-137">Bir klasörü **Cloudfiledirectory** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="d58db-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="d58db-138">Bu cmdlet, bu parametrenin belirttiği klasörü alır.</span><span class="sxs-lookup"><span data-stu-id="d58db-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="d58db-139">Dizin edinmek için New-AzStorageDirectory cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d58db-139">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="d58db-140">Ayrıca **Get-AzStorageFile** cmdlet 'ini kullanarak bir dizin elde edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d58db-140">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d58db-141">-Yol</span><span class="sxs-lookup"><span data-stu-id="d58db-141">-Path</span></span>
<span data-ttu-id="d58db-142">Klasörün yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d58db-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="d58db-143">*Yol* parametresini atlarsanız, **Get-azstoragefile** belirtilen dosya paylaşımında veya dizininde bulunan dizinleri ve dosyaları listeler.</span><span class="sxs-lookup"><span data-stu-id="d58db-143">If you omit the *Path* parameter, **Get-AzStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="d58db-144">*Yol* parametresini eklerseniz, **Get-azstoragefile** belirtilen yoldaki dizinin veya dosyanın bir örneğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d58db-144">If you include the *Path* parameter, **Get-AzStorageFile** returns an instance of a directory or file in the specified path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d58db-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d58db-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d58db-146">İstek için, saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d58db-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="d58db-147">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="d58db-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="d58db-148">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="d58db-148">-Share</span></span>
<span data-ttu-id="d58db-149">Bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d58db-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="d58db-150">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımından bir dosya veya dizin alır.</span><span class="sxs-lookup"><span data-stu-id="d58db-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="d58db-151">**Cloudfileshare** nesnesi edinmek için Get-AzStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d58db-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="d58db-152">Bu nesne depolama bağlamını içerir.</span><span class="sxs-lookup"><span data-stu-id="d58db-152">This object contains the Storage context.</span></span>
<span data-ttu-id="d58db-153">Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="d58db-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d58db-154">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="d58db-154">-ShareName</span></span>
<span data-ttu-id="d58db-155">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d58db-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="d58db-156">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımından bir dosya veya dizin alır.</span><span class="sxs-lookup"><span data-stu-id="d58db-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="d58db-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d58db-157">CommonParameters</span></span>
<span data-ttu-id="d58db-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d58db-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d58db-159">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d58db-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d58db-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d58db-160">INPUTS</span></span>

### <span data-ttu-id="d58db-161">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="d58db-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="d58db-162">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="d58db-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="d58db-163">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="d58db-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d58db-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d58db-164">OUTPUTS</span></span>

### <span data-ttu-id="d58db-165">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="d58db-165">Microsoft.Azure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="d58db-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d58db-166">NOTES</span></span>

## <span data-ttu-id="d58db-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d58db-167">RELATED LINKS</span></span>

[<span data-ttu-id="d58db-168">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d58db-168">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="d58db-169">Yeni-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="d58db-169">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="d58db-170">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="d58db-170">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="d58db-171">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="d58db-171">Remove-AzStorageFile</span></span>](./Remove-AzStorageFile.md)

[<span data-ttu-id="d58db-172">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d58db-172">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)

