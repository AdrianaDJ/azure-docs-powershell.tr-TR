---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmImageOsDisk.md
ms.openlocfilehash: 8deb191a6a26e4fb0001a1cbb78540460256dd97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586792"
---
# <span data-ttu-id="7a0f8-101">Set-AzureRmImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="7a0f8-101">Set-AzureRmImageOsDisk</span></span>

## <span data-ttu-id="7a0f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a0f8-102">SYNOPSIS</span></span>
<span data-ttu-id="7a0f8-103">Görüntü nesnesinde işletim sistemi disk özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7a0f8-103">Sets the operating system disk properties on an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a0f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7a0f8-104">SYNTAX</span></span>

```
Set-AzureRmImageOsDisk [-Image] <Image> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>] [-ManagedDiskId <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a0f8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7a0f8-105">DESCRIPTION</span></span>
<span data-ttu-id="7a0f8-106">**Set-Azurermimageosdısk** cmdlet 'i, görüntü nesnesinde işletim sistemi disk özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7a0f8-106">The **Set-AzureRmImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="7a0f8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7a0f8-107">EXAMPLES</span></span>

### <span data-ttu-id="7a0f8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7a0f8-108">Example 1</span></span>
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

<span data-ttu-id="7a0f8-109">İlk komut bir resim nesnesi oluşturur ve $imageConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7a0f8-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="7a0f8-110">Sonraki üç komut, $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 değişkenlerine işletim sistemi diskinin ve iki veri diskinin yollarını atar.</span><span class="sxs-lookup"><span data-stu-id="7a0f8-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="7a0f8-111">Bu yaklaşım yalnızca aşağıdaki komutların okunurluğu için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7a0f8-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="7a0f8-112">Sonraki üç komut, $imageConfig depolanan resme bir işletim sistemi diski ve iki veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="7a0f8-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="7a0f8-113">Her diskin URI 'SI $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 ' de depolanır.</span><span class="sxs-lookup"><span data-stu-id="7a0f8-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="7a0f8-114">Son komutu, ' ResourceGroup01 ' kaynak grubunda ' ImageName01 ' adlı bir resim oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7a0f8-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="7a0f8-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7a0f8-115">PARAMETERS</span></span>

### <span data-ttu-id="7a0f8-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="7a0f8-116">-BlobUri</span></span>
<span data-ttu-id="7a0f8-117">Blob 'un URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a0f8-117">Specifies the Uri of the blob.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a0f8-118">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="7a0f8-118">-Caching</span></span>
<span data-ttu-id="7a0f8-119">Diskin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a0f8-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a0f8-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="7a0f8-120">-DiskSizeGB</span></span>
<span data-ttu-id="7a0f8-121">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a0f8-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="7a0f8-122">-Image</span><span class="sxs-lookup"><span data-stu-id="7a0f8-122">-Image</span></span>
<span data-ttu-id="7a0f8-123">Yerel bir resim nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a0f8-123">Specifies a local image object.</span></span>

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

### <span data-ttu-id="7a0f8-124">-Manageddiskıd</span><span class="sxs-lookup"><span data-stu-id="7a0f8-124">-ManagedDiskId</span></span>
<span data-ttu-id="7a0f8-125">Yönetilen bir diskin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a0f8-125">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="7a0f8-126">-OsState</span><span class="sxs-lookup"><span data-stu-id="7a0f8-126">-OsState</span></span>
<span data-ttu-id="7a0f8-127">İşletim sisteminin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a0f8-127">Specifies the OS state.</span></span>

```yaml
Type: OperatingSystemStateTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Generalized, Specialized

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a0f8-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="7a0f8-128">-OsType</span></span>
<span data-ttu-id="7a0f8-129">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a0f8-129">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a0f8-130">-Anlık anlık kimliği</span><span class="sxs-lookup"><span data-stu-id="7a0f8-130">-SnapshotId</span></span>
<span data-ttu-id="7a0f8-131">Anlık görüntünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a0f8-131">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="7a0f8-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="7a0f8-132">-StorageAccountType</span></span>
<span data-ttu-id="7a0f8-133">Işletim sistemi görüntü diskinin depolama hesabı türü</span><span class="sxs-lookup"><span data-stu-id="7a0f8-133">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="7a0f8-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="7a0f8-134">-Confirm</span></span>
<span data-ttu-id="7a0f8-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7a0f8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a0f8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a0f8-136">-WhatIf</span></span>
<span data-ttu-id="7a0f8-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7a0f8-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a0f8-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7a0f8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a0f8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a0f8-139">CommonParameters</span></span>
<span data-ttu-id="7a0f8-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7a0f8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a0f8-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a0f8-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a0f8-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7a0f8-142">INPUTS</span></span>

### <span data-ttu-id="7a0f8-143">Microsoft. Azure. Management. COMPUTE. modeller. Image</span><span class="sxs-lookup"><span data-stu-id="7a0f8-143">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="7a0f8-144">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. modeller. OperatingSystemStateTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] System. String System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`</span><span class="sxs-lookup"><span data-stu-id="7a0f8-144">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="7a0f8-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7a0f8-145">OUTPUTS</span></span>

### <span data-ttu-id="7a0f8-146">Microsoft. Azure. Management. COMPUTE. modeller. Image</span><span class="sxs-lookup"><span data-stu-id="7a0f8-146">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="7a0f8-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7a0f8-147">NOTES</span></span>

## <span data-ttu-id="7a0f8-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7a0f8-148">RELATED LINKS</span></span>

