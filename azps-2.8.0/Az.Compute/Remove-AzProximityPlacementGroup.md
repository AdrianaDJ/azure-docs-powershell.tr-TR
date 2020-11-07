---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
ms.openlocfilehash: 2a3f4a6d386f37334908efde31332ed6137ecb74
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752790"
---
# <span data-ttu-id="f1841-101">Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f1841-101">Remove-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="f1841-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1841-102">SYNOPSIS</span></span>
<span data-ttu-id="f1841-103">Yakınlık Yerleşim grubu kaynağını silin.</span><span class="sxs-lookup"><span data-stu-id="f1841-103">Delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="f1841-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1841-104">SYNTAX</span></span>

### <span data-ttu-id="f1841-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f1841-105">DefaultParameter (Default)</span></span>
```
Remove-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1841-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="f1841-106">ResourceIdParameter</span></span>
```
Remove-AzProximityPlacementGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1841-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="f1841-107">ObjectParameter</span></span>
```
Remove-AzProximityPlacementGroup [-InputObject] <PSProximityPlacementGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1841-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1841-108">DESCRIPTION</span></span>
<span data-ttu-id="f1841-109">Bu cmdlet, yakınlık Yerleşim grubu kaynağını silecek.</span><span class="sxs-lookup"><span data-stu-id="f1841-109">This cmdlet will delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="f1841-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1841-110">EXAMPLES</span></span>

### <span data-ttu-id="f1841-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f1841-111">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup  -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName  | Remove-AzureRmProximityPlacementGroup
```

<span data-ttu-id="f1841-112">Bu komut, verilen yakınlık Yerleşim grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f1841-112">This command removes the given proximity placement group.</span></span>

## <span data-ttu-id="f1841-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1841-113">PARAMETERS</span></span>

### <span data-ttu-id="f1841-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="f1841-114">-AsJob</span></span>
<span data-ttu-id="f1841-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f1841-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1841-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1841-116">-DefaultProfile</span></span>
<span data-ttu-id="f1841-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1841-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1841-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f1841-118">-Force</span></span>
<span data-ttu-id="f1841-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f1841-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1841-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1841-120">-InputObject</span></span>
<span data-ttu-id="f1841-121">PS yakınlık Yerleşim grubu nesnesi</span><span class="sxs-lookup"><span data-stu-id="f1841-121">The PS Proximity Placement Group Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup
Parameter Sets: ObjectParameter
Aliases: ProximityPlacementGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1841-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="f1841-122">-Name</span></span>
<span data-ttu-id="f1841-123">Yakınlık Yerleşim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f1841-123">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: ProximityPlacementGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1841-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1841-124">-ResourceGroupName</span></span>
<span data-ttu-id="f1841-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f1841-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="f1841-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f1841-126">-ResourceId</span></span>
<span data-ttu-id="f1841-127">Yakınlık Yerleşim grubu için kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f1841-127">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="f1841-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="f1841-128">-Confirm</span></span>
<span data-ttu-id="f1841-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f1841-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1841-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1841-130">-WhatIf</span></span>
<span data-ttu-id="f1841-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f1841-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1841-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f1841-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1841-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1841-133">CommonParameters</span></span>
<span data-ttu-id="f1841-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1841-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1841-135">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f1841-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1841-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1841-136">INPUTS</span></span>

### <span data-ttu-id="f1841-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f1841-137">System.String</span></span>

### <span data-ttu-id="f1841-138">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f1841-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="f1841-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1841-139">OUTPUTS</span></span>

### <span data-ttu-id="f1841-140">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="f1841-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f1841-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1841-141">NOTES</span></span>

## <span data-ttu-id="f1841-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1841-142">RELATED LINKS</span></span>
