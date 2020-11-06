---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8d84b310a16a73456bcd519332fa76ad1a6566
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572337"
---
# <span data-ttu-id="e6419-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e6419-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="e6419-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6419-102">SYNOPSIS</span></span>
<span data-ttu-id="e6419-103">Bir Azure Depolama Blobu için SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6419-103">Generates an SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="e6419-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6419-104">SYNTAX</span></span>

### <span data-ttu-id="e6419-105">BlobNameWithPermission (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e6419-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="e6419-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="e6419-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="e6419-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="e6419-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="e6419-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="e6419-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="e6419-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6419-109">DESCRIPTION</span></span>
<span data-ttu-id="e6419-110">**New-AzureStorageBlobSASToken** cmdlet 'ı bir Azure Depolama Blobu için paylaşılan bir erişim IMZASı (SAS) belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6419-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="e6419-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6419-111">EXAMPLES</span></span>

### <span data-ttu-id="e6419-112">Örnek 1: tam blob izniyle blob SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="e6419-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="e6419-113">Bu örnek tam blob izni olan bir blob SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6419-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="e6419-114">Örnek 2: ömür ile blob SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="e6419-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="e6419-115">Bu örnek ömür boyu bir blob SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6419-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="e6419-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6419-116">PARAMETERS</span></span>

### <span data-ttu-id="e6419-117">-Blob</span><span class="sxs-lookup"><span data-stu-id="e6419-117">-Blob</span></span>
<span data-ttu-id="e6419-118">Depolama blob adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6419-118">Specifies the storage blob name.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6419-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="e6419-119">-CloudBlob</span></span>
<span data-ttu-id="e6419-120">**Cloudblob** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6419-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="e6419-121">**Cloudblob** nesnesi almak Için, [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e6419-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6419-122">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="e6419-122">-Container</span></span>
<span data-ttu-id="e6419-123">Depolama kapsayıcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6419-123">Specifies the storage container name.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6419-124">-Context</span><span class="sxs-lookup"><span data-stu-id="e6419-124">-Context</span></span>
<span data-ttu-id="e6419-125">Depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6419-125">Specifies the storage context.</span></span>

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

### <span data-ttu-id="e6419-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e6419-126">-ExpiryTime</span></span>
<span data-ttu-id="e6419-127">Paylaşılan erişim imzasının ne zaman sona ereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6419-127">Specifies when the shared access signature expires.</span></span>

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

### <span data-ttu-id="e6419-128">-FullUri</span><span class="sxs-lookup"><span data-stu-id="e6419-128">-FullUri</span></span>
<span data-ttu-id="e6419-129">Bu cmdlet 'in tam blob URI 'sini ve paylaşılan erişim imza belirtecini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6419-129">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="e6419-130">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="e6419-130">-IPAddressOrRange</span></span>
<span data-ttu-id="e6419-131">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6419-131">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="e6419-132">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="e6419-132">The range is inclusive.</span></span>

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

### <span data-ttu-id="e6419-133">-İzin</span><span class="sxs-lookup"><span data-stu-id="e6419-133">-Permission</span></span>
<span data-ttu-id="e6419-134">Bir depolama blob 'una yönelik izinleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6419-134">Specifies the permissions for a storage blob.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6419-135">-İlke</span><span class="sxs-lookup"><span data-stu-id="e6419-135">-Policy</span></span>
<span data-ttu-id="e6419-136">Azure saklı bir erişim Ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6419-136">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6419-137">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="e6419-137">-Protocol</span></span>
<span data-ttu-id="e6419-138">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6419-138">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="e6419-139">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e6419-139">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="e6419-140">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="e6419-140">HttpsOnly</span></span>
* <span data-ttu-id="e6419-141">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="e6419-141">HttpsOrHttp</span></span>

<span data-ttu-id="e6419-142">Varsayılan değer HttpsOrHttp değeridir.</span><span class="sxs-lookup"><span data-stu-id="e6419-142">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="e6419-143">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="e6419-143">-StartTime</span></span>
<span data-ttu-id="e6419-144">Paylaşılan erişim imzasının geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6419-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="e6419-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6419-145">CommonParameters</span></span>
<span data-ttu-id="e6419-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6419-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6419-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6419-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6419-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6419-148">INPUTS</span></span>

## <span data-ttu-id="e6419-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6419-149">OUTPUTS</span></span>

## <span data-ttu-id="e6419-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6419-150">NOTES</span></span>

## <span data-ttu-id="e6419-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6419-151">RELATED LINKS</span></span>

[<span data-ttu-id="e6419-152">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="e6419-152">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="e6419-153">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="e6419-153">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)
