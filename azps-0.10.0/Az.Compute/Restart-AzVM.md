---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: f7965e43c7a294d50d6f0774f76504a90c9d7148
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936889"
---
# <span data-ttu-id="55711-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="55711-101">Restart-AzVM</span></span>

## <span data-ttu-id="55711-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55711-102">SYNOPSIS</span></span>
<span data-ttu-id="55711-103">Azure sanal makinesini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="55711-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="55711-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55711-104">SYNTAX</span></span>

### <span data-ttu-id="55711-105">RestartResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="55711-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55711-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="55711-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55711-107">Restartivseçparametersetname</span><span class="sxs-lookup"><span data-stu-id="55711-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55711-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="55711-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55711-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="55711-109">DESCRIPTION</span></span>
<span data-ttu-id="55711-110">**Restart-AzVM** cmdlet 'ı bir Azure sanal makinesini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="55711-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="55711-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55711-111">EXAMPLES</span></span>

### <span data-ttu-id="55711-112">Örnek 1: sanal makineyi yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="55711-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="55711-113">Bu komut, ResourceGroup11 'da VirtualMachine07 adındaki sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="55711-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="55711-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55711-114">PARAMETERS</span></span>

### <span data-ttu-id="55711-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="55711-115">-AsJob</span></span>
<span data-ttu-id="55711-116">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="55711-116">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55711-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55711-117">-DefaultProfile</span></span>
<span data-ttu-id="55711-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55711-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55711-119">-ID</span><span class="sxs-lookup"><span data-stu-id="55711-119">-Id</span></span>
<span data-ttu-id="55711-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="55711-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55711-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="55711-121">-Name</span></span>
<span data-ttu-id="55711-122">Sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="55711-122">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55711-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="55711-123">-PerformMaintenance</span></span>
<span data-ttu-id="55711-124">Sanal makinenin bakımını yapmak için.</span><span class="sxs-lookup"><span data-stu-id="55711-124">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55711-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55711-125">-ResourceGroupName</span></span>
<span data-ttu-id="55711-126">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55711-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55711-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="55711-127">-Confirm</span></span>
<span data-ttu-id="55711-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="55711-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55711-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55711-129">-WhatIf</span></span>
<span data-ttu-id="55711-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="55711-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55711-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="55711-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55711-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55711-132">CommonParameters</span></span>
<span data-ttu-id="55711-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55711-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55711-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55711-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55711-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55711-135">INPUTS</span></span>

### <span data-ttu-id="55711-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="55711-136">None</span></span>
<span data-ttu-id="55711-137">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="55711-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="55711-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55711-138">OUTPUTS</span></span>

### <span data-ttu-id="55711-139">Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="55711-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="55711-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55711-140">NOTES</span></span>

## <span data-ttu-id="55711-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55711-141">RELATED LINKS</span></span>

[<span data-ttu-id="55711-142">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="55711-142">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="55711-143">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="55711-143">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="55711-144">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="55711-144">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="55711-145">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="55711-145">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="55711-146">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="55711-146">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="55711-147">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="55711-147">Update-AzVM</span></span>](./Update-AzVM.md)


