---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: f71e827769015b7abe4d503064d97ec1d3c1228b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593291"
---
# <span data-ttu-id="e0ba9-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="e0ba9-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="e0ba9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0ba9-102">SYNOPSIS</span></span>
<span data-ttu-id="e0ba9-103">Bir VMSS örneğinin durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e0ba9-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0ba9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0ba9-104">SYNTAX</span></span>

### <span data-ttu-id="e0ba9-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e0ba9-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0ba9-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="e0ba9-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0ba9-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="e0ba9-107">RedeployMethodParameter</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0ba9-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="e0ba9-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0ba9-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0ba9-109">DESCRIPTION</span></span>
<span data-ttu-id="e0ba9-110">**Set-AzureRmVmssVM** cmdlet 'ı sanal makine ölçeği KÜMESI (VMSS) örneğinin durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e0ba9-110">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="e0ba9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0ba9-111">EXAMPLES</span></span>

## <span data-ttu-id="e0ba9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0ba9-112">PARAMETERS</span></span>

### <span data-ttu-id="e0ba9-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="e0ba9-113">-AsJob</span></span>
<span data-ttu-id="e0ba9-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e0ba9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0ba9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ba9-115">-DefaultProfile</span></span>
<span data-ttu-id="e0ba9-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e0ba9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ba9-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="e0ba9-117">-InstanceId</span></span>
<span data-ttu-id="e0ba9-118">Bu cmdlet 'in durumu değiştirdiği VMSS örneğinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0ba9-118">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ba9-119">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="e0ba9-119">-PerformMaintenance</span></span>
<span data-ttu-id="e0ba9-120">Bu cmdlet 'in VMSS 'deki bir sanal makinede bakım gerçekleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0ba9-120">Indicates that this cmdlet performs maintenance on a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="e0ba9-121">-Yeniden dağıtma</span><span class="sxs-lookup"><span data-stu-id="e0ba9-121">-Redeploy</span></span>
<span data-ttu-id="e0ba9-122">Bu cmdlet 'in VMSS 'de bir sanal makineyi yeniden dağıttığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0ba9-122">Indicates that this cmdlet redeploys a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="e0ba9-123">-Yeniden görüntü</span><span class="sxs-lookup"><span data-stu-id="e0ba9-123">-Reimage</span></span>
<span data-ttu-id="e0ba9-124">Bu cmdlet 'in VMSS örneğini yeniden görüntüdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0ba9-124">Indicates that this cmdlet reimages the VMSS instance.</span></span>

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

### <span data-ttu-id="e0ba9-125">-Reımageall</span><span class="sxs-lookup"><span data-stu-id="e0ba9-125">-ReimageAll</span></span>
<span data-ttu-id="e0ba9-126">Cmdlet 'in VMSS örneğindeki tüm diskleri yeniden göndereceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0ba9-126">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

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

### <span data-ttu-id="e0ba9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0ba9-127">-ResourceGroupName</span></span>
<span data-ttu-id="e0ba9-128">VMSS örneğini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0ba9-128">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="e0ba9-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e0ba9-129">-VMScaleSetName</span></span>
<span data-ttu-id="e0ba9-130">Bu cmdlet 'in değiştirdiği VMSS örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0ba9-130">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ba9-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="e0ba9-131">-Confirm</span></span>
<span data-ttu-id="e0ba9-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e0ba9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0ba9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0ba9-133">-WhatIf</span></span>
<span data-ttu-id="e0ba9-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0ba9-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0ba9-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e0ba9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0ba9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ba9-136">CommonParameters</span></span>
<span data-ttu-id="e0ba9-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0ba9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ba9-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0ba9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ba9-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0ba9-139">INPUTS</span></span>

### <span data-ttu-id="e0ba9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e0ba9-140">System.String</span></span>

## <span data-ttu-id="e0ba9-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0ba9-141">OUTPUTS</span></span>

### <span data-ttu-id="e0ba9-142">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="e0ba9-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e0ba9-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0ba9-143">NOTES</span></span>

## <span data-ttu-id="e0ba9-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0ba9-144">RELATED LINKS</span></span>

[<span data-ttu-id="e0ba9-145">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="e0ba9-145">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
