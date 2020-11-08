---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 3c79266c6f6e9b5200e2224f463ac12fe409bf0c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098616"
---
# <span data-ttu-id="9f849-101">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="9f849-101">New-AzStorageAccountSASToken</span></span>

## <span data-ttu-id="9f849-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f849-102">SYNOPSIS</span></span>
<span data-ttu-id="9f849-103">Hesap düzeyi SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9f849-103">Creates an account-level SAS token.</span></span>

## <span data-ttu-id="9f849-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f849-104">SYNTAX</span></span>

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f849-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f849-105">DESCRIPTION</span></span>
<span data-ttu-id="9f849-106">**New-AzStorageSASToken** cmdlet 'ı bir Azure depolama hesabı için hesap düzeyi paylaşılan erişim IMZASı (SAS) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9f849-106">The **New-AzStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="9f849-107">SAS belirtecini birden fazla hizmete yönelik izinler temsilci seçmek veya nesne düzeyinde SAS belirteciyle kullanılamayan hizmetlerin izinlerini temsil etmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9f849-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="9f849-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f849-108">EXAMPLES</span></span>

### <span data-ttu-id="9f849-109">Örnek 1: tam izinli bir hesap düzeyi SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="9f849-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="9f849-110">Bu komut tam izni olan bir hesap düzeyi SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9f849-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="9f849-111">Örnek 2: bir IP adresleri aralığı için hesap düzeyi SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="9f849-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="9f849-112">Bu komut, belirtilen IP adresi aralığından yalnızca HTTPS istekleri için bir hesap düzeyi SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9f849-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="9f849-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f849-113">PARAMETERS</span></span>

### <span data-ttu-id="9f849-114">-Context</span><span class="sxs-lookup"><span data-stu-id="9f849-114">-Context</span></span>
<span data-ttu-id="9f849-115">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f849-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="9f849-116">**Azurestoragecontext** nesnesini almak için New-AzStorageContext cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9f849-116">You can use the New-AzStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="9f849-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f849-117">-DefaultProfile</span></span>
<span data-ttu-id="9f849-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9f849-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f849-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="9f849-119">-ExpiryTime</span></span>
<span data-ttu-id="9f849-120">Paylaşılan erişim imzasının geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f849-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="9f849-121">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="9f849-121">-IPAddressOrRange</span></span>
<span data-ttu-id="9f849-122">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f849-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="9f849-123">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="9f849-123">The range is inclusive.</span></span>

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

### <span data-ttu-id="9f849-124">-İzin</span><span class="sxs-lookup"><span data-stu-id="9f849-124">-Permission</span></span>
<span data-ttu-id="9f849-125">Depolama hesabı izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f849-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="9f849-126">İzinler yalnızca belirtilen kaynak türüyle eşleşirse geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="9f849-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="9f849-127">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="9f849-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="9f849-128">Kabul edilebilir izin değerleri hakkında daha fazla bilgi için bkz: hesap SA 'ları oluşturma http://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="9f849-128">For more information about acceptable permission values, see Constructing an Account SAS http://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="9f849-129">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="9f849-129">-Protocol</span></span>
<span data-ttu-id="9f849-130">Hesap SA 'larının verildiği bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f849-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="9f849-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9f849-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9f849-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="9f849-132">HttpsOnly</span></span>
- <span data-ttu-id="9f849-133">HttpsOrHttp varsayılan değer HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="9f849-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f849-134">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9f849-134">-ResourceType</span></span>
<span data-ttu-id="9f849-135">SAS belirteciyle kullanılabilen kaynak türlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f849-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="9f849-136">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9f849-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9f849-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9f849-137">None</span></span>
- <span data-ttu-id="9f849-138">Hizmetinin</span><span class="sxs-lookup"><span data-stu-id="9f849-138">Service</span></span>
- <span data-ttu-id="9f849-139">Kapsayıcıdaki</span><span class="sxs-lookup"><span data-stu-id="9f849-139">Container</span></span>
- <span data-ttu-id="9f849-140">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="9f849-140">Object</span></span>

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f849-141">-Hizmet</span><span class="sxs-lookup"><span data-stu-id="9f849-141">-Service</span></span>
<span data-ttu-id="9f849-142">Hizmeti belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f849-142">Specifies the service.</span></span>
<span data-ttu-id="9f849-143">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9f849-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9f849-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9f849-144">None</span></span>
- <span data-ttu-id="9f849-145">'Unu</span><span class="sxs-lookup"><span data-stu-id="9f849-145">Blob</span></span>
- <span data-ttu-id="9f849-146">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="9f849-146">File</span></span>
- <span data-ttu-id="9f849-147">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="9f849-147">Queue</span></span>
- <span data-ttu-id="9f849-148">Tablo</span><span class="sxs-lookup"><span data-stu-id="9f849-148">Table</span></span>

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f849-149">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="9f849-149">-StartTime</span></span>
<span data-ttu-id="9f849-150">SAS 'ın geçerli olacağı **Tarih saat** nesnesi olarak saat belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f849-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="9f849-151">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9f849-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="9f849-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f849-152">CommonParameters</span></span>
<span data-ttu-id="9f849-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f849-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f849-154">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f849-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f849-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f849-155">INPUTS</span></span>

### <span data-ttu-id="9f849-156">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="9f849-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9f849-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f849-157">OUTPUTS</span></span>

### <span data-ttu-id="9f849-158">System. String</span><span class="sxs-lookup"><span data-stu-id="9f849-158">System.String</span></span>

## <span data-ttu-id="9f849-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f849-159">NOTES</span></span>

## <span data-ttu-id="9f849-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f849-160">RELATED LINKS</span></span>

[<span data-ttu-id="9f849-161">Yeni-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="9f849-161">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)

[<span data-ttu-id="9f849-162">Yeni-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="9f849-162">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)

[<span data-ttu-id="9f849-163">Yeni-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="9f849-163">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)

[<span data-ttu-id="9f849-164">Yeni-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="9f849-164">New-AzStorageQueueSASToken</span></span>](./New-AzStorageQueueSASToken.md)

[<span data-ttu-id="9f849-165">Yeni-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="9f849-165">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)

[<span data-ttu-id="9f849-166">Yeni-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="9f849-166">New-AzStorageTableSASToken</span></span>](./New-AzStorageTableSASToken.md)

