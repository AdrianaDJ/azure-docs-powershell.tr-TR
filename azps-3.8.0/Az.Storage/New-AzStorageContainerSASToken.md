---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: 4e265fab8df3abd897c27131e0673241ce37b946
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098084"
---
# <span data-ttu-id="9b106-101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="9b106-101">New-AzStorageContainerSASToken</span></span>

## <span data-ttu-id="9b106-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b106-102">SYNOPSIS</span></span>
<span data-ttu-id="9b106-103">Bir Azure depolama kapsayıcısı için SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9b106-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="9b106-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9b106-104">SYNTAX</span></span>

### <span data-ttu-id="9b106-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="9b106-105">SasPolicy</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b106-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="9b106-106">SasPermission</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b106-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9b106-107">DESCRIPTION</span></span>
<span data-ttu-id="9b106-108">**Yeni-AzStorageContainerSASToken** cmdlet 'i, bir Azure depolama kapsayıcısı Için paylaşılan erişim IMZASı (SAS) belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9b106-108">The **New-AzStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="9b106-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9b106-109">EXAMPLES</span></span>

### <span data-ttu-id="9b106-110">Örnek 1: tam kapsayıcı izniyle kapsayıcı SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="9b106-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="9b106-111">Bu örnek, tam kapsayıcı izni olan bir kapsayıcı SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9b106-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="9b106-112">Örnek 2: ardışık düzene göre birden çok kapsayıcı SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="9b106-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="9b106-113">Bu örnek ardışık düzeni kullanarak birden çok kapsayıcı SAS belirteçleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9b106-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="9b106-114">Örnek 3: paylaşılan erişim ilkesiyle kapsayıcı SAS belirteci oluştur</span><span class="sxs-lookup"><span data-stu-id="9b106-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="9b106-115">Bu örnek, paylaşılan erişim ilkesiyle kapsayıcı SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9b106-115">This example generates a container SAS token with shared access policy.</span></span>

### <span data-ttu-id="9b106-116">Örnek 3: OAuth kimlik doğrulaması tabanlı bir depolama bağlamı olan Kullanıcı kimliği kapsayıcısı SAS belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="9b106-116">Example 3: Generate a User Identity container SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageContainerSASToken -Name "ContainerName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="9b106-117">Bu örnek, OAuth kimlik doğrulaması tabanlı depolama bağlamı olan bir kullanıcı kimliği kapsayıcısı SAS belirteci oluşturur</span><span class="sxs-lookup"><span data-stu-id="9b106-117">This example generates a User Identity container SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="9b106-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9b106-118">PARAMETERS</span></span>

### <span data-ttu-id="9b106-119">-Context</span><span class="sxs-lookup"><span data-stu-id="9b106-119">-Context</span></span>
<span data-ttu-id="9b106-120">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b106-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9b106-121">Bunu, New-AzStorageContext cmdlet 'ini kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9b106-121">You can create it by using the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="9b106-122">Depolama bağlamı OAuth kimlik doğrulamasına dayalı olduğunda, Kullanıcı kimliği kapsayıcısı SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9b106-122">When the storage context is based on OAuth authentication, will generates a User Identity container SAS token.</span></span>

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

### <span data-ttu-id="9b106-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b106-123">-DefaultProfile</span></span>
<span data-ttu-id="9b106-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9b106-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b106-125">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="9b106-125">-ExpiryTime</span></span>
<span data-ttu-id="9b106-126">Paylaşılan erişim imzasının geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b106-126">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="9b106-127">Kullanıcı başlangıç saatini ayarlasa da süre sonu zamanını geçmişse, sona erme saati başlangıç saati artı bir saat ile ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="9b106-127">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="9b106-128">Başlangıç saati veya son kullanma tarihi belirtilmemişse, sona erme süresi geçerli saate bir saat eklenerek bir saat eklenerek ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="9b106-128">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>
<span data-ttu-id="9b106-129">Depolama bağlamı OAuth kimlik doğrulamasına dayalı olduğunda, geçerlilik süresi geçerli saatten 7 gün içinde olmalıdır ve geçerli saatten önce olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="9b106-129">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="9b106-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="9b106-130">-FullUri</span></span>
<span data-ttu-id="9b106-131">Bu cmdlet 'in tam blob URI 'sini ve paylaşılan erişim imza belirtecini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b106-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="9b106-132">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="9b106-132">-IPAddressOrRange</span></span>
<span data-ttu-id="9b106-133">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b106-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="9b106-134">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="9b106-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="9b106-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="9b106-135">-Name</span></span>
<span data-ttu-id="9b106-136">Azure depolama kapsayıcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b106-136">Specifies an Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b106-137">-İzin</span><span class="sxs-lookup"><span data-stu-id="9b106-137">-Permission</span></span>
<span data-ttu-id="9b106-138">Bir depolama kapsayıcısının izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b106-138">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="9b106-139">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="9b106-139">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="9b106-140">-İlke</span><span class="sxs-lookup"><span data-stu-id="9b106-140">-Policy</span></span>
<span data-ttu-id="9b106-141">Azure saklı bir erişim Ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b106-141">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="9b106-142">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="9b106-142">-Protocol</span></span>
<span data-ttu-id="9b106-143">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b106-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="9b106-144">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9b106-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="9b106-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="9b106-145">HttpsOnly</span></span>
* <span data-ttu-id="9b106-146">HttpsOrHttp varsayılan değer HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="9b106-146">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="9b106-147">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="9b106-147">-StartTime</span></span>
<span data-ttu-id="9b106-148">Paylaşılan erişim imzasının geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b106-148">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="9b106-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="9b106-149">-Confirm</span></span>
<span data-ttu-id="9b106-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9b106-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b106-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b106-151">-WhatIf</span></span>
<span data-ttu-id="9b106-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9b106-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b106-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9b106-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b106-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b106-154">CommonParameters</span></span>
<span data-ttu-id="9b106-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9b106-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b106-156">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b106-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b106-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9b106-157">INPUTS</span></span>

### <span data-ttu-id="9b106-158">System. String</span><span class="sxs-lookup"><span data-stu-id="9b106-158">System.String</span></span>

### <span data-ttu-id="9b106-159">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="9b106-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9b106-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9b106-160">OUTPUTS</span></span>

### <span data-ttu-id="9b106-161">System. String</span><span class="sxs-lookup"><span data-stu-id="9b106-161">System.String</span></span>

## <span data-ttu-id="9b106-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9b106-162">NOTES</span></span>

## <span data-ttu-id="9b106-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9b106-163">RELATED LINKS</span></span>

[<span data-ttu-id="9b106-164">Yeni-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="9b106-164">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)
