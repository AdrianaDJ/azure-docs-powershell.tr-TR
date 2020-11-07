---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: df4a3676d86027c4b2e8627e8eae87dcb84644c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761377"
---
# <span data-ttu-id="4826c-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="4826c-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="4826c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4826c-102">SYNOPSIS</span></span>
<span data-ttu-id="4826c-103">VMSS 'ye veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="4826c-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="4826c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4826c-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4826c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4826c-105">DESCRIPTION</span></span>
<span data-ttu-id="4826c-106">**Add-Azvmssdatadısk** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) örneğine veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="4826c-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="4826c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4826c-107">EXAMPLES</span></span>

### <span data-ttu-id="4826c-108">Örnek 1: veri disketi ekleme</span><span class="sxs-lookup"><span data-stu-id="4826c-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="4826c-109">Bu komut, VMSS nesnesine boş bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="4826c-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="4826c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4826c-110">PARAMETERS</span></span>

### <span data-ttu-id="4826c-111">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="4826c-111">-Caching</span></span>
<span data-ttu-id="4826c-112">Diskin önbelleğe alma türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4826c-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="4826c-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="4826c-113">-CreateOption</span></span>
<span data-ttu-id="4826c-114">Diskin oluştur seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4826c-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="4826c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4826c-115">-DefaultProfile</span></span>
<span data-ttu-id="4826c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4826c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4826c-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="4826c-117">-DiskSizeGB</span></span>
<span data-ttu-id="4826c-118">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4826c-118">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="4826c-119">-LUN</span><span class="sxs-lookup"><span data-stu-id="4826c-119">-Lun</span></span>
<span data-ttu-id="4826c-120">Diskin mantıksal birim numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4826c-120">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="4826c-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="4826c-121">-Name</span></span>
<span data-ttu-id="4826c-122">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4826c-122">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="4826c-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4826c-123">-StorageAccountType</span></span>
<span data-ttu-id="4826c-124">Diskin depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4826c-124">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="4826c-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4826c-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4826c-126">VMSS nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="4826c-126">Specify the VMSS object.</span></span>
<span data-ttu-id="4826c-127">Nesneyi oluşturmak için [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4826c-127">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="4826c-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="4826c-128">-WriteAccelerator</span></span>
<span data-ttu-id="4826c-129">Veri diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4826c-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="4826c-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="4826c-130">-Confirm</span></span>
<span data-ttu-id="4826c-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4826c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4826c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4826c-132">-WhatIf</span></span>
<span data-ttu-id="4826c-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4826c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4826c-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4826c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4826c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4826c-135">CommonParameters</span></span>
<span data-ttu-id="4826c-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4826c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4826c-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4826c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4826c-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4826c-138">INPUTS</span></span>

### <span data-ttu-id="4826c-139">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4826c-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="4826c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4826c-140">System.String</span></span>

### <span data-ttu-id="4826c-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4826c-141">System.Int32</span></span>

### <span data-ttu-id="4826c-142">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. Önbellekintypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="4826c-142">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="4826c-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4826c-143">OUTPUTS</span></span>

### <span data-ttu-id="4826c-144">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4826c-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4826c-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4826c-145">NOTES</span></span>

## <span data-ttu-id="4826c-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4826c-146">RELATED LINKS</span></span>
