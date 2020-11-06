---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: ''
schema: 2.0.0
ms.openlocfilehash: 427276a496108a48b69fd81cb5835d74859c25b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571913"
---
# <span data-ttu-id="1255c-101">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="1255c-101">New-AzureStorageShareSASToken</span></span>

## <span data-ttu-id="1255c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1255c-102">SYNOPSIS</span></span>
<span data-ttu-id="1255c-103">Azure depolama paylaşımı için paylaşılan erişim Imza belirteci oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1255c-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

## <span data-ttu-id="1255c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1255c-104">SYNTAX</span></span>

### <span data-ttu-id="1255c-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="1255c-105">SasPolicy</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="1255c-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="1255c-106">SasPermission</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="1255c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1255c-107">DESCRIPTION</span></span>
<span data-ttu-id="1255c-108">**New-AzureStorageShareSASToken** cmdlet 'ı bir Azure depolama paylaşımı için paylaşılan erişim imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1255c-108">The **New-AzureStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="1255c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1255c-109">EXAMPLES</span></span>

### <span data-ttu-id="1255c-110">Örnek 1: bir paylaşım için paylaşılan erişim imza belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="1255c-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="1255c-111">Bu komut, ContosoShare adlı paylaşım için paylaşılan bir Access imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1255c-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="1255c-112">Örnek 2: ardışık düzeni kullanarak birden çok paylaşılan erişim imza belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="1255c-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "test" | New-AzureStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="1255c-113">Bu komut, önek testiyle eşleşen tüm depolama paylaşımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="1255c-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="1255c-114">Komut, ardışık düzen işlecini kullanarak bunları geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="1255c-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1255c-115">Geçerli cmdlet, belirtilen izinlere sahip her bir depolama paylaşımı için paylaşılan bir erişim belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1255c-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="1255c-116">Örnek 3: paylaşılan erişim ilkesi kullanan bir paylaşılan erişim imza belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="1255c-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="1255c-117">Bu komut, ContosoPolicy03 adlı ilkeye sahip olan ContosoShare adındaki bir depolama paylaşımı için paylaşılan bir erişim imzası belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1255c-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="1255c-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1255c-118">PARAMETERS</span></span>

### <span data-ttu-id="1255c-119">-Context</span><span class="sxs-lookup"><span data-stu-id="1255c-119">-Context</span></span>
<span data-ttu-id="1255c-120">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1255c-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="1255c-121">Bağlam almak için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1255c-121">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1255c-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="1255c-122">-ExpiryTime</span></span>
<span data-ttu-id="1255c-123">Paylaşılan erişim imzasının geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="1255c-123">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="1255c-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="1255c-124">-FullUri</span></span>
<span data-ttu-id="1255c-125">Bu cmdlet 'in tam blob URI 'sini ve paylaşılan erişim imza belirtecini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1255c-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="1255c-126">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="1255c-126">-IPAddressOrRange</span></span>
<span data-ttu-id="1255c-127">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1255c-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="1255c-128">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="1255c-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="1255c-129">-İzin</span><span class="sxs-lookup"><span data-stu-id="1255c-129">-Permission</span></span>
<span data-ttu-id="1255c-130">Paylaşımın altındaki paylaşım ve dosyalara erişmek için belirteçteki izinleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="1255c-130">Specifies the permissions in the token to access the share and files under the share.</span></span>

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1255c-131">-İlke</span><span class="sxs-lookup"><span data-stu-id="1255c-131">-Policy</span></span>
<span data-ttu-id="1255c-132">Bir paylaşım için depolanan erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1255c-132">Specifies the stored access policy for a share.</span></span>

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1255c-133">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="1255c-133">-Protocol</span></span>
<span data-ttu-id="1255c-134">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1255c-134">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="1255c-135">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1255c-135">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="1255c-136">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="1255c-136">HttpsOnly</span></span>
* <span data-ttu-id="1255c-137">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="1255c-137">HttpsOrHttp</span></span>

<span data-ttu-id="1255c-138">Varsayılan değer HttpsOrHttp değeridir.</span><span class="sxs-lookup"><span data-stu-id="1255c-138">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="1255c-139">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="1255c-139">-ShareName</span></span>
<span data-ttu-id="1255c-140">Depolama paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1255c-140">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1255c-141">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="1255c-141">-StartTime</span></span>
<span data-ttu-id="1255c-142">Paylaşılan erişim imzasının geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="1255c-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="1255c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1255c-143">CommonParameters</span></span>
<span data-ttu-id="1255c-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1255c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1255c-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1255c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1255c-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1255c-146">INPUTS</span></span>

## <span data-ttu-id="1255c-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1255c-147">OUTPUTS</span></span>

## <span data-ttu-id="1255c-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1255c-148">NOTES</span></span>
* <span data-ttu-id="1255c-149">Anahtar sözcükler: ortak, Azure, hizmetler, veri, depolama, blob, kuyruk, tablo</span><span class="sxs-lookup"><span data-stu-id="1255c-149">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="1255c-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1255c-150">RELATED LINKS</span></span>

[<span data-ttu-id="1255c-151">Get-Azurestorages,</span><span class="sxs-lookup"><span data-stu-id="1255c-151">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="1255c-152">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="1255c-152">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)
