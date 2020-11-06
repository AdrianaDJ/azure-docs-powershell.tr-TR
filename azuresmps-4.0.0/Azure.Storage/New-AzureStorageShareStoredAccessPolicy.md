---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: ''
schema: 2.0.0
ms.openlocfilehash: f76cd56055e800dc5d7d5ac15e66be23621ffbe2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571673"
---
# <span data-ttu-id="ea527-101">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ea527-101">New-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="ea527-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea527-102">SYNOPSIS</span></span>
<span data-ttu-id="ea527-103">Depolama paylaşımında depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea527-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="ea527-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea527-104">SYNTAX</span></span>

```
New-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea527-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea527-105">DESCRIPTION</span></span>
<span data-ttu-id="ea527-106">**New-AzureStorageShareStoredAccessPolicy** cmdlet 'ı Azure depolama paylaşımında depolanan bir Access ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea527-106">The **New-AzureStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="ea527-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea527-107">EXAMPLES</span></span>

### <span data-ttu-id="ea527-108">Örnek 1: paylaşımda depolanan bir Access ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="ea527-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="ea527-109">Bu komut, paylaşımda tam izni olan bir depolanmış erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea527-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="ea527-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea527-110">PARAMETERS</span></span>

### <span data-ttu-id="ea527-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ea527-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ea527-112">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea527-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ea527-113">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="ea527-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ea527-114">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="ea527-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ea527-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ea527-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ea527-116">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea527-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ea527-117">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea527-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ea527-118">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="ea527-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ea527-119">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="ea527-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ea527-120">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="ea527-120">The default value is 10.</span></span>

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

### <span data-ttu-id="ea527-121">-Context</span><span class="sxs-lookup"><span data-stu-id="ea527-121">-Context</span></span>
<span data-ttu-id="ea527-122">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea527-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ea527-123">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ea527-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="ea527-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ea527-124">-ExpiryTime</span></span>
<span data-ttu-id="ea527-125">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea527-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea527-126">-İzin</span><span class="sxs-lookup"><span data-stu-id="ea527-126">-Permission</span></span>
<span data-ttu-id="ea527-127">Depolanan erişim ilkesindeki depolama paylaşımına veya bu dosyaların altındaki dosyalara erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea527-127">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea527-128">-İlke</span><span class="sxs-lookup"><span data-stu-id="ea527-128">-Policy</span></span>
<span data-ttu-id="ea527-129">Depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea527-129">Specifies a name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea527-130">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ea527-130">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ea527-131">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea527-131">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="ea527-132">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="ea527-132">-ShareName</span></span>
<span data-ttu-id="ea527-133">Depolama paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea527-133">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea527-134">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="ea527-134">-StartTime</span></span>
<span data-ttu-id="ea527-135">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea527-135">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea527-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea527-136">CommonParameters</span></span>
<span data-ttu-id="ea527-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea527-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea527-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea527-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea527-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea527-139">INPUTS</span></span>

## <span data-ttu-id="ea527-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea527-140">OUTPUTS</span></span>

## <span data-ttu-id="ea527-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea527-141">NOTES</span></span>

## <span data-ttu-id="ea527-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea527-142">RELATED LINKS</span></span>

[<span data-ttu-id="ea527-143">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ea527-143">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="ea527-144">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ea527-144">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="ea527-145">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ea527-145">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="ea527-146">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ea527-146">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
