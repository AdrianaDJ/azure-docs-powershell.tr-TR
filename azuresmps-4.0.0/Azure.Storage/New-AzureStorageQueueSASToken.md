---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac818fd403df9b159671f5889e068bda82a086d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572013"
---
# <span data-ttu-id="f6996-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="f6996-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="f6996-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6996-102">SYNOPSIS</span></span>
<span data-ttu-id="f6996-103">Azure depolama sırası için paylaşılan erişim imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f6996-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="f6996-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6996-104">SYNTAX</span></span>

### <span data-ttu-id="f6996-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="f6996-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="f6996-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="f6996-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="f6996-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6996-107">DESCRIPTION</span></span>
<span data-ttu-id="f6996-108">**Yeni-AzureStorageQueueSASToken** cmdlet 'i Azure depolama sırası için paylaşılan erişim imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f6996-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="f6996-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6996-109">EXAMPLES</span></span>

### <span data-ttu-id="f6996-110">Örnek 1: tam izinle bir sıra SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="f6996-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="f6996-111">Bu örnek tam izni olan bir sıra SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f6996-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="f6996-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6996-112">PARAMETERS</span></span>

### <span data-ttu-id="f6996-113">-Context</span><span class="sxs-lookup"><span data-stu-id="f6996-113">-Context</span></span>
<span data-ttu-id="f6996-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6996-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="f6996-115">Bunu New-AzureStorageContext cmdlet ile oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f6996-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f6996-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f6996-116">-ExpiryTime</span></span>
<span data-ttu-id="f6996-117">Paylaşılan erişim imzasının artık geçerli olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6996-117">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="f6996-118">-FullUri</span><span class="sxs-lookup"><span data-stu-id="f6996-118">-FullUri</span></span>
<span data-ttu-id="f6996-119">Bu cmdlet 'in tam blob URI 'sini ve paylaşılan erişim imza belirtecini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6996-119">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="f6996-120">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="f6996-120">-IPAddressOrRange</span></span>
<span data-ttu-id="f6996-121">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6996-121">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="f6996-122">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="f6996-122">The range is inclusive.</span></span>

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

### <span data-ttu-id="f6996-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="f6996-123">-Name</span></span>
<span data-ttu-id="f6996-124">Bir Azure depolama sırası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6996-124">Specifies an Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6996-125">-İzin</span><span class="sxs-lookup"><span data-stu-id="f6996-125">-Permission</span></span>
<span data-ttu-id="f6996-126">Depolama sırasının izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6996-126">Specifies permissions for a storage queue.</span></span>

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6996-127">-İlke</span><span class="sxs-lookup"><span data-stu-id="f6996-127">-Policy</span></span>
<span data-ttu-id="f6996-128">Azure saklı bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6996-128">Specifies an Azure stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6996-129">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="f6996-129">-Protocol</span></span>
<span data-ttu-id="f6996-130">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6996-130">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="f6996-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f6996-131">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="f6996-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="f6996-132">HttpsOnly</span></span>
* <span data-ttu-id="f6996-133">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="f6996-133">HttpsOrHttp</span></span>

<span data-ttu-id="f6996-134">Varsayılan değer HttpsOrHttp değeridir.</span><span class="sxs-lookup"><span data-stu-id="f6996-134">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6996-135">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="f6996-135">-StartTime</span></span>
<span data-ttu-id="f6996-136">Paylaşılan erişim imzasının ne zaman geçerli olacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6996-136">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="f6996-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6996-137">CommonParameters</span></span>
<span data-ttu-id="f6996-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6996-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6996-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6996-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6996-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6996-140">INPUTS</span></span>

## <span data-ttu-id="f6996-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6996-141">OUTPUTS</span></span>

## <span data-ttu-id="f6996-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6996-142">NOTES</span></span>

## <span data-ttu-id="f6996-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6996-143">RELATED LINKS</span></span>

