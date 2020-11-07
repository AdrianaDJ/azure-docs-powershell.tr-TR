---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: fb35bac6f43ca444762ed1cbf8511d93eab10daf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917195"
---
# <span data-ttu-id="a03ea-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="a03ea-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="a03ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a03ea-102">SYNOPSIS</span></span>
<span data-ttu-id="a03ea-103">Geçerli sanal makine ölçek ayarı çalışırken yükseltmeyi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="a03ea-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="a03ea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a03ea-104">SYNTAX</span></span>

### <span data-ttu-id="a03ea-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a03ea-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a03ea-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="a03ea-106">FriendMethod</span></span>
```
Stop-AzVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a03ea-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a03ea-107">DESCRIPTION</span></span>
<span data-ttu-id="a03ea-108">Geçerli sanal makine ölçek ayarı çalışırken yükseltmeyi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="a03ea-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="a03ea-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a03ea-109">EXAMPLES</span></span>

### <span data-ttu-id="a03ea-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a03ea-110">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="a03ea-111">Bu komut, "Group001" kaynak grubundaki "VMSS001" VM Ölçek kümesi için çalışırken yükseltmeyi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="a03ea-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="a03ea-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a03ea-112">PARAMETERS</span></span>

### <span data-ttu-id="a03ea-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="a03ea-113">-AsJob</span></span>
<span data-ttu-id="a03ea-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a03ea-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a03ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a03ea-115">-DefaultProfile</span></span>
<span data-ttu-id="a03ea-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a03ea-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a03ea-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a03ea-117">-Force</span></span>
<span data-ttu-id="a03ea-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="a03ea-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a03ea-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a03ea-119">-ResourceGroupName</span></span>
<span data-ttu-id="a03ea-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a03ea-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="a03ea-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a03ea-121">-VMScaleSetName</span></span>
<span data-ttu-id="a03ea-122">VM ölçeklendirme kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="a03ea-122">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="a03ea-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="a03ea-123">-Confirm</span></span>
<span data-ttu-id="a03ea-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a03ea-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a03ea-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a03ea-125">-WhatIf</span></span>
<span data-ttu-id="a03ea-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a03ea-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a03ea-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a03ea-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a03ea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a03ea-128">CommonParameters</span></span>
<span data-ttu-id="a03ea-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a03ea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a03ea-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a03ea-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a03ea-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a03ea-131">INPUTS</span></span>

### <span data-ttu-id="a03ea-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a03ea-132">System.String</span></span>

## <span data-ttu-id="a03ea-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a03ea-133">OUTPUTS</span></span>

### <span data-ttu-id="a03ea-134">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="a03ea-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a03ea-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a03ea-135">NOTES</span></span>

## <span data-ttu-id="a03ea-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a03ea-136">RELATED LINKS</span></span>
