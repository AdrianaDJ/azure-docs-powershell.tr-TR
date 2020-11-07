---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: c7804c71ee4cfbccf24e298d2858fa2632f7a2b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752655"
---
# <span data-ttu-id="b8e45-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="b8e45-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="b8e45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8e45-102">SYNOPSIS</span></span>
<span data-ttu-id="b8e45-103">Tüm sanal makine ölçek kümesi örneklerini kullanılabilir en son Platform görüntüsü işletim sistemi sürümüne taşımak için çalışırken yükseltmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="b8e45-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="b8e45-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b8e45-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8e45-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b8e45-105">DESCRIPTION</span></span>
<span data-ttu-id="b8e45-106">Tüm sanal makine ölçek kümesi örneklerini kullanılabilir en son Platform görüntüsü işletim sistemi sürümüne taşımak için çalışırken yükseltmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="b8e45-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="b8e45-107">En son işletim sistemi sürümünü çalıştıran örnekler etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="b8e45-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="b8e45-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b8e45-108">EXAMPLES</span></span>

### <span data-ttu-id="b8e45-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b8e45-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="b8e45-110">Bu komut, "Group001" kaynak grubundaki "VMSS001" VM Ölçek kümesi 'nin tüm VM örneklerinin çalışırken yükseltmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="b8e45-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="b8e45-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b8e45-111">PARAMETERS</span></span>

### <span data-ttu-id="b8e45-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="b8e45-112">-AsJob</span></span>
<span data-ttu-id="b8e45-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b8e45-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8e45-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8e45-114">-DefaultProfile</span></span>
<span data-ttu-id="b8e45-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b8e45-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8e45-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8e45-116">-ResourceGroupName</span></span>
<span data-ttu-id="b8e45-117">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b8e45-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="b8e45-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b8e45-118">-VMScaleSetName</span></span>
<span data-ttu-id="b8e45-119">VM ölçeklendirme kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="b8e45-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="b8e45-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="b8e45-120">-Confirm</span></span>
<span data-ttu-id="b8e45-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b8e45-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8e45-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8e45-122">-WhatIf</span></span>
<span data-ttu-id="b8e45-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b8e45-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8e45-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b8e45-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8e45-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8e45-125">CommonParameters</span></span>
<span data-ttu-id="b8e45-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b8e45-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8e45-127">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b8e45-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8e45-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b8e45-128">INPUTS</span></span>

### <span data-ttu-id="b8e45-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b8e45-129">System.String</span></span>

## <span data-ttu-id="b8e45-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b8e45-130">OUTPUTS</span></span>

### <span data-ttu-id="b8e45-131">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="b8e45-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b8e45-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b8e45-132">NOTES</span></span>

## <span data-ttu-id="b8e45-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b8e45-133">RELATED LINKS</span></span>