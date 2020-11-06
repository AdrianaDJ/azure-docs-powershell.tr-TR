---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
ms.openlocfilehash: 66c89b70b80cf56471e5d12aec975e4e568d5a1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591510"
---
# <span data-ttu-id="3db95-101">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="3db95-101">New-AzureStorageFileSASToken</span></span>

## <span data-ttu-id="3db95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3db95-102">SYNOPSIS</span></span>
<span data-ttu-id="3db95-103">Bir depolama dosyası için paylaşılan erişim imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3db95-103">Generates a shared access signature token for a Storage file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3db95-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3db95-104">SYNTAX</span></span>

### <span data-ttu-id="3db95-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="3db95-105">NameSasPermission</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3db95-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="3db95-106">NameSasPolicy</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3db95-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="3db95-107">FileSasPermission</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3db95-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="3db95-108">FileSasPolicy</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3db95-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="3db95-109">DESCRIPTION</span></span>
<span data-ttu-id="3db95-110">**New-AzureStorageFileSASToken** cmdlet 'i, bir Azure depolama dosyası için paylaşılan bir Access imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3db95-110">The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="3db95-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3db95-111">EXAMPLES</span></span>

### <span data-ttu-id="3db95-112">Örnek 1: tam dosya izinlerine sahip paylaşılan bir Access imza belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="3db95-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="3db95-113">Bu komut, DosyaYolu adlı dosya için tam izinleri olan bir paylaşılan erişim imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3db95-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="3db95-114">Örnek 2: zaman sınırlaması olan bir paylaşılan erişim imza belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="3db95-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="3db95-115">İlk komut, Get-Date cmdlet 'ini kullanarak bir **DateTime** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3db95-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="3db95-116">Komut geçerli zamanı $StartTime değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="3db95-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="3db95-117">İkinci komut $StartTime nesneye iki saat ekler ve sonucu $EndTime değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="3db95-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="3db95-118">Bu nesne gelecek saatte iki saat olur.</span><span class="sxs-lookup"><span data-stu-id="3db95-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="3db95-119">Üçüncü komut, belirtilen izinlere sahip paylaşılan bir Access imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3db95-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="3db95-120">Bu belirteç geçerli saatte geçerli olur.</span><span class="sxs-lookup"><span data-stu-id="3db95-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="3db95-121">Belirteç $EndTime saklanıncaya kadar geçerli kalır.</span><span class="sxs-lookup"><span data-stu-id="3db95-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="3db95-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3db95-122">PARAMETERS</span></span>

### <span data-ttu-id="3db95-123">-Context</span><span class="sxs-lookup"><span data-stu-id="3db95-123">-Context</span></span>
<span data-ttu-id="3db95-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3db95-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="3db95-125">Bağlam almak için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3db95-125">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3db95-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3db95-126">-DefaultProfile</span></span>
<span data-ttu-id="3db95-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3db95-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3db95-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3db95-128">-ExpiryTime</span></span>
<span data-ttu-id="3db95-129">Paylaşılan erişim imzasının geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="3db95-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="3db95-130">-Dosya</span><span class="sxs-lookup"><span data-stu-id="3db95-130">-File</span></span>
<span data-ttu-id="3db95-131">Bir **Cloudfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="3db95-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="3db95-132">Get-AzureStorageFile cmdlet 'ini kullanarak bir bulut dosyası oluşturabilir veya bir tane edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3db95-132">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3db95-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="3db95-133">-FullUri</span></span>
<span data-ttu-id="3db95-134">Bu cmdlet 'in tam blob URI 'sini ve paylaşılan erişim imza belirtecini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3db95-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="3db95-135">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="3db95-135">-IPAddressOrRange</span></span>
<span data-ttu-id="3db95-136">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3db95-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="3db95-137">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="3db95-137">The range is inclusive.</span></span>

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

### <span data-ttu-id="3db95-138">-Yol</span><span class="sxs-lookup"><span data-stu-id="3db95-138">-Path</span></span>
<span data-ttu-id="3db95-139">Bir depolama paylaşımına göre dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3db95-139">Specifies the path of the file relative to a Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3db95-140">-İzin</span><span class="sxs-lookup"><span data-stu-id="3db95-140">-Permission</span></span>
<span data-ttu-id="3db95-141">Depolama dosyasının izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3db95-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="3db95-142">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="3db95-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3db95-143">-İlke</span><span class="sxs-lookup"><span data-stu-id="3db95-143">-Policy</span></span>
<span data-ttu-id="3db95-144">Dosya için depolanan erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3db95-144">Specifies the stored access policy for a file.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3db95-145">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="3db95-145">-Protocol</span></span>
<span data-ttu-id="3db95-146">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3db95-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="3db95-147">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3db95-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="3db95-148">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="3db95-148">HttpsOnly</span></span>
* <span data-ttu-id="3db95-149">HttpsOrHttp varsayılan değer HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="3db95-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="3db95-150">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="3db95-150">-ShareName</span></span>
<span data-ttu-id="3db95-151">Depolama paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3db95-151">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3db95-152">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="3db95-152">-StartTime</span></span>
<span data-ttu-id="3db95-153">Paylaşılan erişim imzasının geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="3db95-153">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="3db95-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3db95-154">CommonParameters</span></span>
<span data-ttu-id="3db95-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3db95-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3db95-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3db95-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3db95-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3db95-157">INPUTS</span></span>

### <span data-ttu-id="3db95-158">System. String</span><span class="sxs-lookup"><span data-stu-id="3db95-158">System.String</span></span>

### <span data-ttu-id="3db95-159">Microsoft. Windowsazde. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="3db95-159">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="3db95-160">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="3db95-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>
<span data-ttu-id="3db95-161">Parametreler: bağlam (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3db95-161">Parameters: Context (ByValue)</span></span>

## <span data-ttu-id="3db95-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3db95-162">OUTPUTS</span></span>

### <span data-ttu-id="3db95-163">System. String</span><span class="sxs-lookup"><span data-stu-id="3db95-163">System.String</span></span>

## <span data-ttu-id="3db95-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3db95-164">NOTES</span></span>

## <span data-ttu-id="3db95-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3db95-165">RELATED LINKS</span></span>

[<span data-ttu-id="3db95-166">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3db95-166">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="3db95-167">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="3db95-167">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)
