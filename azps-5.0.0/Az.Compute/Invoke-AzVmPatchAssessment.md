---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
ms.openlocfilehash: 5ccaccdc5d447ac9ccdc49cf53230c58a5758e4d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276794"
---
# <span data-ttu-id="cd1fa-101">Invoke-AzVMPatchAssessment</span><span class="sxs-lookup"><span data-stu-id="cd1fa-101">Invoke-AzVMPatchAssessment</span></span>

## <span data-ttu-id="cd1fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd1fa-102">SYNOPSIS</span></span>
<span data-ttu-id="cd1fa-103">Sanal makinenin düzeltme eki durumunu değerlendirin.</span><span class="sxs-lookup"><span data-stu-id="cd1fa-103">Assess patch state of a virtual machine.</span></span>

## <span data-ttu-id="cd1fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd1fa-104">SYNTAX</span></span>

### <span data-ttu-id="cd1fa-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cd1fa-105">DefaultParameterSet (Default)</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd1fa-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="cd1fa-106">ResourceIDParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd1fa-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="cd1fa-107">InputObjectParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd1fa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd1fa-108">DESCRIPTION</span></span>
<span data-ttu-id="cd1fa-109">Assesses bir VM 'in düzeltme durumunu bildirir ve tüm algılanan düzeltme eklerini yükleme için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="cd1fa-109">Assesses the patch status of a VM and reports all detected patches that are available for installation.</span></span>

## <span data-ttu-id="cd1fa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd1fa-110">EXAMPLES</span></span>

### <span data-ttu-id="cd1fa-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cd1fa-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmPatchAssessment -ResourceGroupName "myRG" -VMName "myVM"
```

## <span data-ttu-id="cd1fa-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd1fa-112">PARAMETERS</span></span>

### <span data-ttu-id="cd1fa-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="cd1fa-113">-AsJob</span></span>
<span data-ttu-id="cd1fa-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="cd1fa-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd1fa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd1fa-115">-DefaultProfile</span></span>
<span data-ttu-id="cd1fa-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cd1fa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd1fa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd1fa-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd1fa-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd1fa-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd1fa-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cd1fa-119">-ResourceId</span></span>
<span data-ttu-id="cd1fa-120">Sanal makinenizin kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cd1fa-120">Resource ID for your virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd1fa-121">-VM</span><span class="sxs-lookup"><span data-stu-id="cd1fa-121">-VM</span></span>
<span data-ttu-id="cd1fa-122">PowerShell sanal makine nesnesi</span><span class="sxs-lookup"><span data-stu-id="cd1fa-122">PowerShell Virtual Machine Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: InputObjectParameterSet
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd1fa-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="cd1fa-123">-VMName</span></span>
<span data-ttu-id="cd1fa-124">Sanal makine adı</span><span class="sxs-lookup"><span data-stu-id="cd1fa-124">Virtual Machine name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd1fa-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="cd1fa-125">-Confirm</span></span>
<span data-ttu-id="cd1fa-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cd1fa-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd1fa-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd1fa-127">-WhatIf</span></span>
<span data-ttu-id="cd1fa-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd1fa-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd1fa-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cd1fa-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd1fa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd1fa-130">CommonParameters</span></span>
<span data-ttu-id="cd1fa-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd1fa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd1fa-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cd1fa-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd1fa-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd1fa-133">INPUTS</span></span>

### <span data-ttu-id="cd1fa-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cd1fa-134">System.String</span></span>

## <span data-ttu-id="cd1fa-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd1fa-135">OUTPUTS</span></span>

### <span data-ttu-id="cd1fa-136">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachinePatchAssessmentResult</span><span class="sxs-lookup"><span data-stu-id="cd1fa-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span></span>

## <span data-ttu-id="cd1fa-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd1fa-137">NOTES</span></span>

## <span data-ttu-id="cd1fa-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd1fa-138">RELATED LINKS</span></span>
