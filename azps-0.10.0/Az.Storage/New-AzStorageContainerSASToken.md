---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: d09fbb09170aa78579f05fb28d544bb29f98fcc8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936228"
---
# <span data-ttu-id="c732f-101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="c732f-101">New-AzStorageContainerSASToken</span></span>

## <span data-ttu-id="c732f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c732f-102">SYNOPSIS</span></span>
<span data-ttu-id="c732f-103">Bir Azure depolama kapsayıcısı için SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c732f-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="c732f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c732f-104">SYNTAX</span></span>

### <span data-ttu-id="c732f-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="c732f-105">SasPolicy</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c732f-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="c732f-106">SasPermission</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c732f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c732f-107">DESCRIPTION</span></span>
<span data-ttu-id="c732f-108">**Yeni-AzStorageContainerSASToken** cmdlet 'i, bir Azure depolama kapsayıcısı Için paylaşılan erişim IMZASı (SAS) belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c732f-108">The **New-AzStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="c732f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c732f-109">EXAMPLES</span></span>

### <span data-ttu-id="c732f-110">Örnek 1: tam kapsayıcı izniyle kapsayıcı SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="c732f-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="c732f-111">Bu örnek, tam kapsayıcı izni olan bir kapsayıcı SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c732f-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="c732f-112">Örnek 2: ardışık düzene göre birden çok kapsayıcı SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="c732f-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="c732f-113">Bu örnek ardışık düzeni kullanarak birden çok kapsayıcı SAS belirteçleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c732f-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="c732f-114">Örnek 3: paylaşılan erişim ilkesiyle kapsayıcı SAS belirteci oluştur</span><span class="sxs-lookup"><span data-stu-id="c732f-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="c732f-115">Bu örnek, paylaşılan erişim ilkesiyle kapsayıcı SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c732f-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="c732f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c732f-116">PARAMETERS</span></span>

### <span data-ttu-id="c732f-117">-Context</span><span class="sxs-lookup"><span data-stu-id="c732f-117">-Context</span></span>
<span data-ttu-id="c732f-118">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c732f-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c732f-119">Bunu, New-AzStorageContext cmdlet 'ini kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c732f-119">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c732f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c732f-120">-DefaultProfile</span></span>
<span data-ttu-id="c732f-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c732f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c732f-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c732f-122">-ExpiryTime</span></span>
<span data-ttu-id="c732f-123">Paylaşılan erişim imzasının geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="c732f-123">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="c732f-124">Kullanıcı başlangıç saatini ayarlasa da süre sonu zamanını geçmişse, sona erme saati başlangıç saati artı bir saat ile ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="c732f-124">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="c732f-125">Başlangıç saati veya son kullanma tarihi belirtilmemişse, sona erme süresi geçerli saate bir saat eklenerek bir saat eklenerek ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="c732f-125">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="c732f-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="c732f-126">-FullUri</span></span>
<span data-ttu-id="c732f-127">Bu cmdlet 'in tam blob URI 'sini ve paylaşılan erişim imza belirtecini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c732f-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="c732f-128">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="c732f-128">-IPAddressOrRange</span></span>
<span data-ttu-id="c732f-129">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c732f-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="c732f-130">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="c732f-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="c732f-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="c732f-131">-Name</span></span>
<span data-ttu-id="c732f-132">Azure depolama kapsayıcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c732f-132">Specifies an Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c732f-133">-İzin</span><span class="sxs-lookup"><span data-stu-id="c732f-133">-Permission</span></span>
<span data-ttu-id="c732f-134">Bir depolama kapsayıcısının izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c732f-134">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="c732f-135">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="c732f-135">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="c732f-136">-İlke</span><span class="sxs-lookup"><span data-stu-id="c732f-136">-Policy</span></span>
<span data-ttu-id="c732f-137">Azure saklı bir erişim Ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c732f-137">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="c732f-138">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="c732f-138">-Protocol</span></span>
<span data-ttu-id="c732f-139">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c732f-139">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="c732f-140">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c732f-140">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="c732f-141">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c732f-141">HttpsOnly</span></span>
* <span data-ttu-id="c732f-142">HttpsOrHttp varsayılan değer HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="c732f-142">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="c732f-143">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="c732f-143">-StartTime</span></span>
<span data-ttu-id="c732f-144">Paylaşılan erişim imzasının geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="c732f-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="c732f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c732f-145">CommonParameters</span></span>
<span data-ttu-id="c732f-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c732f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c732f-147">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c732f-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c732f-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c732f-148">INPUTS</span></span>

### <span data-ttu-id="c732f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="c732f-149">System.String</span></span>

### <span data-ttu-id="c732f-150">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="c732f-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c732f-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c732f-151">OUTPUTS</span></span>

### <span data-ttu-id="c732f-152">System. String</span><span class="sxs-lookup"><span data-stu-id="c732f-152">System.String</span></span>

## <span data-ttu-id="c732f-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c732f-153">NOTES</span></span>

## <span data-ttu-id="c732f-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c732f-154">RELATED LINKS</span></span>

[<span data-ttu-id="c732f-155">Yeni-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="c732f-155">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)
