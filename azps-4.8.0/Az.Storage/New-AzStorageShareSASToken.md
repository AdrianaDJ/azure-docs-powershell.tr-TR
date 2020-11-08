---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
ms.openlocfilehash: 8dbb6f79a61d388aec033030de471092fa16ba77
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107515"
---
# <span data-ttu-id="0b42f-101">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="0b42f-101">New-AzStorageShareSASToken</span></span>

## <span data-ttu-id="0b42f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b42f-102">SYNOPSIS</span></span>
<span data-ttu-id="0b42f-103">Azure depolama paylaşımı için paylaşılan erişim Imza belirteci oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0b42f-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

## <span data-ttu-id="0b42f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b42f-104">SYNTAX</span></span>

### <span data-ttu-id="0b42f-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="0b42f-105">SasPolicy</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b42f-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="0b42f-106">SasPermission</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b42f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b42f-107">DESCRIPTION</span></span>
<span data-ttu-id="0b42f-108">**Yeni-AzStorageShareSASToken** cmdlet 'ı Azure depolama paylaşımı için paylaşılan bir erişim imzası belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b42f-108">The **New-AzStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="0b42f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b42f-109">EXAMPLES</span></span>

### <span data-ttu-id="0b42f-110">Örnek 1: bir paylaşım için paylaşılan erişim imza belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="0b42f-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="0b42f-111">Bu komut, ContosoShare adlı paylaşım için paylaşılan bir Access imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b42f-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="0b42f-112">Örnek 2: ardışık düzeni kullanarak birden çok paylaşılan erişim imza belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="0b42f-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "test" | New-AzStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="0b42f-113">Bu komut, önek testiyle eşleşen tüm depolama paylaşımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="0b42f-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="0b42f-114">Komut, ardışık düzen işlecini kullanarak bunları geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="0b42f-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0b42f-115">Geçerli cmdlet, belirtilen izinlere sahip her bir depolama paylaşımı için paylaşılan bir erişim belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b42f-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="0b42f-116">Örnek 3: paylaşılan erişim ilkesi kullanan bir paylaşılan erişim imza belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="0b42f-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="0b42f-117">Bu komut, ContosoPolicy03 adlı ilkeye sahip olan ContosoShare adındaki bir depolama paylaşımı için paylaşılan bir erişim imzası belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b42f-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="0b42f-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b42f-118">PARAMETERS</span></span>

### <span data-ttu-id="0b42f-119">-Context</span><span class="sxs-lookup"><span data-stu-id="0b42f-119">-Context</span></span>
<span data-ttu-id="0b42f-120">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b42f-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="0b42f-121">Bağlam almak için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0b42f-121">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0b42f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b42f-122">-DefaultProfile</span></span>
<span data-ttu-id="0b42f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b42f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b42f-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="0b42f-124">-ExpiryTime</span></span>
<span data-ttu-id="0b42f-125">Paylaşılan erişim imzasının geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b42f-125">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="0b42f-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="0b42f-126">-FullUri</span></span>
<span data-ttu-id="0b42f-127">Bu cmdlet 'in tam blob URI 'sini ve paylaşılan erişim imza belirtecini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b42f-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="0b42f-128">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="0b42f-128">-IPAddressOrRange</span></span>
<span data-ttu-id="0b42f-129">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b42f-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="0b42f-130">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="0b42f-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="0b42f-131">-İzin</span><span class="sxs-lookup"><span data-stu-id="0b42f-131">-Permission</span></span>
<span data-ttu-id="0b42f-132">Paylaşımın altındaki paylaşım ve dosyalara erişmek için belirteçteki izinleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b42f-132">Specifies the permissions in the token to access the share and files under the share.</span></span>
<span data-ttu-id="0b42f-133">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="0b42f-133">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="0b42f-134">-İlke</span><span class="sxs-lookup"><span data-stu-id="0b42f-134">-Policy</span></span>
<span data-ttu-id="0b42f-135">Bir paylaşım için depolanan erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b42f-135">Specifies the stored access policy for a share.</span></span>

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

### <span data-ttu-id="0b42f-136">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="0b42f-136">-Protocol</span></span>
<span data-ttu-id="0b42f-137">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b42f-137">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="0b42f-138">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0b42f-138">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="0b42f-139">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="0b42f-139">HttpsOnly</span></span>
* <span data-ttu-id="0b42f-140">HttpsOrHttp varsayılan değer HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="0b42f-140">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="0b42f-141">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="0b42f-141">-ShareName</span></span>
<span data-ttu-id="0b42f-142">Depolama paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b42f-142">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b42f-143">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="0b42f-143">-StartTime</span></span>
<span data-ttu-id="0b42f-144">Paylaşılan erişim imzasının geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b42f-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="0b42f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b42f-145">CommonParameters</span></span>
<span data-ttu-id="0b42f-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b42f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b42f-147">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b42f-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b42f-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b42f-148">INPUTS</span></span>

### <span data-ttu-id="0b42f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0b42f-149">System.String</span></span>

### <span data-ttu-id="0b42f-150">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="0b42f-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0b42f-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b42f-151">OUTPUTS</span></span>

### <span data-ttu-id="0b42f-152">System. String</span><span class="sxs-lookup"><span data-stu-id="0b42f-152">System.String</span></span>

## <span data-ttu-id="0b42f-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b42f-153">NOTES</span></span>
* <span data-ttu-id="0b42f-154">Anahtar sözcükler: ortak, Azure, hizmetler, veri, depolama, blob, kuyruk, tablo</span><span class="sxs-lookup"><span data-stu-id="0b42f-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="0b42f-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b42f-155">RELATED LINKS</span></span>

[<span data-ttu-id="0b42f-156">Get-Azstorages,</span><span class="sxs-lookup"><span data-stu-id="0b42f-156">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="0b42f-157">Yeni-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="0b42f-157">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)
