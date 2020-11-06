---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
ms.openlocfilehash: e5e4eaf5fa6808432dfdb04120bf9ef92a98452b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590568"
---
# <span data-ttu-id="e05ef-101">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="e05ef-101">New-AzureStorageFileSASToken</span></span>

## <span data-ttu-id="e05ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e05ef-102">SYNOPSIS</span></span>
<span data-ttu-id="e05ef-103">Bir depolama dosyası için paylaşılan erişim imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e05ef-103">Generates a shared access signature token for a Storage file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e05ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e05ef-104">SYNTAX</span></span>

### <span data-ttu-id="e05ef-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="e05ef-105">NameSasPermission</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="e05ef-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="e05ef-106">NameSasPolicy</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="e05ef-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="e05ef-107">FileSasPermission</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

### <span data-ttu-id="e05ef-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="e05ef-108">FileSasPolicy</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

## <span data-ttu-id="e05ef-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="e05ef-109">DESCRIPTION</span></span>
<span data-ttu-id="e05ef-110">**New-AzureStorageFileSASToken** cmdlet 'i, bir Azure depolama dosyası için paylaşılan bir Access imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e05ef-110">The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="e05ef-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e05ef-111">EXAMPLES</span></span>

### <span data-ttu-id="e05ef-112">Örnek 1: tam dosya izinlerine sahip paylaşılan bir Access imza belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="e05ef-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="e05ef-113">Bu komut, DosyaYolu adlı dosya için tam izinleri olan bir paylaşılan erişim imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e05ef-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="e05ef-114">Örnek 2: zaman sınırlaması olan bir paylaşılan erişim imza belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="e05ef-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="e05ef-115">İlk komut, Get-Date cmdlet 'ini kullanarak bir **DateTime** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e05ef-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="e05ef-116">Komut geçerli zamanı $StartTime değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="e05ef-116">The command stores the current time in the $StartTime variable.</span></span>

<span data-ttu-id="e05ef-117">İkinci komut $StartTime nesneye iki saat ekler ve sonucu $EndTime değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="e05ef-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="e05ef-118">Bu nesne gelecek saatte iki saat olur.</span><span class="sxs-lookup"><span data-stu-id="e05ef-118">This object is a time two hours in the future.</span></span>

<span data-ttu-id="e05ef-119">Üçüncü komut, belirtilen izinlere sahip paylaşılan bir Access imza belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e05ef-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="e05ef-120">Bu belirteç geçerli saatte geçerli olur.</span><span class="sxs-lookup"><span data-stu-id="e05ef-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="e05ef-121">Belirteç $EndTime saklanıncaya kadar geçerli kalır.</span><span class="sxs-lookup"><span data-stu-id="e05ef-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="e05ef-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e05ef-122">PARAMETERS</span></span>

### <span data-ttu-id="e05ef-123">-Context</span><span class="sxs-lookup"><span data-stu-id="e05ef-123">-Context</span></span>
<span data-ttu-id="e05ef-124">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e05ef-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="e05ef-125">Bağlam almak için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e05ef-125">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e05ef-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e05ef-126">-ExpiryTime</span></span>
<span data-ttu-id="e05ef-127">Paylaşılan erişim imzasının geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e05ef-127">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="e05ef-128">-Dosya</span><span class="sxs-lookup"><span data-stu-id="e05ef-128">-File</span></span>
<span data-ttu-id="e05ef-129">Bir **Cloudfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e05ef-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="e05ef-130">Get-AzureStorageFile cmdlet 'ini kullanarak bir bulut dosyası oluşturabilir veya bir tane edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e05ef-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e05ef-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="e05ef-131">-FullUri</span></span>
<span data-ttu-id="e05ef-132">Bu cmdlet 'in tam blob URI 'sini ve paylaşılan erişim imza belirtecini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e05ef-132">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="e05ef-133">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="e05ef-133">-IPAddressOrRange</span></span>
<span data-ttu-id="e05ef-134">168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e05ef-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="e05ef-135">Bu Aralık dahil.</span><span class="sxs-lookup"><span data-stu-id="e05ef-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="e05ef-136">-Yol</span><span class="sxs-lookup"><span data-stu-id="e05ef-136">-Path</span></span>
<span data-ttu-id="e05ef-137">Bir depolama paylaşımına göre dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e05ef-137">Specifies the path of the file relative to a Storage share.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e05ef-138">-İzin</span><span class="sxs-lookup"><span data-stu-id="e05ef-138">-Permission</span></span>
<span data-ttu-id="e05ef-139">Depolama dosyasının izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e05ef-139">Specifies the permissions for a Storage file.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05ef-140">-İlke</span><span class="sxs-lookup"><span data-stu-id="e05ef-140">-Policy</span></span>
<span data-ttu-id="e05ef-141">Dosya için depolanan erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e05ef-141">Specifies the stored access policy for a file.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05ef-142">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="e05ef-142">-Protocol</span></span>
<span data-ttu-id="e05ef-143">Bir istek için izin verilen protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e05ef-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="e05ef-144">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e05ef-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="e05ef-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="e05ef-145">HttpsOnly</span></span>
* <span data-ttu-id="e05ef-146">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="e05ef-146">HttpsOrHttp</span></span>

<span data-ttu-id="e05ef-147">Varsayılan değer HttpsOrHttp değeridir.</span><span class="sxs-lookup"><span data-stu-id="e05ef-147">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="e05ef-148">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="e05ef-148">-ShareName</span></span>
<span data-ttu-id="e05ef-149">Depolama paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e05ef-149">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e05ef-150">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="e05ef-150">-StartTime</span></span>
<span data-ttu-id="e05ef-151">Paylaşılan erişim imzasının geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="e05ef-151">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="e05ef-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e05ef-152">CommonParameters</span></span>
<span data-ttu-id="e05ef-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e05ef-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e05ef-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e05ef-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e05ef-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e05ef-155">INPUTS</span></span>

### <span data-ttu-id="e05ef-156">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="e05ef-156">IStorageContext</span></span>

<span data-ttu-id="e05ef-157">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e05ef-157">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="e05ef-158">CloudFile</span><span class="sxs-lookup"><span data-stu-id="e05ef-158">CloudFile</span></span>

<span data-ttu-id="e05ef-159">' File ' parametresi ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="e05ef-159">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="e05ef-160">Dizisi</span><span class="sxs-lookup"><span data-stu-id="e05ef-160">String</span></span>

<span data-ttu-id="e05ef-161">' Path ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e05ef-161">Parameter 'Path' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="e05ef-162">Dizisi</span><span class="sxs-lookup"><span data-stu-id="e05ef-162">String</span></span>

<span data-ttu-id="e05ef-163">' PaylaşımAdı ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e05ef-163">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="e05ef-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e05ef-164">OUTPUTS</span></span>

### <span data-ttu-id="e05ef-165">System. String</span><span class="sxs-lookup"><span data-stu-id="e05ef-165">System.String</span></span>

## <span data-ttu-id="e05ef-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e05ef-166">NOTES</span></span>

## <span data-ttu-id="e05ef-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e05ef-167">RELATED LINKS</span></span>

[<span data-ttu-id="e05ef-168">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e05ef-168">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e05ef-169">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="e05ef-169">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)
