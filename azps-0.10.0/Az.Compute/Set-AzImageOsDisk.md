---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 5bc92ea5aa49cb97be457fd937c7b9deb492bb0e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936865"
---
# <span data-ttu-id="a4213-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="a4213-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="a4213-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4213-102">SYNOPSIS</span></span>
<span data-ttu-id="a4213-103">Görüntü nesnesinde işletim sistemi disk özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a4213-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="a4213-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a4213-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4213-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a4213-105">DESCRIPTION</span></span>
<span data-ttu-id="a4213-106">**Set-Azimageosdısk** cmdlet 'i, görüntü nesnesinde işletim sistemi disk özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a4213-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="a4213-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a4213-107">EXAMPLES</span></span>

### <span data-ttu-id="a4213-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a4213-108">Example 1</span></span>
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

<span data-ttu-id="a4213-109">İlk komut bir resim nesnesi oluşturur ve $imageConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a4213-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="a4213-110">Sonraki üç komut, $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 değişkenlerine işletim sistemi diskinin ve iki veri diskinin yollarını atar.</span><span class="sxs-lookup"><span data-stu-id="a4213-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="a4213-111">Bu yaklaşım yalnızca aşağıdaki komutların okunurluğu için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a4213-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="a4213-112">Sonraki üç komut, $imageConfig depolanan resme bir işletim sistemi diski ve iki veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="a4213-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="a4213-113">Her diskin URI 'SI $osDiskVhdUri, $dataDiskVhdUri 1 ve $dataDiskVhdUri 2 ' de depolanır.</span><span class="sxs-lookup"><span data-stu-id="a4213-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="a4213-114">Son komutu, ' ResourceGroup01 ' kaynak grubunda ' ImageName01 ' adlı bir resim oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a4213-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a4213-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a4213-115">PARAMETERS</span></span>

### <span data-ttu-id="a4213-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="a4213-116">-BlobUri</span></span>
<span data-ttu-id="a4213-117">Blob 'un URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4213-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="a4213-118">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="a4213-118">-Caching</span></span>
<span data-ttu-id="a4213-119">Diskin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4213-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="a4213-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4213-120">-DefaultProfile</span></span>
<span data-ttu-id="a4213-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a4213-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4213-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="a4213-122">-DiskSizeGB</span></span>
<span data-ttu-id="a4213-123">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4213-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="a4213-124">-Image</span><span class="sxs-lookup"><span data-stu-id="a4213-124">-Image</span></span>
<span data-ttu-id="a4213-125">Yerel bir resim nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4213-125">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4213-126">-Manageddiskıd</span><span class="sxs-lookup"><span data-stu-id="a4213-126">-ManagedDiskId</span></span>
<span data-ttu-id="a4213-127">Yönetilen bir diskin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4213-127">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="a4213-128">-OsState</span><span class="sxs-lookup"><span data-stu-id="a4213-128">-OsState</span></span>
<span data-ttu-id="a4213-129">İşletim sisteminin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4213-129">Specifies the OS state.</span></span>

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

### <span data-ttu-id="a4213-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="a4213-130">-OsType</span></span>
<span data-ttu-id="a4213-131">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4213-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="a4213-132">-Anlık anlık kimliği</span><span class="sxs-lookup"><span data-stu-id="a4213-132">-SnapshotId</span></span>
<span data-ttu-id="a4213-133">Anlık görüntünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4213-133">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="a4213-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="a4213-134">-StorageAccountType</span></span>
<span data-ttu-id="a4213-135">Işletim sistemi görüntü diskinin depolama hesabı türü</span><span class="sxs-lookup"><span data-stu-id="a4213-135">The Storage Account type of Os Image Disk</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4213-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="a4213-136">-Confirm</span></span>
<span data-ttu-id="a4213-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a4213-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4213-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4213-138">-WhatIf</span></span>
<span data-ttu-id="a4213-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a4213-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a4213-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a4213-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4213-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4213-141">CommonParameters</span></span>
<span data-ttu-id="a4213-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a4213-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4213-143">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4213-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4213-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a4213-144">INPUTS</span></span>

### <span data-ttu-id="a4213-145">Microsoft. Azure. Management. COMPUTE. modeller. Image</span><span class="sxs-lookup"><span data-stu-id="a4213-145">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="a4213-146">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. modeller. OperatingSystemStateTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] System. String System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`</span><span class="sxs-lookup"><span data-stu-id="a4213-146">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a4213-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a4213-147">OUTPUTS</span></span>

### <span data-ttu-id="a4213-148">Microsoft. Azure. Management. COMPUTE. modeller. Image</span><span class="sxs-lookup"><span data-stu-id="a4213-148">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="a4213-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a4213-149">NOTES</span></span>

## <span data-ttu-id="a4213-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a4213-150">RELATED LINKS</span></span>
