---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: 6bcb5163e31f2acbdd3e180cf76aef8fcfb33571
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098615"
---
# <span data-ttu-id="04fc8-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="04fc8-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="04fc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="04fc8-103">Bir Azure Depolama Blobu için SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04fc8-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="04fc8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="04fc8-104">SYNTAX</span></span>

### <span data-ttu-id="04fc8-105">BlobNameWithPermission (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="04fc8-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04fc8-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="04fc8-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04fc8-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="04fc8-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04fc8-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="04fc8-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04fc8-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="04fc8-109">DESCRIPTION</span></span>
<span data-ttu-id="04fc8-110">**Yeni-AzStorageBlobSASToken** cmdlet 'i, bir Azure Depolama Blobu Için paylaşılan erişim IMZASı (SAS) belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04fc8-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="04fc8-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="04fc8-111">EXAMPLES</span></span>

### <span data-ttu-id="04fc8-112">Örnek 1: tam blob izniyle blob SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="04fc8-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="04fc8-113">Bu örnek tam blob izni olan bir blob SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04fc8-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="04fc8-114">Örnek 2: ömür ile blob SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="04fc8-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="04fc8-115">Bu örnek ömür boyu bir blob SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04fc8-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="04fc8-116">Örnek 3: OAuth kimlik doğrulaması tabanlı bir depolama bağlamı olan Kullanıcı kimliği SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="04fc8-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="04fc8-117">Bu örnek, OAuth kimlik doğrulamasını temel alan depolama bağlamı içeren bir kullanıcı kimliği blob SAS belirteci oluşturur</span><span class="sxs-lookup"><span data-stu-id="04fc8-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="04fc8-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="04fc8-118">PARAMETERS</span></span>

### <span data-ttu-id="04fc8-119">-Blob</span><span class="sxs-lookup"><span data-stu-id="04fc8-119">-Blob</span></span>
<span data-ttu-id="04fc8-120">Depolama blob adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="04fc8-120">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="04fc8-121">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="04fc8-121">-CloudBlob</span></span>
<span data-ttu-id="04fc8-122">**Cloudblob** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="04fc8-122">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="04fc8-123">**Cloudblob** nesnesi edinmek için [Get-azstorageblob](./Get-AzStorageBlob.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="04fc8-123">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04fc8-124">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="04fc8-124">-Container</span></span>
<span data-ttu-id="04fc8-125">Depolama kapsayıcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="04fc8-125">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="04fc8-126">-Context</span><span class="sxs-lookup"><span data-stu-id="04fc8-126">-Context</span></span>
<span data-ttu-id="04fc8-127">Depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="04fc8-127">Specifies the storage context.</span></span>
<span data-ttu-id="04fc8-128">Depolama bağlamı OAuth kimlik doğrulamasına dayalı olduğunda, Kullanıcı kimliği blob SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04fc8-128">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="04fc8-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04fc8-129">-DefaultProfile</span></span>
<span data-ttu-id="04fc8-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="04fc8-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04fc8-131">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="04fc8-131">-ExpiryTime</span></span>
<span data-ttu-id="04fc8-132">Paylaşılan erişim imzasının ne zaman sona ereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="04fc8-132">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="04fc8-133">Depolama bağlamı OAuth kimlik doğrulamasına dayalı olduğunda, geçerlilik süresi geçerli saatten 7 gün içinde olmalıdır ve geçerli saatten önce olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="04fc8-133">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="04fc8-134">-FullUri</span><span class="sxs-lookup"><span data-stu-id="04fc8-134">-FullUri</span></span>
<span data-ttu-id="04fc8-135">Bu cmdlet 'in tam blob URI 'sini ve paylaşılan erişim imza belirtecini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="04fc8-135">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="04fc8-136">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="04fc8-136">-IPAddressOrRange</span></span>
<span data-ttu-id="04fc8-137">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="04fc8-137">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="04fc8-138">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="04fc8-138">The range is inclusive.</span></span>

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

### <span data-ttu-id="04fc8-139">-İzin</span><span class="sxs-lookup"><span data-stu-id="04fc8-139">-Permission</span></span>
<span data-ttu-id="04fc8-140">Bir depolama blob 'una yönelik izinleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="04fc8-140">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="04fc8-141">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="04fc8-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

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

### <span data-ttu-id="04fc8-142">-İlke</span><span class="sxs-lookup"><span data-stu-id="04fc8-142">-Policy</span></span>
<span data-ttu-id="04fc8-143">Azure saklı bir erişim Ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="04fc8-143">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="04fc8-144">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="04fc8-144">-Protocol</span></span>
<span data-ttu-id="04fc8-145">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="04fc8-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="04fc8-146">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="04fc8-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="04fc8-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="04fc8-147">HttpsOnly</span></span>
* <span data-ttu-id="04fc8-148">HttpsOrHttp varsayılan değer HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="04fc8-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04fc8-149">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="04fc8-149">-StartTime</span></span>
<span data-ttu-id="04fc8-150">Paylaşılan erişim imzasının geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="04fc8-150">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="04fc8-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="04fc8-151">-Confirm</span></span>
<span data-ttu-id="04fc8-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="04fc8-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04fc8-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04fc8-153">-WhatIf</span></span>
<span data-ttu-id="04fc8-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="04fc8-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04fc8-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="04fc8-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04fc8-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04fc8-156">CommonParameters</span></span>
<span data-ttu-id="04fc8-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="04fc8-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04fc8-158">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04fc8-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04fc8-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="04fc8-159">INPUTS</span></span>

### <span data-ttu-id="04fc8-160">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="04fc8-160">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="04fc8-161">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="04fc8-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="04fc8-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="04fc8-162">OUTPUTS</span></span>

### <span data-ttu-id="04fc8-163">System. String</span><span class="sxs-lookup"><span data-stu-id="04fc8-163">System.String</span></span>

## <span data-ttu-id="04fc8-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="04fc8-164">NOTES</span></span>

## <span data-ttu-id="04fc8-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="04fc8-165">RELATED LINKS</span></span>

[<span data-ttu-id="04fc8-166">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="04fc8-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="04fc8-167">Yeni-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="04fc8-167">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
