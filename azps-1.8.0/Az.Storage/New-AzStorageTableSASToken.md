---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
ms.openlocfilehash: 743baee44cc038dd54ab2a09d4362848e3d4c9a8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758592"
---
# <span data-ttu-id="8a30d-101">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="8a30d-101">New-AzStorageTableSASToken</span></span>

## <span data-ttu-id="8a30d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a30d-102">SYNOPSIS</span></span>
<span data-ttu-id="8a30d-103">Bir Azure depolama tablosu için SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a30d-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="8a30d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a30d-104">SYNTAX</span></span>

### <span data-ttu-id="8a30d-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="8a30d-105">SasPolicy</span></span>
```
New-AzStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a30d-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="8a30d-106">SasPermission</span></span>
```
New-AzStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a30d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a30d-107">DESCRIPTION</span></span>
<span data-ttu-id="8a30d-108">**New-AzStorageTableSASToken** cmdlet 'ı bir Azure depolama tablosu Için paylaşılan erişim IMZASı (SAS) belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a30d-108">The **New-AzStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="8a30d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a30d-109">EXAMPLES</span></span>

### <span data-ttu-id="8a30d-110">Örnek 1: tablo için tam izinleri olan SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="8a30d-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="8a30d-111">Bu komut, ContosoResources adlı tablo için tam izinlerle bir SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a30d-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="8a30d-112">Bu belirteç okuma, ekleme, güncelleştirme ve silme izinleri içindir.</span><span class="sxs-lookup"><span data-stu-id="8a30d-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="8a30d-113">Örnek 2: bir bölüm aralığı için SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="8a30d-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="8a30d-114">Bu komut, ContosoResources adlı tablo için tam izinlerle SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a30d-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="8a30d-115">Komut, belirteci *startpartitionkey* ve *endpartitionkey* parametrelerinin belirttiğiniz aralıkla sınırlar.</span><span class="sxs-lookup"><span data-stu-id="8a30d-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="8a30d-116">Örnek 3: tablo için depolanan bir erişim ilkesine sahip SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="8a30d-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="8a30d-117">Bu komut, ContosoResources adlı tablo için bir SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a30d-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="8a30d-118">Komut, ClientPolicy01 adlı depolanan erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a30d-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="8a30d-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a30d-119">PARAMETERS</span></span>

### <span data-ttu-id="8a30d-120">-Context</span><span class="sxs-lookup"><span data-stu-id="8a30d-120">-Context</span></span>
<span data-ttu-id="8a30d-121">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a30d-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8a30d-122">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8a30d-122">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8a30d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a30d-123">-DefaultProfile</span></span>
<span data-ttu-id="8a30d-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8a30d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a30d-125">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="8a30d-125">-EndPartitionKey</span></span>
<span data-ttu-id="8a30d-126">Bu cmdlet 'in oluşturduğu belirteç için aralığın sonundaki bölüm anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a30d-126">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8a30d-127">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="8a30d-127">-EndRowKey</span></span>
<span data-ttu-id="8a30d-128">Bu cmdlet 'in oluşturduğu belirteç için aralığın sonundaki satır tuşunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a30d-128">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8a30d-129">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8a30d-129">-ExpiryTime</span></span>
<span data-ttu-id="8a30d-130">SAS belirtecinin ne zaman dolacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a30d-130">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="8a30d-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="8a30d-131">-FullUri</span></span>
<span data-ttu-id="8a30d-132">Bu cmdlet 'in SAS belirtecine sahip tam sıra URI olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a30d-132">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="8a30d-133">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="8a30d-133">-IPAddressOrRange</span></span>
<span data-ttu-id="8a30d-134">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a30d-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="8a30d-135">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="8a30d-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="8a30d-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="8a30d-136">-Name</span></span>
<span data-ttu-id="8a30d-137">Azure depolama tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a30d-137">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="8a30d-138">Bu cmdlet, bu parametrenin belirttiği tablo için bir SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a30d-138">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

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

### <span data-ttu-id="8a30d-139">-İzin</span><span class="sxs-lookup"><span data-stu-id="8a30d-139">-Permission</span></span>
<span data-ttu-id="8a30d-140">Azure depolama tablosunun izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a30d-140">Specifies permissions for an Azure Storage table.</span></span>
<span data-ttu-id="8a30d-141">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="8a30d-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="8a30d-142">-İlke</span><span class="sxs-lookup"><span data-stu-id="8a30d-142">-Policy</span></span>
<span data-ttu-id="8a30d-143">Bu SAS belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a30d-143">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="8a30d-144">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="8a30d-144">-Protocol</span></span>
<span data-ttu-id="8a30d-145">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a30d-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="8a30d-146">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8a30d-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="8a30d-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="8a30d-147">HttpsOnly</span></span>
* <span data-ttu-id="8a30d-148">HttpsOrHttp varsayılan değer HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="8a30d-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Cosmos.Table.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a30d-149">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="8a30d-149">-StartPartitionKey</span></span>
<span data-ttu-id="8a30d-150">Bu cmdlet 'in oluşturduğu belirteç için aralığın başlangıç aralığının bölüm anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a30d-150">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8a30d-151">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="8a30d-151">-StartRowKey</span></span>
<span data-ttu-id="8a30d-152">Bu cmdlet 'in oluşturduğu belirteç için aralığın başlangıç satır anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a30d-152">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8a30d-153">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="8a30d-153">-StartTime</span></span>
<span data-ttu-id="8a30d-154">SAS belirtecinin ne zaman geçerli olacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a30d-154">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="8a30d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a30d-155">CommonParameters</span></span>
<span data-ttu-id="8a30d-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a30d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a30d-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a30d-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a30d-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a30d-158">INPUTS</span></span>

### <span data-ttu-id="8a30d-159">System. String</span><span class="sxs-lookup"><span data-stu-id="8a30d-159">System.String</span></span>

### <span data-ttu-id="8a30d-160">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="8a30d-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8a30d-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a30d-161">OUTPUTS</span></span>

### <span data-ttu-id="8a30d-162">System. String</span><span class="sxs-lookup"><span data-stu-id="8a30d-162">System.String</span></span>

## <span data-ttu-id="8a30d-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a30d-163">NOTES</span></span>

## <span data-ttu-id="8a30d-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a30d-164">RELATED LINKS</span></span>

[<span data-ttu-id="8a30d-165">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8a30d-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
