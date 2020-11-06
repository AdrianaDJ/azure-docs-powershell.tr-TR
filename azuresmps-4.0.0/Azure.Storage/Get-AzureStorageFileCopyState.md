---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75e94fe8270287410902b215ec4e33ac9cd51624
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572373"
---
# <span data-ttu-id="1a10d-101">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="1a10d-101">Get-AzureStorageFileCopyState</span></span>

## <span data-ttu-id="1a10d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a10d-102">SYNOPSIS</span></span>
<span data-ttu-id="1a10d-103">Kopyalama işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="1a10d-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="1a10d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a10d-104">SYNTAX</span></span>

### <span data-ttu-id="1a10d-105">PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="1a10d-105">ShareName</span></span>
```
Get-AzureStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1a10d-106">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="1a10d-106">File</span></span>
```
Get-AzureStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="1a10d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a10d-107">DESCRIPTION</span></span>
<span data-ttu-id="1a10d-108">**Get-AzureStorageFileCopyState** cmdlet 'i, bir Azure depolama dosya kopyalama işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="1a10d-108">The **Get-AzureStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="1a10d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a10d-109">EXAMPLES</span></span>

### <span data-ttu-id="1a10d-110">Örnek 1: dosya adına göre kopyalama durumunu alma</span><span class="sxs-lookup"><span data-stu-id="1a10d-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzureStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="1a10d-111">Bu komut, belirtilen ada sahip bir dosya için kopyalama işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="1a10d-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="1a10d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a10d-112">PARAMETERS</span></span>

### <span data-ttu-id="1a10d-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1a10d-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1a10d-114">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a10d-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1a10d-115">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="1a10d-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1a10d-116">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="1a10d-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1a10d-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1a10d-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1a10d-118">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a10d-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1a10d-119">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1a10d-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1a10d-120">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="1a10d-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1a10d-121">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="1a10d-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1a10d-122">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="1a10d-122">The default value is 10.</span></span>

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

### <span data-ttu-id="1a10d-123">-Context</span><span class="sxs-lookup"><span data-stu-id="1a10d-123">-Context</span></span>
<span data-ttu-id="1a10d-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a10d-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="1a10d-125">Bağlam almak için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1a10d-125">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="1a10d-126">-Dosya</span><span class="sxs-lookup"><span data-stu-id="1a10d-126">-File</span></span>
<span data-ttu-id="1a10d-127">Bir **Cloudfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a10d-127">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="1a10d-128">Get-AzureStorageFile cmdlet 'ini kullanarak bir bulut dosyası oluşturabilir veya bir tane edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1a10d-128">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="1a10d-129">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="1a10d-129">-FilePath</span></span>
<span data-ttu-id="1a10d-130">Bir Azure depolama paylaşımına göre dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a10d-130">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="1a10d-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1a10d-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1a10d-132">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a10d-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="1a10d-133">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="1a10d-133">-ShareName</span></span>
<span data-ttu-id="1a10d-134">Bir paylaşımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a10d-134">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="1a10d-135">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="1a10d-135">-WaitForComplete</span></span>
<span data-ttu-id="1a10d-136">Bu cmdlet 'in kopyanın bitmesini beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a10d-136">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="1a10d-137">Bu parametreyi belirtmezseniz, bu cmdlet hemen bir sonuç döndürür.</span><span class="sxs-lookup"><span data-stu-id="1a10d-137">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="1a10d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a10d-138">CommonParameters</span></span>
<span data-ttu-id="1a10d-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a10d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a10d-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a10d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a10d-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a10d-141">INPUTS</span></span>

## <span data-ttu-id="1a10d-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a10d-142">OUTPUTS</span></span>

## <span data-ttu-id="1a10d-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a10d-143">NOTES</span></span>

## <span data-ttu-id="1a10d-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a10d-144">RELATED LINKS</span></span>

[<span data-ttu-id="1a10d-145">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="1a10d-145">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="1a10d-146">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1a10d-146">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="1a10d-147">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1a10d-147">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)

[<span data-ttu-id="1a10d-148">Stop-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1a10d-148">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)
