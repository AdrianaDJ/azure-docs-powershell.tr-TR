---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragesharesastoken
schema: 2.0.0
ms.openlocfilehash: dbfee49f6e6fcd083350a5ab818ac33309e4b672
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939625"
---
# <span data-ttu-id="18fe5-101">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="18fe5-101">New-AzureStorageShareSASToken</span></span>

## <span data-ttu-id="18fe5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="18fe5-103">Azure depolama paylaşımı için paylaşılan erişim Imza belirteci oluşturun.</span><span class="sxs-lookup"><span data-stu-id="18fe5-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18fe5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18fe5-104">SYNTAX</span></span>

### <span data-ttu-id="18fe5-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="18fe5-105">SasPolicy</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18fe5-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="18fe5-106">SasPermission</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18fe5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="18fe5-107">DESCRIPTION</span></span>
<span data-ttu-id="18fe5-108">**New-AzureStorageShareSASToken** cmdlet 'ı bir Azure depolama paylaşımı için paylaşılan erişim imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="18fe5-108">The **New-AzureStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="18fe5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18fe5-109">EXAMPLES</span></span>

### <span data-ttu-id="18fe5-110">Örnek 1: bir paylaşım için paylaşılan erişim imza belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="18fe5-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="18fe5-111">Bu komut, ContosoShare adlı paylaşım için paylaşılan bir Access imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="18fe5-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="18fe5-112">Örnek 2: ardışık düzeni kullanarak birden çok paylaşılan erişim imza belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="18fe5-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "test" | New-AzureStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="18fe5-113">Bu komut, önek testiyle eşleşen tüm depolama paylaşımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="18fe5-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="18fe5-114">Komut, ardışık düzen işlecini kullanarak bunları geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="18fe5-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="18fe5-115">Geçerli cmdlet, belirtilen izinlere sahip her bir depolama paylaşımı için paylaşılan bir erişim belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="18fe5-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="18fe5-116">Örnek 3: paylaşılan erişim ilkesi kullanan bir paylaşılan erişim imza belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="18fe5-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="18fe5-117">Bu komut, ContosoPolicy03 adlı ilkeye sahip olan ContosoShare adındaki bir depolama paylaşımı için paylaşılan bir erişim imzası belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="18fe5-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="18fe5-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18fe5-118">PARAMETERS</span></span>

### <span data-ttu-id="18fe5-119">-Context</span><span class="sxs-lookup"><span data-stu-id="18fe5-119">-Context</span></span>
<span data-ttu-id="18fe5-120">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18fe5-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="18fe5-121">Bağlam almak için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="18fe5-121">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="18fe5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18fe5-122">-DefaultProfile</span></span>
<span data-ttu-id="18fe5-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="18fe5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18fe5-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="18fe5-124">-ExpiryTime</span></span>
<span data-ttu-id="18fe5-125">Paylaşılan erişim imzasının geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="18fe5-125">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="18fe5-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="18fe5-126">-FullUri</span></span>
<span data-ttu-id="18fe5-127">Bu cmdlet 'in tam blob URI 'sini ve paylaşılan erişim imza belirtecini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18fe5-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="18fe5-128">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="18fe5-128">-IPAddressOrRange</span></span>
<span data-ttu-id="18fe5-129">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18fe5-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="18fe5-130">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="18fe5-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="18fe5-131">-İzin</span><span class="sxs-lookup"><span data-stu-id="18fe5-131">-Permission</span></span>
<span data-ttu-id="18fe5-132">Paylaşımın altındaki paylaşım ve dosyalara erişmek için belirteçteki izinleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="18fe5-132">Specifies the permissions in the token to access the share and files under the share.</span></span>
<span data-ttu-id="18fe5-133">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="18fe5-133">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="18fe5-134">-İlke</span><span class="sxs-lookup"><span data-stu-id="18fe5-134">-Policy</span></span>
<span data-ttu-id="18fe5-135">Bir paylaşım için depolanan erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18fe5-135">Specifies the stored access policy for a share.</span></span>

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

### <span data-ttu-id="18fe5-136">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="18fe5-136">-Protocol</span></span>
<span data-ttu-id="18fe5-137">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="18fe5-137">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="18fe5-138">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="18fe5-138">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="18fe5-139">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="18fe5-139">HttpsOnly</span></span>
* <span data-ttu-id="18fe5-140">HttpsOrHttp varsayılan değer HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="18fe5-140">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="18fe5-141">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="18fe5-141">-ShareName</span></span>
<span data-ttu-id="18fe5-142">Depolama paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18fe5-142">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="18fe5-143">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="18fe5-143">-StartTime</span></span>
<span data-ttu-id="18fe5-144">Paylaşılan erişim imzasının geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="18fe5-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="18fe5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18fe5-145">CommonParameters</span></span>
<span data-ttu-id="18fe5-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18fe5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18fe5-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18fe5-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18fe5-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18fe5-148">INPUTS</span></span>

### <span data-ttu-id="18fe5-149">System. String</span><span class="sxs-lookup"><span data-stu-id="18fe5-149">System.String</span></span>

### <span data-ttu-id="18fe5-150">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="18fe5-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="18fe5-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18fe5-151">OUTPUTS</span></span>

### <span data-ttu-id="18fe5-152">System. String</span><span class="sxs-lookup"><span data-stu-id="18fe5-152">System.String</span></span>

## <span data-ttu-id="18fe5-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18fe5-153">NOTES</span></span>
* <span data-ttu-id="18fe5-154">Anahtar sözcükler: ortak, Azure, hizmetler, veri, depolama, blob, kuyruk, tablo</span><span class="sxs-lookup"><span data-stu-id="18fe5-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="18fe5-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18fe5-155">RELATED LINKS</span></span>

[<span data-ttu-id="18fe5-156">Get-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="18fe5-156">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="18fe5-157">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="18fe5-157">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)
