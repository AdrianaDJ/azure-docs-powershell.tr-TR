---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: ''
schema: 2.0.0
ms.openlocfilehash: 39870fe9fe9ac4223bccf15908c960db29d25252
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572537"
---
# <span data-ttu-id="54c3d-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="54c3d-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="54c3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="54c3d-103">Bir Azure depolama tablosu için SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54c3d-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="54c3d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54c3d-104">SYNTAX</span></span>

### <span data-ttu-id="54c3d-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="54c3d-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="54c3d-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="54c3d-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="54c3d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="54c3d-107">DESCRIPTION</span></span>
<span data-ttu-id="54c3d-108">**New-AzureStorageTableSASToken** cmdlet 'ı bir Azure depolama tablosu Için paylaşılan erişim IMZASı (SAS) belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54c3d-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="54c3d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54c3d-109">EXAMPLES</span></span>

### <span data-ttu-id="54c3d-110">Örnek 1: tablo için tam izinleri olan SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="54c3d-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="54c3d-111">Bu komut, ContosoResources adlı tablo için tam izinlerle bir SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54c3d-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="54c3d-112">Bu belirteç okuma, ekleme, güncelleştirme ve silme izinleri içindir.</span><span class="sxs-lookup"><span data-stu-id="54c3d-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="54c3d-113">Örnek 2: bir bölüm aralığı için SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="54c3d-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="54c3d-114">Bu komut, ContosoResources adlı tablo için tam izinlerle SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54c3d-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="54c3d-115">Komut, belirteci *startpartitionkey* ve *endpartitionkey* parametrelerinin belirttiğiniz aralıkla sınırlar.</span><span class="sxs-lookup"><span data-stu-id="54c3d-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="54c3d-116">Örnek 3: tablo için depolanan bir erişim ilkesine sahip SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="54c3d-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="54c3d-117">Bu komut, ContosoResources adlı tablo için bir SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54c3d-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="54c3d-118">Komut, ClientPolicy01 adlı depolanan erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="54c3d-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="54c3d-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54c3d-119">PARAMETERS</span></span>

### <span data-ttu-id="54c3d-120">-Context</span><span class="sxs-lookup"><span data-stu-id="54c3d-120">-Context</span></span>
<span data-ttu-id="54c3d-121">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54c3d-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="54c3d-122">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="54c3d-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="54c3d-123">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="54c3d-123">-EndPartitionKey</span></span>
<span data-ttu-id="54c3d-124">Bu cmdlet 'in oluşturduğu belirteç için aralığın sonundaki bölüm anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54c3d-124">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="54c3d-125">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="54c3d-125">-EndRowKey</span></span>
<span data-ttu-id="54c3d-126">Bu cmdlet 'in oluşturduğu belirteç için aralığın sonundaki satır tuşunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="54c3d-126">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="54c3d-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="54c3d-127">-ExpiryTime</span></span>
<span data-ttu-id="54c3d-128">SAS belirtecinin ne zaman dolacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54c3d-128">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="54c3d-129">-FullUri</span><span class="sxs-lookup"><span data-stu-id="54c3d-129">-FullUri</span></span>
<span data-ttu-id="54c3d-130">Bu cmdlet 'in SAS belirtecine sahip tam sıra URI olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="54c3d-130">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="54c3d-131">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="54c3d-131">-IPAddressOrRange</span></span>
<span data-ttu-id="54c3d-132">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54c3d-132">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="54c3d-133">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="54c3d-133">The range is inclusive.</span></span>

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

### <span data-ttu-id="54c3d-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="54c3d-134">-Name</span></span>
<span data-ttu-id="54c3d-135">Azure depolama tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54c3d-135">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="54c3d-136">Bu cmdlet, bu parametrenin belirttiği tablo için bir SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54c3d-136">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

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

### <span data-ttu-id="54c3d-137">-İzin</span><span class="sxs-lookup"><span data-stu-id="54c3d-137">-Permission</span></span>
<span data-ttu-id="54c3d-138">Azure depolama tablosunun izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="54c3d-138">Specifies permissions for an Azure Storage table.</span></span>

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

### <span data-ttu-id="54c3d-139">-İlke</span><span class="sxs-lookup"><span data-stu-id="54c3d-139">-Policy</span></span>
<span data-ttu-id="54c3d-140">Bu SAS belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="54c3d-140">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="54c3d-141">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="54c3d-141">-Protocol</span></span>
<span data-ttu-id="54c3d-142">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="54c3d-142">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="54c3d-143">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="54c3d-143">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="54c3d-144">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="54c3d-144">HttpsOnly</span></span>
* <span data-ttu-id="54c3d-145">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="54c3d-145">HttpsOrHttp</span></span>

<span data-ttu-id="54c3d-146">Varsayılan değer HttpsOrHttp değeridir.</span><span class="sxs-lookup"><span data-stu-id="54c3d-146">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="54c3d-147">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="54c3d-147">-StartPartitionKey</span></span>
<span data-ttu-id="54c3d-148">Bu cmdlet 'in oluşturduğu belirteç için aralığın başlangıç aralığının bölüm anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54c3d-148">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="54c3d-149">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="54c3d-149">-StartRowKey</span></span>
<span data-ttu-id="54c3d-150">Bu cmdlet 'in oluşturduğu belirteç için aralığın başlangıç satır anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54c3d-150">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="54c3d-151">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="54c3d-151">-StartTime</span></span>
<span data-ttu-id="54c3d-152">SAS belirtecinin ne zaman geçerli olacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54c3d-152">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="54c3d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c3d-153">CommonParameters</span></span>
<span data-ttu-id="54c3d-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54c3d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c3d-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54c3d-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c3d-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54c3d-156">INPUTS</span></span>

## <span data-ttu-id="54c3d-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54c3d-157">OUTPUTS</span></span>

## <span data-ttu-id="54c3d-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54c3d-158">NOTES</span></span>

## <span data-ttu-id="54c3d-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54c3d-159">RELATED LINKS</span></span>

[<span data-ttu-id="54c3d-160">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="54c3d-160">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
