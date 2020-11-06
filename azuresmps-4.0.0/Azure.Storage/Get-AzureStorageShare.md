---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e816d29784ea8b2e69ba4b36162938f7a82007d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572349"
---
# <span data-ttu-id="4c963-101">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="4c963-101">Get-AzureStorageShare</span></span>

## <span data-ttu-id="4c963-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c963-102">SYNOPSIS</span></span>
<span data-ttu-id="4c963-103">Dosya paylaşımlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="4c963-103">Gets a list of file shares.</span></span>

## <span data-ttu-id="4c963-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c963-104">SYNTAX</span></span>

### <span data-ttu-id="4c963-105">MatchingPrefix (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4c963-105">MatchingPrefix (Default)</span></span>
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4c963-106">Belli</span><span class="sxs-lookup"><span data-stu-id="4c963-106">Specific</span></span>
```
Get-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4c963-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c963-107">DESCRIPTION</span></span>
<span data-ttu-id="4c963-108">**Get-Azurestoragesshares** cmdlet 'i depolama hesabı için dosya paylaşımlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="4c963-108">The **Get-AzureStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="4c963-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c963-109">EXAMPLES</span></span>

### <span data-ttu-id="4c963-110">Örnek 1: dosya paylaşımı alma</span><span class="sxs-lookup"><span data-stu-id="4c963-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="4c963-111">Bu komut, ContosoShare06 adındaki dosya paylaşımını alır.</span><span class="sxs-lookup"><span data-stu-id="4c963-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="4c963-112">Örnek 2: dizeyle başlayan tüm dosya paylaşımlarını alma</span><span class="sxs-lookup"><span data-stu-id="4c963-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

<span data-ttu-id="4c963-113">Bu komut, contoso ile başlayan tüm dosya paylaşımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="4c963-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="4c963-114">Örnek 3: belirtilen bağlamdaki tüm dosya paylaşımlarını alma</span><span class="sxs-lookup"><span data-stu-id="4c963-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

<span data-ttu-id="4c963-115">İlk komut, *Yerel* parametreyi kullanarak bağlam oluşturmak için **New-AzureStorageContext** cmdlet 'ini kullanır ve sonra bu bağlam nesnesini $Context değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4c963-115">The first command uses the **New-AzureStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>

<span data-ttu-id="4c963-116">İkinci komut, $Context depolanan bağlam nesnesinin dosya paylaşımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="4c963-116">The second command gets the file shares for the context object stored in $Context.</span></span>

## <span data-ttu-id="4c963-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c963-117">PARAMETERS</span></span>

### <span data-ttu-id="4c963-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4c963-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4c963-119">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c963-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4c963-120">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="4c963-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4c963-121">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="4c963-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4c963-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4c963-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4c963-123">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c963-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4c963-124">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c963-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4c963-125">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="4c963-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4c963-126">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="4c963-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4c963-127">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="4c963-127">The default value is 10.</span></span>

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

### <span data-ttu-id="4c963-128">-Context</span><span class="sxs-lookup"><span data-stu-id="4c963-128">-Context</span></span>
<span data-ttu-id="4c963-129">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c963-129">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="4c963-130">Bağlam almak için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4c963-130">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c963-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="4c963-131">-Name</span></span>
<span data-ttu-id="4c963-132">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c963-132">Specifies the name of the file share.</span></span>
<span data-ttu-id="4c963-133">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımını alır veya varolmayan bir dosya paylaşımının adını belirtmezseniz hiçbir şey yapmaz.</span><span class="sxs-lookup"><span data-stu-id="4c963-133">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: String
Parameter Sets: Specific
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c963-134">-Önek</span><span class="sxs-lookup"><span data-stu-id="4c963-134">-Prefix</span></span>
<span data-ttu-id="4c963-135">Dosya paylaşımlarının önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c963-135">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="4c963-136">Bu cmdlet, bu parametrenin belirttiği önekle eşleşen dosya paylaşımlarını alır veya belirtilen önekle eşleşen dosya paylaşımı yoksa dosya paylaşımı içermez.</span><span class="sxs-lookup"><span data-stu-id="4c963-136">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: String
Parameter Sets: MatchingPrefix
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c963-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4c963-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4c963-138">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c963-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4c963-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c963-139">CommonParameters</span></span>
<span data-ttu-id="4c963-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c963-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c963-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c963-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c963-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c963-142">INPUTS</span></span>

## <span data-ttu-id="4c963-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c963-143">OUTPUTS</span></span>

## <span data-ttu-id="4c963-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c963-144">NOTES</span></span>

## <span data-ttu-id="4c963-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c963-145">RELATED LINKS</span></span>

[<span data-ttu-id="4c963-146">New-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="4c963-146">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)

[<span data-ttu-id="4c963-147">Remove-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="4c963-147">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
