---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVM.md
ms.openlocfilehash: f8451f4164b58c2d6599778ab86dfca4e5ff79dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588531"
---
# <span data-ttu-id="ce134-101">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ce134-101">Restart-AzureRmVM</span></span>

## <span data-ttu-id="ce134-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce134-102">SYNOPSIS</span></span>
<span data-ttu-id="ce134-103">Azure sanal makinesini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="ce134-103">Restarts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce134-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce134-104">SYNTAX</span></span>

### <span data-ttu-id="ce134-105">RestartResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ce134-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce134-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ce134-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce134-107">Restartivseçparametersetname</span><span class="sxs-lookup"><span data-stu-id="ce134-107">RestartIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce134-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ce134-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce134-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce134-109">DESCRIPTION</span></span>
<span data-ttu-id="ce134-110">**Restart-AzureRmVM** cmdlet 'ı bir Azure sanal makinesini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="ce134-110">The **Restart-AzureRmVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="ce134-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce134-111">EXAMPLES</span></span>

### <span data-ttu-id="ce134-112">Örnek 1: sanal makineyi yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="ce134-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="ce134-113">Bu komut, ResourceGroup11 'da VirtualMachine07 adındaki sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="ce134-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="ce134-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce134-114">PARAMETERS</span></span>

### <span data-ttu-id="ce134-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="ce134-115">-AsJob</span></span>
<span data-ttu-id="ce134-116">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="ce134-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ce134-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce134-117">-DefaultProfile</span></span>
<span data-ttu-id="ce134-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ce134-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce134-119">-ID</span><span class="sxs-lookup"><span data-stu-id="ce134-119">-Id</span></span>
<span data-ttu-id="ce134-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ce134-120">The resource group name.</span></span>

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

### <span data-ttu-id="ce134-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="ce134-121">-Name</span></span>
<span data-ttu-id="ce134-122">Sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="ce134-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="ce134-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="ce134-123">-PerformMaintenance</span></span>
<span data-ttu-id="ce134-124">Sanal makinenin bakımını yapmak için.</span><span class="sxs-lookup"><span data-stu-id="ce134-124">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="ce134-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce134-125">-ResourceGroupName</span></span>
<span data-ttu-id="ce134-126">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce134-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ce134-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="ce134-127">-Confirm</span></span>
<span data-ttu-id="ce134-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ce134-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce134-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce134-129">-WhatIf</span></span>
<span data-ttu-id="ce134-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce134-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce134-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ce134-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce134-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce134-132">CommonParameters</span></span>
<span data-ttu-id="ce134-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce134-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce134-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce134-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce134-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce134-135">INPUTS</span></span>

### <span data-ttu-id="ce134-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ce134-136">System.String</span></span>

### <span data-ttu-id="ce134-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ce134-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ce134-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce134-138">OUTPUTS</span></span>

### <span data-ttu-id="ce134-139">Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="ce134-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="ce134-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce134-140">NOTES</span></span>

## <span data-ttu-id="ce134-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce134-141">RELATED LINKS</span></span>

[<span data-ttu-id="ce134-142">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ce134-142">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="ce134-143">Yeni-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ce134-143">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="ce134-144">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ce134-144">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="ce134-145">Başlangıç-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ce134-145">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="ce134-146">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ce134-146">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="ce134-147">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ce134-147">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


