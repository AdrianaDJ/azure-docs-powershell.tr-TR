---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: fb349f2c5c8d394fb7af31190f58ea2ee10425ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277173"
---
# <span data-ttu-id="a814d-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a814d-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="a814d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a814d-102">SYNOPSIS</span></span>
<span data-ttu-id="a814d-103">Bir Azure Depolama Blobu için SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a814d-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="a814d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a814d-104">SYNTAX</span></span>

### <span data-ttu-id="a814d-105">BlobNameWithPermission (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a814d-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a814d-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="a814d-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a814d-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="a814d-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a814d-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="a814d-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a814d-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a814d-109">DESCRIPTION</span></span>
<span data-ttu-id="a814d-110">**Yeni-AzStorageBlobSASToken** cmdlet 'i, bir Azure Depolama Blobu Için paylaşılan erişim IMZASı (SAS) belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a814d-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="a814d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a814d-111">EXAMPLES</span></span>

### <span data-ttu-id="a814d-112">Örnek 1: tam blob izniyle blob SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="a814d-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="a814d-113">Bu örnek tam blob izni olan bir blob SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a814d-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="a814d-114">Örnek 2: ömür ile blob SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="a814d-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="a814d-115">Bu örnek ömür boyu bir blob SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a814d-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="a814d-116">Örnek 3: OAuth kimlik doğrulaması tabanlı bir depolama bağlamı olan Kullanıcı kimliği SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="a814d-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="a814d-117">Bu örnek, OAuth kimlik doğrulamasını temel alan depolama bağlamı içeren bir kullanıcı kimliği blob SAS belirteci oluşturur</span><span class="sxs-lookup"><span data-stu-id="a814d-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="a814d-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a814d-118">PARAMETERS</span></span>

### <span data-ttu-id="a814d-119">-Blob</span><span class="sxs-lookup"><span data-stu-id="a814d-119">-Blob</span></span>
<span data-ttu-id="a814d-120">Depolama blob adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a814d-120">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="a814d-121">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="a814d-121">-BlobBaseClient</span></span>
<span data-ttu-id="a814d-122">BlobBaseClient nesnesi</span><span class="sxs-lookup"><span data-stu-id="a814d-122">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a814d-123">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a814d-123">-CloudBlob</span></span>
<span data-ttu-id="a814d-124">**Cloudblob** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a814d-124">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="a814d-125">**Cloudblob** nesnesi edinmek için [Get-azstorageblob](./Get-AzStorageBlob.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a814d-125">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

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

### <span data-ttu-id="a814d-126">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="a814d-126">-Container</span></span>
<span data-ttu-id="a814d-127">Depolama kapsayıcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a814d-127">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="a814d-128">-Context</span><span class="sxs-lookup"><span data-stu-id="a814d-128">-Context</span></span>
<span data-ttu-id="a814d-129">Depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a814d-129">Specifies the storage context.</span></span>
<span data-ttu-id="a814d-130">Depolama bağlamı OAuth kimlik doğrulamasına dayalı olduğunda, Kullanıcı kimliği blob SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a814d-130">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="a814d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a814d-131">-DefaultProfile</span></span>
<span data-ttu-id="a814d-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a814d-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a814d-133">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a814d-133">-ExpiryTime</span></span>
<span data-ttu-id="a814d-134">Paylaşılan erişim imzasının ne zaman sona ereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a814d-134">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="a814d-135">Depolama bağlamı OAuth kimlik doğrulamasına dayalı olduğunda, geçerlilik süresi geçerli saatten 7 gün içinde olmalıdır ve geçerli saatten önce olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="a814d-135">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="a814d-136">-FullUri</span><span class="sxs-lookup"><span data-stu-id="a814d-136">-FullUri</span></span>
<span data-ttu-id="a814d-137">Bu cmdlet 'in tam blob URI 'sini ve paylaşılan erişim imza belirtecini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a814d-137">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="a814d-138">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="a814d-138">-IPAddressOrRange</span></span>
<span data-ttu-id="a814d-139">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a814d-139">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="a814d-140">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="a814d-140">The range is inclusive.</span></span>

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

### <span data-ttu-id="a814d-141">-İzin</span><span class="sxs-lookup"><span data-stu-id="a814d-141">-Permission</span></span>
<span data-ttu-id="a814d-142">Bir depolama blob 'una yönelik izinleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="a814d-142">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="a814d-143">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="a814d-143">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

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

### <span data-ttu-id="a814d-144">-İlke</span><span class="sxs-lookup"><span data-stu-id="a814d-144">-Policy</span></span>
<span data-ttu-id="a814d-145">Azure saklı bir erişim Ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a814d-145">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="a814d-146">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="a814d-146">-Protocol</span></span>
<span data-ttu-id="a814d-147">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a814d-147">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="a814d-148">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a814d-148">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="a814d-149">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="a814d-149">HttpsOnly</span></span>
* <span data-ttu-id="a814d-150">HttpsOrHttp varsayılan değer HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="a814d-150">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="a814d-151">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="a814d-151">-StartTime</span></span>
<span data-ttu-id="a814d-152">Paylaşılan erişim imzasının geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="a814d-152">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="a814d-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="a814d-153">-Confirm</span></span>
<span data-ttu-id="a814d-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a814d-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a814d-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a814d-155">-WhatIf</span></span>
<span data-ttu-id="a814d-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a814d-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a814d-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a814d-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a814d-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a814d-158">CommonParameters</span></span>
<span data-ttu-id="a814d-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a814d-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a814d-160">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a814d-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a814d-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a814d-161">INPUTS</span></span>

### <span data-ttu-id="a814d-162">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a814d-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="a814d-163">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="a814d-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a814d-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a814d-164">OUTPUTS</span></span>

### <span data-ttu-id="a814d-165">System. String</span><span class="sxs-lookup"><span data-stu-id="a814d-165">System.String</span></span>

## <span data-ttu-id="a814d-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a814d-166">NOTES</span></span>

## <span data-ttu-id="a814d-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a814d-167">RELATED LINKS</span></span>

[<span data-ttu-id="a814d-168">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a814d-168">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="a814d-169">Yeni-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="a814d-169">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
