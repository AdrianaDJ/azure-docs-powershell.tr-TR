---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 4bec3773b4446e7467346acd4701fbe75298eac5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934294"
---
# <span data-ttu-id="13b2b-101">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="13b2b-101">Set-AzStorageFileContent</span></span>

## <span data-ttu-id="13b2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13b2b-102">SYNOPSIS</span></span>
<span data-ttu-id="13b2b-103">Dosyanın içeriğini karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="13b2b-103">Uploads the contents of a file.</span></span>

## <span data-ttu-id="13b2b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="13b2b-104">SYNTAX</span></span>

### <span data-ttu-id="13b2b-105">PaylaşımAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="13b2b-105">ShareName (Default)</span></span>
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="13b2b-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="13b2b-106">Share</span></span>
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="13b2b-107">Directory</span><span class="sxs-lookup"><span data-stu-id="13b2b-107">Directory</span></span>
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="13b2b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="13b2b-108">DESCRIPTION</span></span>
<span data-ttu-id="13b2b-109">**Set-AzStorageFileContent** cmdlet 'i, dosyanın içeriğini belirtilen paylaşımda bir dosyaya yükler.</span><span class="sxs-lookup"><span data-stu-id="13b2b-109">The **Set-AzStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="13b2b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="13b2b-110">EXAMPLES</span></span>

### <span data-ttu-id="13b2b-111">Örnek 1: geçerli klasöre dosya yükleme</span><span class="sxs-lookup"><span data-stu-id="13b2b-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="13b2b-112">Bu komut, geçerli klasörde DataFile37 adlı bir dosyayı, Contosoworkingklasöründeki Currentveri dosyası adlı bir dosya olarak yükler.</span><span class="sxs-lookup"><span data-stu-id="13b2b-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="13b2b-113">Örnek 2: geçerli klasördeki tüm dosyaları yükleme</span><span class="sxs-lookup"><span data-stu-id="13b2b-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="13b2b-114">Bu örnekte, geçerli klasördeki tüm dosyaları Container ContosoShare06 kök klasörüne yüklemek için en yaygın Windows PowerShell cmdlet 'leri ve geçerli cmdlet kullanılır.</span><span class="sxs-lookup"><span data-stu-id="13b2b-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="13b2b-115">İlk komut geçerli klasörün adını alır ve $CurrentFolder değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="13b2b-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="13b2b-116">İkinci komut **Get-Azstoragesshare** cmdlet 'Ini kullanarak ContosoShare06 adlı dosya paylaşımını alır ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="13b2b-116">The second command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="13b2b-117">Final komutu, geçerli klasörün içeriğini alır ve her birini Where-Object cmdlet 'ine aktarır ve ardışık düzen işlecini kullanın.</span><span class="sxs-lookup"><span data-stu-id="13b2b-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="13b2b-118">Bu cmdlet dosyaları olmayan nesneleri filtreler ve dosyaları ForEach-Object cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="13b2b-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="13b2b-119">Bu cmdlet, kendisi için uygun yolu oluşturan her dosya için bir betik bloğu çalıştırır ve ardından dosyayı karşıya yüklemek için geçerli cmdlet 'i kullanır.</span><span class="sxs-lookup"><span data-stu-id="13b2b-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="13b2b-120">Sonuçta, bu örnekte karşıya yüklenen diğer dosyalarla ilgili olarak aynı ad ve aynı göreli konum aynıdır.</span><span class="sxs-lookup"><span data-stu-id="13b2b-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="13b2b-121">Betik blokları hakkında daha fazla bilgi için, yazın `Get-Help about_Script_Blocks` .</span><span class="sxs-lookup"><span data-stu-id="13b2b-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

### <span data-ttu-id="13b2b-122">Örnek 3: Azure dosyasına yerel bir dosya yükleyin ve Azure dosyasındaki yerel dosya SMB özelliklerini (dosya Attribut, dosya oluşturma saati, dosya son yazma saati) sunar.</span><span class="sxs-lookup"><span data-stu-id="13b2b-122">Example 3: Upload a local file to an Azure file, and perserve the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>
```
PS C:\>Get-AzStorageFileContent -source $localFilePath -ShareName sample -Path "dir1/file1" -PreserveSMBAttribute
```

<span data-ttu-id="13b2b-123">Bu örnek, bir Azure dosyasına yerel bir dosya yükler ve bu, Azure dosyasındaki yerel dosya SMB özelliklerini (dosya attri</span><span class="sxs-lookup"><span data-stu-id="13b2b-123">This example uploads a local file to an Azure file, and perserves the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>

## <span data-ttu-id="13b2b-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="13b2b-124">PARAMETERS</span></span>

### <span data-ttu-id="13b2b-125">-Iş</span><span class="sxs-lookup"><span data-stu-id="13b2b-125">-AsJob</span></span>
<span data-ttu-id="13b2b-126">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="13b2b-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="13b2b-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="13b2b-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="13b2b-128">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="13b2b-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="13b2b-129">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="13b2b-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="13b2b-130">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="13b2b-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="13b2b-131">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="13b2b-131">-ConcurrentTaskCount</span></span>
<span data-ttu-id="13b2b-132">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="13b2b-132">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="13b2b-133">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="13b2b-133">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="13b2b-134">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="13b2b-134">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="13b2b-135">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="13b2b-135">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="13b2b-136">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="13b2b-136">The default value is 10.</span></span>

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

### <span data-ttu-id="13b2b-137">-Context</span><span class="sxs-lookup"><span data-stu-id="13b2b-137">-Context</span></span>
<span data-ttu-id="13b2b-138">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="13b2b-138">Specifies an Azure storage context.</span></span>
<span data-ttu-id="13b2b-139">Depolama bağlamı edinmek için, [New-AzStorageContext](./New-AzStorageContext.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="13b2b-139">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="13b2b-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13b2b-140">-DefaultProfile</span></span>
<span data-ttu-id="13b2b-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="13b2b-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13b2b-142">-Dizin</span><span class="sxs-lookup"><span data-stu-id="13b2b-142">-Directory</span></span>
<span data-ttu-id="13b2b-143">Bir klasörü **Cloudfiledirectory** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="13b2b-143">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="13b2b-144">Bu cmdlet, dosyayı bu parametrenin belirttiği klasöre yükler.</span><span class="sxs-lookup"><span data-stu-id="13b2b-144">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="13b2b-145">Dizin edinmek için New-AzStorageDirectory cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="13b2b-145">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="13b2b-146">Dizin edinmek için Get-AzStorageFile cmdlet 'ini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="13b2b-146">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="13b2b-147">-Force</span><span class="sxs-lookup"><span data-stu-id="13b2b-147">-Force</span></span>
<span data-ttu-id="13b2b-148">Bu cmdlet 'in var olan bir Azure depolama dosyasının üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="13b2b-148">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="13b2b-149">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="13b2b-149">-PassThru</span></span>
<span data-ttu-id="13b2b-150">Bu cmdlet 'in oluşturduğu veya karşıya yükleyen **Azurestoragefile** nesnesini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="13b2b-150">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="13b2b-151">-Yol</span><span class="sxs-lookup"><span data-stu-id="13b2b-151">-Path</span></span>
<span data-ttu-id="13b2b-152">Bir dosya veya klasörün yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="13b2b-152">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="13b2b-153">Bu cmdlet, içeriği bu parametrenin belirttiği dosyaya veya bu parametrenin belirttiği klasörde karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="13b2b-153">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="13b2b-154">Bir klasör belirtirseniz, bu cmdlet kaynak dosyayla aynı ada sahip bir dosya oluşturur.</span><span class="sxs-lookup"><span data-stu-id="13b2b-154">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="13b2b-155">Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği bu dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="13b2b-155">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="13b2b-156">Var olan bir dosyayı belirtirseniz ve _Force_ parametresini belirtirseniz, bu cmdlet dosya içeriğinin üzerine yazar.</span><span class="sxs-lookup"><span data-stu-id="13b2b-156">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="13b2b-157">Var olan bir dosyayı belirtirseniz ve _Force_ belirtmezseniz, bu cmdlet hiçbir değişiklik yapmaz ve hata verir.</span><span class="sxs-lookup"><span data-stu-id="13b2b-157">If you specify a file that already exists and you do not specify _Force_ , this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="13b2b-158">Varolmayan bir klasörün yolunu belirtirseniz, bu cmdlet hiçbir değişiklik yapmaz ve hata verir.</span><span class="sxs-lookup"><span data-stu-id="13b2b-158">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="13b2b-159">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="13b2b-159">-PreserveSMBAttribute</span></span>
<span data-ttu-id="13b2b-160">Hedef dosyada kaynak dosyası SMB özelliklerini (dosya Attrialın, dosya oluşturma zamanı, dosya son yazma zamanı) saklayın.</span><span class="sxs-lookup"><span data-stu-id="13b2b-160">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="13b2b-161">Bu parametre yalnızca Windows 'ta kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="13b2b-161">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="13b2b-162">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="13b2b-162">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="13b2b-163">İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="13b2b-163">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="13b2b-164">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="13b2b-164">-Share</span></span>
<span data-ttu-id="13b2b-165">Bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="13b2b-165">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="13b2b-166">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımındaki bir dosyaya yükler.</span><span class="sxs-lookup"><span data-stu-id="13b2b-166">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="13b2b-167">**Cloudfileshare** nesnesi edinmek için Get-AzStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="13b2b-167">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="13b2b-168">Bu nesne depolama bağlamını içerir.</span><span class="sxs-lookup"><span data-stu-id="13b2b-168">This object contains the storage context.</span></span>
<span data-ttu-id="13b2b-169">Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="13b2b-169">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="13b2b-170">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="13b2b-170">-ShareName</span></span>
<span data-ttu-id="13b2b-171">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="13b2b-171">Specifies the name of the file share.</span></span>
<span data-ttu-id="13b2b-172">Bu cmdlet, bu parametrenin belirttiği dosya paylaşımındaki bir dosyaya yükler.</span><span class="sxs-lookup"><span data-stu-id="13b2b-172">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="13b2b-173">-Kaynak</span><span class="sxs-lookup"><span data-stu-id="13b2b-173">-Source</span></span>
<span data-ttu-id="13b2b-174">Bu cmdlet 'in karşıya yükleolduğu kaynak dosyayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="13b2b-174">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="13b2b-175">Varolmayan bir dosya belirtirseniz, bu cmdlet bir hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="13b2b-175">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="13b2b-176">-Onay</span><span class="sxs-lookup"><span data-stu-id="13b2b-176">-Confirm</span></span>
<span data-ttu-id="13b2b-177">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="13b2b-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13b2b-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13b2b-178">-WhatIf</span></span>
<span data-ttu-id="13b2b-179">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="13b2b-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13b2b-180">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="13b2b-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13b2b-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13b2b-181">CommonParameters</span></span>
<span data-ttu-id="13b2b-182">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="13b2b-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13b2b-183">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13b2b-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13b2b-184">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="13b2b-184">INPUTS</span></span>

### <span data-ttu-id="13b2b-185">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="13b2b-185">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="13b2b-186">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="13b2b-186">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="13b2b-187">System. String</span><span class="sxs-lookup"><span data-stu-id="13b2b-187">System.String</span></span>

### <span data-ttu-id="13b2b-188">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="13b2b-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="13b2b-189">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="13b2b-189">OUTPUTS</span></span>

### <span data-ttu-id="13b2b-190">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="13b2b-190">Microsoft.Azure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="13b2b-191">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="13b2b-191">NOTES</span></span>

## <span data-ttu-id="13b2b-192">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="13b2b-192">RELATED LINKS</span></span>

[<span data-ttu-id="13b2b-193">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="13b2b-193">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="13b2b-194">Yeni-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="13b2b-194">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="13b2b-195">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="13b2b-195">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)