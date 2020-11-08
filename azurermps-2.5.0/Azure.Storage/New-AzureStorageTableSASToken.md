---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablesastoken
schema: 2.0.0
ms.openlocfilehash: 29c5cf9b48126d4b8544cf80ad6fa78acc51ae93
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940216"
---
# <span data-ttu-id="a9bd6-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="a9bd6-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="a9bd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9bd6-102">SYNOPSIS</span></span>
<span data-ttu-id="a9bd6-103">Bir Azure depolama tablosu için SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-103">Generates an SAS token for an Azure Storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9bd6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9bd6-104">SYNTAX</span></span>

### <span data-ttu-id="a9bd6-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="a9bd6-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9bd6-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="a9bd6-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9bd6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9bd6-107">DESCRIPTION</span></span>
<span data-ttu-id="a9bd6-108">**New-AzureStorageTableSASToken** cmdlet 'ı bir Azure depolama tablosu Için paylaşılan erişim IMZASı (SAS) belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="a9bd6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9bd6-109">EXAMPLES</span></span>

### <span data-ttu-id="a9bd6-110">Örnek 1: tablo için tam izinleri olan SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="a9bd6-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="a9bd6-111">Bu komut, ContosoResources adlı tablo için tam izinlerle bir SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="a9bd6-112">Bu belirteç okuma, ekleme, güncelleştirme ve silme izinleri içindir.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="a9bd6-113">Örnek 2: bir bölüm aralığı için SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="a9bd6-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="a9bd6-114">Bu komut, ContosoResources adlı tablo için tam izinlerle SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="a9bd6-115">Komut, belirteci *startpartitionkey* ve *endpartitionkey* parametrelerinin belirttiğiniz aralıkla sınırlar.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="a9bd6-116">Örnek 3: tablo için depolanan bir erişim ilkesine sahip SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="a9bd6-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="a9bd6-117">Bu komut, ContosoResources adlı tablo için bir SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="a9bd6-118">Komut, ClientPolicy01 adlı depolanan erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="a9bd6-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9bd6-119">PARAMETERS</span></span>

### <span data-ttu-id="a9bd6-120">-Context</span><span class="sxs-lookup"><span data-stu-id="a9bd6-120">-Context</span></span>
<span data-ttu-id="a9bd6-121">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a9bd6-122">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a9bd6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9bd6-123">-DefaultProfile</span></span>
<span data-ttu-id="a9bd6-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9bd6-125">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="a9bd6-125">-EndPartitionKey</span></span>
<span data-ttu-id="a9bd6-126">Bu cmdlet 'in oluşturduğu belirteç için aralığın sonundaki bölüm anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-126">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bd6-127">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="a9bd6-127">-EndRowKey</span></span>
<span data-ttu-id="a9bd6-128">Bu cmdlet 'in oluşturduğu belirteç için aralığın sonundaki satır tuşunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-128">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bd6-129">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a9bd6-129">-ExpiryTime</span></span>
<span data-ttu-id="a9bd6-130">SAS belirtecinin ne zaman dolacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-130">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="a9bd6-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="a9bd6-131">-FullUri</span></span>
<span data-ttu-id="a9bd6-132">Bu cmdlet 'in SAS belirtecine sahip tam sıra URI olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-132">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="a9bd6-133">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="a9bd6-133">-IPAddressOrRange</span></span>
<span data-ttu-id="a9bd6-134">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="a9bd6-135">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="a9bd6-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="a9bd6-136">-Name</span></span>
<span data-ttu-id="a9bd6-137">Azure depolama tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-137">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="a9bd6-138">Bu cmdlet, bu parametrenin belirttiği tablo için bir SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-138">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9bd6-139">-İzin</span><span class="sxs-lookup"><span data-stu-id="a9bd6-139">-Permission</span></span>
<span data-ttu-id="a9bd6-140">Azure depolama tablosunun izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-140">Specifies permissions for an Azure Storage table.</span></span>
<span data-ttu-id="a9bd6-141">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="a9bd6-142">-İlke</span><span class="sxs-lookup"><span data-stu-id="a9bd6-142">-Policy</span></span>
<span data-ttu-id="a9bd6-143">Bu SAS belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-143">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="a9bd6-144">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="a9bd6-144">-Protocol</span></span>
<span data-ttu-id="a9bd6-145">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="a9bd6-146">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a9bd6-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="a9bd6-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="a9bd6-147">HttpsOnly</span></span>
* <span data-ttu-id="a9bd6-148">HttpsOrHttp varsayılan değer HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="a9bd6-149">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="a9bd6-149">-StartPartitionKey</span></span>
<span data-ttu-id="a9bd6-150">Bu cmdlet 'in oluşturduğu belirteç için aralığın başlangıç aralığının bölüm anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-150">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bd6-151">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="a9bd6-151">-StartRowKey</span></span>
<span data-ttu-id="a9bd6-152">Bu cmdlet 'in oluşturduğu belirteç için aralığın başlangıç satır anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-152">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bd6-153">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="a9bd6-153">-StartTime</span></span>
<span data-ttu-id="a9bd6-154">SAS belirtecinin ne zaman geçerli olacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-154">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="a9bd6-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9bd6-155">CommonParameters</span></span>
<span data-ttu-id="a9bd6-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9bd6-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9bd6-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9bd6-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9bd6-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9bd6-158">INPUTS</span></span>

### <span data-ttu-id="a9bd6-159">System. String</span><span class="sxs-lookup"><span data-stu-id="a9bd6-159">System.String</span></span>

### <span data-ttu-id="a9bd6-160">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="a9bd6-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a9bd6-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9bd6-161">OUTPUTS</span></span>

### <span data-ttu-id="a9bd6-162">System. String</span><span class="sxs-lookup"><span data-stu-id="a9bd6-162">System.String</span></span>

## <span data-ttu-id="a9bd6-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9bd6-163">NOTES</span></span>

## <span data-ttu-id="a9bd6-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9bd6-164">RELATED LINKS</span></span>

[<span data-ttu-id="a9bd6-165">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a9bd6-165">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)