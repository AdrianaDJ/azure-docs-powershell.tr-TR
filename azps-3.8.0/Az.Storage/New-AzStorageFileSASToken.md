---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
ms.openlocfilehash: b38f7d0463062f07e425decae98f8b6acba8c4ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104687"
---
# <span data-ttu-id="3b067-101">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="3b067-101">New-AzStorageFileSASToken</span></span>

## <span data-ttu-id="3b067-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b067-102">SYNOPSIS</span></span>
<span data-ttu-id="3b067-103">Bir depolama dosyası için paylaşılan erişim imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3b067-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="3b067-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b067-104">SYNTAX</span></span>

### <span data-ttu-id="3b067-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="3b067-105">NameSasPermission</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3b067-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="3b067-106">NameSasPolicy</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3b067-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="3b067-107">FileSasPermission</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b067-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="3b067-108">FileSasPolicy</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b067-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b067-109">DESCRIPTION</span></span>
<span data-ttu-id="3b067-110">**New-AzStorageFileSASToken** cmdlet 'ı bir Azure depolama dosyası için paylaşılan bir Access imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3b067-110">The **New-AzStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="3b067-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b067-111">EXAMPLES</span></span>

### <span data-ttu-id="3b067-112">Örnek 1: tam dosya izinlerine sahip paylaşılan bir Access imza belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="3b067-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="3b067-113">Bu komut, DosyaYolu adlı dosya için tam izinleri olan bir paylaşılan erişim imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3b067-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="3b067-114">Örnek 2: zaman sınırlaması olan bir paylaşılan erişim imza belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="3b067-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="3b067-115">İlk komut, Get-Date cmdlet 'ini kullanarak bir **DateTime** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3b067-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="3b067-116">Komut geçerli zamanı $StartTime değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="3b067-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="3b067-117">İkinci komut $StartTime nesneye iki saat ekler ve sonucu $EndTime değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="3b067-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="3b067-118">Bu nesne gelecek saatte iki saat olur.</span><span class="sxs-lookup"><span data-stu-id="3b067-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="3b067-119">Üçüncü komut, belirtilen izinlere sahip paylaşılan bir Access imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3b067-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="3b067-120">Bu belirteç geçerli saatte geçerli olur.</span><span class="sxs-lookup"><span data-stu-id="3b067-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="3b067-121">Belirteç $EndTime saklanıncaya kadar geçerli kalır.</span><span class="sxs-lookup"><span data-stu-id="3b067-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="3b067-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b067-122">PARAMETERS</span></span>

### <span data-ttu-id="3b067-123">-Context</span><span class="sxs-lookup"><span data-stu-id="3b067-123">-Context</span></span>
<span data-ttu-id="3b067-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b067-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="3b067-125">Bağlam almak için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3b067-125">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3b067-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b067-126">-DefaultProfile</span></span>
<span data-ttu-id="3b067-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3b067-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b067-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3b067-128">-ExpiryTime</span></span>
<span data-ttu-id="3b067-129">Paylaşılan erişim imzasının geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b067-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="3b067-130">-Dosya</span><span class="sxs-lookup"><span data-stu-id="3b067-130">-File</span></span>
<span data-ttu-id="3b067-131">Bir **Cloudfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b067-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="3b067-132">Get-AzStorageFile cmdlet 'ini kullanarak bir bulut dosyası oluşturabilir veya bir tane edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b067-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b067-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="3b067-133">-FullUri</span></span>
<span data-ttu-id="3b067-134">Bu cmdlet 'in tam blob URI 'sini ve paylaşılan erişim imza belirtecini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b067-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="3b067-135">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="3b067-135">-IPAddressOrRange</span></span>
<span data-ttu-id="3b067-136">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b067-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="3b067-137">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="3b067-137">The range is inclusive.</span></span>

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

### <span data-ttu-id="3b067-138">-Yol</span><span class="sxs-lookup"><span data-stu-id="3b067-138">-Path</span></span>
<span data-ttu-id="3b067-139">Bir depolama paylaşımına göre dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b067-139">Specifies the path of the file relative to a Storage share.</span></span>

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

### <span data-ttu-id="3b067-140">-İzin</span><span class="sxs-lookup"><span data-stu-id="3b067-140">-Permission</span></span>
<span data-ttu-id="3b067-141">Depolama dosyasının izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b067-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="3b067-142">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="3b067-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="3b067-143">-İlke</span><span class="sxs-lookup"><span data-stu-id="3b067-143">-Policy</span></span>
<span data-ttu-id="3b067-144">Dosya için depolanan erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b067-144">Specifies the stored access policy for a file.</span></span>

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

### <span data-ttu-id="3b067-145">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="3b067-145">-Protocol</span></span>
<span data-ttu-id="3b067-146">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b067-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="3b067-147">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3b067-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="3b067-148">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="3b067-148">HttpsOnly</span></span>
* <span data-ttu-id="3b067-149">HttpsOrHttp varsayılan değer HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="3b067-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="3b067-150">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="3b067-150">-ShareName</span></span>
<span data-ttu-id="3b067-151">Depolama paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b067-151">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="3b067-152">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="3b067-152">-StartTime</span></span>
<span data-ttu-id="3b067-153">Paylaşılan erişim imzasının geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b067-153">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="3b067-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b067-154">CommonParameters</span></span>
<span data-ttu-id="3b067-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b067-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b067-156">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b067-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b067-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b067-157">INPUTS</span></span>

### <span data-ttu-id="3b067-158">System. String</span><span class="sxs-lookup"><span data-stu-id="3b067-158">System.String</span></span>

### <span data-ttu-id="3b067-159">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="3b067-159">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="3b067-160">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="3b067-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3b067-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b067-161">OUTPUTS</span></span>

### <span data-ttu-id="3b067-162">System. String</span><span class="sxs-lookup"><span data-stu-id="3b067-162">System.String</span></span>

## <span data-ttu-id="3b067-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b067-163">NOTES</span></span>

## <span data-ttu-id="3b067-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b067-164">RELATED LINKS</span></span>

[<span data-ttu-id="3b067-165">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3b067-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="3b067-166">Yeni-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="3b067-166">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)
