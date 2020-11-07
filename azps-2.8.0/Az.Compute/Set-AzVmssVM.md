---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
ms.openlocfilehash: 1fdd45c36d085b376ed900f0054dd98bc28c7525
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752658"
---
# <span data-ttu-id="0b5c4-101">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="0b5c4-101">Set-AzVmssVM</span></span>

## <span data-ttu-id="0b5c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b5c4-102">SYNOPSIS</span></span>
<span data-ttu-id="0b5c4-103">Bir VMSS örneğinin durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0b5c4-103">Modifies the state of a VMSS instance.</span></span>

## <span data-ttu-id="0b5c4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b5c4-104">SYNTAX</span></span>

### <span data-ttu-id="0b5c4-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0b5c4-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b5c4-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="0b5c4-106">FriendMethod</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b5c4-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="0b5c4-107">RedeployMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b5c4-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="0b5c4-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b5c4-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b5c4-109">DESCRIPTION</span></span>
<span data-ttu-id="0b5c4-110">**Set-AzVmssVM** cmdlet 'ı sanal makine ölçeği KÜMESI (VMSS) örneğinin durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0b5c4-110">The **Set-AzVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="0b5c4-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b5c4-111">EXAMPLES</span></span>

## <span data-ttu-id="0b5c4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b5c4-112">PARAMETERS</span></span>

### <span data-ttu-id="0b5c4-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="0b5c4-113">-AsJob</span></span>
<span data-ttu-id="0b5c4-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0b5c4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b5c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b5c4-115">-DefaultProfile</span></span>
<span data-ttu-id="0b5c4-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b5c4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b5c4-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="0b5c4-117">-InstanceId</span></span>
<span data-ttu-id="0b5c4-118">Bu cmdlet 'in durumu değiştirdiği VMSS örneğinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b5c4-118">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

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

### <span data-ttu-id="0b5c4-119">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="0b5c4-119">-PerformMaintenance</span></span>
<span data-ttu-id="0b5c4-120">Bu cmdlet 'in VMSS 'deki bir sanal makinede bakım gerçekleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b5c4-120">Indicates that this cmdlet performs maintenance on a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="0b5c4-121">-Yeniden dağıtma</span><span class="sxs-lookup"><span data-stu-id="0b5c4-121">-Redeploy</span></span>
<span data-ttu-id="0b5c4-122">Bu cmdlet 'in VMSS 'de bir sanal makineyi yeniden dağıttığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b5c4-122">Indicates that this cmdlet redeploys a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="0b5c4-123">-Yeniden görüntü</span><span class="sxs-lookup"><span data-stu-id="0b5c4-123">-Reimage</span></span>
<span data-ttu-id="0b5c4-124">Bu cmdlet 'in VMSS örneğini yeniden görüntüdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b5c4-124">Indicates that this cmdlet reimages the VMSS instance.</span></span>

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

### <span data-ttu-id="0b5c4-125">-Reımageall</span><span class="sxs-lookup"><span data-stu-id="0b5c4-125">-ReimageAll</span></span>
<span data-ttu-id="0b5c4-126">Cmdlet 'in VMSS örneğindeki tüm diskleri yeniden göndereceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b5c4-126">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

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

### <span data-ttu-id="0b5c4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b5c4-127">-ResourceGroupName</span></span>
<span data-ttu-id="0b5c4-128">VMSS örneğini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b5c4-128">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="0b5c4-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0b5c4-129">-VMScaleSetName</span></span>
<span data-ttu-id="0b5c4-130">Bu cmdlet 'in değiştirdiği VMSS örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b5c4-130">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0b5c4-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="0b5c4-131">-Confirm</span></span>
<span data-ttu-id="0b5c4-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0b5c4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b5c4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b5c4-133">-WhatIf</span></span>
<span data-ttu-id="0b5c4-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b5c4-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b5c4-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0b5c4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b5c4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b5c4-136">CommonParameters</span></span>
<span data-ttu-id="0b5c4-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b5c4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b5c4-138">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0b5c4-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b5c4-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b5c4-139">INPUTS</span></span>

### <span data-ttu-id="0b5c4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0b5c4-140">System.String</span></span>

## <span data-ttu-id="0b5c4-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b5c4-141">OUTPUTS</span></span>

### <span data-ttu-id="0b5c4-142">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="0b5c4-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="0b5c4-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b5c4-143">NOTES</span></span>

## <span data-ttu-id="0b5c4-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b5c4-144">RELATED LINKS</span></span>

[<span data-ttu-id="0b5c4-145">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="0b5c4-145">Get-AzVmssVM</span></span>](./Get-AzVmssVM.md)
