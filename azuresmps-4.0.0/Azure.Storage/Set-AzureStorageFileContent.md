---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd066a57ac63b0126120652750c669e6afde36bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571670"
---
# <span data-ttu-id="8bb1a-101">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8bb1a-101">Set-AzureStorageFileContent</span></span>

## <span data-ttu-id="8bb1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bb1a-102">SYNOPSIS</span></span>
<span data-ttu-id="8bb1a-103">Dosyanın içeriğini karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-103">Uploads the contents of a file.</span></span>

## <span data-ttu-id="8bb1a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8bb1a-104">SYNTAX</span></span>

### <span data-ttu-id="8bb1a-105">PaylaşımAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8bb1a-105">ShareName (Default)</span></span>
```
Set-AzureStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bb1a-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="8bb1a-106">Share</span></span>
```
Set-AzureStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bb1a-107">Directory</span><span class="sxs-lookup"><span data-stu-id="8bb1a-107">Directory</span></span>
```
Set-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bb1a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8bb1a-108">DESCRIPTION</span></span>
<span data-ttu-id="8bb1a-109">**Set-AzureStorageFileContent** cmdlet 'i, dosyanın içeriğini belirtilen paylaşımda bir dosyaya yükler.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-109">The **Set-AzureStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="8bb1a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8bb1a-110">EXAMPLES</span></span>

### <span data-ttu-id="8bb1a-111">Örnek 1: geçerli klasöre dosya yükleme</span><span class="sxs-lookup"><span data-stu-id="8bb1a-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzureStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="8bb1a-112">Bu komut, geçerli klasörde DataFile37 adlı bir dosyayı, Contosoworkingklasöründeki Currentveri dosyası adlı bir dosya olarak yükler.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="8bb1a-113">Örnek 2: geçerli klasördeki tüm dosyaları yükleme</span><span class="sxs-lookup"><span data-stu-id="8bb1a-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzureStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzureStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="8bb1a-114">Bu örnekte, geçerli klasördeki tüm dosyaları Container ContosoShare06 kök klasörüne yüklemek için en yaygın Windows PowerShell cmdlet 'leri ve geçerli cmdlet kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>

<span data-ttu-id="8bb1a-115">İlk komut geçerli klasörün adını alır ve $CurrentFolder değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>

<span data-ttu-id="8bb1a-116">İkinci komut, ContosoShare06 adlı dosya paylaşımını almak için **Get-Azurestoragesshare** cmdlet 'ini kullanır ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-116">The second command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="8bb1a-117">Final komutu, geçerli klasörün içeriğini alır ve her birini Where-Object cmdlet 'ine aktarır ve ardışık düzen işlecini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8bb1a-118">Bu cmdlet dosyaları olmayan nesneleri filtreler ve dosyaları ForEach-Object cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="8bb1a-119">Bu cmdlet, kendisi için uygun yolu oluşturan her dosya için bir betik bloğu çalıştırır ve ardından dosyayı karşıya yüklemek için geçerli cmdlet 'i kullanır.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="8bb1a-120">Sonuçta, bu örnekte karşıya yüklenen diğer dosyalarla ilgili olarak aynı ad ve aynı göreli konum aynıdır.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="8bb1a-121">Betik blokları hakkında daha fazla bilgi için, yazın `Get-Help about_Script_Blocks` .</span><span class="sxs-lookup"><span data-stu-id="8bb1a-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

## <span data-ttu-id="8bb1a-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8bb1a-122">PARAMETERS</span></span>

### <span data-ttu-id="8bb1a-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8bb1a-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8bb1a-124">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8bb1a-125">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8bb1a-126">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8bb1a-127">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8bb1a-127">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8bb1a-128">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-128">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8bb1a-129">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-129">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8bb1a-130">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-130">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8bb1a-131">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-131">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8bb1a-132">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-132">The default value is 10.</span></span>

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

### <span data-ttu-id="8bb1a-133">-Context</span><span class="sxs-lookup"><span data-stu-id="8bb1a-133">-Context</span></span>
<span data-ttu-id="8bb1a-134">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-134">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8bb1a-135">Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-135">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="8bb1a-136">-Dizin</span><span class="sxs-lookup"><span data-stu-id="8bb1a-136">-Directory</span></span>
<span data-ttu-id="8bb1a-137">Bir klasörü **Cloudfiledirectory** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="8bb1a-138">Bu cmdlet, dosyayı bu parametrenin belirttiği klasöre yükler.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-138">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="8bb1a-139">Dizin edinmek için New-AzureStorageDirectory cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-139">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="8bb1a-140">Dizin edinmek için Get-AzureStorageFile cmdlet 'ini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-140">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="8bb1a-141">-Force</span><span class="sxs-lookup"><span data-stu-id="8bb1a-141">-Force</span></span>
<span data-ttu-id="8bb1a-142">Bu cmdlet 'in var olan bir Azure depolama dosyasının üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-142">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="8bb1a-143">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8bb1a-143">-PassThru</span></span>
<span data-ttu-id="8bb1a-144">Bu cmdlet 'in oluşturduğu veya karşıya yükleyen **Azurestoragefile** nesnesini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-144">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="8bb1a-145">-Yol</span><span class="sxs-lookup"><span data-stu-id="8bb1a-145">-Path</span></span>
<span data-ttu-id="8bb1a-146">Bir dosya veya klasörün yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-146">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="8bb1a-147">Bu cmdlet, içeriği bu parametrenin belirttiği dosyaya veya bu parametrenin belirttiği klasörde karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-147">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="8bb1a-148">Bir klasör belirtirseniz, bu cmdlet kaynak dosyayla aynı ada sahip bir dosya oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-148">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>

<span data-ttu-id="8bb1a-149">Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği bu dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-149">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="8bb1a-150">Var olan bir dosyayı belirtirseniz ve _Force_ parametresini belirtirseniz, bu cmdlet dosya içeriğinin üzerine yazar.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-150">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="8bb1a-151">Var olan bir dosyayı belirtirseniz ve _Force_ belirtmezseniz, bu cmdlet hiçbir değişiklik yapmaz ve hata verir.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-151">If you specify a file that already exists and you do not specify _Force_ , this cmdlet makes no change, and returns an error.</span></span>

<span data-ttu-id="8bb1a-152">Varolmayan bir klasörün yolunu belirtirseniz, bu cmdlet hiçbir değişiklik yapmaz ve hata verir.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-152">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>


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

### <span data-ttu-id="8bb1a-153">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8bb1a-153">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8bb1a-154">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-154">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="8bb1a-155">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="8bb1a-155">-Share</span></span>
<span data-ttu-id="8bb1a-156">Bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-156">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="8bb1a-157">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımındaki bir dosyaya yükler.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-157">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="8bb1a-158">**Cloudfileshare** nesnesi edinmek için Get-AzureStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-158">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="8bb1a-159">Bu nesne depolama bağlamını içerir.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-159">This object contains the storage context.</span></span>
<span data-ttu-id="8bb1a-160">Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-160">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="8bb1a-161">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="8bb1a-161">-ShareName</span></span>
<span data-ttu-id="8bb1a-162">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-162">Specifies the name of the file share.</span></span>
<span data-ttu-id="8bb1a-163">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımındaki bir dosyaya yükler.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-163">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="8bb1a-164">-Kaynak</span><span class="sxs-lookup"><span data-stu-id="8bb1a-164">-Source</span></span>
<span data-ttu-id="8bb1a-165">Bu cmdlet 'in karşıya yükleolduğu kaynak dosyayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-165">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="8bb1a-166">Varolmayan bir dosya belirtirseniz, bu cmdlet bir hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-166">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8bb1a-167">-Onay</span><span class="sxs-lookup"><span data-stu-id="8bb1a-167">-Confirm</span></span>
<span data-ttu-id="8bb1a-168">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bb1a-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bb1a-169">-WhatIf</span></span>
<span data-ttu-id="8bb1a-170">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bb1a-171">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bb1a-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bb1a-172">CommonParameters</span></span>
<span data-ttu-id="8bb1a-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bb1a-174">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bb1a-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bb1a-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8bb1a-175">INPUTS</span></span>

## <span data-ttu-id="8bb1a-176">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8bb1a-176">OUTPUTS</span></span>

## <span data-ttu-id="8bb1a-177">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8bb1a-177">NOTES</span></span>

## <span data-ttu-id="8bb1a-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8bb1a-178">RELATED LINKS</span></span>

[<span data-ttu-id="8bb1a-179">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="8bb1a-179">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="8bb1a-180">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="8bb1a-180">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="8bb1a-181">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8bb1a-181">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)
