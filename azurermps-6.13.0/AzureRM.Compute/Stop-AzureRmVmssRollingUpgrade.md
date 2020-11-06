---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
ms.openlocfilehash: 92a3a98ba5e6743b5d52ad619501fd6ed56c10c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588523"
---
# <span data-ttu-id="f2255-101">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="f2255-101">Stop-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="f2255-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2255-102">SYNOPSIS</span></span>
<span data-ttu-id="f2255-103">Geçerli sanal makine ölçek ayarı çalışırken yükseltmeyi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="f2255-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2255-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2255-104">SYNTAX</span></span>

### <span data-ttu-id="f2255-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f2255-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2255-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="f2255-106">FriendMethod</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2255-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2255-107">DESCRIPTION</span></span>
<span data-ttu-id="f2255-108">Geçerli sanal makine ölçek ayarı çalışırken yükseltmeyi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="f2255-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="f2255-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2255-109">EXAMPLES</span></span>

### <span data-ttu-id="f2255-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f2255-110">Example 1</span></span>
```
PS C:\> Stop-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="f2255-111">Bu komut, "Group001" kaynak grubundaki "VMSS001" VM Ölçek kümesi için çalışırken yükseltmeyi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="f2255-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="f2255-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2255-112">PARAMETERS</span></span>

### <span data-ttu-id="f2255-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="f2255-113">-AsJob</span></span>
<span data-ttu-id="f2255-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f2255-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2255-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2255-115">-DefaultProfile</span></span>
<span data-ttu-id="f2255-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f2255-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2255-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f2255-117">-Force</span></span>
<span data-ttu-id="f2255-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f2255-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f2255-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2255-119">-ResourceGroupName</span></span>
<span data-ttu-id="f2255-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f2255-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2255-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f2255-121">-VMScaleSetName</span></span>
<span data-ttu-id="f2255-122">VM ölçeklendirme kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="f2255-122">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2255-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="f2255-123">-Confirm</span></span>
<span data-ttu-id="f2255-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f2255-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2255-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2255-125">-WhatIf</span></span>
<span data-ttu-id="f2255-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f2255-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2255-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f2255-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2255-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2255-128">CommonParameters</span></span>
<span data-ttu-id="f2255-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2255-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2255-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2255-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2255-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2255-131">INPUTS</span></span>

### <span data-ttu-id="f2255-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f2255-132">System.String</span></span>

## <span data-ttu-id="f2255-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2255-133">OUTPUTS</span></span>

### <span data-ttu-id="f2255-134">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="f2255-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f2255-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2255-135">NOTES</span></span>

## <span data-ttu-id="f2255-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2255-136">RELATED LINKS</span></span>
