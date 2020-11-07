---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
ms.openlocfilehash: d75111b27b03317f757cbf0def4d9d66c43427c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763305"
---
# <span data-ttu-id="ca8f3-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ca8f3-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="ca8f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca8f3-102">SYNOPSIS</span></span>
<span data-ttu-id="ca8f3-103">Bir Azure Depolama Blobu için SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca8f3-103">Generates a SAS token for an Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca8f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca8f3-104">SYNTAX</span></span>

### <span data-ttu-id="ca8f3-105">BlobNameWithPermission (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ca8f3-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="ca8f3-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="ca8f3-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="ca8f3-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="ca8f3-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="ca8f3-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="ca8f3-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="ca8f3-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca8f3-109">DESCRIPTION</span></span>
<span data-ttu-id="ca8f3-110">**New-AzureStorageBlobSASToken** cmdlet 'ı bir Azure Depolama Blobu için paylaşılan bir erişim IMZASı (SAS) belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca8f3-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="ca8f3-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca8f3-111">EXAMPLES</span></span>

### <span data-ttu-id="ca8f3-112">Örnek 1: tam blob izniyle blob SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="ca8f3-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="ca8f3-113">Bu örnek tam blob izni olan bir blob SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca8f3-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="ca8f3-114">Örnek 2: ömür ile blob SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="ca8f3-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="ca8f3-115">Bu örnek ömür boyu bir blob SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca8f3-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="ca8f3-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca8f3-116">PARAMETERS</span></span>

### <span data-ttu-id="ca8f3-117">-Blob</span><span class="sxs-lookup"><span data-stu-id="ca8f3-117">-Blob</span></span>
<span data-ttu-id="ca8f3-118">Depolama blob adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca8f3-118">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="ca8f3-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ca8f3-119">-CloudBlob</span></span>
<span data-ttu-id="ca8f3-120">**Cloudblob** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca8f3-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="ca8f3-121">**Cloudblob** nesnesi almak Için, [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ca8f3-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

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

### <span data-ttu-id="ca8f3-122">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="ca8f3-122">-Container</span></span>
<span data-ttu-id="ca8f3-123">Depolama kapsayıcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca8f3-123">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="ca8f3-124">-Context</span><span class="sxs-lookup"><span data-stu-id="ca8f3-124">-Context</span></span>
<span data-ttu-id="ca8f3-125">Depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca8f3-125">Specifies the storage context.</span></span>

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

### <span data-ttu-id="ca8f3-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ca8f3-126">-ExpiryTime</span></span>
<span data-ttu-id="ca8f3-127">Paylaşılan erişim imzasının ne zaman sona ereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca8f3-127">Specifies when the shared access signature expires.</span></span>

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

### <span data-ttu-id="ca8f3-128">-FullUri</span><span class="sxs-lookup"><span data-stu-id="ca8f3-128">-FullUri</span></span>
<span data-ttu-id="ca8f3-129">Bu cmdlet 'in tam blob URI 'sini ve paylaşılan erişim imza belirtecini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca8f3-129">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="ca8f3-130">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="ca8f3-130">-IPAddressOrRange</span></span>
<span data-ttu-id="ca8f3-131">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca8f3-131">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="ca8f3-132">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="ca8f3-132">The range is inclusive.</span></span>

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

### <span data-ttu-id="ca8f3-133">-İzin</span><span class="sxs-lookup"><span data-stu-id="ca8f3-133">-Permission</span></span>
<span data-ttu-id="ca8f3-134">Bir depolama blob 'una yönelik izinleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca8f3-134">Specifies the permissions for a storage blob.</span></span>

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

### <span data-ttu-id="ca8f3-135">-İlke</span><span class="sxs-lookup"><span data-stu-id="ca8f3-135">-Policy</span></span>
<span data-ttu-id="ca8f3-136">Azure saklı bir erişim Ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca8f3-136">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="ca8f3-137">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="ca8f3-137">-Protocol</span></span>
<span data-ttu-id="ca8f3-138">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca8f3-138">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="ca8f3-139">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ca8f3-139">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="ca8f3-140">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="ca8f3-140">HttpsOnly</span></span>
* <span data-ttu-id="ca8f3-141">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="ca8f3-141">HttpsOrHttp</span></span>

<span data-ttu-id="ca8f3-142">Varsayılan değer HttpsOrHttp değeridir.</span><span class="sxs-lookup"><span data-stu-id="ca8f3-142">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="ca8f3-143">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="ca8f3-143">-StartTime</span></span>
<span data-ttu-id="ca8f3-144">Paylaşılan erişim imzasının geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca8f3-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="ca8f3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca8f3-145">CommonParameters</span></span>
<span data-ttu-id="ca8f3-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca8f3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca8f3-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca8f3-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca8f3-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca8f3-148">INPUTS</span></span>

### <span data-ttu-id="ca8f3-149">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="ca8f3-149">IStorageContext</span></span>

<span data-ttu-id="ca8f3-150">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ca8f3-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="ca8f3-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca8f3-151">OUTPUTS</span></span>

### <span data-ttu-id="ca8f3-152">System. String</span><span class="sxs-lookup"><span data-stu-id="ca8f3-152">System.String</span></span>

## <span data-ttu-id="ca8f3-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca8f3-153">NOTES</span></span>

## <span data-ttu-id="ca8f3-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca8f3-154">RELATED LINKS</span></span>

[<span data-ttu-id="ca8f3-155">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ca8f3-155">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="ca8f3-156">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="ca8f3-156">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)