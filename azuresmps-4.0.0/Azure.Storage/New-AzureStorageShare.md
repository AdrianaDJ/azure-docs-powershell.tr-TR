---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: ''
schema: 2.0.0
ms.openlocfilehash: 381bfc62ed3a80b650b61b11790a87658a75ee9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571914"
---
# <span data-ttu-id="98111-101">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="98111-101">New-AzureStorageShare</span></span>

## <span data-ttu-id="98111-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98111-102">SYNOPSIS</span></span>
<span data-ttu-id="98111-103">Dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98111-103">Creates a file share.</span></span>

## <span data-ttu-id="98111-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98111-104">SYNTAX</span></span>

```
New-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="98111-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="98111-105">DESCRIPTION</span></span>
<span data-ttu-id="98111-106">**New-Azurestoragesshare** cmdlet 'i bir dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98111-106">The **New-AzureStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="98111-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98111-107">EXAMPLES</span></span>

### <span data-ttu-id="98111-108">Örnek 1: dosya paylaşımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="98111-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="98111-109">Bu komut, ContosoShare06 adlı bir dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98111-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="98111-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98111-110">PARAMETERS</span></span>

### <span data-ttu-id="98111-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="98111-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="98111-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="98111-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="98111-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="98111-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="98111-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="98111-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="98111-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="98111-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="98111-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="98111-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="98111-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="98111-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="98111-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="98111-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="98111-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="98111-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="98111-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="98111-120">The default value is 10.</span></span>

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

### <span data-ttu-id="98111-121">-Context</span><span class="sxs-lookup"><span data-stu-id="98111-121">-Context</span></span>
<span data-ttu-id="98111-122">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="98111-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="98111-123">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="98111-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="98111-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="98111-124">-Name</span></span>
<span data-ttu-id="98111-125">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="98111-125">Specifies the name of a file share.</span></span>
<span data-ttu-id="98111-126">Bu cmdlet, bu parametrenin belirttiği adı içeren bir dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98111-126">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98111-127">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="98111-127">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="98111-128">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="98111-128">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="98111-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98111-129">CommonParameters</span></span>
<span data-ttu-id="98111-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98111-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98111-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98111-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98111-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98111-132">INPUTS</span></span>

## <span data-ttu-id="98111-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98111-133">OUTPUTS</span></span>

## <span data-ttu-id="98111-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98111-134">NOTES</span></span>

## <span data-ttu-id="98111-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98111-135">RELATED LINKS</span></span>

[<span data-ttu-id="98111-136">Get-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="98111-136">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="98111-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="98111-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="98111-138">Remove-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="98111-138">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
