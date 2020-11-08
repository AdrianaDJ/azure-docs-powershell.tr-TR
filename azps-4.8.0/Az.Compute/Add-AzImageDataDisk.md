---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
ms.openlocfilehash: 0a50aa781177adb6ff457c3cc7d0a59ad8b350d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266677"
---
# <span data-ttu-id="2993f-101">Add-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="2993f-101">Add-AzImageDataDisk</span></span>

## <span data-ttu-id="2993f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2993f-102">SYNOPSIS</span></span>
<span data-ttu-id="2993f-103">Bir resim nesnesine veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="2993f-103">Adds a data disk to an image object.</span></span>

## <span data-ttu-id="2993f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2993f-104">SYNTAX</span></span>

```
Add-AzImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2993f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2993f-105">DESCRIPTION</span></span>
<span data-ttu-id="2993f-106">**Add-Azımagedatadısk** cmdlet 'i bir resim nesnesine veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="2993f-106">The **Add-AzImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="2993f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2993f-107">EXAMPLES</span></span>

### <span data-ttu-id="2993f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2993f-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="2993f-109">İlk komut bir resim nesnesi oluşturur ve $imageConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2993f-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="2993f-110">Sonraki üç komut, $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 değişkenine işletim sistemi diskinin ve iki veri diskinin yollarını atar.</span><span class="sxs-lookup"><span data-stu-id="2993f-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="2993f-111">Bu yaklaşım yalnızca aşağıdaki komutların okunurluğu için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2993f-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="2993f-112">Sonraki üç komut, $imageConfig depolanan resme bir işletim sistemi diski ve iki veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="2993f-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="2993f-113">Her diskin URI 'SI $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 ' de depolanır.</span><span class="sxs-lookup"><span data-stu-id="2993f-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="2993f-114">Son komutu, kaynak grubunda ImageName01 adlı bir resim oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2993f-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="2993f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2993f-115">PARAMETERS</span></span>

### <span data-ttu-id="2993f-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="2993f-116">-BlobUri</span></span>
<span data-ttu-id="2993f-117">Blob 'un bir URI 'SI olan bağlantısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2993f-117">Specifies the link, as a URI, of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2993f-118">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="2993f-118">-Caching</span></span>
<span data-ttu-id="2993f-119">Diskin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2993f-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2993f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2993f-120">-DefaultProfile</span></span>
<span data-ttu-id="2993f-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2993f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2993f-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="2993f-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="2993f-123">Müşterinin yönettiği disk şifrelemesi kümesinin kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2993f-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="2993f-124">Bu yalnızca yönetilen disk için belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="2993f-124">This can only be specified for managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2993f-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="2993f-125">-DiskSizeGB</span></span>
<span data-ttu-id="2993f-126">Diskin boyutunu gigabayt (GB) cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="2993f-126">Specifies the size of the disk in Gigabytes (GB).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2993f-127">-Image</span><span class="sxs-lookup"><span data-stu-id="2993f-127">-Image</span></span>
<span data-ttu-id="2993f-128">Yerel bir resim nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2993f-128">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2993f-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="2993f-129">-Lun</span></span>
<span data-ttu-id="2993f-130">Mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="2993f-130">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2993f-131">-Manageddiskıd</span><span class="sxs-lookup"><span data-stu-id="2993f-131">-ManagedDiskId</span></span>
<span data-ttu-id="2993f-132">Yönetilen bir diskin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2993f-132">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2993f-133">-Anlık anlık kimliği</span><span class="sxs-lookup"><span data-stu-id="2993f-133">-SnapshotId</span></span>
<span data-ttu-id="2993f-134">Anlık görüntünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2993f-134">Specifies the ID of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2993f-135">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="2993f-135">-StorageAccountType</span></span>
<span data-ttu-id="2993f-136">Veri görüntüsü diskinin depolama hesabı türü</span><span class="sxs-lookup"><span data-stu-id="2993f-136">The Storage Account type of the data image disk</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2993f-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="2993f-137">-Confirm</span></span>
<span data-ttu-id="2993f-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2993f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2993f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2993f-139">-WhatIf</span></span>
<span data-ttu-id="2993f-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2993f-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2993f-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2993f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2993f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2993f-142">CommonParameters</span></span>
<span data-ttu-id="2993f-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2993f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2993f-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2993f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2993f-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2993f-145">INPUTS</span></span>

### <span data-ttu-id="2993f-146">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psımage</span><span class="sxs-lookup"><span data-stu-id="2993f-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="2993f-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2993f-147">System.Int32</span></span>

### <span data-ttu-id="2993f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="2993f-148">System.String</span></span>

### <span data-ttu-id="2993f-149">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. Önbellekintypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2993f-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="2993f-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2993f-150">OUTPUTS</span></span>

### <span data-ttu-id="2993f-151">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psımage</span><span class="sxs-lookup"><span data-stu-id="2993f-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="2993f-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2993f-152">NOTES</span></span>

## <span data-ttu-id="2993f-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2993f-153">RELATED LINKS</span></span>
