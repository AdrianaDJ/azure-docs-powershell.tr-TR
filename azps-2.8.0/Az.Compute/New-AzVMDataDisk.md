---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
ms.openlocfilehash: d7ce0b96c4ab286e21c253d701ec6d21c385ac56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752833"
---
# <span data-ttu-id="551f3-101">New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="551f3-101">New-AzVMDataDisk</span></span>

## <span data-ttu-id="551f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="551f3-102">SYNOPSIS</span></span>
<span data-ttu-id="551f3-103">Sanal makine ya da bir VMSS VM için yerel bir veri diski nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="551f3-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="551f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="551f3-104">SYNTAX</span></span>

### <span data-ttu-id="551f3-105">NormalDiskParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="551f3-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="551f3-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="551f3-106">ManagedDiskParameterSetName</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="551f3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="551f3-107">DESCRIPTION</span></span>
<span data-ttu-id="551f3-108">**New-AzVMDataDisk** cmdlet 'i sanal makine ya da bir VMSS VM için yerel bir veri diski nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="551f3-108">The **New-AzVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="551f3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="551f3-109">EXAMPLES</span></span>

### <span data-ttu-id="551f3-110">Örnek 1: bir VMSS VM 'ye yönetilen veri diski ekleyin.</span><span class="sxs-lookup"><span data-stu-id="551f3-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="551f3-111">İlk komut, varolan bir yönetilen diski alır.</span><span class="sxs-lookup"><span data-stu-id="551f3-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="551f3-112">Next komutu, yönetilen diskle bir veri diski nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="551f3-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="551f3-113">Next komutu, kaynak grup adı, VMSS adı ve örnek KIMLIĞI tarafından verilen mevcut bir VMSS VM 'yi alır.</span><span class="sxs-lookup"><span data-stu-id="551f3-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="551f3-114">Son komutu, yeni veri diski ekleyerek VMSS VM 'yi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="551f3-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

## <span data-ttu-id="551f3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="551f3-115">PARAMETERS</span></span>

### <span data-ttu-id="551f3-116">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="551f3-116">-Caching</span></span>
<span data-ttu-id="551f3-117">Sanal makine veri diskinin önbellekleme işlemi.</span><span class="sxs-lookup"><span data-stu-id="551f3-117">The virtual machine data disk's caching.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="551f3-118">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="551f3-118">-CreateOption</span></span>
<span data-ttu-id="551f3-119">Sanal makine veri diskinin Create seçeneği.</span><span class="sxs-lookup"><span data-stu-id="551f3-119">The virtual machine data disk's create option.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="551f3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="551f3-120">-DefaultProfile</span></span>
<span data-ttu-id="551f3-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="551f3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="551f3-122">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="551f3-122">-DiskSizeInGB</span></span>
<span data-ttu-id="551f3-123">GB cinsinden sanal makine veri diskinin boyutu.</span><span class="sxs-lookup"><span data-stu-id="551f3-123">The virtual machine data disk's size in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="551f3-124">-LUN</span><span class="sxs-lookup"><span data-stu-id="551f3-124">-Lun</span></span>
<span data-ttu-id="551f3-125">Sanal makine veri diskinin LUN 'U.</span><span class="sxs-lookup"><span data-stu-id="551f3-125">The virtual machine data disk's Lun.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="551f3-126">-Manageddiskıd</span><span class="sxs-lookup"><span data-stu-id="551f3-126">-ManagedDiskId</span></span>
<span data-ttu-id="551f3-127">Sanal makinenin yönetilen diskinin kimliği.</span><span class="sxs-lookup"><span data-stu-id="551f3-127">The virtual machine managed disk's Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="551f3-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="551f3-128">-Name</span></span>
<span data-ttu-id="551f3-129">Sanal makine veri diskinin adı.</span><span class="sxs-lookup"><span data-stu-id="551f3-129">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="551f3-130">-Sourceımageuri</span><span class="sxs-lookup"><span data-stu-id="551f3-130">-SourceImageUri</span></span>
<span data-ttu-id="551f3-131">Sanal makine işletim sistemi diskinin kaynak görüntü URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="551f3-131">The virtual machine OS disk's source image Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="551f3-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="551f3-132">-StorageAccountType</span></span>
<span data-ttu-id="551f3-133">Sanal makine yönetilen diskinin hesap türü.</span><span class="sxs-lookup"><span data-stu-id="551f3-133">The virtual machine managed disk's account type.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="551f3-134">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="551f3-134">-VhdUri</span></span>
<span data-ttu-id="551f3-135">Sanal makine veri diskinin VHD URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="551f3-135">The virtual machine data disk's Vhd Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="551f3-136">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="551f3-136">-WriteAccelerator</span></span>
<span data-ttu-id="551f3-137">Yönetilen veri diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="551f3-137">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="551f3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="551f3-138">CommonParameters</span></span>
<span data-ttu-id="551f3-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="551f3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="551f3-140">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="551f3-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="551f3-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="551f3-141">INPUTS</span></span>

### <span data-ttu-id="551f3-142">System. Int32</span><span class="sxs-lookup"><span data-stu-id="551f3-142">System.Int32</span></span>

### <span data-ttu-id="551f3-143">System. String</span><span class="sxs-lookup"><span data-stu-id="551f3-143">System.String</span></span>

### <span data-ttu-id="551f3-144">Microsoft. Azure. Management. COMPUTE. model. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="551f3-144">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="551f3-145">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="551f3-145">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="551f3-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="551f3-146">OUTPUTS</span></span>

### <span data-ttu-id="551f3-147">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="551f3-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="551f3-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="551f3-148">NOTES</span></span>

## <span data-ttu-id="551f3-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="551f3-149">RELATED LINKS</span></span>