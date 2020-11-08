---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
ms.openlocfilehash: 32e04fb16d0e3360abb22177e453d5d629dbb098
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104607"
---
# <span data-ttu-id="7f81f-101">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="7f81f-101">Set-AzVmssVM</span></span>

## <span data-ttu-id="7f81f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f81f-102">SYNOPSIS</span></span>
<span data-ttu-id="7f81f-103">Bir VMSS örneğinin durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7f81f-103">Modifies the state of a VMSS instance.</span></span>

## <span data-ttu-id="7f81f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f81f-104">SYNTAX</span></span>

### <span data-ttu-id="7f81f-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7f81f-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f81f-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="7f81f-106">FriendMethod</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f81f-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="7f81f-107">RedeployMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f81f-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="7f81f-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f81f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f81f-109">DESCRIPTION</span></span>
<span data-ttu-id="7f81f-110">**Set-AzVmssVM** cmdlet 'ı sanal makine ölçeği KÜMESI (VMSS) örneğinin durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7f81f-110">The **Set-AzVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="7f81f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f81f-111">EXAMPLES</span></span>

## <span data-ttu-id="7f81f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f81f-112">PARAMETERS</span></span>

### <span data-ttu-id="7f81f-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="7f81f-113">-AsJob</span></span>
<span data-ttu-id="7f81f-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7f81f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f81f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f81f-115">-DefaultProfile</span></span>
<span data-ttu-id="7f81f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f81f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f81f-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="7f81f-117">-InstanceId</span></span>
<span data-ttu-id="7f81f-118">Bu cmdlet 'in durumu değiştirdiği VMSS örneğinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f81f-118">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f81f-119">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="7f81f-119">-PerformMaintenance</span></span>
<span data-ttu-id="7f81f-120">Bu cmdlet 'in VMSS 'deki bir sanal makinede bakım gerçekleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f81f-120">Indicates that this cmdlet performs maintenance on a virtual machine in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f81f-121">-Yeniden dağıtma</span><span class="sxs-lookup"><span data-stu-id="7f81f-121">-Redeploy</span></span>
<span data-ttu-id="7f81f-122">Bu cmdlet 'in VMSS 'de bir sanal makineyi yeniden dağıttığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f81f-122">Indicates that this cmdlet redeploys a virtual machine in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f81f-123">-Yeniden görüntü</span><span class="sxs-lookup"><span data-stu-id="7f81f-123">-Reimage</span></span>
<span data-ttu-id="7f81f-124">Bu cmdlet 'in VMSS örneğini yeniden görüntüdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f81f-124">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f81f-125">-Reımageall</span><span class="sxs-lookup"><span data-stu-id="7f81f-125">-ReimageAll</span></span>
<span data-ttu-id="7f81f-126">Cmdlet 'in VMSS örneğindeki tüm diskleri yeniden göndereceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f81f-126">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f81f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f81f-127">-ResourceGroupName</span></span>
<span data-ttu-id="7f81f-128">VMSS örneğini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f81f-128">Specifies the name of the resource group that contains the VMSS instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f81f-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7f81f-129">-VMScaleSetName</span></span>
<span data-ttu-id="7f81f-130">Bu cmdlet 'in değiştirdiği VMSS örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f81f-130">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f81f-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="7f81f-131">-Confirm</span></span>
<span data-ttu-id="7f81f-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7f81f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f81f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f81f-133">-WhatIf</span></span>
<span data-ttu-id="7f81f-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f81f-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f81f-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7f81f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f81f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f81f-136">CommonParameters</span></span>
<span data-ttu-id="7f81f-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f81f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f81f-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7f81f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f81f-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f81f-139">INPUTS</span></span>

### <span data-ttu-id="7f81f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7f81f-140">System.String</span></span>

## <span data-ttu-id="7f81f-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f81f-141">OUTPUTS</span></span>

### <span data-ttu-id="7f81f-142">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="7f81f-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="7f81f-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f81f-143">NOTES</span></span>

## <span data-ttu-id="7f81f-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f81f-144">RELATED LINKS</span></span>

[<span data-ttu-id="7f81f-145">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="7f81f-145">Get-AzVmssVM</span></span>](./Get-AzVmssVM.md)
