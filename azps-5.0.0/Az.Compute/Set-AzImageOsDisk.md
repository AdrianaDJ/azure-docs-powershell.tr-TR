---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 45f3e8f76e6f8ff3a5684fbd8f9ebf42e7a8e252
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277499"
---
# <span data-ttu-id="67d54-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="67d54-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="67d54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67d54-102">SYNOPSIS</span></span>
<span data-ttu-id="67d54-103">Görüntü nesnesinde işletim sistemi disk özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="67d54-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="67d54-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67d54-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67d54-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="67d54-105">DESCRIPTION</span></span>
<span data-ttu-id="67d54-106">**Set-Azimageosdısk** cmdlet 'i, görüntü nesnesinde işletim sistemi disk özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="67d54-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="67d54-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67d54-107">EXAMPLES</span></span>

### <span data-ttu-id="67d54-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="67d54-108">Example 1</span></span>
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

<span data-ttu-id="67d54-109">İlk komut bir resim nesnesi oluşturur ve $imageConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="67d54-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="67d54-110">Sonraki üç komut, $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 değişkenlerine işletim sistemi diskinin ve iki veri diskinin yollarını atar.</span><span class="sxs-lookup"><span data-stu-id="67d54-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="67d54-111">Bu yaklaşım yalnızca aşağıdaki komutların okunurluğu için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="67d54-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="67d54-112">Sonraki üç komut, $imageConfig depolanan resme bir işletim sistemi diski ve iki veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="67d54-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="67d54-113">Her diskin URI 'SI $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 ' de depolanır.</span><span class="sxs-lookup"><span data-stu-id="67d54-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="67d54-114">Son komutu, ' ResourceGroup01 ' kaynak grubunda ' ImageName01 ' adlı bir resim oluşturur.</span><span class="sxs-lookup"><span data-stu-id="67d54-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="67d54-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67d54-115">PARAMETERS</span></span>

### <span data-ttu-id="67d54-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="67d54-116">-BlobUri</span></span>
<span data-ttu-id="67d54-117">Blob 'un URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="67d54-117">Specifies the Uri of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67d54-118">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="67d54-118">-Caching</span></span>
<span data-ttu-id="67d54-119">Diskin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="67d54-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67d54-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d54-120">-DefaultProfile</span></span>
<span data-ttu-id="67d54-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="67d54-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67d54-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="67d54-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="67d54-123">Müşterinin yönettiği disk şifrelemesi kümesinin kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="67d54-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="67d54-124">Bu yalnızca yönetilen disk için belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="67d54-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="67d54-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="67d54-125">-DiskSizeGB</span></span>
<span data-ttu-id="67d54-126">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="67d54-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="67d54-127">-Image</span><span class="sxs-lookup"><span data-stu-id="67d54-127">-Image</span></span>
<span data-ttu-id="67d54-128">Yerel bir resim nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="67d54-128">Specifies a local image object.</span></span>

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

### <span data-ttu-id="67d54-129">-Manageddiskıd</span><span class="sxs-lookup"><span data-stu-id="67d54-129">-ManagedDiskId</span></span>
<span data-ttu-id="67d54-130">Yönetilen bir diskin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="67d54-130">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="67d54-131">-OsState</span><span class="sxs-lookup"><span data-stu-id="67d54-131">-OsState</span></span>
<span data-ttu-id="67d54-132">İşletim sisteminin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="67d54-132">Specifies the OS state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67d54-133">-OsType</span><span class="sxs-lookup"><span data-stu-id="67d54-133">-OsType</span></span>
<span data-ttu-id="67d54-134">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="67d54-134">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67d54-135">-Anlık anlık kimliği</span><span class="sxs-lookup"><span data-stu-id="67d54-135">-SnapshotId</span></span>
<span data-ttu-id="67d54-136">Anlık görüntünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="67d54-136">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="67d54-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="67d54-137">-StorageAccountType</span></span>
<span data-ttu-id="67d54-138">Işletim sistemi görüntü diskinin depolama hesabı türü</span><span class="sxs-lookup"><span data-stu-id="67d54-138">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="67d54-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="67d54-139">-Confirm</span></span>
<span data-ttu-id="67d54-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="67d54-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67d54-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67d54-141">-WhatIf</span></span>
<span data-ttu-id="67d54-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="67d54-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67d54-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="67d54-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67d54-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d54-144">CommonParameters</span></span>
<span data-ttu-id="67d54-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67d54-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d54-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="67d54-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d54-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67d54-147">INPUTS</span></span>

### <span data-ttu-id="67d54-148">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psımage</span><span class="sxs-lookup"><span data-stu-id="67d54-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="67d54-149">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="67d54-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="67d54-150">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. OperatingSystemStateTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="67d54-150">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="67d54-151">System. String</span><span class="sxs-lookup"><span data-stu-id="67d54-151">System.String</span></span>

### <span data-ttu-id="67d54-152">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. Önbellekintypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="67d54-152">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="67d54-153">System. Int32</span><span class="sxs-lookup"><span data-stu-id="67d54-153">System.Int32</span></span>

## <span data-ttu-id="67d54-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67d54-154">OUTPUTS</span></span>

### <span data-ttu-id="67d54-155">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psımage</span><span class="sxs-lookup"><span data-stu-id="67d54-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="67d54-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67d54-156">NOTES</span></span>

## <span data-ttu-id="67d54-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67d54-157">RELATED LINKS</span></span>
