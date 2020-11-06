---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: ''
schema: 2.0.0
ms.openlocfilehash: becdf63590b5c5abc5e7095b96e13586232311d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572333"
---
# <span data-ttu-id="aa16d-101">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="aa16d-101">New-AzureStorageContainerSASToken</span></span>

## <span data-ttu-id="aa16d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa16d-102">SYNOPSIS</span></span>
<span data-ttu-id="aa16d-103">Bir Azure depolama kapsayıcısı için SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aa16d-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="aa16d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aa16d-104">SYNTAX</span></span>

### <span data-ttu-id="aa16d-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="aa16d-105">SasPolicy</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="aa16d-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="aa16d-106">SasPermission</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="aa16d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="aa16d-107">DESCRIPTION</span></span>
<span data-ttu-id="aa16d-108">**New-AzureStorageContainerSASToken** cmdlet 'i, bir Azure depolama kapsayıcısı Için paylaşılan erişim IMZASı (SAS) belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aa16d-108">The **New-AzureStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="aa16d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aa16d-109">EXAMPLES</span></span>

### <span data-ttu-id="aa16d-110">Örnek 1: tam kapsayıcı izniyle kapsayıcı SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="aa16d-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="aa16d-111">Bu örnek, tam kapsayıcı izni olan bir kapsayıcı SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aa16d-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="aa16d-112">Örnek 2: ardışık düzene göre birden çok kapsayıcı SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="aa16d-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container test* | New-AzureStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="aa16d-113">Bu örnek ardışık düzeni kullanarak birden çok kapsayıcı SAS belirteçleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aa16d-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="aa16d-114">Örnek 3: paylaşılan erişim ilkesiyle kapsayıcı SAS belirteci oluştur</span><span class="sxs-lookup"><span data-stu-id="aa16d-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="aa16d-115">Bu örnek, paylaşılan erişim ilkesiyle kapsayıcı SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aa16d-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="aa16d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aa16d-116">PARAMETERS</span></span>

### <span data-ttu-id="aa16d-117">-Context</span><span class="sxs-lookup"><span data-stu-id="aa16d-117">-Context</span></span>
<span data-ttu-id="aa16d-118">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa16d-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="aa16d-119">Bunu, New-AzureStorageContext cmdlet 'ini kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aa16d-119">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="aa16d-120">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="aa16d-120">-ExpiryTime</span></span>
<span data-ttu-id="aa16d-121">Paylaşılan erişim imzasının geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa16d-121">Specifies the time at which the shared access signature becomes invalid.</span></span>

<span data-ttu-id="aa16d-122">Kullanıcı başlangıç saatini ayarlasa da süre sonu zamanını geçmişse, sona erme saati başlangıç saati artı bir saat ile ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="aa16d-122">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="aa16d-123">Başlangıç saati veya son kullanma tarihi belirtilmemişse, sona erme süresi geçerli saate bir saat eklenerek bir saat eklenerek ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="aa16d-123">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="aa16d-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="aa16d-124">-FullUri</span></span>
<span data-ttu-id="aa16d-125">Bu cmdlet 'in tam blob URI 'sini ve paylaşılan erişim imza belirtecini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa16d-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="aa16d-126">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="aa16d-126">-IPAddressOrRange</span></span>
<span data-ttu-id="aa16d-127">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa16d-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="aa16d-128">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="aa16d-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="aa16d-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="aa16d-129">-Name</span></span>
<span data-ttu-id="aa16d-130">Azure depolama kapsayıcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa16d-130">Specifies an Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa16d-131">-İzin</span><span class="sxs-lookup"><span data-stu-id="aa16d-131">-Permission</span></span>
<span data-ttu-id="aa16d-132">Bir depolama kapsayıcısının izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa16d-132">Specifies permissions for a storage container.</span></span>

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

### <span data-ttu-id="aa16d-133">-İlke</span><span class="sxs-lookup"><span data-stu-id="aa16d-133">-Policy</span></span>
<span data-ttu-id="aa16d-134">Azure saklı bir erişim Ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa16d-134">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="aa16d-135">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="aa16d-135">-Protocol</span></span>
<span data-ttu-id="aa16d-136">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa16d-136">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="aa16d-137">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="aa16d-137">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="aa16d-138">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="aa16d-138">HttpsOnly</span></span>
* <span data-ttu-id="aa16d-139">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="aa16d-139">HttpsOrHttp</span></span>

<span data-ttu-id="aa16d-140">Varsayılan değer HttpsOrHttp değeridir.</span><span class="sxs-lookup"><span data-stu-id="aa16d-140">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="aa16d-141">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="aa16d-141">-StartTime</span></span>
<span data-ttu-id="aa16d-142">Paylaşılan erişim imzasının geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa16d-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="aa16d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa16d-143">CommonParameters</span></span>
<span data-ttu-id="aa16d-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aa16d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa16d-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa16d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa16d-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aa16d-146">INPUTS</span></span>

## <span data-ttu-id="aa16d-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aa16d-147">OUTPUTS</span></span>

## <span data-ttu-id="aa16d-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aa16d-148">NOTES</span></span>

## <span data-ttu-id="aa16d-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aa16d-149">RELATED LINKS</span></span>

[<span data-ttu-id="aa16d-150">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="aa16d-150">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)
