---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/repair-azvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: 43e92594d8a67dbb3ade0b66a065b8c6c097d60d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097579"
---
# <span data-ttu-id="8d20b-101">Repair-AzVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="8d20b-101">Repair-AzVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="8d20b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d20b-102">SYNOPSIS</span></span>
<span data-ttu-id="8d20b-103">El ile platform güncelleştirme etki alanı hizmet yapısı sanal makine ölçek kümesindeki sanal makineleri güncelleştirmeye yönelik ilerleme.</span><span class="sxs-lookup"><span data-stu-id="8d20b-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="8d20b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8d20b-104">SYNTAX</span></span>

### <span data-ttu-id="8d20b-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8d20b-105">DefaultParameter (Default)</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d20b-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="8d20b-106">ResourceIdParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d20b-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="8d20b-107">ObjectParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d20b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8d20b-108">DESCRIPTION</span></span>
<span data-ttu-id="8d20b-109">El ile platform güncelleştirme etki alanını zorla hizmet yapısı sanal makine ölçek kümesindeki sanal makineleri güncelleştirmeye ilerleme.</span><span class="sxs-lookup"><span data-stu-id="8d20b-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="8d20b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8d20b-110">EXAMPLES</span></span>

### <span data-ttu-id="8d20b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8d20b-111">Example 1</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="8d20b-112">Bu komut, kaynak grubu adı ve ölçek kümesi adıyla belirtilen sanal makine ölçek kümesi</span><span class="sxs-lookup"><span data-stu-id="8d20b-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="8d20b-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="8d20b-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="8d20b-114">Bu komut, VM Ölçek kümesi nesnesinin belirttiği sanal makine ölçeği kümesi için UD 1 ' de hizmet yapısı güncelleştirmesini zorlar.</span><span class="sxs-lookup"><span data-stu-id="8d20b-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="8d20b-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="8d20b-115">Example 3</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceId $resourceId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="8d20b-116">Bu komut, kaynak kimliği tarafından belirtilen sanal makine ölçeği kümesi için UD 2 ' ye hizmet yapısı güncelleştirmesini zorlar.</span><span class="sxs-lookup"><span data-stu-id="8d20b-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="8d20b-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8d20b-117">PARAMETERS</span></span>

### <span data-ttu-id="8d20b-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="8d20b-118">-AsJob</span></span>
<span data-ttu-id="8d20b-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8d20b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8d20b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d20b-120">-DefaultProfile</span></span>
<span data-ttu-id="8d20b-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8d20b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d20b-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="8d20b-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="8d20b-123">El ile kurtarma işlemi istenmiştir.</span><span class="sxs-lookup"><span data-stu-id="8d20b-123">The platform update domain for which a manual recovery walk is requested.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d20b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d20b-124">-ResourceGroupName</span></span>
<span data-ttu-id="8d20b-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8d20b-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d20b-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8d20b-126">-ResourceId</span></span>
<span data-ttu-id="8d20b-127">Sanal makine ölçek kümesi için kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="8d20b-127">The resource id for the virtual machine scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d20b-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8d20b-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8d20b-129">Yerel sanal makine ölçek kümesi nesnesi</span><span class="sxs-lookup"><span data-stu-id="8d20b-129">Local virtual machine scale set object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d20b-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8d20b-130">-VMScaleSetName</span></span>
<span data-ttu-id="8d20b-131">Sanal makine ölçek kümesi adı</span><span class="sxs-lookup"><span data-stu-id="8d20b-131">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d20b-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="8d20b-132">-Confirm</span></span>
<span data-ttu-id="8d20b-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8d20b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d20b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d20b-134">-WhatIf</span></span>
<span data-ttu-id="8d20b-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8d20b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d20b-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8d20b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d20b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d20b-137">CommonParameters</span></span>
<span data-ttu-id="8d20b-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8d20b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d20b-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8d20b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d20b-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8d20b-140">INPUTS</span></span>

### <span data-ttu-id="8d20b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8d20b-141">System.String</span></span>

### <span data-ttu-id="8d20b-142">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8d20b-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8d20b-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8d20b-143">OUTPUTS</span></span>

### <span data-ttu-id="8d20b-144">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSRecoveryWalkResponse</span><span class="sxs-lookup"><span data-stu-id="8d20b-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="8d20b-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8d20b-145">NOTES</span></span>

## <span data-ttu-id="8d20b-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8d20b-146">RELATED LINKS</span></span>