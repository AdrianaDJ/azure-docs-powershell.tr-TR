---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShare.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: a1be5816427ac1aa91b9daa98701abaec044c20f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595052"
---
# <span data-ttu-id="4797f-101">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="4797f-101">New-AzureStorageShare</span></span>

## <span data-ttu-id="4797f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4797f-102">SYNOPSIS</span></span>
<span data-ttu-id="4797f-103">Dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4797f-103">Creates a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4797f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4797f-104">SYNTAX</span></span>

```
New-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4797f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4797f-105">DESCRIPTION</span></span>
<span data-ttu-id="4797f-106">**New-Azurestoragesshare** cmdlet 'i bir dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4797f-106">The **New-AzureStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="4797f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4797f-107">EXAMPLES</span></span>

### <span data-ttu-id="4797f-108">Örnek 1: dosya paylaşımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="4797f-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="4797f-109">Bu komut, ContosoShare06 adlı bir dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4797f-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="4797f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4797f-110">PARAMETERS</span></span>

### <span data-ttu-id="4797f-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4797f-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4797f-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="4797f-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4797f-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="4797f-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4797f-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="4797f-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4797f-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4797f-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4797f-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4797f-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4797f-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4797f-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4797f-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="4797f-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4797f-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="4797f-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4797f-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="4797f-120">The default value is 10.</span></span>

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

### <span data-ttu-id="4797f-121">-Context</span><span class="sxs-lookup"><span data-stu-id="4797f-121">-Context</span></span>
<span data-ttu-id="4797f-122">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4797f-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4797f-123">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4797f-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4797f-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="4797f-124">-Name</span></span>
<span data-ttu-id="4797f-125">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4797f-125">Specifies the name of a file share.</span></span>
<span data-ttu-id="4797f-126">Bu cmdlet, bu parametrenin belirttiği adı içeren bir dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4797f-126">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

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

### <span data-ttu-id="4797f-127">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4797f-127">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4797f-128">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4797f-128">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4797f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4797f-129">CommonParameters</span></span>
<span data-ttu-id="4797f-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4797f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4797f-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4797f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4797f-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4797f-132">INPUTS</span></span>

### <span data-ttu-id="4797f-133">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="4797f-133">IStorageContext</span></span>

<span data-ttu-id="4797f-134">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4797f-134">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="4797f-135">Dizisi</span><span class="sxs-lookup"><span data-stu-id="4797f-135">String</span></span>

<span data-ttu-id="4797f-136">' Name ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4797f-136">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="4797f-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4797f-137">OUTPUTS</span></span>

## <span data-ttu-id="4797f-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4797f-138">NOTES</span></span>

## <span data-ttu-id="4797f-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4797f-139">RELATED LINKS</span></span>

[<span data-ttu-id="4797f-140">Get-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="4797f-140">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="4797f-141">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="4797f-141">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="4797f-142">Remove-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="4797f-142">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
