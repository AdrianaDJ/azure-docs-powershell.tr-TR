---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 739cd5b12cfc33abb57e4e04d2834b195966b126
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765074"
---
# <span data-ttu-id="1ae2f-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="1ae2f-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="1ae2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ae2f-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae2f-103">Bir Azure depolama tablosu için SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-103">Generates an SAS token for an Azure Storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ae2f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ae2f-104">SYNTAX</span></span>

### <span data-ttu-id="1ae2f-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="1ae2f-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="1ae2f-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="1ae2f-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="1ae2f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ae2f-107">DESCRIPTION</span></span>
<span data-ttu-id="1ae2f-108">**New-AzureStorageTableSASToken** cmdlet 'ı bir Azure depolama tablosu Için paylaşılan erişim IMZASı (SAS) belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="1ae2f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ae2f-109">EXAMPLES</span></span>

### <span data-ttu-id="1ae2f-110">Örnek 1: tablo için tam izinleri olan SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="1ae2f-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="1ae2f-111">Bu komut, ContosoResources adlı tablo için tam izinlerle bir SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="1ae2f-112">Bu belirteç okuma, ekleme, güncelleştirme ve silme izinleri içindir.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="1ae2f-113">Örnek 2: bir bölüm aralığı için SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="1ae2f-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="1ae2f-114">Bu komut, ContosoResources adlı tablo için tam izinlerle SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="1ae2f-115">Komut, belirteci *startpartitionkey* ve *endpartitionkey* parametrelerinin belirttiğiniz aralıkla sınırlar.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="1ae2f-116">Örnek 3: tablo için depolanan bir erişim ilkesine sahip SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="1ae2f-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="1ae2f-117">Bu komut, ContosoResources adlı tablo için bir SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="1ae2f-118">Komut, ClientPolicy01 adlı depolanan erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="1ae2f-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ae2f-119">PARAMETERS</span></span>

### <span data-ttu-id="1ae2f-120">-Context</span><span class="sxs-lookup"><span data-stu-id="1ae2f-120">-Context</span></span>
<span data-ttu-id="1ae2f-121">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1ae2f-122">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1ae2f-123">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="1ae2f-123">-EndPartitionKey</span></span>
<span data-ttu-id="1ae2f-124">Bu cmdlet 'in oluşturduğu belirteç için aralığın sonundaki bölüm anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-124">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae2f-125">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="1ae2f-125">-EndRowKey</span></span>
<span data-ttu-id="1ae2f-126">Bu cmdlet 'in oluşturduğu belirteç için aralığın sonundaki satır tuşunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-126">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae2f-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="1ae2f-127">-ExpiryTime</span></span>
<span data-ttu-id="1ae2f-128">SAS belirtecinin ne zaman dolacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-128">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="1ae2f-129">-FullUri</span><span class="sxs-lookup"><span data-stu-id="1ae2f-129">-FullUri</span></span>
<span data-ttu-id="1ae2f-130">Bu cmdlet 'in SAS belirtecine sahip tam sıra URI olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-130">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="1ae2f-131">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="1ae2f-131">-IPAddressOrRange</span></span>
<span data-ttu-id="1ae2f-132">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-132">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="1ae2f-133">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-133">The range is inclusive.</span></span>

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

### <span data-ttu-id="1ae2f-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="1ae2f-134">-Name</span></span>
<span data-ttu-id="1ae2f-135">Azure depolama tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-135">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="1ae2f-136">Bu cmdlet, bu parametrenin belirttiği tablo için bir SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-136">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae2f-137">-İzin</span><span class="sxs-lookup"><span data-stu-id="1ae2f-137">-Permission</span></span>
<span data-ttu-id="1ae2f-138">Azure depolama tablosunun izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-138">Specifies permissions for an Azure Storage table.</span></span>

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

### <span data-ttu-id="1ae2f-139">-İlke</span><span class="sxs-lookup"><span data-stu-id="1ae2f-139">-Policy</span></span>
<span data-ttu-id="1ae2f-140">Bu SAS belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-140">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="1ae2f-141">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="1ae2f-141">-Protocol</span></span>
<span data-ttu-id="1ae2f-142">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-142">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="1ae2f-143">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1ae2f-143">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="1ae2f-144">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="1ae2f-144">HttpsOnly</span></span>
* <span data-ttu-id="1ae2f-145">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="1ae2f-145">HttpsOrHttp</span></span>

<span data-ttu-id="1ae2f-146">Varsayılan değer HttpsOrHttp değeridir.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-146">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="1ae2f-147">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="1ae2f-147">-StartPartitionKey</span></span>
<span data-ttu-id="1ae2f-148">Bu cmdlet 'in oluşturduğu belirteç için aralığın başlangıç aralığının bölüm anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-148">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae2f-149">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="1ae2f-149">-StartRowKey</span></span>
<span data-ttu-id="1ae2f-150">Bu cmdlet 'in oluşturduğu belirteç için aralığın başlangıç satır anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-150">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae2f-151">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="1ae2f-151">-StartTime</span></span>
<span data-ttu-id="1ae2f-152">SAS belirtecinin ne zaman geçerli olacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-152">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="1ae2f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae2f-153">CommonParameters</span></span>
<span data-ttu-id="1ae2f-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ae2f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae2f-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ae2f-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae2f-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ae2f-156">INPUTS</span></span>

### <span data-ttu-id="1ae2f-157">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="1ae2f-157">IStorageContext</span></span>

<span data-ttu-id="1ae2f-158">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1ae2f-158">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="1ae2f-159">Dizisi</span><span class="sxs-lookup"><span data-stu-id="1ae2f-159">String</span></span>

<span data-ttu-id="1ae2f-160">' Name ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1ae2f-160">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="1ae2f-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ae2f-161">OUTPUTS</span></span>

### <span data-ttu-id="1ae2f-162">System. String</span><span class="sxs-lookup"><span data-stu-id="1ae2f-162">System.String</span></span>

## <span data-ttu-id="1ae2f-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ae2f-163">NOTES</span></span>

## <span data-ttu-id="1ae2f-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ae2f-164">RELATED LINKS</span></span>

[<span data-ttu-id="1ae2f-165">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1ae2f-165">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
