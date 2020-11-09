---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssorchestrationservicestate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
ms.openlocfilehash: c1fbc45a9d82733f73a13b13985bdd6746f4c075
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319646"
---
# <span data-ttu-id="61645-101">Set-AzVmssOrchestrationServiceState</span><span class="sxs-lookup"><span data-stu-id="61645-101">Set-AzVmssOrchestrationServiceState</span></span>

## <span data-ttu-id="61645-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61645-102">SYNOPSIS</span></span>
<span data-ttu-id="61645-103">VMSS için Orchestration hizmeti durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="61645-103">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="61645-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61645-104">SYNTAX</span></span>

### <span data-ttu-id="61645-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="61645-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssOrchestrationServiceState [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-ServiceName] <String> [-Action] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61645-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="61645-106">ResourceIdParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61645-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="61645-107">ObjectParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String>
 [-InputObject] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61645-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="61645-108">DESCRIPTION</span></span>
<span data-ttu-id="61645-109">VMSS için Orchestration hizmeti durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="61645-109">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="61645-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61645-110">EXAMPLES</span></span>

### <span data-ttu-id="61645-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="61645-111">Example 1</span></span>
```
PS C:\> Set-AzVmssOrchestrationServiceState -ResourceGroupName "rg" -VMScaleSetName "vmss1" -ServiceName "AutomaticRepairs" -Action "Suspend"
```

<span data-ttu-id="61645-112">Bu komut, "RG" kaynak grubundaki VMSS "vmss1" üzerinde otomatik onarım hizmetini askıya alır.</span><span class="sxs-lookup"><span data-stu-id="61645-112">This command suspends Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

### <span data-ttu-id="61645-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="61645-113">Example 2</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "rg" -VMScaleSetName "vmss1" | Set-AzVmssOrchestrationServiceState -ServiceName "AutomaticRepairs" -Action "Resume"
```

<span data-ttu-id="61645-114">Bu komut, "RG" kaynak grubundaki VMSS "vmss1" üzerinde otomatik onarım hizmetini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="61645-114">This command resumes Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

## <span data-ttu-id="61645-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61645-115">PARAMETERS</span></span>

### <span data-ttu-id="61645-116">-Eylem</span><span class="sxs-lookup"><span data-stu-id="61645-116">-Action</span></span>
<span data-ttu-id="61645-117">Gerçekleştirilecek eylem.</span><span class="sxs-lookup"><span data-stu-id="61645-117">The action to be performed.</span></span>  <span data-ttu-id="61645-118">Olası değerler: özgeçmiş, askıya al.</span><span class="sxs-lookup"><span data-stu-id="61645-118">Possible values are: Resume, Suspend.</span></span>

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

### <span data-ttu-id="61645-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="61645-119">-AsJob</span></span>
<span data-ttu-id="61645-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="61645-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61645-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61645-121">-DefaultProfile</span></span>
<span data-ttu-id="61645-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="61645-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61645-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61645-123">-InputObject</span></span>
<span data-ttu-id="61645-124">Sanal makine ölçek kümesinin yerel nesnesi.</span><span class="sxs-lookup"><span data-stu-id="61645-124">The local object of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="61645-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61645-125">-ResourceGroupName</span></span>
<span data-ttu-id="61645-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="61645-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="61645-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="61645-127">-ResourceId</span></span>
<span data-ttu-id="61645-128">Kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="61645-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="61645-129">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="61645-129">-ServiceName</span></span>
<span data-ttu-id="61645-130">Hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="61645-130">The name of the service.</span></span>

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

### <span data-ttu-id="61645-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="61645-131">-VMScaleSetName</span></span>
<span data-ttu-id="61645-132">Sanal makine ölçek kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="61645-132">The name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="61645-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="61645-133">-Confirm</span></span>
<span data-ttu-id="61645-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="61645-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61645-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61645-135">-WhatIf</span></span>
<span data-ttu-id="61645-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61645-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61645-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="61645-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61645-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61645-138">CommonParameters</span></span>
<span data-ttu-id="61645-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61645-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61645-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="61645-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61645-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61645-141">INPUTS</span></span>

### <span data-ttu-id="61645-142">System. String</span><span class="sxs-lookup"><span data-stu-id="61645-142">System.String</span></span>

### <span data-ttu-id="61645-143">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="61645-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="61645-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61645-144">OUTPUTS</span></span>

### <span data-ttu-id="61645-145">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="61645-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="61645-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61645-146">NOTES</span></span>

## <span data-ttu-id="61645-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61645-147">RELATED LINKS</span></span>
