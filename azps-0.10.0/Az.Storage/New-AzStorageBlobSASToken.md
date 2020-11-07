---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: 2d2094c22b2aa3b1ca1bb2107af8cd5f434f0eba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936231"
---
# <span data-ttu-id="d4c42-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d4c42-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="d4c42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4c42-102">SYNOPSIS</span></span>
<span data-ttu-id="d4c42-103">Bir Azure Depolama Blobu için SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d4c42-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="d4c42-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4c42-104">SYNTAX</span></span>

### <span data-ttu-id="d4c42-105">BlobNameWithPermission (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d4c42-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d4c42-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="d4c42-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4c42-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="d4c42-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4c42-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="d4c42-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4c42-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4c42-109">DESCRIPTION</span></span>
<span data-ttu-id="d4c42-110">**Yeni-AzStorageBlobSASToken** cmdlet 'i, bir Azure Depolama Blobu Için paylaşılan erişim IMZASı (SAS) belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d4c42-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="d4c42-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4c42-111">EXAMPLES</span></span>

### <span data-ttu-id="d4c42-112">Örnek 1: tam blob izniyle blob SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="d4c42-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="d4c42-113">Bu örnek tam blob izni olan bir blob SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d4c42-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="d4c42-114">Örnek 2: ömür ile blob SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="d4c42-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="d4c42-115">Bu örnek ömür boyu bir blob SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d4c42-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="d4c42-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4c42-116">PARAMETERS</span></span>

### <span data-ttu-id="d4c42-117">-Blob</span><span class="sxs-lookup"><span data-stu-id="d4c42-117">-Blob</span></span>
<span data-ttu-id="d4c42-118">Depolama blob adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4c42-118">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="d4c42-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="d4c42-119">-CloudBlob</span></span>
<span data-ttu-id="d4c42-120">**Cloudblob** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4c42-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="d4c42-121">**Cloudblob** nesnesi edinmek için [Get-azstorageblob](./Get-AzStorageBlob.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d4c42-121">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4c42-122">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="d4c42-122">-Container</span></span>
<span data-ttu-id="d4c42-123">Depolama kapsayıcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4c42-123">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="d4c42-124">-Context</span><span class="sxs-lookup"><span data-stu-id="d4c42-124">-Context</span></span>
<span data-ttu-id="d4c42-125">Depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4c42-125">Specifies the storage context.</span></span>

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

### <span data-ttu-id="d4c42-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4c42-126">-DefaultProfile</span></span>
<span data-ttu-id="d4c42-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d4c42-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4c42-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d4c42-128">-ExpiryTime</span></span>
<span data-ttu-id="d4c42-129">Paylaşılan erişim imzasının ne zaman sona ereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4c42-129">Specifies when the shared access signature expires.</span></span>

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

### <span data-ttu-id="d4c42-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="d4c42-130">-FullUri</span></span>
<span data-ttu-id="d4c42-131">Bu cmdlet 'in tam blob URI 'sini ve paylaşılan erişim imza belirtecini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4c42-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="d4c42-132">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="d4c42-132">-IPAddressOrRange</span></span>
<span data-ttu-id="d4c42-133">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4c42-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="d4c42-134">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="d4c42-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="d4c42-135">-İzin</span><span class="sxs-lookup"><span data-stu-id="d4c42-135">-Permission</span></span>
<span data-ttu-id="d4c42-136">Bir depolama blob 'una yönelik izinleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4c42-136">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="d4c42-137">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="d4c42-137">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

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

### <span data-ttu-id="d4c42-138">-İlke</span><span class="sxs-lookup"><span data-stu-id="d4c42-138">-Policy</span></span>
<span data-ttu-id="d4c42-139">Azure saklı bir erişim Ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4c42-139">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="d4c42-140">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="d4c42-140">-Protocol</span></span>
<span data-ttu-id="d4c42-141">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4c42-141">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="d4c42-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d4c42-142">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="d4c42-143">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d4c42-143">HttpsOnly</span></span>
* <span data-ttu-id="d4c42-144">HttpsOrHttp varsayılan değer HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="d4c42-144">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAz.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4c42-145">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="d4c42-145">-StartTime</span></span>
<span data-ttu-id="d4c42-146">Paylaşılan erişim imzasının geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4c42-146">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="d4c42-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4c42-147">CommonParameters</span></span>
<span data-ttu-id="d4c42-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4c42-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4c42-149">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4c42-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4c42-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4c42-150">INPUTS</span></span>

### <span data-ttu-id="d4c42-151">Microsoft. WindowsAz. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="d4c42-151">Microsoft.WindowsAz.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="d4c42-152">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="d4c42-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d4c42-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4c42-153">OUTPUTS</span></span>

### <span data-ttu-id="d4c42-154">System. String</span><span class="sxs-lookup"><span data-stu-id="d4c42-154">System.String</span></span>

## <span data-ttu-id="d4c42-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4c42-155">NOTES</span></span>

## <span data-ttu-id="d4c42-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4c42-156">RELATED LINKS</span></span>

[<span data-ttu-id="d4c42-157">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d4c42-157">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="d4c42-158">Yeni-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="d4c42-158">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
