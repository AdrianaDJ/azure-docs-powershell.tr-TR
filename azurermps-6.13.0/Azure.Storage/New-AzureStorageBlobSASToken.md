---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
ms.openlocfilehash: 60c93d851e173dd8ee8a5f33ff96bb4e2e12299b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591520"
---
# <span data-ttu-id="5789f-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="5789f-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="5789f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5789f-102">SYNOPSIS</span></span>
<span data-ttu-id="5789f-103">Bir Azure Depolama Blobu için SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5789f-103">Generates a SAS token for an Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5789f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5789f-104">SYNTAX</span></span>

### <span data-ttu-id="5789f-105">BlobNameWithPermission (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5789f-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5789f-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="5789f-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5789f-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="5789f-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5789f-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="5789f-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5789f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="5789f-109">DESCRIPTION</span></span>
<span data-ttu-id="5789f-110">**New-AzureStorageBlobSASToken** cmdlet 'ı bir Azure Depolama Blobu için paylaşılan bir erişim IMZASı (SAS) belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5789f-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="5789f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5789f-111">EXAMPLES</span></span>

### <span data-ttu-id="5789f-112">Örnek 1: tam blob izniyle blob SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="5789f-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="5789f-113">Bu örnek tam blob izni olan bir blob SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5789f-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="5789f-114">Örnek 2: ömür ile blob SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="5789f-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="5789f-115">Bu örnek ömür boyu bir blob SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5789f-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="5789f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5789f-116">PARAMETERS</span></span>

### <span data-ttu-id="5789f-117">-Blob</span><span class="sxs-lookup"><span data-stu-id="5789f-117">-Blob</span></span>
<span data-ttu-id="5789f-118">Depolama blob adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5789f-118">Specifies the storage blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5789f-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="5789f-119">-CloudBlob</span></span>
<span data-ttu-id="5789f-120">**Cloudblob** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5789f-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="5789f-121">**Cloudblob** nesnesi almak Için, [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5789f-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5789f-122">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="5789f-122">-Container</span></span>
<span data-ttu-id="5789f-123">Depolama kapsayıcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5789f-123">Specifies the storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5789f-124">-Context</span><span class="sxs-lookup"><span data-stu-id="5789f-124">-Context</span></span>
<span data-ttu-id="5789f-125">Depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5789f-125">Specifies the storage context.</span></span>

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

### <span data-ttu-id="5789f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5789f-126">-DefaultProfile</span></span>
<span data-ttu-id="5789f-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5789f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5789f-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5789f-128">-ExpiryTime</span></span>
<span data-ttu-id="5789f-129">Paylaşılan erişim imzasının ne zaman sona ereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5789f-129">Specifies when the shared access signature expires.</span></span>

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

### <span data-ttu-id="5789f-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="5789f-130">-FullUri</span></span>
<span data-ttu-id="5789f-131">Bu cmdlet 'in tam blob URI 'sini ve paylaşılan erişim imza belirtecini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5789f-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="5789f-132">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="5789f-132">-IPAddressOrRange</span></span>
<span data-ttu-id="5789f-133">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5789f-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="5789f-134">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="5789f-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="5789f-135">-İzin</span><span class="sxs-lookup"><span data-stu-id="5789f-135">-Permission</span></span>
<span data-ttu-id="5789f-136">Bir depolama blob 'una yönelik izinleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="5789f-136">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="5789f-137">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="5789f-137">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5789f-138">-İlke</span><span class="sxs-lookup"><span data-stu-id="5789f-138">-Policy</span></span>
<span data-ttu-id="5789f-139">Azure saklı bir erişim Ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5789f-139">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5789f-140">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="5789f-140">-Protocol</span></span>
<span data-ttu-id="5789f-141">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5789f-141">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="5789f-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5789f-142">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="5789f-143">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="5789f-143">HttpsOnly</span></span>
* <span data-ttu-id="5789f-144">HttpsOrHttp varsayılan değer HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="5789f-144">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="5789f-145">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="5789f-145">-StartTime</span></span>
<span data-ttu-id="5789f-146">Paylaşılan erişim imzasının geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="5789f-146">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="5789f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5789f-147">CommonParameters</span></span>
<span data-ttu-id="5789f-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5789f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5789f-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5789f-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5789f-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5789f-150">INPUTS</span></span>

### <span data-ttu-id="5789f-151">Microsoft. Windowsazde. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="5789f-151">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="5789f-152">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="5789f-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5789f-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5789f-153">OUTPUTS</span></span>

### <span data-ttu-id="5789f-154">System. String</span><span class="sxs-lookup"><span data-stu-id="5789f-154">System.String</span></span>

## <span data-ttu-id="5789f-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5789f-155">NOTES</span></span>

## <span data-ttu-id="5789f-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5789f-156">RELATED LINKS</span></span>

[<span data-ttu-id="5789f-157">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="5789f-157">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="5789f-158">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="5789f-158">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)