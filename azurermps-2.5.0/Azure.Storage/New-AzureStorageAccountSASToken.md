---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageaccountsastoken
schema: 2.0.0
ms.openlocfilehash: 4addd74f4a57c261886ef3323517663d02ffbcba
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939640"
---
# <span data-ttu-id="99d0e-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="99d0e-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="99d0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99d0e-102">SYNOPSIS</span></span>
<span data-ttu-id="99d0e-103">Hesap düzeyi SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="99d0e-103">Creates an account-level SAS token.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99d0e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99d0e-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99d0e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="99d0e-105">DESCRIPTION</span></span>
<span data-ttu-id="99d0e-106">**New-AzureStorageSASToken** cmdlet 'i, bir Azure depolama hesabı için hesap düzeyi paylaşılan erişim IMZASı (SAS) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="99d0e-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="99d0e-107">SAS belirtecini birden fazla hizmete yönelik izinler temsilci seçmek veya nesne düzeyinde SAS belirteciyle kullanılamayan hizmetlerin izinlerini temsil etmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="99d0e-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="99d0e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99d0e-108">EXAMPLES</span></span>

### <span data-ttu-id="99d0e-109">Örnek 1: tam izinli bir hesap düzeyi SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="99d0e-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="99d0e-110">Bu komut tam izni olan bir hesap düzeyi SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="99d0e-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="99d0e-111">Örnek 2: bir IP adresleri aralığı için hesap düzeyi SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="99d0e-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="99d0e-112">Bu komut, belirtilen IP adresi aralığından yalnızca HTTPS istekleri için bir hesap düzeyi SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="99d0e-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="99d0e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99d0e-113">PARAMETERS</span></span>

### <span data-ttu-id="99d0e-114">-Context</span><span class="sxs-lookup"><span data-stu-id="99d0e-114">-Context</span></span>
<span data-ttu-id="99d0e-115">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99d0e-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="99d0e-116">**Azurestoragecontext** nesnesini almak için New-AzureStorageContext cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="99d0e-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="99d0e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d0e-117">-DefaultProfile</span></span>
<span data-ttu-id="99d0e-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="99d0e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99d0e-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="99d0e-119">-ExpiryTime</span></span>
<span data-ttu-id="99d0e-120">Paylaşılan erişim imzasının geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="99d0e-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="99d0e-121">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="99d0e-121">-IPAddressOrRange</span></span>
<span data-ttu-id="99d0e-122">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99d0e-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="99d0e-123">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="99d0e-123">The range is inclusive.</span></span>

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

### <span data-ttu-id="99d0e-124">-İzin</span><span class="sxs-lookup"><span data-stu-id="99d0e-124">-Permission</span></span>
<span data-ttu-id="99d0e-125">Depolama hesabı izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="99d0e-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="99d0e-126">İzinler yalnızca belirtilen kaynak türüyle eşleşirse geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="99d0e-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="99d0e-127">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="99d0e-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="99d0e-128">Kabul edilebilir izin değerleri hakkında daha fazla bilgi için bkz: hesap SA 'ları oluşturma https://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="99d0e-128">For more information about acceptable permission values, see Constructing an Account SAS https://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="99d0e-129">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="99d0e-129">-Protocol</span></span>
<span data-ttu-id="99d0e-130">Hesap SA 'larının verildiği bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="99d0e-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="99d0e-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="99d0e-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="99d0e-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="99d0e-132">HttpsOnly</span></span>
- <span data-ttu-id="99d0e-133">HttpsOrHttp varsayılan değer HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="99d0e-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="99d0e-134">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="99d0e-134">-ResourceType</span></span>
<span data-ttu-id="99d0e-135">SAS belirteciyle kullanılabilen kaynak türlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="99d0e-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="99d0e-136">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="99d0e-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="99d0e-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="99d0e-137">None</span></span>
- <span data-ttu-id="99d0e-138">Hizmetinin</span><span class="sxs-lookup"><span data-stu-id="99d0e-138">Service</span></span>
- <span data-ttu-id="99d0e-139">Kapsayıcıdaki</span><span class="sxs-lookup"><span data-stu-id="99d0e-139">Container</span></span>
- <span data-ttu-id="99d0e-140">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="99d0e-140">Object</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d0e-141">-Hizmet</span><span class="sxs-lookup"><span data-stu-id="99d0e-141">-Service</span></span>
<span data-ttu-id="99d0e-142">Hizmeti belirtir.</span><span class="sxs-lookup"><span data-stu-id="99d0e-142">Specifies the service.</span></span>
<span data-ttu-id="99d0e-143">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="99d0e-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="99d0e-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="99d0e-144">None</span></span>
- <span data-ttu-id="99d0e-145">'Unu</span><span class="sxs-lookup"><span data-stu-id="99d0e-145">Blob</span></span>
- <span data-ttu-id="99d0e-146">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="99d0e-146">File</span></span>
- <span data-ttu-id="99d0e-147">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="99d0e-147">Queue</span></span>
- <span data-ttu-id="99d0e-148">Tablo</span><span class="sxs-lookup"><span data-stu-id="99d0e-148">Table</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d0e-149">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="99d0e-149">-StartTime</span></span>
<span data-ttu-id="99d0e-150">SAS 'ın geçerli olacağı **Tarih saat** nesnesi olarak saat belirtir.</span><span class="sxs-lookup"><span data-stu-id="99d0e-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="99d0e-151">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="99d0e-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="99d0e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d0e-152">CommonParameters</span></span>
<span data-ttu-id="99d0e-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99d0e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d0e-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99d0e-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d0e-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99d0e-155">INPUTS</span></span>

### <span data-ttu-id="99d0e-156">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="99d0e-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="99d0e-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99d0e-157">OUTPUTS</span></span>

### <span data-ttu-id="99d0e-158">System. String</span><span class="sxs-lookup"><span data-stu-id="99d0e-158">System.String</span></span>

## <span data-ttu-id="99d0e-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99d0e-159">NOTES</span></span>

## <span data-ttu-id="99d0e-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99d0e-160">RELATED LINKS</span></span>

[<span data-ttu-id="99d0e-161">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="99d0e-161">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="99d0e-162">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="99d0e-162">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="99d0e-163">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="99d0e-163">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="99d0e-164">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="99d0e-164">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="99d0e-165">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="99d0e-165">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="99d0e-166">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="99d0e-166">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)


