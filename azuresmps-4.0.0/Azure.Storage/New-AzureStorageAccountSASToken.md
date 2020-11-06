---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c888c5e7a4083fd91fdddfd6d2442cb65056d42
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572338"
---
# <span data-ttu-id="21137-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="21137-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="21137-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21137-102">SYNOPSIS</span></span>
<span data-ttu-id="21137-103">SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21137-103">Creates an SAS token.</span></span>

## <span data-ttu-id="21137-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21137-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="21137-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="21137-105">DESCRIPTION</span></span>
<span data-ttu-id="21137-106">**New-AzureStorageSASToken** cmdlet 'i, bir Azure depolama hesabı için hesap düzeyi paylaşılan erişim IMZASı (SAS) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21137-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>

<span data-ttu-id="21137-107">SAS belirtecini birden fazla hizmete yönelik izinler temsilci seçmek veya nesne düzeyinde SAS belirteciyle kullanılamayan hizmetlerin izinlerini temsil etmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="21137-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="21137-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21137-108">EXAMPLES</span></span>

### <span data-ttu-id="21137-109">Örnek 1: SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="21137-109">Example 1: Create an SAS token</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="21137-110">Bu komut tam izni olan bir hesap düzeyi SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21137-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="21137-111">Örnek 2: bir IP adresleri aralığı için SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="21137-111">Example 2: Create an SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="21137-112">Bu komut, belirtilen IP adresi aralığından yalnızca HTTPS istekleri için SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21137-112">This command creates an SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="21137-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21137-113">PARAMETERS</span></span>

### <span data-ttu-id="21137-114">-Context</span><span class="sxs-lookup"><span data-stu-id="21137-114">-Context</span></span>
<span data-ttu-id="21137-115">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21137-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="21137-116">**Azurestoragecontext** nesnesini almak için New-AzureStorageContext cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="21137-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="21137-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="21137-117">-ExpiryTime</span></span>
<span data-ttu-id="21137-118">Paylaşılan erişim imzasının geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="21137-118">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="21137-119">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="21137-119">-IPAddressOrRange</span></span>
<span data-ttu-id="21137-120">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21137-120">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="21137-121">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="21137-121">The range is inclusive.</span></span>

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

### <span data-ttu-id="21137-122">-İzin</span><span class="sxs-lookup"><span data-stu-id="21137-122">-Permission</span></span>
<span data-ttu-id="21137-123">Depolama hesabı izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="21137-123">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="21137-124">İzinler yalnızca belirtilen kaynak türüyle eşleşirse geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="21137-124">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="21137-125">Kabul edilebilir izin değerleri hakkında daha fazla bilgi için bkz: hesap SA 'ları oluşturmahttps://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="21137-125">For more information about acceptable permission values, see Constructing an Account SAShttps://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="21137-126">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="21137-126">-Protocol</span></span>
<span data-ttu-id="21137-127">Hesap SA 'larının verildiği bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="21137-127">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="21137-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="21137-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="21137-129">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="21137-129">HttpsOnly</span></span>
- <span data-ttu-id="21137-130">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="21137-130">HttpsOrHttp</span></span>

<span data-ttu-id="21137-131">Varsayılan değer HttpsOrHttp değeridir.</span><span class="sxs-lookup"><span data-stu-id="21137-131">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="21137-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="21137-132">-ResourceType</span></span>
<span data-ttu-id="21137-133">SAS belirteciyle kullanılabilen kaynak türlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="21137-133">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="21137-134">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="21137-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="21137-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="21137-135">None</span></span>
- <span data-ttu-id="21137-136">Hizmetinin</span><span class="sxs-lookup"><span data-stu-id="21137-136">Service</span></span>
- <span data-ttu-id="21137-137">Kapsayıcıdaki</span><span class="sxs-lookup"><span data-stu-id="21137-137">Container</span></span>
- <span data-ttu-id="21137-138">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="21137-138">Object</span></span>

```yaml
Type: SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21137-139">-Hizmet</span><span class="sxs-lookup"><span data-stu-id="21137-139">-Service</span></span>
<span data-ttu-id="21137-140">Hizmeti belirtir.</span><span class="sxs-lookup"><span data-stu-id="21137-140">Specifies the service.</span></span>
<span data-ttu-id="21137-141">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="21137-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="21137-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="21137-142">None</span></span>
- <span data-ttu-id="21137-143">'Unu</span><span class="sxs-lookup"><span data-stu-id="21137-143">Blob</span></span>
- <span data-ttu-id="21137-144">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="21137-144">File</span></span>
- <span data-ttu-id="21137-145">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="21137-145">Queue</span></span>
- <span data-ttu-id="21137-146">Tablo</span><span class="sxs-lookup"><span data-stu-id="21137-146">Table</span></span>

```yaml
Type: SharedAccessAccountServices
Parameter Sets: (All)
Aliases: 
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21137-147">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="21137-147">-StartTime</span></span>
<span data-ttu-id="21137-148">SAS 'ın geçerli olacağı **Tarih saat** nesnesi olarak saat belirtir.</span><span class="sxs-lookup"><span data-stu-id="21137-148">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="21137-149">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="21137-149">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="21137-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21137-150">CommonParameters</span></span>
<span data-ttu-id="21137-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="21137-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21137-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21137-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21137-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21137-153">INPUTS</span></span>

## <span data-ttu-id="21137-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21137-154">OUTPUTS</span></span>

## <span data-ttu-id="21137-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21137-155">NOTES</span></span>

## <span data-ttu-id="21137-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21137-156">RELATED LINKS</span></span>

[<span data-ttu-id="21137-157">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="21137-157">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="21137-158">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="21137-158">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="21137-159">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="21137-159">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="21137-160">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="21137-160">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="21137-161">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="21137-161">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="21137-162">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="21137-162">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)


