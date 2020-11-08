---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
ms.openlocfilehash: d25ebb69521ea1e16dc5ff5103ea64819202e2d1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097757"
---
# <span data-ttu-id="f6298-101">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="f6298-101">Get-AzStorageShare</span></span>

## <span data-ttu-id="f6298-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6298-102">SYNOPSIS</span></span>
<span data-ttu-id="f6298-103">Dosya paylaşımlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="f6298-103">Gets a list of file shares.</span></span>

## <span data-ttu-id="f6298-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6298-104">SYNTAX</span></span>

### <span data-ttu-id="f6298-105">MatchingPrefix (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f6298-105">MatchingPrefix (Default)</span></span>
```
Get-AzStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6298-106">Belli</span><span class="sxs-lookup"><span data-stu-id="f6298-106">Specific</span></span>
```
Get-AzStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="f6298-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6298-107">DESCRIPTION</span></span>
<span data-ttu-id="f6298-108">**Get-Azstoragesshares** cmdlet 'i depolama hesabı için dosya paylaşımlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="f6298-108">The **Get-AzStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="f6298-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6298-109">EXAMPLES</span></span>

### <span data-ttu-id="f6298-110">Örnek 1: dosya paylaşımı alma</span><span class="sxs-lookup"><span data-stu-id="f6298-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="f6298-111">Bu komut, ContosoShare06 adındaki dosya paylaşımını alır.</span><span class="sxs-lookup"><span data-stu-id="f6298-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="f6298-112">Örnek 2: dizeyle başlayan tüm dosya paylaşımlarını alma</span><span class="sxs-lookup"><span data-stu-id="f6298-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "Contoso"
```

<span data-ttu-id="f6298-113">Bu komut, contoso ile başlayan tüm dosya paylaşımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="f6298-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="f6298-114">Örnek 3: belirtilen bağlamdaki tüm dosya paylaşımlarını alma</span><span class="sxs-lookup"><span data-stu-id="f6298-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzStorageContext -Local
PS C:\> Get-AzStorageShare -Context $Context
```

<span data-ttu-id="f6298-115">İlk komut, *Yerel* parametreyi kullanarak bağlam oluşturmak için **New-azstoragecontext** cmdlet 'ini kullanır ve sonra bu bağlam nesnesini $Context değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f6298-115">The first command uses the **New-AzStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>
<span data-ttu-id="f6298-116">İkinci komut, $Context depolanan bağlam nesnesinin dosya paylaşımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="f6298-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="f6298-117">Örnek 4: belirli bir paylaşım adı ve SnapshotTime ile dosya paylaşımı anlık görüntüsü alma</span><span class="sxs-lookup"><span data-stu-id="f6298-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="f6298-118">Bu komut, belirli bir paylaşım adı ve SnapshotTime ile dosya paylaşımı anlık görüntüsünü alır.</span><span class="sxs-lookup"><span data-stu-id="f6298-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="f6298-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6298-119">PARAMETERS</span></span>

### <span data-ttu-id="f6298-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f6298-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f6298-121">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6298-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f6298-122">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="f6298-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f6298-123">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="f6298-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f6298-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f6298-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f6298-125">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6298-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f6298-126">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f6298-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f6298-127">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="f6298-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f6298-128">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="f6298-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f6298-129">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="f6298-129">The default value is 10.</span></span>

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

### <span data-ttu-id="f6298-130">-Context</span><span class="sxs-lookup"><span data-stu-id="f6298-130">-Context</span></span>
<span data-ttu-id="f6298-131">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6298-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="f6298-132">Bağlam almak için, [New-AzStorageContext](./New-AzStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f6298-132">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6298-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6298-133">-DefaultProfile</span></span>
<span data-ttu-id="f6298-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f6298-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6298-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="f6298-135">-Name</span></span>
<span data-ttu-id="f6298-136">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6298-136">Specifies the name of the file share.</span></span>
<span data-ttu-id="f6298-137">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımını alır veya varolmayan bir dosya paylaşımının adını belirtmezseniz hiçbir şey yapmaz.</span><span class="sxs-lookup"><span data-stu-id="f6298-137">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6298-138">-Önek</span><span class="sxs-lookup"><span data-stu-id="f6298-138">-Prefix</span></span>
<span data-ttu-id="f6298-139">Dosya paylaşımlarının önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6298-139">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="f6298-140">Bu cmdlet, bu parametrenin belirttiği önekle eşleşen dosya paylaşımlarını alır veya belirtilen önekle eşleşen dosya paylaşımı yoksa dosya paylaşımı içermez.</span><span class="sxs-lookup"><span data-stu-id="f6298-140">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: MatchingPrefix
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6298-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f6298-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f6298-142">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6298-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f6298-143">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="f6298-143">-SnapshotTime</span></span>
<span data-ttu-id="f6298-144">Dosya paylaşımı anlık görüntüsünün alınabilmesi için Snapshotsaati.</span><span class="sxs-lookup"><span data-stu-id="f6298-144">SnapshotTime of the file share snapshot to be received.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: Specific
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6298-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6298-145">CommonParameters</span></span>
<span data-ttu-id="f6298-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6298-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6298-147">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6298-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6298-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6298-148">INPUTS</span></span>

### <span data-ttu-id="f6298-149">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="f6298-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f6298-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6298-150">OUTPUTS</span></span>

### <span data-ttu-id="f6298-151">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="f6298-151">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="f6298-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6298-152">NOTES</span></span>

## <span data-ttu-id="f6298-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6298-153">RELATED LINKS</span></span>

[<span data-ttu-id="f6298-154">Yeni-Azstoragesbir</span><span class="sxs-lookup"><span data-stu-id="f6298-154">New-AzStorageShare</span></span>](./New-AzStorageShare.md)

[<span data-ttu-id="f6298-155">Remove-Azstoragesbir</span><span class="sxs-lookup"><span data-stu-id="f6298-155">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)