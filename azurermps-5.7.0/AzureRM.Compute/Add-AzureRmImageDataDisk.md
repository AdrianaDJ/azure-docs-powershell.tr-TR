---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmImageDataDisk.md
ms.openlocfilehash: 13f98e0e0b34e4e192f108e20bcb6f52047b7611
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591723"
---
# <span data-ttu-id="11f66-101">Add-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="11f66-101">Add-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="11f66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11f66-102">SYNOPSIS</span></span>
<span data-ttu-id="11f66-103">Bir resim nesnesine veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="11f66-103">Adds a data disk to an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11f66-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11f66-104">SYNTAX</span></span>

```
Add-AzureRmImageDataDisk [-Image] <Image> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>]
 [-ManagedDiskId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11f66-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="11f66-105">DESCRIPTION</span></span>
<span data-ttu-id="11f66-106">**Add-Azurermimagedatadısk** cmdlet 'i bir resim nesnesine veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="11f66-106">The **Add-AzureRmImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="11f66-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11f66-107">EXAMPLES</span></span>

### <span data-ttu-id="11f66-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="11f66-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzureRmImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzureRmImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzureRmImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="11f66-109">İlk komut bir resim nesnesi oluşturur ve $imageConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="11f66-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="11f66-110">Sonraki üç komut, $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 değişkenine işletim sistemi diskinin ve iki veri diskinin yollarını atar.</span><span class="sxs-lookup"><span data-stu-id="11f66-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="11f66-111">Bu yaklaşım yalnızca aşağıdaki komutların okunurluğu için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="11f66-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="11f66-112">Sonraki üç komut, $imageConfig depolanan resme bir işletim sistemi diski ve iki veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="11f66-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="11f66-113">Her diskin URI 'SI $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 ' de depolanır.</span><span class="sxs-lookup"><span data-stu-id="11f66-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="11f66-114">Son komutu, kaynak grubunda ImageName01 adlı bir resim oluşturur.</span><span class="sxs-lookup"><span data-stu-id="11f66-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="11f66-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11f66-115">PARAMETERS</span></span>

### <span data-ttu-id="11f66-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="11f66-116">-BlobUri</span></span>
<span data-ttu-id="11f66-117">Blob 'un bir URI 'SI olan bağlantısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="11f66-117">Specifies the link, as a URI, of the blob.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f66-118">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="11f66-118">-Caching</span></span>
<span data-ttu-id="11f66-119">Diskin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="11f66-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f66-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="11f66-120">-DiskSizeGB</span></span>
<span data-ttu-id="11f66-121">Diskin boyutunu gigabayt (GB) cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="11f66-121">Specifies the size of the disk in Gigabytes (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f66-122">-Image</span><span class="sxs-lookup"><span data-stu-id="11f66-122">-Image</span></span>
<span data-ttu-id="11f66-123">Yerel bir resim nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="11f66-123">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11f66-124">-LUN</span><span class="sxs-lookup"><span data-stu-id="11f66-124">-Lun</span></span>
<span data-ttu-id="11f66-125">Mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="11f66-125">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f66-126">-Manageddiskıd</span><span class="sxs-lookup"><span data-stu-id="11f66-126">-ManagedDiskId</span></span>
<span data-ttu-id="11f66-127">Yönetilen bir diskin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="11f66-127">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f66-128">-Anlık anlık kimliği</span><span class="sxs-lookup"><span data-stu-id="11f66-128">-SnapshotId</span></span>
<span data-ttu-id="11f66-129">Anlık görüntünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="11f66-129">Specifies the ID of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f66-130">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="11f66-130">-StorageAccountType</span></span>
<span data-ttu-id="11f66-131">Veri görüntüsü diskinin depolama hesabı türü</span><span class="sxs-lookup"><span data-stu-id="11f66-131">The Storage Account type of the data image disk</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f66-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="11f66-132">-Confirm</span></span>
<span data-ttu-id="11f66-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="11f66-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f66-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11f66-134">-WhatIf</span></span>
<span data-ttu-id="11f66-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="11f66-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11f66-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="11f66-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f66-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11f66-137">CommonParameters</span></span>
<span data-ttu-id="11f66-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11f66-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11f66-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11f66-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11f66-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11f66-140">INPUTS</span></span>

### <span data-ttu-id="11f66-141">Microsoft. Azure. Management. COMPUTE. modeller. Image</span><span class="sxs-lookup"><span data-stu-id="11f66-141">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="11f66-142">System. Int32 System. String System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="11f66-142">System.Int32 System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="11f66-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11f66-143">OUTPUTS</span></span>

### <span data-ttu-id="11f66-144">Microsoft. Azure. Management. COMPUTE. modeller. Image</span><span class="sxs-lookup"><span data-stu-id="11f66-144">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="11f66-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11f66-145">NOTES</span></span>

## <span data-ttu-id="11f66-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11f66-146">RELATED LINKS</span></span>