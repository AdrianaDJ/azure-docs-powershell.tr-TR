---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 35a4ebeeb456b9234ed61b8010dd66bffd89165b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936159"
---
# <span data-ttu-id="f1419-101">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f1419-101">Set-AzStorageFileContent</span></span>

## <span data-ttu-id="f1419-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1419-102">SYNOPSIS</span></span>
<span data-ttu-id="f1419-103">Dosyanın içeriğini karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="f1419-103">Uploads the contents of a file.</span></span>

## <span data-ttu-id="f1419-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1419-104">SYNTAX</span></span>

### <span data-ttu-id="f1419-105">PaylaşımAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f1419-105">ShareName (Default)</span></span>
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1419-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="f1419-106">Share</span></span>
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1419-107">Directory</span><span class="sxs-lookup"><span data-stu-id="f1419-107">Directory</span></span>
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1419-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1419-108">DESCRIPTION</span></span>
<span data-ttu-id="f1419-109">**Set-AzStorageFileContent** cmdlet 'i, dosyanın içeriğini belirtilen paylaşımda bir dosyaya yükler.</span><span class="sxs-lookup"><span data-stu-id="f1419-109">The **Set-AzStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="f1419-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1419-110">EXAMPLES</span></span>

### <span data-ttu-id="f1419-111">Örnek 1: geçerli klasöre dosya yükleme</span><span class="sxs-lookup"><span data-stu-id="f1419-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="f1419-112">Bu komut, geçerli klasörde DataFile37 adlı bir dosyayı, Contosoworkingklasöründeki Currentveri dosyası adlı bir dosya olarak yükler.</span><span class="sxs-lookup"><span data-stu-id="f1419-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="f1419-113">Örnek 2: geçerli klasördeki tüm dosyaları yükleme</span><span class="sxs-lookup"><span data-stu-id="f1419-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="f1419-114">Bu örnekte, geçerli klasördeki tüm dosyaları Container ContosoShare06 kök klasörüne yüklemek için en yaygın Windows PowerShell cmdlet 'leri ve geçerli cmdlet kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f1419-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="f1419-115">İlk komut geçerli klasörün adını alır ve $CurrentFolder değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f1419-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="f1419-116">İkinci komut **Get-Azstoragesshare** cmdlet 'Ini kullanarak ContosoShare06 adlı dosya paylaşımını alır ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f1419-116">The second command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="f1419-117">Final komutu, geçerli klasörün içeriğini alır ve her birini Where-Object cmdlet 'ine aktarır ve ardışık düzen işlecini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f1419-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f1419-118">Bu cmdlet dosyaları olmayan nesneleri filtreler ve dosyaları ForEach-Object cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="f1419-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="f1419-119">Bu cmdlet, kendisi için uygun yolu oluşturan her dosya için bir betik bloğu çalıştırır ve ardından dosyayı karşıya yüklemek için geçerli cmdlet 'i kullanır.</span><span class="sxs-lookup"><span data-stu-id="f1419-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="f1419-120">Sonuçta, bu örnekte karşıya yüklenen diğer dosyalarla ilgili olarak aynı ad ve aynı göreli konum aynıdır.</span><span class="sxs-lookup"><span data-stu-id="f1419-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="f1419-121">Betik blokları hakkında daha fazla bilgi için, yazın `Get-Help about_Script_Blocks` .</span><span class="sxs-lookup"><span data-stu-id="f1419-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

## <span data-ttu-id="f1419-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1419-122">PARAMETERS</span></span>

### <span data-ttu-id="f1419-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f1419-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f1419-124">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1419-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f1419-125">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="f1419-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f1419-126">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="f1419-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f1419-127">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f1419-127">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f1419-128">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1419-128">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f1419-129">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f1419-129">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f1419-130">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="f1419-130">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f1419-131">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="f1419-131">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f1419-132">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="f1419-132">The default value is 10.</span></span>

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

### <span data-ttu-id="f1419-133">-Context</span><span class="sxs-lookup"><span data-stu-id="f1419-133">-Context</span></span>
<span data-ttu-id="f1419-134">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1419-134">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f1419-135">Depolama bağlamı edinmek için, [New-AzStorageContext](./New-AzStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f1419-135">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="f1419-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1419-136">-DefaultProfile</span></span>
<span data-ttu-id="f1419-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1419-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1419-138">-Dizin</span><span class="sxs-lookup"><span data-stu-id="f1419-138">-Directory</span></span>
<span data-ttu-id="f1419-139">Bir klasörü **Cloudfiledirectory** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1419-139">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="f1419-140">Bu cmdlet, dosyayı bu parametrenin belirttiği klasöre yükler.</span><span class="sxs-lookup"><span data-stu-id="f1419-140">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="f1419-141">Dizin edinmek için New-AzStorageDirectory cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f1419-141">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="f1419-142">Dizin edinmek için Get-AzStorageFile cmdlet 'ini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f1419-142">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1419-143">-Force</span><span class="sxs-lookup"><span data-stu-id="f1419-143">-Force</span></span>
<span data-ttu-id="f1419-144">Bu cmdlet 'in var olan bir Azure depolama dosyasının üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f1419-144">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="f1419-145">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f1419-145">-PassThru</span></span>
<span data-ttu-id="f1419-146">Bu cmdlet 'in oluşturduğu veya karşıya yükleyen **Azurestoragefile** nesnesini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1419-146">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="f1419-147">-Yol</span><span class="sxs-lookup"><span data-stu-id="f1419-147">-Path</span></span>
<span data-ttu-id="f1419-148">Bir dosya veya klasörün yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1419-148">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="f1419-149">Bu cmdlet, içeriği bu parametrenin belirttiği dosyaya veya bu parametrenin belirttiği klasörde karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="f1419-149">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="f1419-150">Bir klasör belirtirseniz, bu cmdlet kaynak dosyayla aynı ada sahip bir dosya oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f1419-150">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="f1419-151">Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği bu dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="f1419-151">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="f1419-152">Var olan bir dosyayı belirtirseniz ve _Force_ parametresini belirtirseniz, bu cmdlet dosya içeriğinin üzerine yazar.</span><span class="sxs-lookup"><span data-stu-id="f1419-152">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="f1419-153">Var olan bir dosyayı belirtirseniz ve _Force_ belirtmezseniz, bu cmdlet hiçbir değişiklik yapmaz ve hata verir.</span><span class="sxs-lookup"><span data-stu-id="f1419-153">If you specify a file that already exists and you do not specify _Force_ , this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="f1419-154">Varolmayan bir klasörün yolunu belirtirseniz, bu cmdlet hiçbir değişiklik yapmaz ve hata verir.</span><span class="sxs-lookup"><span data-stu-id="f1419-154">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1419-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f1419-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f1419-156">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1419-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f1419-157">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="f1419-157">-Share</span></span>
<span data-ttu-id="f1419-158">Bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1419-158">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="f1419-159">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımındaki bir dosyaya yükler.</span><span class="sxs-lookup"><span data-stu-id="f1419-159">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="f1419-160">**Cloudfileshare** nesnesi edinmek için Get-AzStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f1419-160">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="f1419-161">Bu nesne depolama bağlamını içerir.</span><span class="sxs-lookup"><span data-stu-id="f1419-161">This object contains the storage context.</span></span>
<span data-ttu-id="f1419-162">Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="f1419-162">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1419-163">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="f1419-163">-ShareName</span></span>
<span data-ttu-id="f1419-164">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1419-164">Specifies the name of the file share.</span></span>
<span data-ttu-id="f1419-165">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımındaki bir dosyaya yükler.</span><span class="sxs-lookup"><span data-stu-id="f1419-165">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="f1419-166">-Kaynak</span><span class="sxs-lookup"><span data-stu-id="f1419-166">-Source</span></span>
<span data-ttu-id="f1419-167">Bu cmdlet 'in karşıya yükleolduğu kaynak dosyayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1419-167">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="f1419-168">Varolmayan bir dosya belirtirseniz, bu cmdlet bir hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="f1419-168">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1419-169">-Onay</span><span class="sxs-lookup"><span data-stu-id="f1419-169">-Confirm</span></span>
<span data-ttu-id="f1419-170">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f1419-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1419-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1419-171">-WhatIf</span></span>
<span data-ttu-id="f1419-172">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f1419-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1419-173">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f1419-173">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1419-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1419-174">CommonParameters</span></span>
<span data-ttu-id="f1419-175">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1419-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1419-176">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f1419-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1419-177">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1419-177">INPUTS</span></span>

### <span data-ttu-id="f1419-178">Microsoft. WindowsAz. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="f1419-178">Microsoft.WindowsAz.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="f1419-179">Parametreler: paylaşma (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f1419-179">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="f1419-180">Microsoft. WindowsAz. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="f1419-180">Microsoft.WindowsAz.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="f1419-181">Parametreler: Dizin (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f1419-181">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="f1419-182">System. String</span><span class="sxs-lookup"><span data-stu-id="f1419-182">System.String</span></span>

### <span data-ttu-id="f1419-183">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="f1419-183">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f1419-184">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1419-184">OUTPUTS</span></span>

### <span data-ttu-id="f1419-185">Microsoft. WindowsAz. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="f1419-185">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>

## <span data-ttu-id="f1419-186">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1419-186">NOTES</span></span>

## <span data-ttu-id="f1419-187">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1419-187">RELATED LINKS</span></span>

[<span data-ttu-id="f1419-188">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="f1419-188">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="f1419-189">Yeni-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="f1419-189">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="f1419-190">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f1419-190">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)
