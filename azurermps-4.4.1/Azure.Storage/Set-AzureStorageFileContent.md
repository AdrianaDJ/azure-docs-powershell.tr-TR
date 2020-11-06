---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 6f0421c9b442bfc92dc693326542882ba2b0e8d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593872"
---
# <span data-ttu-id="3a72b-101">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3a72b-101">Set-AzureStorageFileContent</span></span>

## <span data-ttu-id="3a72b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a72b-102">SYNOPSIS</span></span>
<span data-ttu-id="3a72b-103">Dosyanın içeriğini karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="3a72b-103">Uploads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a72b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a72b-104">SYNTAX</span></span>

### <span data-ttu-id="3a72b-105">PaylaşımAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3a72b-105">ShareName (Default)</span></span>
```
Set-AzureStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a72b-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="3a72b-106">Share</span></span>
```
Set-AzureStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a72b-107">Directory</span><span class="sxs-lookup"><span data-stu-id="3a72b-107">Directory</span></span>
```
Set-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a72b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a72b-108">DESCRIPTION</span></span>
<span data-ttu-id="3a72b-109">**Set-AzureStorageFileContent** cmdlet 'i, dosyanın içeriğini belirtilen paylaşımda bir dosyaya yükler.</span><span class="sxs-lookup"><span data-stu-id="3a72b-109">The **Set-AzureStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="3a72b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a72b-110">EXAMPLES</span></span>

### <span data-ttu-id="3a72b-111">Örnek 1: geçerli klasöre dosya yükleme</span><span class="sxs-lookup"><span data-stu-id="3a72b-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzureStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="3a72b-112">Bu komut, geçerli klasörde DataFile37 adlı bir dosyayı, Contosoworkingklasöründeki Currentveri dosyası adlı bir dosya olarak yükler.</span><span class="sxs-lookup"><span data-stu-id="3a72b-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="3a72b-113">Örnek 2: geçerli klasördeki tüm dosyaları yükleme</span><span class="sxs-lookup"><span data-stu-id="3a72b-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzureStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzureStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="3a72b-114">Bu örnekte, geçerli klasördeki tüm dosyaları Container ContosoShare06 kök klasörüne yüklemek için en yaygın Windows PowerShell cmdlet 'leri ve geçerli cmdlet kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3a72b-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>

<span data-ttu-id="3a72b-115">İlk komut geçerli klasörün adını alır ve $CurrentFolder değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3a72b-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>

<span data-ttu-id="3a72b-116">İkinci komut, ContosoShare06 adlı dosya paylaşımını almak için **Get-Azurestoragesshare** cmdlet 'ini kullanır ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3a72b-116">The second command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="3a72b-117">Final komutu, geçerli klasörün içeriğini alır ve her birini Where-Object cmdlet 'ine aktarır ve ardışık düzen işlecini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3a72b-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3a72b-118">Bu cmdlet dosyaları olmayan nesneleri filtreler ve dosyaları ForEach-Object cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="3a72b-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="3a72b-119">Bu cmdlet, kendisi için uygun yolu oluşturan her dosya için bir betik bloğu çalıştırır ve ardından dosyayı karşıya yüklemek için geçerli cmdlet 'i kullanır.</span><span class="sxs-lookup"><span data-stu-id="3a72b-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="3a72b-120">Sonuçta, bu örnekte karşıya yüklenen diğer dosyalarla ilgili olarak aynı ad ve aynı göreli konum aynıdır.</span><span class="sxs-lookup"><span data-stu-id="3a72b-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="3a72b-121">Betik blokları hakkında daha fazla bilgi için, yazın `Get-Help about_Script_Blocks` .</span><span class="sxs-lookup"><span data-stu-id="3a72b-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

## <span data-ttu-id="3a72b-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a72b-122">PARAMETERS</span></span>

### <span data-ttu-id="3a72b-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3a72b-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3a72b-124">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a72b-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3a72b-125">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="3a72b-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3a72b-126">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="3a72b-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a72b-127">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3a72b-127">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3a72b-128">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a72b-128">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3a72b-129">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3a72b-129">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3a72b-130">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="3a72b-130">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3a72b-131">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="3a72b-131">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3a72b-132">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="3a72b-132">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a72b-133">-Context</span><span class="sxs-lookup"><span data-stu-id="3a72b-133">-Context</span></span>
<span data-ttu-id="3a72b-134">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a72b-134">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3a72b-135">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3a72b-135">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a72b-136">-Dizin</span><span class="sxs-lookup"><span data-stu-id="3a72b-136">-Directory</span></span>
<span data-ttu-id="3a72b-137">Bir klasörü **Cloudfiledirectory** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a72b-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="3a72b-138">Bu cmdlet, dosyayı bu parametrenin belirttiği klasöre yükler.</span><span class="sxs-lookup"><span data-stu-id="3a72b-138">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="3a72b-139">Dizin edinmek için New-AzureStorageDirectory cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3a72b-139">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="3a72b-140">Dizin edinmek için Get-AzureStorageFile cmdlet 'ini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3a72b-140">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a72b-141">-Force</span><span class="sxs-lookup"><span data-stu-id="3a72b-141">-Force</span></span>
<span data-ttu-id="3a72b-142">Bu cmdlet 'in var olan bir Azure depolama dosyasının üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a72b-142">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="3a72b-143">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3a72b-143">-PassThru</span></span>
<span data-ttu-id="3a72b-144">Bu cmdlet 'in oluşturduğu veya karşıya yükleyen **Azurestoragefile** nesnesini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a72b-144">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="3a72b-145">-Yol</span><span class="sxs-lookup"><span data-stu-id="3a72b-145">-Path</span></span>
<span data-ttu-id="3a72b-146">Bir dosya veya klasörün yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a72b-146">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="3a72b-147">Bu cmdlet, içeriği bu parametrenin belirttiği dosyaya veya bu parametrenin belirttiği klasörde karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="3a72b-147">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="3a72b-148">Bir klasör belirtirseniz, bu cmdlet kaynak dosyayla aynı ada sahip bir dosya oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3a72b-148">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>

<span data-ttu-id="3a72b-149">Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği bu dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="3a72b-149">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="3a72b-150">Var olan bir dosyayı belirtirseniz ve _Force_ parametresini belirtirseniz, bu cmdlet dosya içeriğinin üzerine yazar.</span><span class="sxs-lookup"><span data-stu-id="3a72b-150">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="3a72b-151">Var olan bir dosyayı belirtirseniz ve _Force_ belirtmezseniz, bu cmdlet hiçbir değişiklik yapmaz ve hata verir.</span><span class="sxs-lookup"><span data-stu-id="3a72b-151">If you specify a file that already exists and you do not specify _Force_ , this cmdlet makes no change, and returns an error.</span></span>

<span data-ttu-id="3a72b-152">Varolmayan bir klasörün yolunu belirtirseniz, bu cmdlet hiçbir değişiklik yapmaz ve hata verir.</span><span class="sxs-lookup"><span data-stu-id="3a72b-152">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>


```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a72b-153">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3a72b-153">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3a72b-154">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a72b-154">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a72b-155">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="3a72b-155">-Share</span></span>
<span data-ttu-id="3a72b-156">Bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a72b-156">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="3a72b-157">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımındaki bir dosyaya yükler.</span><span class="sxs-lookup"><span data-stu-id="3a72b-157">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="3a72b-158">**Cloudfileshare** nesnesi edinmek için Get-AzureStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3a72b-158">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="3a72b-159">Bu nesne depolama bağlamını içerir.</span><span class="sxs-lookup"><span data-stu-id="3a72b-159">This object contains the storage context.</span></span>
<span data-ttu-id="3a72b-160">Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="3a72b-160">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a72b-161">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="3a72b-161">-ShareName</span></span>
<span data-ttu-id="3a72b-162">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a72b-162">Specifies the name of the file share.</span></span>
<span data-ttu-id="3a72b-163">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımındaki bir dosyaya yükler.</span><span class="sxs-lookup"><span data-stu-id="3a72b-163">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a72b-164">-Kaynak</span><span class="sxs-lookup"><span data-stu-id="3a72b-164">-Source</span></span>
<span data-ttu-id="3a72b-165">Bu cmdlet 'in karşıya yükleolduğu kaynak dosyayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a72b-165">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="3a72b-166">Varolmayan bir dosya belirtirseniz, bu cmdlet bir hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="3a72b-166">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a72b-167">-Onay</span><span class="sxs-lookup"><span data-stu-id="3a72b-167">-Confirm</span></span>
<span data-ttu-id="3a72b-168">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3a72b-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a72b-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a72b-169">-WhatIf</span></span>
<span data-ttu-id="3a72b-170">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a72b-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a72b-171">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3a72b-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a72b-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a72b-172">CommonParameters</span></span>
<span data-ttu-id="3a72b-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a72b-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a72b-174">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a72b-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a72b-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a72b-175">INPUTS</span></span>

### <span data-ttu-id="3a72b-176">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="3a72b-176">IStorageContext</span></span>

<span data-ttu-id="3a72b-177">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3a72b-177">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="3a72b-178">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="3a72b-178">CloudFileDirectory</span></span>

<span data-ttu-id="3a72b-179">' Directory ' parametresi ardışık düzenin ' CloudFileDirectory ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3a72b-179">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="3a72b-180">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="3a72b-180">CloudFileShare</span></span>

<span data-ttu-id="3a72b-181">' Share ' parametresi ardışık düzenin ' CloudFileShare ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3a72b-181">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="3a72b-182">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a72b-182">OUTPUTS</span></span>

## <span data-ttu-id="3a72b-183">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a72b-183">NOTES</span></span>

## <span data-ttu-id="3a72b-184">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a72b-184">RELATED LINKS</span></span>

[<span data-ttu-id="3a72b-185">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="3a72b-185">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="3a72b-186">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="3a72b-186">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="3a72b-187">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3a72b-187">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)
