---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
ms.openlocfilehash: 399df44123766e27c3d0b892ce1ca7b04b27e688
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098937"
---
# <span data-ttu-id="c0915-101">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="c0915-101">New-AzStorageShare</span></span>

## <span data-ttu-id="c0915-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0915-102">SYNOPSIS</span></span>
<span data-ttu-id="c0915-103">Dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c0915-103">Creates a file share.</span></span>

## <span data-ttu-id="c0915-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0915-104">SYNTAX</span></span>

```
New-AzStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0915-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0915-105">DESCRIPTION</span></span>
<span data-ttu-id="c0915-106">**Yeni-Azstoragesshare** cmdlet 'i dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c0915-106">The **New-AzStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="c0915-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0915-107">EXAMPLES</span></span>

### <span data-ttu-id="c0915-108">Örnek 1: dosya paylaşımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="c0915-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="c0915-109">Bu komut, ContosoShare06 adlı bir dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c0915-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="c0915-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0915-110">PARAMETERS</span></span>

### <span data-ttu-id="c0915-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c0915-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c0915-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0915-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c0915-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="c0915-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c0915-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="c0915-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c0915-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c0915-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c0915-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0915-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c0915-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0915-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c0915-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="c0915-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c0915-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="c0915-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c0915-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="c0915-120">The default value is 10.</span></span>

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

### <span data-ttu-id="c0915-121">-Context</span><span class="sxs-lookup"><span data-stu-id="c0915-121">-Context</span></span>
<span data-ttu-id="c0915-122">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0915-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c0915-123">Depolama bağlamı edinmek için, [New-AzStorageContext](./New-AzStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c0915-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="c0915-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0915-124">-DefaultProfile</span></span>
<span data-ttu-id="c0915-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c0915-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0915-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="c0915-126">-Name</span></span>
<span data-ttu-id="c0915-127">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0915-127">Specifies the name of a file share.</span></span>
<span data-ttu-id="c0915-128">Bu cmdlet, bu parametrenin belirttiği adı içeren bir dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c0915-128">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0915-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c0915-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c0915-130">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0915-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c0915-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0915-131">CommonParameters</span></span>
<span data-ttu-id="c0915-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0915-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0915-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0915-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0915-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0915-134">INPUTS</span></span>

### <span data-ttu-id="c0915-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c0915-135">System.String</span></span>

### <span data-ttu-id="c0915-136">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="c0915-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c0915-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0915-137">OUTPUTS</span></span>

### <span data-ttu-id="c0915-138">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="c0915-138">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="c0915-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0915-139">NOTES</span></span>

## <span data-ttu-id="c0915-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0915-140">RELATED LINKS</span></span>

[<span data-ttu-id="c0915-141">Get-Azstorages,</span><span class="sxs-lookup"><span data-stu-id="c0915-141">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="c0915-142">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c0915-142">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="c0915-143">Remove-Azstoragesbir</span><span class="sxs-lookup"><span data-stu-id="c0915-143">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
