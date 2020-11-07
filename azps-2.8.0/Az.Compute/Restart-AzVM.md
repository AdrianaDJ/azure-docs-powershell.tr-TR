---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 8fe939bfb959a1a6bc2dc043dbc3948943aa2c05
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752745"
---
# <span data-ttu-id="3f4d5-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="3f4d5-101">Restart-AzVM</span></span>

## <span data-ttu-id="3f4d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f4d5-102">SYNOPSIS</span></span>
<span data-ttu-id="3f4d5-103">Azure sanal makinesini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="3f4d5-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="3f4d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3f4d5-104">SYNTAX</span></span>

### <span data-ttu-id="3f4d5-105">RestartResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3f4d5-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f4d5-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3f4d5-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f4d5-107">Restartivseçparametersetname</span><span class="sxs-lookup"><span data-stu-id="3f4d5-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f4d5-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3f4d5-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f4d5-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="3f4d5-109">DESCRIPTION</span></span>
<span data-ttu-id="3f4d5-110">**Restart-AzVM** cmdlet 'ı bir Azure sanal makinesini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="3f4d5-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="3f4d5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3f4d5-111">EXAMPLES</span></span>

### <span data-ttu-id="3f4d5-112">Örnek 1: sanal makineyi yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="3f4d5-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="3f4d5-113">Bu komut, ResourceGroup11 'da VirtualMachine07 adındaki sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="3f4d5-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="3f4d5-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3f4d5-114">PARAMETERS</span></span>

### <span data-ttu-id="3f4d5-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="3f4d5-115">-AsJob</span></span>
<span data-ttu-id="3f4d5-116">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="3f4d5-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3f4d5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f4d5-117">-DefaultProfile</span></span>
<span data-ttu-id="3f4d5-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3f4d5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f4d5-119">-ID</span><span class="sxs-lookup"><span data-stu-id="3f4d5-119">-Id</span></span>
<span data-ttu-id="3f4d5-120">Sanal makinenin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3f4d5-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d5-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="3f4d5-121">-Name</span></span>
<span data-ttu-id="3f4d5-122">Sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="3f4d5-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d5-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3f4d5-123">-NoWait</span></span>
<span data-ttu-id="3f4d5-124">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="3f4d5-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="3f4d5-125">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="3f4d5-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="3f4d5-126">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="3f4d5-126">-PerformMaintenance</span></span>
<span data-ttu-id="3f4d5-127">Sanal makinenin bakımını yapmak için.</span><span class="sxs-lookup"><span data-stu-id="3f4d5-127">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f4d5-128">-ResourceGroupName</span></span>
<span data-ttu-id="3f4d5-129">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f4d5-129">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d5-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="3f4d5-130">-Confirm</span></span>
<span data-ttu-id="3f4d5-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3f4d5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f4d5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f4d5-132">-WhatIf</span></span>
<span data-ttu-id="3f4d5-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f4d5-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f4d5-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3f4d5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f4d5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f4d5-135">CommonParameters</span></span>
<span data-ttu-id="3f4d5-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3f4d5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f4d5-137">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3f4d5-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f4d5-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3f4d5-138">INPUTS</span></span>

### <span data-ttu-id="3f4d5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3f4d5-139">System.String</span></span>

### <span data-ttu-id="3f4d5-140">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3f4d5-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3f4d5-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3f4d5-141">OUTPUTS</span></span>

### <span data-ttu-id="3f4d5-142">Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="3f4d5-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="3f4d5-143">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3f4d5-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3f4d5-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3f4d5-144">NOTES</span></span>

## <span data-ttu-id="3f4d5-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3f4d5-145">RELATED LINKS</span></span>

[<span data-ttu-id="3f4d5-146">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="3f4d5-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="3f4d5-147">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="3f4d5-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="3f4d5-148">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="3f4d5-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="3f4d5-149">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="3f4d5-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="3f4d5-150">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="3f4d5-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="3f4d5-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="3f4d5-151">Update-AzVM</span></span>](./Update-AzVM.md)


