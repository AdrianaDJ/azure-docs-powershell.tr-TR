---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuesastoken
schema: 2.0.0
ms.openlocfilehash: b002f518d63fb3ed4ed34d007f72b57e4db41ae5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939630"
---
# <span data-ttu-id="18f12-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="18f12-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="18f12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18f12-102">SYNOPSIS</span></span>
<span data-ttu-id="18f12-103">Azure depolama sırası için paylaşılan erişim imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="18f12-103">Generates a shared access signature token for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18f12-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18f12-104">SYNTAX</span></span>

### <span data-ttu-id="18f12-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="18f12-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18f12-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="18f12-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18f12-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="18f12-107">DESCRIPTION</span></span>
<span data-ttu-id="18f12-108">**Yeni-AzureStorageQueueSASToken** cmdlet 'i Azure depolama sırası için paylaşılan erişim imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="18f12-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="18f12-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18f12-109">EXAMPLES</span></span>

### <span data-ttu-id="18f12-110">Örnek 1: tam izinle bir sıra SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="18f12-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="18f12-111">Bu örnek tam izni olan bir sıra SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="18f12-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="18f12-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18f12-112">PARAMETERS</span></span>

### <span data-ttu-id="18f12-113">-Context</span><span class="sxs-lookup"><span data-stu-id="18f12-113">-Context</span></span>
<span data-ttu-id="18f12-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f12-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="18f12-115">Bunu New-AzureStorageContext cmdlet ile oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18f12-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="18f12-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18f12-116">-DefaultProfile</span></span>
<span data-ttu-id="18f12-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="18f12-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18f12-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="18f12-118">-ExpiryTime</span></span>
<span data-ttu-id="18f12-119">Paylaşılan erişim imzasının artık geçerli olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f12-119">Specifies when the shared access signature is no longer valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f12-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="18f12-120">-FullUri</span></span>
<span data-ttu-id="18f12-121">Bu cmdlet 'in tam blob URI 'sini ve paylaşılan erişim imza belirtecini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f12-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f12-122">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="18f12-122">-IPAddressOrRange</span></span>
<span data-ttu-id="18f12-123">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f12-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="18f12-124">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="18f12-124">The range is inclusive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f12-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="18f12-125">-Name</span></span>
<span data-ttu-id="18f12-126">Bir Azure depolama sırası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f12-126">Specifies an Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18f12-127">-İzin</span><span class="sxs-lookup"><span data-stu-id="18f12-127">-Permission</span></span>
<span data-ttu-id="18f12-128">Depolama sırasının izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f12-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="18f12-129">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="18f12-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f12-130">-İlke</span><span class="sxs-lookup"><span data-stu-id="18f12-130">-Policy</span></span>
<span data-ttu-id="18f12-131">Azure saklı bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f12-131">Specifies an Azure stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f12-132">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="18f12-132">-Protocol</span></span>
<span data-ttu-id="18f12-133">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f12-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="18f12-134">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="18f12-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="18f12-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="18f12-135">HttpsOnly</span></span>
* <span data-ttu-id="18f12-136">HttpsOrHttp varsayılan değer HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="18f12-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f12-137">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="18f12-137">-StartTime</span></span>
<span data-ttu-id="18f12-138">Paylaşılan erişim imzasının ne zaman geçerli olacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18f12-138">Specifies when the shared access signature becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f12-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18f12-139">CommonParameters</span></span>
<span data-ttu-id="18f12-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18f12-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18f12-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18f12-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18f12-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18f12-142">INPUTS</span></span>

### <span data-ttu-id="18f12-143">System. String</span><span class="sxs-lookup"><span data-stu-id="18f12-143">System.String</span></span>

### <span data-ttu-id="18f12-144">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="18f12-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="18f12-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18f12-145">OUTPUTS</span></span>

### <span data-ttu-id="18f12-146">System. String</span><span class="sxs-lookup"><span data-stu-id="18f12-146">System.String</span></span>

## <span data-ttu-id="18f12-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18f12-147">NOTES</span></span>

## <span data-ttu-id="18f12-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18f12-148">RELATED LINKS</span></span>
