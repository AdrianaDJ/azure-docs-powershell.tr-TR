---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShare.md
ms.openlocfilehash: b332ed4ec47e5baaa07f579e6ccdbc867b64608e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591507"
---
# <span data-ttu-id="70bac-101">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="70bac-101">New-AzureStorageShare</span></span>

## <span data-ttu-id="70bac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70bac-102">SYNOPSIS</span></span>
<span data-ttu-id="70bac-103">Dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70bac-103">Creates a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70bac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70bac-104">SYNTAX</span></span>

```
New-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="70bac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="70bac-105">DESCRIPTION</span></span>
<span data-ttu-id="70bac-106">**New-Azurestoragesshare** cmdlet 'i bir dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70bac-106">The **New-AzureStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="70bac-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70bac-107">EXAMPLES</span></span>

### <span data-ttu-id="70bac-108">Örnek 1: dosya paylaşımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="70bac-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="70bac-109">Bu komut, ContosoShare06 adlı bir dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70bac-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="70bac-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70bac-110">PARAMETERS</span></span>

### <span data-ttu-id="70bac-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="70bac-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="70bac-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="70bac-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="70bac-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="70bac-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="70bac-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="70bac-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="70bac-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="70bac-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="70bac-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="70bac-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="70bac-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="70bac-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="70bac-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="70bac-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="70bac-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="70bac-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="70bac-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="70bac-120">The default value is 10.</span></span>

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

### <span data-ttu-id="70bac-121">-Context</span><span class="sxs-lookup"><span data-stu-id="70bac-121">-Context</span></span>
<span data-ttu-id="70bac-122">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="70bac-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="70bac-123">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="70bac-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="70bac-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70bac-124">-DefaultProfile</span></span>
<span data-ttu-id="70bac-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="70bac-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70bac-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="70bac-126">-Name</span></span>
<span data-ttu-id="70bac-127">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="70bac-127">Specifies the name of a file share.</span></span>
<span data-ttu-id="70bac-128">Bu cmdlet, bu parametrenin belirttiği adı içeren bir dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70bac-128">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

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

### <span data-ttu-id="70bac-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="70bac-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="70bac-130">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="70bac-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="70bac-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70bac-131">CommonParameters</span></span>
<span data-ttu-id="70bac-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70bac-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70bac-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70bac-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70bac-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70bac-134">INPUTS</span></span>

### <span data-ttu-id="70bac-135">System. String</span><span class="sxs-lookup"><span data-stu-id="70bac-135">System.String</span></span>

### <span data-ttu-id="70bac-136">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="70bac-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="70bac-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70bac-137">OUTPUTS</span></span>

### <span data-ttu-id="70bac-138">Microsoft. Windowsazde. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="70bac-138">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="70bac-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70bac-139">NOTES</span></span>

## <span data-ttu-id="70bac-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70bac-140">RELATED LINKS</span></span>

[<span data-ttu-id="70bac-141">Get-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="70bac-141">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="70bac-142">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="70bac-142">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="70bac-143">Remove-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="70bac-143">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
