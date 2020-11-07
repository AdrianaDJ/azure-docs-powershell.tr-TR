---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
ms.openlocfilehash: daf7493ba21673359a11a9cdc4efaa068f629c03
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937386"
---
# <span data-ttu-id="417b2-101">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="417b2-101">New-AzStorageDirectory</span></span>

## <span data-ttu-id="417b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="417b2-102">SYNOPSIS</span></span>
<span data-ttu-id="417b2-103">Dizin oluşturur.</span><span class="sxs-lookup"><span data-stu-id="417b2-103">Creates a directory.</span></span>

## <span data-ttu-id="417b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="417b2-104">SYNTAX</span></span>

### <span data-ttu-id="417b2-105">PaylaşımAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="417b2-105">ShareName (Default)</span></span>
```
New-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="417b2-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="417b2-106">Share</span></span>
```
New-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="417b2-107">Directory</span><span class="sxs-lookup"><span data-stu-id="417b2-107">Directory</span></span>
```
New-AzStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="417b2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="417b2-108">DESCRIPTION</span></span>
<span data-ttu-id="417b2-109">**Yeni-AzStorageDirectory** cmdlet 'i bir dizin oluşturur.</span><span class="sxs-lookup"><span data-stu-id="417b2-109">The **New-AzStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="417b2-110">Bu cmdlet, bir **Cloudfiledirectory** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="417b2-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="417b2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="417b2-111">EXAMPLES</span></span>

### <span data-ttu-id="417b2-112">Örnek 1: dosya paylaşımında klasör oluşturma</span><span class="sxs-lookup"><span data-stu-id="417b2-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="417b2-113">Bu komut, ContosoShare06 adlı dosya paylaşımında Contosoworkingklasörü adlı bir klasör oluşturur.</span><span class="sxs-lookup"><span data-stu-id="417b2-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="417b2-114">Örnek 2: dosya paylaşımı nesnesinde belirtilen dosya paylaşımında klasör oluşturma</span><span class="sxs-lookup"><span data-stu-id="417b2-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | New-AzStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="417b2-115">Bu komut, ContosoShare06 adlı dosya paylaşımını almak için **Get-Azstoragesshare** cmdlet 'ini kullanır ve ardından ardışık düzen işlecini kullanarak bunu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="417b2-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="417b2-116">Current cmdlet, ContosoShare06 'da Contosoworkingklasörü adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="417b2-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="417b2-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="417b2-117">PARAMETERS</span></span>

### <span data-ttu-id="417b2-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="417b2-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="417b2-119">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="417b2-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="417b2-120">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="417b2-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="417b2-121">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="417b2-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="417b2-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="417b2-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="417b2-123">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="417b2-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="417b2-124">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="417b2-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="417b2-125">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="417b2-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="417b2-126">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="417b2-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="417b2-127">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="417b2-127">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="417b2-128">-Context</span><span class="sxs-lookup"><span data-stu-id="417b2-128">-Context</span></span>
<span data-ttu-id="417b2-129">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="417b2-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="417b2-130">Depolama bağlamı edinmek için, [New-AzStorageContext](./New-AzStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="417b2-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="417b2-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="417b2-131">-DefaultProfile</span></span>
<span data-ttu-id="417b2-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="417b2-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="417b2-133">-Dizin</span><span class="sxs-lookup"><span data-stu-id="417b2-133">-Directory</span></span>
<span data-ttu-id="417b2-134">Bir klasörü **Cloudfiledirectory** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="417b2-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="417b2-135">Bu cmdlet, klasörü bu parametrenin belirttiği konumda oluşturur.</span><span class="sxs-lookup"><span data-stu-id="417b2-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="417b2-136">Dizin edinmek için New-AzStorageDirectory cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="417b2-136">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="417b2-137">Dizin edinmek için Get-AzStorageFile cmdlet 'ini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="417b2-137">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="417b2-138">-Yol</span><span class="sxs-lookup"><span data-stu-id="417b2-138">-Path</span></span>
<span data-ttu-id="417b2-139">Klasörün yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="417b2-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="417b2-140">Bu cmdlet, bu cmdlet 'in belirttiği yol için bir klasör oluşturur.</span><span class="sxs-lookup"><span data-stu-id="417b2-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="417b2-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="417b2-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="417b2-142">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="417b2-142">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="417b2-143">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="417b2-143">-Share</span></span>
<span data-ttu-id="417b2-144">Bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="417b2-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="417b2-145">Bu cmdlet, dosya paylaşımında bu parametrenin belirttiği bir klasör oluşturur.</span><span class="sxs-lookup"><span data-stu-id="417b2-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="417b2-146">**Cloudfileshare** nesnesi edinmek için Get-AzStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="417b2-146">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="417b2-147">Bu nesne depolama bağlamını içerir.</span><span class="sxs-lookup"><span data-stu-id="417b2-147">This object contains the storage context.</span></span>
<span data-ttu-id="417b2-148">Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="417b2-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="417b2-149">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="417b2-149">-ShareName</span></span>
<span data-ttu-id="417b2-150">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="417b2-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="417b2-151">Bu cmdlet, dosya paylaşımında bu parametrenin belirttiği bir klasör oluşturur.</span><span class="sxs-lookup"><span data-stu-id="417b2-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="417b2-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="417b2-152">CommonParameters</span></span>
<span data-ttu-id="417b2-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="417b2-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="417b2-154">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="417b2-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="417b2-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="417b2-155">INPUTS</span></span>

### <span data-ttu-id="417b2-156">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="417b2-156">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="417b2-157">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="417b2-157">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="417b2-158">System. String</span><span class="sxs-lookup"><span data-stu-id="417b2-158">System.String</span></span>

### <span data-ttu-id="417b2-159">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="417b2-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="417b2-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="417b2-160">OUTPUTS</span></span>

### <span data-ttu-id="417b2-161">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="417b2-161">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="417b2-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="417b2-162">NOTES</span></span>

## <span data-ttu-id="417b2-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="417b2-163">RELATED LINKS</span></span>

[<span data-ttu-id="417b2-164">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="417b2-164">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="417b2-165">Get-Azstorages,</span><span class="sxs-lookup"><span data-stu-id="417b2-165">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="417b2-166">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="417b2-166">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="417b2-167">Yeni-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="417b2-167">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="417b2-168">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="417b2-168">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)
