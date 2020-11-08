---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
ms.openlocfilehash: 4c3715a3c6228e45bfa52fd9a222be2cae84ef01
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936217"
---
# <span data-ttu-id="4c4bd-101">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="4c4bd-101">New-AzStorageQueueSASToken</span></span>

## <span data-ttu-id="4c4bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c4bd-102">SYNOPSIS</span></span>
<span data-ttu-id="4c4bd-103">Azure depolama sırası için paylaşılan erişim imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4c4bd-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="4c4bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c4bd-104">SYNTAX</span></span>

### <span data-ttu-id="4c4bd-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="4c4bd-105">SasPolicy</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c4bd-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="4c4bd-106">SasPermission</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c4bd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c4bd-107">DESCRIPTION</span></span>
<span data-ttu-id="4c4bd-108">**Yeni-AzStorageQueueSASToken** cmdlet 'i Azure depolama sırası için paylaşılan erişim imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4c4bd-108">The **New-AzStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="4c4bd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c4bd-109">EXAMPLES</span></span>

### <span data-ttu-id="4c4bd-110">Örnek 1: tam izinle bir sıra SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="4c4bd-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="4c4bd-111">Bu örnek tam izni olan bir sıra SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4c4bd-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="4c4bd-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c4bd-112">PARAMETERS</span></span>

### <span data-ttu-id="4c4bd-113">-Context</span><span class="sxs-lookup"><span data-stu-id="4c4bd-113">-Context</span></span>
<span data-ttu-id="4c4bd-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c4bd-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="4c4bd-115">Bunu New-AzStorageContext cmdlet ile oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c4bd-115">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4c4bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c4bd-116">-DefaultProfile</span></span>
<span data-ttu-id="4c4bd-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c4bd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c4bd-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4c4bd-118">-ExpiryTime</span></span>
<span data-ttu-id="4c4bd-119">Paylaşılan erişim imzasının artık geçerli olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c4bd-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="4c4bd-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="4c4bd-120">-FullUri</span></span>
<span data-ttu-id="4c4bd-121">Bu cmdlet 'in tam blob URI 'sini ve paylaşılan erişim imza belirtecini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c4bd-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="4c4bd-122">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="4c4bd-122">-IPAddressOrRange</span></span>
<span data-ttu-id="4c4bd-123">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c4bd-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="4c4bd-124">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="4c4bd-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="4c4bd-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="4c4bd-125">-Name</span></span>
<span data-ttu-id="4c4bd-126">Bir Azure depolama sırası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c4bd-126">Specifies an Azure storage queue name.</span></span>

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

### <span data-ttu-id="4c4bd-127">-İzin</span><span class="sxs-lookup"><span data-stu-id="4c4bd-127">-Permission</span></span>
<span data-ttu-id="4c4bd-128">Depolama sırasının izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c4bd-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="4c4bd-129">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="4c4bd-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="4c4bd-130">-İlke</span><span class="sxs-lookup"><span data-stu-id="4c4bd-130">-Policy</span></span>
<span data-ttu-id="4c4bd-131">Azure saklı bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c4bd-131">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="4c4bd-132">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="4c4bd-132">-Protocol</span></span>
<span data-ttu-id="4c4bd-133">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c4bd-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="4c4bd-134">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4c4bd-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="4c4bd-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="4c4bd-135">HttpsOnly</span></span>
* <span data-ttu-id="4c4bd-136">HttpsOrHttp varsayılan değer HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="4c4bd-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAz.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c4bd-137">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="4c4bd-137">-StartTime</span></span>
<span data-ttu-id="4c4bd-138">Paylaşılan erişim imzasının ne zaman geçerli olacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c4bd-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="4c4bd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c4bd-139">CommonParameters</span></span>
<span data-ttu-id="4c4bd-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c4bd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c4bd-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c4bd-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c4bd-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c4bd-142">INPUTS</span></span>

### <span data-ttu-id="4c4bd-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4c4bd-143">System.String</span></span>

### <span data-ttu-id="4c4bd-144">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="4c4bd-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4c4bd-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c4bd-145">OUTPUTS</span></span>

### <span data-ttu-id="4c4bd-146">System. String</span><span class="sxs-lookup"><span data-stu-id="4c4bd-146">System.String</span></span>

## <span data-ttu-id="4c4bd-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c4bd-147">NOTES</span></span>

## <span data-ttu-id="4c4bd-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c4bd-148">RELATED LINKS</span></span>