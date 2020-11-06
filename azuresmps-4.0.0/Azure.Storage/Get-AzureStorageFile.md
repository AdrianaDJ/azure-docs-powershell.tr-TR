---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3b84deae0307114efa274cdfa6fc708d1b268ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572381"
---
# <span data-ttu-id="03d17-101">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="03d17-101">Get-AzureStorageFile</span></span>

## <span data-ttu-id="03d17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03d17-102">SYNOPSIS</span></span>
<span data-ttu-id="03d17-103">Bir yolun dizinlerini ve dosyalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="03d17-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="03d17-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03d17-104">SYNTAX</span></span>

### <span data-ttu-id="03d17-105">PaylaşımAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="03d17-105">ShareName (Default)</span></span>
```
Get-AzureStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="03d17-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="03d17-106">Share</span></span>
```
Get-AzureStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="03d17-107">Directory</span><span class="sxs-lookup"><span data-stu-id="03d17-107">Directory</span></span>
```
Get-AzureStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="03d17-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="03d17-108">DESCRIPTION</span></span>
<span data-ttu-id="03d17-109">**Get-Azurestoragefıle** cmdlet 'i belirttiğiniz paylaşımın veya dizinin dizinlerini ve dosyalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="03d17-109">The **Get-AzureStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="03d17-110">Belirtilen yoldaki bir dizinin veya dosyanın bir örneğinin alınacağı *yol* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="03d17-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>

<span data-ttu-id="03d17-111">Bu cmdlet, **Azurestoragefile** ve **Azurestoragedirectory** nesnelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="03d17-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="03d17-112">Dosya ve klasörleri birbirinden ayırt etmek için **IsDirectory** özelliğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03d17-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="03d17-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03d17-113">EXAMPLES</span></span>

### <span data-ttu-id="03d17-114">Örnek 1: paylaşımdaki dizinleri listeleme</span><span class="sxs-lookup"><span data-stu-id="03d17-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName "share1" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

<span data-ttu-id="03d17-115">Bu komut yalnızca paylaşım ContosoShare06 dizinleri listeler.</span><span class="sxs-lookup"><span data-stu-id="03d17-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="03d17-116">Önce hem dosyaları hem de dizinleri alır, ardışık düzen işlecini kullanarak bunları **WHERE** operatörüne geçirir ve sonra türü "CloudFileDirectory" olmayan tüm nesneleri atar.</span><span class="sxs-lookup"><span data-stu-id="03d17-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "CloudFileDirectory".</span></span>

### <span data-ttu-id="03d17-117">Örnek 2: dosya dizini listeleme</span><span class="sxs-lookup"><span data-stu-id="03d17-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzureStorageFile
```

<span data-ttu-id="03d17-118">Bu komut, Share ContosoShare06 'in altındaki Contosoworkingklasöründeki dosya ve klasörleri listeler.</span><span class="sxs-lookup"><span data-stu-id="03d17-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="03d17-119">Önce dizin örneğini alır ve ardından dizini listelemek için **Get-Azurestoragefıle** cmdlet 'ine ardışık düzen.</span><span class="sxs-lookup"><span data-stu-id="03d17-119">It first gets the directory instance, and then pipelines it to the **Get-AzureStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="03d17-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03d17-120">PARAMETERS</span></span>

### <span data-ttu-id="03d17-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="03d17-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="03d17-122">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="03d17-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="03d17-123">Önceki çağrı belirtilen aralıkta başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="03d17-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="03d17-124">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="03d17-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="03d17-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="03d17-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="03d17-126">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="03d17-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="03d17-127">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03d17-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="03d17-128">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="03d17-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="03d17-129">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="03d17-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="03d17-130">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="03d17-130">The default value is 10.</span></span>

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

### <span data-ttu-id="03d17-131">-Context</span><span class="sxs-lookup"><span data-stu-id="03d17-131">-Context</span></span>
<span data-ttu-id="03d17-132">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="03d17-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="03d17-133">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="03d17-133">To obtain a Storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="03d17-134">-Dizin</span><span class="sxs-lookup"><span data-stu-id="03d17-134">-Directory</span></span>
<span data-ttu-id="03d17-135">Bir klasörü **Cloudfiledirectory** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="03d17-135">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="03d17-136">Bu cmdlet, bu parametrenin belirttiği klasörü alır.</span><span class="sxs-lookup"><span data-stu-id="03d17-136">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="03d17-137">Dizin edinmek için New-AzureStorageDirectory cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="03d17-137">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="03d17-138">Bir dizin edinmek için **Get-Azurestoragefıle** cmdlet 'ini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03d17-138">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03d17-139">-Yol</span><span class="sxs-lookup"><span data-stu-id="03d17-139">-Path</span></span>
<span data-ttu-id="03d17-140">Klasörün yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="03d17-140">Specifies the path of a folder.</span></span>

<span data-ttu-id="03d17-141">*Yol* parametresini atlarsanız, **Get-AzureStorageFile** belirtilen dosya paylaşımında veya dizininde bulunan dizinleri ve dosyaları listeler.</span><span class="sxs-lookup"><span data-stu-id="03d17-141">If you omit the *Path* parameter, **Get-AzureStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="03d17-142">*Yol* parametresini eklerseniz, **Get-AzureStorageFile** belirtilen yoldaki bir dizinin veya dosyanın bir örneğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="03d17-142">If you include the *Path* parameter, **Get-AzureStorageFile** returns an instance of a directory or file in the specified path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03d17-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="03d17-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="03d17-144">İstek için, saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="03d17-144">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="03d17-145">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="03d17-145">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="03d17-146">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="03d17-146">-Share</span></span>
<span data-ttu-id="03d17-147">Bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="03d17-147">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="03d17-148">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımından bir dosya veya dizin alır.</span><span class="sxs-lookup"><span data-stu-id="03d17-148">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="03d17-149">**Cloudfileshare** nesnesi edinmek için Get-AzureStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="03d17-149">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="03d17-150">Bu nesne depolama bağlamını içerir.</span><span class="sxs-lookup"><span data-stu-id="03d17-150">This object contains the Storage context.</span></span>
<span data-ttu-id="03d17-151">Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="03d17-151">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03d17-152">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="03d17-152">-ShareName</span></span>
<span data-ttu-id="03d17-153">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="03d17-153">Specifies the name of the file share.</span></span>
<span data-ttu-id="03d17-154">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımından bir dosya veya dizin alır.</span><span class="sxs-lookup"><span data-stu-id="03d17-154">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="03d17-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03d17-155">CommonParameters</span></span>
<span data-ttu-id="03d17-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03d17-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03d17-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03d17-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03d17-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03d17-158">INPUTS</span></span>

## <span data-ttu-id="03d17-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03d17-159">OUTPUTS</span></span>

## <span data-ttu-id="03d17-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03d17-160">NOTES</span></span>

## <span data-ttu-id="03d17-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03d17-161">RELATED LINKS</span></span>

[<span data-ttu-id="03d17-162">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="03d17-162">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="03d17-163">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="03d17-163">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="03d17-164">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="03d17-164">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="03d17-165">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="03d17-165">Remove-AzureStorageFile</span></span>](./Remove-AzureStorageFile.md)

[<span data-ttu-id="03d17-166">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="03d17-166">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


