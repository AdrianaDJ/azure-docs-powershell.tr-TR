---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvmssrollingupgrade
schema: 2.0.0
ms.openlocfilehash: 8893f5fc8f6bf798635fdfd5e9a16bc4179815e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940168"
---
# <span data-ttu-id="8ec77-101">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="8ec77-101">Stop-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="8ec77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ec77-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec77-103">Geçerli sanal makine ölçek ayarı çalışırken yükseltmeyi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="8ec77-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ec77-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ec77-104">SYNTAX</span></span>

### <span data-ttu-id="8ec77-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8ec77-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ec77-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="8ec77-106">FriendMethod</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ec77-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ec77-107">DESCRIPTION</span></span>
<span data-ttu-id="8ec77-108">Geçerli sanal makine ölçek ayarı çalışırken yükseltmeyi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="8ec77-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="8ec77-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ec77-109">EXAMPLES</span></span>

### <span data-ttu-id="8ec77-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8ec77-110">Example 1</span></span>
```
PS C:\> Stop-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="8ec77-111">Bu komut, "Group001" kaynak grubundaki "VMSS001" VM Ölçek kümesi için çalışırken yükseltmeyi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="8ec77-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="8ec77-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ec77-112">PARAMETERS</span></span>

### <span data-ttu-id="8ec77-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="8ec77-113">-AsJob</span></span>
<span data-ttu-id="8ec77-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8ec77-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ec77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ec77-115">-DefaultProfile</span></span>
<span data-ttu-id="8ec77-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8ec77-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ec77-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8ec77-117">-Force</span></span>
<span data-ttu-id="8ec77-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="8ec77-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8ec77-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ec77-119">-ResourceGroupName</span></span>
<span data-ttu-id="8ec77-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8ec77-120">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec77-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8ec77-121">-VMScaleSetName</span></span>
<span data-ttu-id="8ec77-122">VM ölçeklendirme kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="8ec77-122">The name of the VM scale set.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec77-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="8ec77-123">-Confirm</span></span>
<span data-ttu-id="8ec77-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8ec77-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ec77-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ec77-125">-WhatIf</span></span>
<span data-ttu-id="8ec77-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8ec77-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ec77-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8ec77-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ec77-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec77-128">CommonParameters</span></span>
<span data-ttu-id="8ec77-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ec77-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec77-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ec77-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec77-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ec77-131">INPUTS</span></span>

### <span data-ttu-id="8ec77-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8ec77-132">System.String</span></span>

## <span data-ttu-id="8ec77-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ec77-133">OUTPUTS</span></span>

### <span data-ttu-id="8ec77-134">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="8ec77-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="8ec77-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ec77-135">NOTES</span></span>

## <span data-ttu-id="8ec77-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ec77-136">RELATED LINKS</span></span>

