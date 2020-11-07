---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
ms.openlocfilehash: 07adbff46713136ec412d10bd428765230e1838c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938533"
---
# <span data-ttu-id="b4ed0-101">Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="b4ed0-101">Remove-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="b4ed0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4ed0-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ed0-103">Yakınlık Yerleşim grubu kaynağını silin.</span><span class="sxs-lookup"><span data-stu-id="b4ed0-103">Delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="b4ed0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4ed0-104">SYNTAX</span></span>

### <span data-ttu-id="b4ed0-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4ed0-105">DefaultParameter (Default)</span></span>
```
Remove-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4ed0-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="b4ed0-106">ResourceIdParameter</span></span>
```
Remove-AzProximityPlacementGroup [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4ed0-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="b4ed0-107">ObjectParameter</span></span>
```
Remove-AzProximityPlacementGroup [-Force] [-InputObject] <PSProximityPlacementGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4ed0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4ed0-108">DESCRIPTION</span></span>
<span data-ttu-id="b4ed0-109">Bu cmdlet, yakınlık Yerleşim grubu kaynağını silecek.</span><span class="sxs-lookup"><span data-stu-id="b4ed0-109">This cmdlet will delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="b4ed0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4ed0-110">EXAMPLES</span></span>

### <span data-ttu-id="b4ed0-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b4ed0-111">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup  -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName  | Remove-AzureRmProximityPlacementGroup
```

<span data-ttu-id="b4ed0-112">Bu komut, verilen yakınlık Yerleşim grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b4ed0-112">This command removes the given proximity placement group.</span></span>

## <span data-ttu-id="b4ed0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4ed0-113">PARAMETERS</span></span>

### <span data-ttu-id="b4ed0-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="b4ed0-114">-AsJob</span></span>
<span data-ttu-id="b4ed0-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b4ed0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4ed0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ed0-116">-DefaultProfile</span></span>
<span data-ttu-id="b4ed0-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4ed0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4ed0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b4ed0-118">-Force</span></span>
<span data-ttu-id="b4ed0-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b4ed0-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4ed0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4ed0-120">-InputObject</span></span>
<span data-ttu-id="b4ed0-121">PS yakınlık Yerleşim grubu nesnesi</span><span class="sxs-lookup"><span data-stu-id="b4ed0-121">The PS Proximity Placement Group Object</span></span>

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

### <span data-ttu-id="b4ed0-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="b4ed0-122">-Name</span></span>
<span data-ttu-id="b4ed0-123">Yakınlık Yerleşim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b4ed0-123">The name of the proximity placement group.</span></span>

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

### <span data-ttu-id="b4ed0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4ed0-124">-ResourceGroupName</span></span>
<span data-ttu-id="b4ed0-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b4ed0-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="b4ed0-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b4ed0-126">-ResourceId</span></span>
<span data-ttu-id="b4ed0-127">Yakınlık Yerleşim grubu için kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="b4ed0-127">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="b4ed0-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="b4ed0-128">-Confirm</span></span>
<span data-ttu-id="b4ed0-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b4ed0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4ed0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4ed0-130">-WhatIf</span></span>
<span data-ttu-id="b4ed0-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4ed0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4ed0-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b4ed0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4ed0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ed0-133">CommonParameters</span></span>
<span data-ttu-id="b4ed0-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4ed0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ed0-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b4ed0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ed0-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4ed0-136">INPUTS</span></span>

### <span data-ttu-id="b4ed0-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b4ed0-137">System.String</span></span>

### <span data-ttu-id="b4ed0-138">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="b4ed0-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="b4ed0-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4ed0-139">OUTPUTS</span></span>

### <span data-ttu-id="b4ed0-140">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="b4ed0-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b4ed0-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4ed0-141">NOTES</span></span>

## <span data-ttu-id="b4ed0-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4ed0-142">RELATED LINKS</span></span>
