---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/move-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
ms.openlocfilehash: b8d46d85d00f00afdfa326b22a759f60af7b5bbe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108594"
---
# <span data-ttu-id="264c9-101">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="264c9-101">Move-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="264c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="264c9-102">SYNOPSIS</span></span>
<span data-ttu-id="264c9-103">Bir dosya veya dizini aynı depolama hesabında bir dosya veya dizine taşıma.</span><span class="sxs-lookup"><span data-stu-id="264c9-103">Move a file or directory to another a file or directory in same Storage account.</span></span>

## <span data-ttu-id="264c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="264c9-104">SYNTAX</span></span>

### <span data-ttu-id="264c9-105">ReceiveManual (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="264c9-105">ReceiveManual (Default)</span></span>
```
Move-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="264c9-106">Itempipeline</span><span class="sxs-lookup"><span data-stu-id="264c9-106">ItemPipeline</span></span>
```
Move-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="264c9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="264c9-107">DESCRIPTION</span></span>
<span data-ttu-id="264c9-108">**Taþý-AzDataLakeGen2Item** cmdlet 'i, bir dosya veya dizini aynı depolama hesabındaki bir dosya veya dizine taşır.</span><span class="sxs-lookup"><span data-stu-id="264c9-108">The **Move-AzDataLakeGen2Item** cmdlet moves a a file or directory to another a file or directory in same Storage account.</span></span>
<span data-ttu-id="264c9-109">Bu cmdlet yalnızca depolama hesabı için hiyerarşik ad alanı etkinleştirilmişse çalışır.</span><span class="sxs-lookup"><span data-stu-id="264c9-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="264c9-110">Bu hesap türü, "New-AzStorageAccount" cmdlet 'i "-EnableHierarchicalNamespace $true" ile çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="264c9-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="264c9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="264c9-111">EXAMPLES</span></span>

### <span data-ttu-id="264c9-112">Örnek 1: aynı dosya sisteminde bir katlamayı taşıma</span><span class="sxs-lookup"><span data-stu-id="264c9-112">Example 1: Move a fold in same Filesystem</span></span>
```
PS C:\> Move-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/" -DestFileSystem "filesystem1" -DestPath "dir3/"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir3                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="264c9-113">Bu komut ' dir1 ' dizinini aynı FileSystem 'daki ' dir3 ' dizinine taşır.</span><span class="sxs-lookup"><span data-stu-id="264c9-113">This command move directory 'dir1' to directory 'dir3' in the same Filesystem.</span></span>

### <span data-ttu-id="264c9-114">Örnek 2: bir dosyayı ardışık düzene göre aynı depolama hesabındaki başka bir FileSystem 'a sormadan taşıma</span><span class="sxs-lookup"><span data-stu-id="264c9-114">Example 2: Move a file by pipeline, to another Filesystem in the same Storage account without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" | Move-AzDataLakeGen2Item -DestFileSystem "filesystem2" -DestPath "dir2/file2" -Force

   FileSystem Name: filesystem2

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir2/file2           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="264c9-115">Bu komut ' filesystem1 ' içindeki ' dir1/File1 ' dosyasını, aynı depolama hesabında sormadan ' File2 ' ' dir2/filesystem2 ' dosyasına taşır.</span><span class="sxs-lookup"><span data-stu-id="264c9-115">This command move file 'dir1/file1' in 'filesystem1' to file 'dir2/file2' in 'filesystem2' in the same Storage account without prompt.</span></span>

## <span data-ttu-id="264c9-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="264c9-116">PARAMETERS</span></span>

### <span data-ttu-id="264c9-117">-Context</span><span class="sxs-lookup"><span data-stu-id="264c9-117">-Context</span></span>
<span data-ttu-id="264c9-118">Azure depolama bağlamı nesnesi</span><span class="sxs-lookup"><span data-stu-id="264c9-118">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="264c9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="264c9-119">-DefaultProfile</span></span>
<span data-ttu-id="264c9-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="264c9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="264c9-121">-DestFileSystem</span><span class="sxs-lookup"><span data-stu-id="264c9-121">-DestFileSystem</span></span>
<span data-ttu-id="264c9-122">Hedef FileSystem adı</span><span class="sxs-lookup"><span data-stu-id="264c9-122">Dest FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="264c9-123">-DestPath</span><span class="sxs-lookup"><span data-stu-id="264c9-123">-DestPath</span></span>
<span data-ttu-id="264c9-124">Hedef blob yolu</span><span class="sxs-lookup"><span data-stu-id="264c9-124">Dest Blob path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="264c9-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="264c9-125">-FileSystem</span></span>
<span data-ttu-id="264c9-126">FileSystem adı</span><span class="sxs-lookup"><span data-stu-id="264c9-126">FileSystem name</span></span>

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

### <span data-ttu-id="264c9-127">-Force</span><span class="sxs-lookup"><span data-stu-id="264c9-127">-Force</span></span>
<span data-ttu-id="264c9-128">Hedefin üzerine yazmayı zorlayın.</span><span class="sxs-lookup"><span data-stu-id="264c9-128">Force to over write the destination.</span></span>

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

### <span data-ttu-id="264c9-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="264c9-129">-InputObject</span></span>
<span data-ttu-id="264c9-130">Taşınacak Azure Datalake Gen2 öğe nesnesi.</span><span class="sxs-lookup"><span data-stu-id="264c9-130">Azure Datalake Gen2 Item Object to move from.</span></span>

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

### <span data-ttu-id="264c9-131">-Yol</span><span class="sxs-lookup"><span data-stu-id="264c9-131">-Path</span></span>
<span data-ttu-id="264c9-132">Belirtilen FileSystem 'ın taşınması gereken yolu.</span><span class="sxs-lookup"><span data-stu-id="264c9-132">The path in the specified Filesystem that should be move from.</span></span>
<span data-ttu-id="264c9-133">' Dizin/file.txt ' veya ' directory1/directory2/' biçiminde bir dosya veya dizin olabilir</span><span class="sxs-lookup"><span data-stu-id="264c9-133">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="264c9-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="264c9-134">-Confirm</span></span>
<span data-ttu-id="264c9-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="264c9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="264c9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="264c9-136">-WhatIf</span></span>
<span data-ttu-id="264c9-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="264c9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="264c9-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="264c9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="264c9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="264c9-139">CommonParameters</span></span>
<span data-ttu-id="264c9-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="264c9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="264c9-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="264c9-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="264c9-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="264c9-142">INPUTS</span></span>

### <span data-ttu-id="264c9-143">System. String</span><span class="sxs-lookup"><span data-stu-id="264c9-143">System.String</span></span>

### <span data-ttu-id="264c9-144">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="264c9-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="264c9-145">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="264c9-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="264c9-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="264c9-146">OUTPUTS</span></span>

### <span data-ttu-id="264c9-147">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="264c9-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="264c9-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="264c9-148">NOTES</span></span>

## <span data-ttu-id="264c9-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="264c9-149">RELATED LINKS</span></span>
