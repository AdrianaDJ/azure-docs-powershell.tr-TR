---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 0777c24aa5cb9b505ffc3495c9a9220da912f055
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758659"
---
# <span data-ttu-id="46ac1-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="46ac1-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="46ac1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="46ac1-103">Dosyanın içeriğini indirir.</span><span class="sxs-lookup"><span data-stu-id="46ac1-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="46ac1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46ac1-104">SYNTAX</span></span>

### <span data-ttu-id="46ac1-105">PaylaşımAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="46ac1-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46ac1-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="46ac1-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46ac1-107">Directory</span><span class="sxs-lookup"><span data-stu-id="46ac1-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46ac1-108">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="46ac1-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46ac1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="46ac1-109">DESCRIPTION</span></span>
<span data-ttu-id="46ac1-110">**Get-AzStorageFileContent** cmdlet 'inin içeriğini indirir ve bunu belirttiğiniz bir hedefe kaydeder.</span><span class="sxs-lookup"><span data-stu-id="46ac1-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="46ac1-111">Bu cmdlet dosyanın içeriğini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="46ac1-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="46ac1-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46ac1-112">EXAMPLES</span></span>

### <span data-ttu-id="46ac1-113">Örnek 1: klasörden dosya Indirme</span><span class="sxs-lookup"><span data-stu-id="46ac1-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="46ac1-114">Bu komut, ContosoShare06 dosya paylaşımı klasöründeki GeçerliVeri dosyası adlı dosyayı geçerli klasöre indirir.</span><span class="sxs-lookup"><span data-stu-id="46ac1-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="46ac1-115">Örnek 2: örnek dosya paylaşımı altındaki dosyaları Indirir</span><span class="sxs-lookup"><span data-stu-id="46ac1-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="46ac1-116">Bu örnekte, örnek dosya paylaşımı altındaki dosyalar indirilir</span><span class="sxs-lookup"><span data-stu-id="46ac1-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="46ac1-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46ac1-117">PARAMETERS</span></span>

### <span data-ttu-id="46ac1-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="46ac1-118">-AsJob</span></span>
<span data-ttu-id="46ac1-119">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="46ac1-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="46ac1-120">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="46ac1-120">-CheckMd5</span></span>
<span data-ttu-id="46ac1-121">İndirilen dosyanın MD5 toplamının olup olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46ac1-121">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="46ac1-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="46ac1-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="46ac1-123">Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="46ac1-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="46ac1-124">Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="46ac1-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="46ac1-125">Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="46ac1-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="46ac1-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="46ac1-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="46ac1-127">Maksimum eşzamanlı ağ çağrılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46ac1-127">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="46ac1-128">Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46ac1-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="46ac1-129">Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.</span><span class="sxs-lookup"><span data-stu-id="46ac1-129">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="46ac1-130">Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.</span><span class="sxs-lookup"><span data-stu-id="46ac1-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="46ac1-131">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="46ac1-131">The default value is 10.</span></span>

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

### <span data-ttu-id="46ac1-132">-Context</span><span class="sxs-lookup"><span data-stu-id="46ac1-132">-Context</span></span>
<span data-ttu-id="46ac1-133">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46ac1-133">Specifies an Azure Storage context.</span></span> <span data-ttu-id="46ac1-134">Bağlam almak için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="46ac1-134">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="46ac1-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46ac1-135">-DefaultProfile</span></span>
<span data-ttu-id="46ac1-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="46ac1-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46ac1-137">-Hedef</span><span class="sxs-lookup"><span data-stu-id="46ac1-137">-Destination</span></span>
<span data-ttu-id="46ac1-138">Hedef yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="46ac1-138">Specifies the destination path.</span></span>
<span data-ttu-id="46ac1-139">Bu cmdlet, dosya içeriğini bu parametrenin belirttiği konuma indirir.</span><span class="sxs-lookup"><span data-stu-id="46ac1-139">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="46ac1-140">Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği yeni dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="46ac1-140">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="46ac1-141">Var olan bir dosyanın yolunu belirtirseniz ve *Force* parametresini belirtirseniz, cmdlet dosyanın üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="46ac1-141">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="46ac1-142">Var olan bir dosyanın yolunu belirtirseniz ve *Force* belirtmezseniz, cmdlet devam etmeden önce sorar.</span><span class="sxs-lookup"><span data-stu-id="46ac1-142">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="46ac1-143">Bir klasörün yolunu belirtirseniz, bu cmdlet, Azure depolama dosyasının adını içeren bir dosya oluşturmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="46ac1-143">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="46ac1-144">-Dizin</span><span class="sxs-lookup"><span data-stu-id="46ac1-144">-Directory</span></span>
<span data-ttu-id="46ac1-145">Bir klasörü **Cloudfiledirectory** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="46ac1-145">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="46ac1-146">Bu cmdlet, bu parametrenin belirttiği klasördeki bir dosyanın içeriğini alır.</span><span class="sxs-lookup"><span data-stu-id="46ac1-146">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="46ac1-147">Dizin edinmek için New-AzStorageDirectory cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="46ac1-147">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="46ac1-148">Dizin edinmek için Get-AzStorageFile cmdlet 'ini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46ac1-148">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="46ac1-149">-Dosya</span><span class="sxs-lookup"><span data-stu-id="46ac1-149">-File</span></span>
<span data-ttu-id="46ac1-150">Bir dosyayı **cloudfile** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="46ac1-150">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="46ac1-151">Bu cmdlet, bu parametrenin belirttiği dosyayı alır.</span><span class="sxs-lookup"><span data-stu-id="46ac1-151">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="46ac1-152">**Cloudfile** nesnesi edinmek için Get-AzStorageFile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="46ac1-152">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46ac1-153">-Force</span><span class="sxs-lookup"><span data-stu-id="46ac1-153">-Force</span></span>
<span data-ttu-id="46ac1-154">Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği yeni dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="46ac1-154">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="46ac1-155">Var olan bir dosyanın yolunu belirtirseniz ve *Force* parametresini belirtirseniz, cmdlet dosyanın üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="46ac1-155">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="46ac1-156">Var olan bir dosyanın yolunu belirtirseniz ve *Force* belirtmezseniz, cmdlet devam etmeden önce sorar.</span><span class="sxs-lookup"><span data-stu-id="46ac1-156">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="46ac1-157">Bir klasörün yolunu belirtirseniz, bu cmdlet, Azure depolama dosyasının adını içeren bir dosya oluşturmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="46ac1-157">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="46ac1-158">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="46ac1-158">-PassThru</span></span>
<span data-ttu-id="46ac1-159">Bu cmdlet 'in indiren **Ragefıle** nesnesini geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46ac1-159">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

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

### <span data-ttu-id="46ac1-160">-Yol</span><span class="sxs-lookup"><span data-stu-id="46ac1-160">-Path</span></span>
<span data-ttu-id="46ac1-161">Dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="46ac1-161">Specifies the path of a file.</span></span>
<span data-ttu-id="46ac1-162">Bu cmdlet, içeriği bu parametrenin belirttiği dosyaya alır.</span><span class="sxs-lookup"><span data-stu-id="46ac1-162">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="46ac1-163">Dosya yoksa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="46ac1-163">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="46ac1-164">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="46ac1-164">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="46ac1-165">İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46ac1-165">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="46ac1-166">Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="46ac1-166">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="46ac1-167">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="46ac1-167">-Share</span></span>
<span data-ttu-id="46ac1-168">Bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="46ac1-168">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="46ac1-169">Bu cmdlet, bu parametrenin belirttiği paylaşımın dosya içeriğini indirir.</span><span class="sxs-lookup"><span data-stu-id="46ac1-169">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="46ac1-170">**Cloudfileshare** nesnesi edinmek için Get-AzStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="46ac1-170">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="46ac1-171">Bu nesne depolama bağlamını içerir.</span><span class="sxs-lookup"><span data-stu-id="46ac1-171">This object contains the storage context.</span></span>
<span data-ttu-id="46ac1-172">Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="46ac1-172">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="46ac1-173">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="46ac1-173">-ShareName</span></span>
<span data-ttu-id="46ac1-174">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46ac1-174">Specifies the name of the file share.</span></span>
<span data-ttu-id="46ac1-175">Bu cmdlet, bu parametrenin belirttiği paylaşımın dosya içeriğini indirir.</span><span class="sxs-lookup"><span data-stu-id="46ac1-175">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="46ac1-176">-Onay</span><span class="sxs-lookup"><span data-stu-id="46ac1-176">-Confirm</span></span>
<span data-ttu-id="46ac1-177">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="46ac1-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46ac1-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46ac1-178">-WhatIf</span></span>
<span data-ttu-id="46ac1-179">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46ac1-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46ac1-180">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="46ac1-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46ac1-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46ac1-181">CommonParameters</span></span>
<span data-ttu-id="46ac1-182">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46ac1-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46ac1-183">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46ac1-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46ac1-184">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46ac1-184">INPUTS</span></span>

### <span data-ttu-id="46ac1-185">Microsoft. Windowsazde. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="46ac1-185">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="46ac1-186">Microsoft. Windowsazde. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="46ac1-186">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="46ac1-187">Microsoft. Windowsazde. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="46ac1-187">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="46ac1-188">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="46ac1-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="46ac1-189">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46ac1-189">OUTPUTS</span></span>

### <span data-ttu-id="46ac1-190">Microsoft. Windowsazde. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="46ac1-190">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="46ac1-191">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46ac1-191">NOTES</span></span>

## <span data-ttu-id="46ac1-192">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46ac1-192">RELATED LINKS</span></span>

[<span data-ttu-id="46ac1-193">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="46ac1-193">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="46ac1-194">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="46ac1-194">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


