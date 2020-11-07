---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: aa1c7cebbcb6fe24b06638644d19b07c83c2ff04
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936263"
---
# <span data-ttu-id="1d555-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1d555-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="1d555-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d555-102">SYNOPSIS</span></span>
<span data-ttu-id="1d555-103">Dosyanın içeriğini indirir.</span><span class="sxs-lookup"><span data-stu-id="1d555-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="1d555-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1d555-104">SYNTAX</span></span>

### <span data-ttu-id="1d555-105">PaylaşımAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1d555-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d555-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="1d555-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1d555-107">Directory</span><span class="sxs-lookup"><span data-stu-id="1d555-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1d555-108">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="1d555-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d555-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d555-109">DESCRIPTION</span></span>
<span data-ttu-id="1d555-110">**Get-AzStorageFileContent** cmdlet 'inin içeriğini indirir ve bunu belirttiğiniz bir hedefe kaydeder.</span><span class="sxs-lookup"><span data-stu-id="1d555-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="1d555-111">Bu cmdlet dosyanın içeriğini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="1d555-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="1d555-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1d555-112">EXAMPLES</span></span>

### <span data-ttu-id="1d555-113">Örnek 1: klasörden dosya Indirme</span><span class="sxs-lookup"><span data-stu-id="1d555-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="1d555-114">Bu komut, ContosoShare06 dosya paylaşımı klasöründeki GeçerliVeri dosyası adlı dosyayı geçerli klasöre indirir.</span><span class="sxs-lookup"><span data-stu-id="1d555-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="1d555-115">Örnek 2: örnek dosya paylaşımı altındaki dosyaları Indirir</span><span class="sxs-lookup"><span data-stu-id="1d555-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="1d555-116">Bu örnekte, örnek dosya paylaşımı altındaki dosyalar indirilir</span><span class="sxs-lookup"><span data-stu-id="1d555-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="1d555-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1d555-117">PARAMETERS</span></span>

### <span data-ttu-id="1d555-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="1d555-118">-CheckMd5</span></span>
<span data-ttu-id="1d555-119">Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği yeni dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="1d555-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="1d555-120">Var olan bir dosyanın yolunu belirtirseniz ve *Force* parametresini belirtirseniz, cmdlet dosyanın üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="1d555-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="1d555-121">Var olan bir dosyanın yolunu belirtirseniz ve *Force* belirtmezseniz, cmdlet devam etmeden önce sorar.</span><span class="sxs-lookup"><span data-stu-id="1d555-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="1d555-122">Bir klasörün yolunu belirtirseniz, bu cmdlet, Azure depolama dosyasının adını içeren bir dosya oluşturmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="1d555-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="1d555-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1d555-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1d555-124">Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği yeni dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="1d555-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="1d555-125">Var olan bir dosyanın yolunu belirtirseniz ve *Force* parametresini belirtirseniz, cmdlet dosyanın üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="1d555-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="1d555-126">Var olan bir dosyanın yolunu belirtirseniz ve *Force* belirtmezseniz, cmdlet devam etmeden önce sorar.</span><span class="sxs-lookup"><span data-stu-id="1d555-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="1d555-127">Bir klasörün yolunu belirtirseniz, bu cmdlet, Azure depolama dosyasının adını içeren bir dosya oluşturmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="1d555-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="1d555-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1d555-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1d555-129">Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği yeni dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="1d555-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="1d555-130">Var olan bir dosyanın yolunu belirtirseniz ve *Force* parametresini belirtirseniz, cmdlet dosyanın üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="1d555-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="1d555-131">Var olan bir dosyanın yolunu belirtirseniz ve *Force* belirtmezseniz, cmdlet devam etmeden önce sorar.</span><span class="sxs-lookup"><span data-stu-id="1d555-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="1d555-132">Bir klasörün yolunu belirtirseniz, bu cmdlet, Azure depolama dosyasının adını içeren bir dosya oluşturmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="1d555-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="1d555-133">-Context</span><span class="sxs-lookup"><span data-stu-id="1d555-133">-Context</span></span>
<span data-ttu-id="1d555-134">Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği yeni dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="1d555-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="1d555-135">Var olan bir dosyanın yolunu belirtirseniz ve *Force* parametresini belirtirseniz, cmdlet dosyanın üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="1d555-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="1d555-136">Var olan bir dosyanın yolunu belirtirseniz ve *Force* belirtmezseniz, cmdlet devam etmeden önce sorar.</span><span class="sxs-lookup"><span data-stu-id="1d555-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="1d555-137">Bir klasörün yolunu belirtirseniz, bu cmdlet, Azure depolama dosyasının adını içeren bir dosya oluşturmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="1d555-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="1d555-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d555-138">-DefaultProfile</span></span>
<span data-ttu-id="1d555-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1d555-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d555-140">-Hedef</span><span class="sxs-lookup"><span data-stu-id="1d555-140">-Destination</span></span>
<span data-ttu-id="1d555-141">Hedef yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d555-141">Specifies the destination path.</span></span>
<span data-ttu-id="1d555-142">Bu cmdlet, dosya içeriğini bu parametrenin belirttiği konuma indirir.</span><span class="sxs-lookup"><span data-stu-id="1d555-142">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="1d555-143">Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği yeni dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="1d555-143">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="1d555-144">Var olan bir dosyanın yolunu belirtirseniz ve *Force* parametresini belirtirseniz, cmdlet dosyanın üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="1d555-144">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="1d555-145">Var olan bir dosyanın yolunu belirtirseniz ve *Force* belirtmezseniz, cmdlet devam etmeden önce sorar.</span><span class="sxs-lookup"><span data-stu-id="1d555-145">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="1d555-146">Bir klasörün yolunu belirtirseniz, bu cmdlet, Azure depolama dosyasının adını içeren bir dosya oluşturmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="1d555-146">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="1d555-147">-Dizin</span><span class="sxs-lookup"><span data-stu-id="1d555-147">-Directory</span></span>
<span data-ttu-id="1d555-148">Bir klasörü **Cloudfiledirectory** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d555-148">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="1d555-149">Bu cmdlet, bu parametrenin belirttiği klasördeki bir dosyanın içeriğini alır.</span><span class="sxs-lookup"><span data-stu-id="1d555-149">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="1d555-150">Dizin edinmek için New-AzStorageDirectory cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1d555-150">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="1d555-151">Dizin edinmek için Get-AzStorageFile cmdlet 'ini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d555-151">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="1d555-152">-Dosya</span><span class="sxs-lookup"><span data-stu-id="1d555-152">-File</span></span>
<span data-ttu-id="1d555-153">Bir dosyayı **cloudfile** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d555-153">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="1d555-154">Bu cmdlet, bu parametrenin belirttiği dosyayı alır.</span><span class="sxs-lookup"><span data-stu-id="1d555-154">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="1d555-155">**Cloudfile** nesnesi edinmek için Get-AzStorageFile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1d555-155">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="1d555-156">-Force</span><span class="sxs-lookup"><span data-stu-id="1d555-156">-Force</span></span>
<span data-ttu-id="1d555-157">Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği yeni dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="1d555-157">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="1d555-158">Var olan bir dosyanın yolunu belirtirseniz ve *Force* parametresini belirtirseniz, cmdlet dosyanın üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="1d555-158">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="1d555-159">Var olan bir dosyanın yolunu belirtirseniz ve *Force* belirtmezseniz, cmdlet devam etmeden önce sorar.</span><span class="sxs-lookup"><span data-stu-id="1d555-159">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="1d555-160">Bir klasörün yolunu belirtirseniz, bu cmdlet, Azure depolama dosyasının adını içeren bir dosya oluşturmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="1d555-160">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="1d555-161">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1d555-161">-PassThru</span></span>
<span data-ttu-id="1d555-162">Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği yeni dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="1d555-162">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="1d555-163">Var olan bir dosyanın yolunu belirtirseniz ve *Force* parametresini belirtirseniz, cmdlet dosyanın üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="1d555-163">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="1d555-164">Var olan bir dosyanın yolunu belirtirseniz ve *Force* belirtmezseniz, cmdlet devam etmeden önce sorar.</span><span class="sxs-lookup"><span data-stu-id="1d555-164">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="1d555-165">Bir klasörün yolunu belirtirseniz, bu cmdlet, Azure depolama dosyasının adını içeren bir dosya oluşturmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="1d555-165">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="1d555-166">-Yol</span><span class="sxs-lookup"><span data-stu-id="1d555-166">-Path</span></span>
<span data-ttu-id="1d555-167">Dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d555-167">Specifies the path of a file.</span></span>
<span data-ttu-id="1d555-168">Bu cmdlet, içeriği bu parametrenin belirttiği dosyaya alır.</span><span class="sxs-lookup"><span data-stu-id="1d555-168">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="1d555-169">Dosya yoksa, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="1d555-169">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1d555-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1d555-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1d555-171">Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği yeni dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="1d555-171">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="1d555-172">Var olan bir dosyanın yolunu belirtirseniz ve *Force* parametresini belirtirseniz, cmdlet dosyanın üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="1d555-172">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="1d555-173">Var olan bir dosyanın yolunu belirtirseniz ve *Force* belirtmezseniz, cmdlet devam etmeden önce sorar.</span><span class="sxs-lookup"><span data-stu-id="1d555-173">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="1d555-174">Bir klasörün yolunu belirtirseniz, bu cmdlet, Azure depolama dosyasının adını içeren bir dosya oluşturmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="1d555-174">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="1d555-175">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="1d555-175">-Share</span></span>
<span data-ttu-id="1d555-176">Bir **Cloudfileshare** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d555-176">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="1d555-177">Bu cmdlet, bu parametrenin belirttiği paylaşımın dosya içeriğini indirir.</span><span class="sxs-lookup"><span data-stu-id="1d555-177">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="1d555-178">**Cloudfileshare** nesnesi edinmek için Get-AzStorageShare cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1d555-178">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="1d555-179">Bu nesne depolama bağlamını içerir.</span><span class="sxs-lookup"><span data-stu-id="1d555-179">This object contains the storage context.</span></span>
<span data-ttu-id="1d555-180">Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="1d555-180">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="1d555-181">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="1d555-181">-ShareName</span></span>
<span data-ttu-id="1d555-182">Dosya paylaşımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d555-182">Specifies the name of the file share.</span></span>
<span data-ttu-id="1d555-183">Bu cmdlet, bu parametrenin belirttiği paylaşımın dosya içeriğini indirir.</span><span class="sxs-lookup"><span data-stu-id="1d555-183">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="1d555-184">-Onay</span><span class="sxs-lookup"><span data-stu-id="1d555-184">-Confirm</span></span>
<span data-ttu-id="1d555-185">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1d555-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d555-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d555-186">-WhatIf</span></span>
<span data-ttu-id="1d555-187">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d555-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d555-188">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1d555-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d555-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d555-189">CommonParameters</span></span>
<span data-ttu-id="1d555-190">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1d555-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d555-191">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1d555-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d555-192">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1d555-192">INPUTS</span></span>

### <span data-ttu-id="1d555-193">Microsoft. WindowsAz. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="1d555-193">Microsoft.WindowsAz.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="1d555-194">Parametreler: paylaşma (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1d555-194">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="1d555-195">Microsoft. WindowsAz. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="1d555-195">Microsoft.WindowsAz.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="1d555-196">Parametreler: Dizin (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1d555-196">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="1d555-197">Microsoft. WindowsAz. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="1d555-197">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>
<span data-ttu-id="1d555-198">Parametreler: FILE (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1d555-198">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="1d555-199">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="1d555-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1d555-200">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1d555-200">OUTPUTS</span></span>

### <span data-ttu-id="1d555-201">Microsoft. WindowsAz. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="1d555-201">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>

## <span data-ttu-id="1d555-202">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1d555-202">NOTES</span></span>

## <span data-ttu-id="1d555-203">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1d555-203">RELATED LINKS</span></span>

[<span data-ttu-id="1d555-204">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="1d555-204">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="1d555-205">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1d555-205">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


