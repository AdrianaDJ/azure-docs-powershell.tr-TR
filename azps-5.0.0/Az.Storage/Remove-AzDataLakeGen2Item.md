---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
ms.openlocfilehash: 06bb30dd98c491267675893192f61d4eb61529bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279340"
---
# <span data-ttu-id="3c013-101">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="3c013-101">Remove-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="3c013-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c013-102">SYNOPSIS</span></span>
<span data-ttu-id="3c013-103">Dosya veya dizini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="3c013-103">Remove a file or directory.</span></span>

## <span data-ttu-id="3c013-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c013-104">SYNTAX</span></span>

### <span data-ttu-id="3c013-105">ReceiveManual (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3c013-105">ReceiveManual (Default)</span></span>
```
Remove-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c013-106">Itempipeline</span><span class="sxs-lookup"><span data-stu-id="3c013-106">ItemPipeline</span></span>
```
Remove-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3c013-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c013-107">DESCRIPTION</span></span>
<span data-ttu-id="3c013-108">**Remove-AzDataLakeGen2Item** cmdlet 'i, bir dosya veya dizini depolama hesabından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3c013-108">The **Remove-AzDataLakeGen2Item** cmdlet removes a file or directory from a Storage account.</span></span>
<span data-ttu-id="3c013-109">Bu cmdlet yalnızca depolama hesabı için hiyerarşik ad alanı etkinleştirilmişse çalışır.</span><span class="sxs-lookup"><span data-stu-id="3c013-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="3c013-110">Bu hesap türü, "New-AzStorageAccount" cmdlet 'i "-EnableHierarchicalNamespace $true" ile çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="3c013-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="3c013-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c013-111">EXAMPLES</span></span>

### <span data-ttu-id="3c013-112">Örnek 1: dizini kaldırır</span><span class="sxs-lookup"><span data-stu-id="3c013-112">Example 1: Removes a directory</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
```

<span data-ttu-id="3c013-113">Bu komut FileSystem 'dan bir dizini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3c013-113">This command removes a directory from a Filesystem.</span></span>

### <span data-ttu-id="3c013-114">Örnek 2: sormadan dosyayı kaldırır</span><span class="sxs-lookup"><span data-stu-id="3c013-114">Example 2: Removes a file without prompt</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/file1" -Force
```

<span data-ttu-id="3c013-115">Bu komut, sormadan bir dizini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3c013-115">This command removes a directory from a Filesystem, without prompt.</span></span>

### <span data-ttu-id="3c013-116">Örnek 3: bir FileSystem ile bir FileSystem 'daki tüm öğeleri kaldırma</span><span class="sxs-lookup"><span data-stu-id="3c013-116">Example 3: Remove all items in a Filesystem with pipeline</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" | Remove-AzDataLakeGen2Item -Force
```

<span data-ttu-id="3c013-117">Bu komut FileSystem 'daki tüm öğeleri ardışık düzene çıkarır.</span><span class="sxs-lookup"><span data-stu-id="3c013-117">This command removes all items in a Filesystem with pipeline.</span></span>

## <span data-ttu-id="3c013-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c013-118">PARAMETERS</span></span>

### <span data-ttu-id="3c013-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="3c013-119">-AsJob</span></span>
<span data-ttu-id="3c013-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3c013-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c013-121">-Context</span><span class="sxs-lookup"><span data-stu-id="3c013-121">-Context</span></span>
<span data-ttu-id="3c013-122">Azure depolama bağlamı nesnesi</span><span class="sxs-lookup"><span data-stu-id="3c013-122">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="3c013-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c013-123">-DefaultProfile</span></span>
<span data-ttu-id="3c013-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3c013-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c013-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="3c013-125">-FileSystem</span></span>
<span data-ttu-id="3c013-126">FileSystem adı</span><span class="sxs-lookup"><span data-stu-id="3c013-126">FileSystem name</span></span>

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

### <span data-ttu-id="3c013-127">-Force</span><span class="sxs-lookup"><span data-stu-id="3c013-127">-Force</span></span>
<span data-ttu-id="3c013-128">FileSystem 'ı ve içerdiği tüm içeriği kaldırmaya zorla</span><span class="sxs-lookup"><span data-stu-id="3c013-128">Force to remove the Filesystem and all content in it</span></span>

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

### <span data-ttu-id="3c013-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c013-129">-InputObject</span></span>
<span data-ttu-id="3c013-130">Kaldırılacak Azure Datalake Gen2 öğesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="3c013-130">Azure Datalake Gen2 Item Object to remove.</span></span>

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

### <span data-ttu-id="3c013-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3c013-131">-PassThru</span></span>
<span data-ttu-id="3c013-132">Belirtilen FileSystem 'ın başarıyla kaldırılıp kaldırılmadığını döndürme</span><span class="sxs-lookup"><span data-stu-id="3c013-132">Return whether the specified Filesystem is successfully removed</span></span>

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

### <span data-ttu-id="3c013-133">-Yol</span><span class="sxs-lookup"><span data-stu-id="3c013-133">-Path</span></span>
<span data-ttu-id="3c013-134">Belirtilen FileSystem 'da kaldırılması gereken yol.</span><span class="sxs-lookup"><span data-stu-id="3c013-134">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="3c013-135">' Dizin/file.txt ' veya ' directory1/directory2/' biçiminde bir dosya veya dizin olabilir</span><span class="sxs-lookup"><span data-stu-id="3c013-135">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="3c013-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="3c013-136">-Confirm</span></span>
<span data-ttu-id="3c013-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3c013-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c013-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c013-138">-WhatIf</span></span>
<span data-ttu-id="3c013-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c013-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c013-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3c013-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c013-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c013-141">CommonParameters</span></span>
<span data-ttu-id="3c013-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c013-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c013-143">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c013-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c013-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c013-144">INPUTS</span></span>

### <span data-ttu-id="3c013-145">System. String</span><span class="sxs-lookup"><span data-stu-id="3c013-145">System.String</span></span>

### <span data-ttu-id="3c013-146">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="3c013-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="3c013-147">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="3c013-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3c013-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c013-148">OUTPUTS</span></span>

### <span data-ttu-id="3c013-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c013-149">System.Boolean</span></span>

## <span data-ttu-id="3c013-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c013-150">NOTES</span></span>

## <span data-ttu-id="3c013-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c013-151">RELATED LINKS</span></span>
