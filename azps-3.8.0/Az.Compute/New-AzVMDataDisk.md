---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
ms.openlocfilehash: 7f67b8b6ff287a98fc505cb63c3a6eda90f46ef7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096920"
---
# <span data-ttu-id="d36dd-101">New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d36dd-101">New-AzVMDataDisk</span></span>

## <span data-ttu-id="d36dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d36dd-102">SYNOPSIS</span></span>
<span data-ttu-id="d36dd-103">Sanal makine ya da bir VMSS VM için yerel bir veri diski nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d36dd-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="d36dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d36dd-104">SYNTAX</span></span>

### <span data-ttu-id="d36dd-105">NormalDiskParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d36dd-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d36dd-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d36dd-106">ManagedDiskParameterSetName</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d36dd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d36dd-107">DESCRIPTION</span></span>
<span data-ttu-id="d36dd-108">**New-AzVMDataDisk** cmdlet 'i sanal makine ya da bir VMSS VM için yerel bir veri diski nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d36dd-108">The **New-AzVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="d36dd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d36dd-109">EXAMPLES</span></span>

### <span data-ttu-id="d36dd-110">Örnek 1: bir VMSS VM 'ye yönetilen veri diski ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d36dd-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="d36dd-111">İlk komut, varolan bir yönetilen diski alır.</span><span class="sxs-lookup"><span data-stu-id="d36dd-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="d36dd-112">Next komutu, yönetilen diskle bir veri diski nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d36dd-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="d36dd-113">Next komutu, kaynak grup adı, VMSS adı ve örnek KIMLIĞI tarafından verilen mevcut bir VMSS VM 'yi alır.</span><span class="sxs-lookup"><span data-stu-id="d36dd-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="d36dd-114">Son komutu, yeni veri diski ekleyerek VMSS VM 'yi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d36dd-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

## <span data-ttu-id="d36dd-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d36dd-115">PARAMETERS</span></span>

### <span data-ttu-id="d36dd-116">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="d36dd-116">-Caching</span></span>
<span data-ttu-id="d36dd-117">Sanal makine veri diskinin önbellekleme işlemi.</span><span class="sxs-lookup"><span data-stu-id="d36dd-117">The virtual machine data disk's caching.</span></span>

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

### <span data-ttu-id="d36dd-118">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="d36dd-118">-CreateOption</span></span>
<span data-ttu-id="d36dd-119">Sanal makine veri diskinin Create seçeneği.</span><span class="sxs-lookup"><span data-stu-id="d36dd-119">The virtual machine data disk's create option.</span></span>

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

### <span data-ttu-id="d36dd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d36dd-120">-DefaultProfile</span></span>
<span data-ttu-id="d36dd-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d36dd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d36dd-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="d36dd-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="d36dd-123">Sanal makine yönetilen disk şifrelemesi kümesinin kimliği.</span><span class="sxs-lookup"><span data-stu-id="d36dd-123">The virtual machine managed disk encryption set's Id.</span></span>

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

### <span data-ttu-id="d36dd-124">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="d36dd-124">-DiskSizeInGB</span></span>
<span data-ttu-id="d36dd-125">GB cinsinden sanal makine veri diskinin boyutu.</span><span class="sxs-lookup"><span data-stu-id="d36dd-125">The virtual machine data disk's size in GB.</span></span>

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

### <span data-ttu-id="d36dd-126">-LUN</span><span class="sxs-lookup"><span data-stu-id="d36dd-126">-Lun</span></span>
<span data-ttu-id="d36dd-127">Sanal makine veri diskinin LUN 'U.</span><span class="sxs-lookup"><span data-stu-id="d36dd-127">The virtual machine data disk's Lun.</span></span>

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

### <span data-ttu-id="d36dd-128">-Manageddiskıd</span><span class="sxs-lookup"><span data-stu-id="d36dd-128">-ManagedDiskId</span></span>
<span data-ttu-id="d36dd-129">Sanal makinenin yönetilen diskinin kimliği.</span><span class="sxs-lookup"><span data-stu-id="d36dd-129">The virtual machine managed disk's Id.</span></span>

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

### <span data-ttu-id="d36dd-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="d36dd-130">-Name</span></span>
<span data-ttu-id="d36dd-131">Sanal makine veri diskinin adı.</span><span class="sxs-lookup"><span data-stu-id="d36dd-131">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="d36dd-132">-Sourceımageuri</span><span class="sxs-lookup"><span data-stu-id="d36dd-132">-SourceImageUri</span></span>
<span data-ttu-id="d36dd-133">Sanal makine işletim sistemi diskinin kaynak görüntü URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="d36dd-133">The virtual machine OS disk's source image Uri.</span></span>

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

### <span data-ttu-id="d36dd-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d36dd-134">-StorageAccountType</span></span>
<span data-ttu-id="d36dd-135">Sanal makine yönetilen diskinin hesap türü.</span><span class="sxs-lookup"><span data-stu-id="d36dd-135">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="d36dd-136">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="d36dd-136">-VhdUri</span></span>
<span data-ttu-id="d36dd-137">Sanal makine veri diskinin VHD URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="d36dd-137">The virtual machine data disk's Vhd Uri.</span></span>

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

### <span data-ttu-id="d36dd-138">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="d36dd-138">-WriteAccelerator</span></span>
<span data-ttu-id="d36dd-139">Yönetilen veri diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d36dd-139">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="d36dd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d36dd-140">CommonParameters</span></span>
<span data-ttu-id="d36dd-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d36dd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d36dd-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d36dd-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d36dd-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d36dd-143">INPUTS</span></span>

### <span data-ttu-id="d36dd-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d36dd-144">System.Int32</span></span>

### <span data-ttu-id="d36dd-145">System. String</span><span class="sxs-lookup"><span data-stu-id="d36dd-145">System.String</span></span>

### <span data-ttu-id="d36dd-146">Microsoft. Azure. Management. COMPUTE. model. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="d36dd-146">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="d36dd-147">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="d36dd-147">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d36dd-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d36dd-148">OUTPUTS</span></span>

### <span data-ttu-id="d36dd-149">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="d36dd-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="d36dd-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d36dd-150">NOTES</span></span>

## <span data-ttu-id="d36dd-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d36dd-151">RELATED LINKS</span></span>
