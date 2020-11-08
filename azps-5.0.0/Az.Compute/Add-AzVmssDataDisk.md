---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: 41728fe644148a575e92136838aaf7f120f89ab7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279505"
---
# <span data-ttu-id="24103-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="24103-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="24103-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24103-102">SYNOPSIS</span></span>
<span data-ttu-id="24103-103">VMSS 'ye veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="24103-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="24103-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24103-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24103-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="24103-105">DESCRIPTION</span></span>
<span data-ttu-id="24103-106">**Add-Azvmssdatadısk** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) örneğine veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="24103-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="24103-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24103-107">EXAMPLES</span></span>

### <span data-ttu-id="24103-108">Örnek 1: veri disketi ekleme</span><span class="sxs-lookup"><span data-stu-id="24103-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="24103-109">Bu komut, VMSS nesnesine boş bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="24103-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="24103-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24103-110">PARAMETERS</span></span>

### <span data-ttu-id="24103-111">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="24103-111">-Caching</span></span>
<span data-ttu-id="24103-112">Diskin önbelleğe alma türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="24103-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="24103-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="24103-113">-CreateOption</span></span>
<span data-ttu-id="24103-114">Diskin oluştur seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="24103-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="24103-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24103-115">-DefaultProfile</span></span>
<span data-ttu-id="24103-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="24103-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24103-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="24103-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="24103-118">Müşterinin yönettiği disk şifrelemesi kümesinin kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="24103-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="24103-119">Bu yalnızca yönetilen disk için belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="24103-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="24103-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="24103-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="24103-121">Yönetilen disk için Read-Write ıOPS 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="24103-121">Specifies the Read-Write IOPS for the managed disk.</span></span> <span data-ttu-id="24103-122">Yalnızca StorageAccountType UltraSSD_LRS olarak kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="24103-122">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="24103-123">Belirtilmemişse, diskSizeGB 'ye dayalı olarak varsayılan bir değer atanacaktır.</span><span class="sxs-lookup"><span data-stu-id="24103-123">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24103-124">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="24103-124">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="24103-125">Yönetilen disk için MB cinsinden bant genişliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="24103-125">Specifies the bandwidth in MB per second for the managed disk.</span></span> <span data-ttu-id="24103-126">Yalnızca StorageAccountType UltraSSD_LRS olarak kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="24103-126">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="24103-127">Belirtilmemişse, diskSizeGB 'ye dayalı olarak varsayılan bir değer atanacaktır.</span><span class="sxs-lookup"><span data-stu-id="24103-127">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24103-128">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="24103-128">-DiskSizeGB</span></span>
<span data-ttu-id="24103-129">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="24103-129">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="24103-130">-LUN</span><span class="sxs-lookup"><span data-stu-id="24103-130">-Lun</span></span>
<span data-ttu-id="24103-131">Diskin mantıksal birim numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24103-131">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24103-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="24103-132">-Name</span></span>
<span data-ttu-id="24103-133">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24103-133">Specifies the name of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24103-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="24103-134">-StorageAccountType</span></span>
<span data-ttu-id="24103-135">Diskin depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="24103-135">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="24103-136">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="24103-136">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="24103-137">VMSS nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="24103-137">Specify the VMSS object.</span></span>
<span data-ttu-id="24103-138">Nesneyi oluşturmak için [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="24103-138">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24103-139">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="24103-139">-WriteAccelerator</span></span>
<span data-ttu-id="24103-140">Veri diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="24103-140">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="24103-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="24103-141">-Confirm</span></span>
<span data-ttu-id="24103-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="24103-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24103-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24103-143">-WhatIf</span></span>
<span data-ttu-id="24103-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="24103-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24103-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="24103-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24103-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24103-146">CommonParameters</span></span>
<span data-ttu-id="24103-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24103-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24103-148">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="24103-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24103-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24103-149">INPUTS</span></span>

### <span data-ttu-id="24103-150">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="24103-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="24103-151">System. String</span><span class="sxs-lookup"><span data-stu-id="24103-151">System.String</span></span>

### <span data-ttu-id="24103-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="24103-152">System.Int32</span></span>

### <span data-ttu-id="24103-153">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. Önbellekintypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="24103-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="24103-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24103-154">OUTPUTS</span></span>

### <span data-ttu-id="24103-155">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="24103-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="24103-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24103-156">NOTES</span></span>

## <span data-ttu-id="24103-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24103-157">RELATED LINKS</span></span>
