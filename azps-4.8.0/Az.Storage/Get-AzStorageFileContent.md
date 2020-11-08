---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 3c90e02194fa761bbb0fc00e11ea09d03ca00c1c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110180"
---
# <span data-ttu-id="bb466-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bb466-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="bb466-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb466-102">SYNOPSIS</span></span>
<span data-ttu-id="bb466-103">Dosyanın içeriğini indirir.</span><span class="sxs-lookup"><span data-stu-id="bb466-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="bb466-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb466-104">SYNTAX</span></span>

### <span data-ttu-id="bb466-105">PaylaşımAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bb466-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="bb466-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="bb466-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="bb466-107">Directory</span><span class="sxs-lookup"><span data-stu-id="bb466-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="bb466-108">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="bb466-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="bb466-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb466-109">DESCRIPTION</span></span>
<span data-ttu-id="bb466-110">**Get-AzStorageFileContent** cmdlet 'inin içeriğini indirir ve bunu belirttiğiniz bir hedefe kaydeder.</span><span class="sxs-lookup"><span data-stu-id="bb466-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="bb466-111">Bu cmdlet dosyanın içeriğini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="bb466-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="bb466-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb466-112">EXAMPLES</span></span>

### <span data-ttu-id="bb466-113">Örnek 1: klasörden dosya Indirme</span><span class="sxs-lookup"><span data-stu-id="bb466-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="bb466-114">Bu komut, ContosoShare06 dosya paylaşımı klasöründeki GeçerliVeri dosyası adlı dosyayı geçerli klasöre indirir.</span><span class="sxs-lookup"><span data-stu-id="bb466-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="bb466-115">Örnek 2: örnek dosya paylaşımı altındaki dosyaları Indirir</span><span class="sxs-lookup"><span data-stu-id="bb466-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="bb466-116">Bu örnekte, örnek dosya paylaşımı altındaki dosyalar indirilir</span><span class="sxs-lookup"><span data-stu-id="bb466-116">This example downloads the files under sample file share</span></span>

### <span data-ttu-id="bb466-117">Örnek 3: yerel dosyaya bir Azure dosyası Indirin ve yerel dosyadaki (dosya Attributu, dosya oluşturma saati, dosya son yazma saati)</span><span class="sxs-lookup"><span data-stu-id="bb466-117">Example 3: Download an Azure file to a local file, and perserve the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

<span data-ttu-id="bb466-118">Bu örnekte, bir Azure dosyası yerel dosyaya indirilir ve yerel dosyadaki (dosya Attributu, dosya oluşturma zamanı, dosya son yazma zamanı)</span><span class="sxs-lookup"><span data-stu-id="bb466-118">This example downloads an Azure file to a local file, and perserves the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>

## <span data-ttu-id="bb466-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb466-119">PARAMETERS</span></span>

### <span data-ttu-id="bb466-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="bb466-120">-AsJob</span></span>
<span data-ttu-id="bb466-121">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="bb466-121">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="bb466-122">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="bb466-122">-CheckMd5</span></span>
<span data-ttu-id="bb466-123">İndirilen dosyanın MD5 toplamının olup olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb466-123">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="bb466-124">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bb466-124">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bb466-125">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb466-125">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="bb466-126">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="bb466-126">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="bb466-127">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="bb466-127">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bb466-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bb466-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bb466-129">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb466-129">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="bb466-130">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb466-130">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="bb466-131">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="bb466-131">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="bb466-132">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="bb466-132">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="bb466-133">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="bb466-133">The default value is 10.</span></span>

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

### <span data-ttu-id="bb466-134">-Context</span><span class="sxs-lookup"><span data-stu-id="bb466-134">-Context</span></span>
<span data-ttu-id="bb466-135">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb466-135">Specifies an Azure Storage context.</span></span> <span data-ttu-id="bb466-136">Bağlam almak için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bb466-136">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bb466-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb466-137">-DefaultProfile</span></span>
<span data-ttu-id="bb466-138">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bb466-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb466-139">-Hedef</span><span class="sxs-lookup"><span data-stu-id="bb466-139">-Destination</span></span>
<span data-ttu-id="bb466-140">Hedef yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb466-140">Specifies the destination path.</span></span>
<span data-ttu-id="bb466-141">Bu cmdlet, dosya içeriğini bu parametrenin belirttiği konuma indirir.</span><span class="sxs-lookup"><span data-stu-id="bb466-141">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="bb466-142">Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği yeni dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="bb466-142">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="bb466-143">Var olan bir dosyanın yolunu belirtirseniz ve *Force* parametresini belirtirseniz, cmdlet dosyanın üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="bb466-143">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="bb466-144">Var olan bir dosyanın yolunu belirtirseniz ve *Force* belirtmezseniz, cmdlet devam etmeden önce sorar.</span><span class="sxs-lookup"><span data-stu-id="bb466-144">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="bb466-145">Bir klasörün yolunu belirtirseniz, bu cmdlet, Azure depolama dosyasının adını içeren bir dosya oluşturmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="bb466-145">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="bb466-146">-Dizin</span><span class="sxs-lookup"><span data-stu-id="bb466-146">-Directory</span></span>
<span data-ttu-id="bb466-147">Bir klasörü **Cloudfiledirectory** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb466-147">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="bb466-148">Bu cmdlet, bu parametrenin belirttiği klasördeki bir dosyanın içeriğini alır.</span><span class="sxs-lookup"><span data-stu-id="bb466-148">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="bb466-149">Dizin edinmek için New-AzStorageDirectory cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bb466-149">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="bb466-150">Dizin edinmek için Get-AzStorageFile cmdlet 'ini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb466-150">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb466-151">-Dosya</span><span class="sxs-lookup"><span data-stu-id="bb466-151">-File</span></span>
<span data-ttu-id="bb466-152">Bir dosyayı **cloudfile** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb466-152">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="bb466-153">Bu cmdlet, bu parametrenin belirttiği dosyayı alır.</span><span class="sxs-lookup"><span data-stu-id="bb466-153">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="bb466-154">**Cloudfile** nesnesi edinmek için Get-AzStorageFile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bb466-154">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb466-155">-Force</span><span class="sxs-lookup"><span data-stu-id="bb466-155">-Force</span></span>
<span data-ttu-id="bb466-156">Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği yeni dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="bb466-156">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="bb466-157">Var olan bir dosyanın yolunu belirtirseniz ve *Force* parametresini belirtirseniz, cmdlet dosyanın üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="bb466-157">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="bb466-158">Var olan bir dosyanın yolunu belirtirseniz ve *Force* belirtmezseniz, cmdlet devam etmeden önce sorar.</span><span class="sxs-lookup"><span data-stu-id="bb466-158">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="bb466-159">Bir klasörün yolunu belirtirseniz, bu cmdlet, Azure depolama dosyasının adını içeren bir dosya oluşturmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="bb466-159">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="bb466-160">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bb466-160">-PassThru</span></span>
<span data-ttu-id="bb466-161">Bu cmdlet 'in indiren **Ragefıle** nesnesini geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bb466-161">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

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

### <span data-ttu-id="bb466-162">-Yol</span><span class="sxs-lookup"><span data-stu-id="bb466-162">-Path</span></span>
<span data-ttu-id="bb466-163">Dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb466-163">Specifies the path of a file.</span></span>
<span data-ttu-id="bb466-164">Bu cmdlet, içeriği bu parametrenin belirttiği dosyaya alır.</span><span class="sxs-lookup"><span data-stu-id="bb466-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="bb466-165">Dosya yoksa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="bb466-165">If the file does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb466-166">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="bb466-166">-PreserveSMBAttribute</span></span>
<span data-ttu-id="bb466-167">Hedef dosyada kaynak dosyası SMB özelliklerini (dosya Attrialın, dosya oluşturma zamanı, dosya son yazma zamanı) saklayın.</span><span class="sxs-lookup"><span data-stu-id="bb466-167">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="bb466-168">Bu parametre yalnızca Windows 'ta kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bb466-168">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="bb466-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bb466-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bb466-170">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb466-170">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="bb466-171">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="bb466-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="bb466-172">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="bb466-172">-Share</span></span>
<span data-ttu-id="bb466-173">Bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb466-173">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="bb466-174">Bu cmdlet, bu parametrenin belirttiği paylaşımın dosya içeriğini indirir.</span><span class="sxs-lookup"><span data-stu-id="bb466-174">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="bb466-175">**Cloudfileshare** nesnesi edinmek için Get-AzStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bb466-175">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="bb466-176">Bu nesne depolama bağlamını içerir.</span><span class="sxs-lookup"><span data-stu-id="bb466-176">This object contains the storage context.</span></span>
<span data-ttu-id="bb466-177">Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="bb466-177">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb466-178">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="bb466-178">-ShareName</span></span>
<span data-ttu-id="bb466-179">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb466-179">Specifies the name of the file share.</span></span>
<span data-ttu-id="bb466-180">Bu cmdlet, bu parametrenin belirttiği paylaşımın dosya içeriğini indirir.</span><span class="sxs-lookup"><span data-stu-id="bb466-180">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="bb466-181">-Onay</span><span class="sxs-lookup"><span data-stu-id="bb466-181">-Confirm</span></span>
<span data-ttu-id="bb466-182">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bb466-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb466-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb466-183">-WhatIf</span></span>
<span data-ttu-id="bb466-184">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bb466-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb466-185">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bb466-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb466-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb466-186">CommonParameters</span></span>
<span data-ttu-id="bb466-187">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb466-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb466-188">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb466-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb466-189">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb466-189">INPUTS</span></span>

### <span data-ttu-id="bb466-190">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="bb466-190">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="bb466-191">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="bb466-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="bb466-192">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="bb466-192">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="bb466-193">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="bb466-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bb466-194">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb466-194">OUTPUTS</span></span>

### <span data-ttu-id="bb466-195">Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="bb466-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="bb466-196">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb466-196">NOTES</span></span>

## <span data-ttu-id="bb466-197">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb466-197">RELATED LINKS</span></span>

[<span data-ttu-id="bb466-198">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="bb466-198">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="bb466-199">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bb466-199">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


