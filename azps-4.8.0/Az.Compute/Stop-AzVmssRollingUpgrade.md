---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 331f390890e6349c5a48f9b57c3d0e99fa972532
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108105"
---
# <span data-ttu-id="baf43-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="baf43-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="baf43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baf43-102">SYNOPSIS</span></span>
<span data-ttu-id="baf43-103">Geçerli sanal makine ölçek ayarı çalışırken yükseltmeyi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="baf43-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="baf43-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="baf43-104">SYNTAX</span></span>

```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baf43-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="baf43-105">DESCRIPTION</span></span>
<span data-ttu-id="baf43-106">Geçerli sanal makine ölçek ayarı çalışırken yükseltmeyi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="baf43-106">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="baf43-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="baf43-107">EXAMPLES</span></span>

### <span data-ttu-id="baf43-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="baf43-108">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="baf43-109">Bu komut, "Group001" kaynak grubundaki "VMSS001" VM Ölçek kümesi için çalışırken yükseltmeyi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="baf43-109">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="baf43-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="baf43-110">PARAMETERS</span></span>

### <span data-ttu-id="baf43-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="baf43-111">-AsJob</span></span>
<span data-ttu-id="baf43-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="baf43-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="baf43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baf43-113">-DefaultProfile</span></span>
<span data-ttu-id="baf43-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="baf43-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baf43-115">-Force</span><span class="sxs-lookup"><span data-stu-id="baf43-115">-Force</span></span>
<span data-ttu-id="baf43-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="baf43-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="baf43-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baf43-117">-ResourceGroupName</span></span>
<span data-ttu-id="baf43-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="baf43-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="baf43-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="baf43-119">-VMScaleSetName</span></span>
<span data-ttu-id="baf43-120">VM ölçeklendirme kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="baf43-120">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="baf43-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="baf43-121">-Confirm</span></span>
<span data-ttu-id="baf43-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="baf43-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baf43-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baf43-123">-WhatIf</span></span>
<span data-ttu-id="baf43-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="baf43-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baf43-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="baf43-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baf43-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baf43-126">CommonParameters</span></span>
<span data-ttu-id="baf43-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="baf43-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baf43-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="baf43-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baf43-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="baf43-129">INPUTS</span></span>

### <span data-ttu-id="baf43-130">System. String</span><span class="sxs-lookup"><span data-stu-id="baf43-130">System.String</span></span>

## <span data-ttu-id="baf43-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="baf43-131">OUTPUTS</span></span>

### <span data-ttu-id="baf43-132">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="baf43-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="baf43-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="baf43-133">NOTES</span></span>

## <span data-ttu-id="baf43-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="baf43-134">RELATED LINKS</span></span>
