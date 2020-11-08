---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2itemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
ms.openlocfilehash: 9721305494ffd9b1d6a6f260008f050c9600437a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096727"
---
# <span data-ttu-id="b67b9-101">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="b67b9-101">Get-AzDataLakeGen2ItemContent</span></span>

## <span data-ttu-id="b67b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b67b9-102">SYNOPSIS</span></span>
<span data-ttu-id="b67b9-103">Dosyayı indirin.</span><span class="sxs-lookup"><span data-stu-id="b67b9-103">Download a file.</span></span>

## <span data-ttu-id="b67b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b67b9-104">SYNTAX</span></span>

### <span data-ttu-id="b67b9-105">ReceiveManual (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b67b9-105">ReceiveManual (Default)</span></span>
```
Get-AzDataLakeGen2ItemContent [-FileSystem] <String> [-Path] <String> [-Destination <String>] [-CheckMd5]
 [-Force] [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b67b9-106">Itempipeline</span><span class="sxs-lookup"><span data-stu-id="b67b9-106">ItemPipeline</span></span>
```
Get-AzDataLakeGen2ItemContent -InputObject <AzureDataLakeGen2Item> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b67b9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b67b9-107">DESCRIPTION</span></span>
<span data-ttu-id="b67b9-108">**Get-AzDataLakeGen2ItemContent** cmdlet 'ı bir Azure depolama hesabındaki FileSystem 'da bir dosyayı indirin.</span><span class="sxs-lookup"><span data-stu-id="b67b9-108">The **Get-AzDataLakeGen2ItemContent** cmdlet download a file in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="b67b9-109">Bu cmdlet yalnızca depolama hesabı için hiyerarşik ad alanı etkinleştirilmişse çalışır.</span><span class="sxs-lookup"><span data-stu-id="b67b9-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="b67b9-110">Bu hesap türü, "New-AzStorageAccount" cmdlet 'i "-EnableHierarchicalNamespace $true" ile çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="b67b9-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="b67b9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b67b9-111">EXAMPLES</span></span>

### <span data-ttu-id="b67b9-112">Örnek 1: sormadan dosya Indir</span><span class="sxs-lookup"><span data-stu-id="b67b9-112">Example 1: Download a file without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2ItemContent -FileSystem "filesystem1" -Path "dir1/file1" -Destination $localDestFile -Force

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="b67b9-113">Bu komut, dosyayı sormadan yerel bir dosyaya indirir.</span><span class="sxs-lookup"><span data-stu-id="b67b9-113">This command downloads a file to a local file without prompt.</span></span>

### <span data-ttu-id="b67b9-114">Örnek 2: dosya alma, ardından dosyayı yerel dosyaya indirme</span><span class="sxs-lookup"><span data-stu-id="b67b9-114">Example 2: Get a file, then pipeline to download the file to a local file</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" |  Get-AzDataLakeGen2ItemContent -Destination $localDestFile 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="b67b9-115">Bu komut önce dosyayı alır, ardından bir yerel dosyaya indirmek için ardışık düzen.</span><span class="sxs-lookup"><span data-stu-id="b67b9-115">This command first gets a file, then pipeline to download the file to a local file.</span></span>

## <span data-ttu-id="b67b9-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b67b9-116">PARAMETERS</span></span>

### <span data-ttu-id="b67b9-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="b67b9-117">-AsJob</span></span>
<span data-ttu-id="b67b9-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b67b9-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b67b9-119">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="b67b9-119">-CheckMd5</span></span>
<span data-ttu-id="b67b9-120">md5sum</span><span class="sxs-lookup"><span data-stu-id="b67b9-120">check the md5sum</span></span>

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

### <span data-ttu-id="b67b9-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b67b9-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b67b9-122">Eşzamanlı eşzamansız görevlerin toplam miktarı.</span><span class="sxs-lookup"><span data-stu-id="b67b9-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="b67b9-123">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="b67b9-123">The default value is 10.</span></span>

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

### <span data-ttu-id="b67b9-124">-Context</span><span class="sxs-lookup"><span data-stu-id="b67b9-124">-Context</span></span>
<span data-ttu-id="b67b9-125">Azure depolama bağlamı nesnesi</span><span class="sxs-lookup"><span data-stu-id="b67b9-125">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b67b9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b67b9-126">-DefaultProfile</span></span>
<span data-ttu-id="b67b9-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b67b9-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b67b9-128">-Hedef</span><span class="sxs-lookup"><span data-stu-id="b67b9-128">-Destination</span></span>
<span data-ttu-id="b67b9-129">Hedef yerel dosya yolu.</span><span class="sxs-lookup"><span data-stu-id="b67b9-129">Destination local file path.</span></span>

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

### <span data-ttu-id="b67b9-130">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="b67b9-130">-FileSystem</span></span>
<span data-ttu-id="b67b9-131">FileSystem adı</span><span class="sxs-lookup"><span data-stu-id="b67b9-131">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b67b9-132">-Force</span><span class="sxs-lookup"><span data-stu-id="b67b9-132">-Force</span></span>
<span data-ttu-id="b67b9-133">Var olan blob veya dosyanın üzerine yazmayı zorla</span><span class="sxs-lookup"><span data-stu-id="b67b9-133">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="b67b9-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b67b9-134">-InputObject</span></span>
<span data-ttu-id="b67b9-135">İndirilecek Azure Datalake Gen2 öğesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b67b9-135">Azure Datalake Gen2 Item Object to download.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item
Parameter Sets: ItemPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b67b9-136">-Yol</span><span class="sxs-lookup"><span data-stu-id="b67b9-136">-Path</span></span>
<span data-ttu-id="b67b9-137">Belirtilen FileSystem 'da kaldırılması gereken yol.</span><span class="sxs-lookup"><span data-stu-id="b67b9-137">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="b67b9-138">' Dizin/file.txt ' veya ' directory1/directory2/' biçiminde bir dosya veya dizin olabilir</span><span class="sxs-lookup"><span data-stu-id="b67b9-138">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b67b9-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="b67b9-139">-Confirm</span></span>
<span data-ttu-id="b67b9-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b67b9-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b67b9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b67b9-141">-WhatIf</span></span>
<span data-ttu-id="b67b9-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b67b9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b67b9-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b67b9-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b67b9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b67b9-144">CommonParameters</span></span>
<span data-ttu-id="b67b9-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b67b9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b67b9-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b67b9-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b67b9-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b67b9-147">INPUTS</span></span>

### <span data-ttu-id="b67b9-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b67b9-148">System.String</span></span>

### <span data-ttu-id="b67b9-149">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="b67b9-149">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="b67b9-150">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="b67b9-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b67b9-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b67b9-151">OUTPUTS</span></span>

### <span data-ttu-id="b67b9-152">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="b67b9-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="b67b9-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b67b9-153">NOTES</span></span>

## <span data-ttu-id="b67b9-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b67b9-154">RELATED LINKS</span></span>
