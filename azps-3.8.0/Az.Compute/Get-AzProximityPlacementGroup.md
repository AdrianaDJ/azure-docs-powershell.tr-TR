---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: a6308120303684a8e87280ef903056361fbaf848
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098909"
---
# <span data-ttu-id="cb6dd-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="cb6dd-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="cb6dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb6dd-102">SYNOPSIS</span></span>
<span data-ttu-id="cb6dd-103">Yakınlık Yerleşim grubu kaynakları alın veya listeleyin.</span><span class="sxs-lookup"><span data-stu-id="cb6dd-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="cb6dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb6dd-104">SYNTAX</span></span>

### <span data-ttu-id="cb6dd-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cb6dd-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-ColocationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb6dd-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="cb6dd-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ColocationStatus] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb6dd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb6dd-107">DESCRIPTION</span></span>
<span data-ttu-id="cb6dd-108">Bu cmdlet, yakınlık Yerleşim grubu kaynakları 'nı alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="cb6dd-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="cb6dd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb6dd-109">EXAMPLES</span></span>

### <span data-ttu-id="cb6dd-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cb6dd-110">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName

ResourceGroupName           : rg0
ProximityPlacementGroupType : Standard
VirtualMachines             : {}
VirtualMachineScaleSets     : {}
AvailabilitySets            : {}
Id                          : /subscriptions/5393f919-a68a-43d0-9063-4b2bda6bffdf/resourceGroups/rg0/providers/Microsoft.Compute/proximityPlacementGroups/ppg0
Name                        : ppg0
Type                        : Microsoft.Compute/proximityPlacementGroups
Location                    : westcentralus
Tags                        : {[key1, val1]}
```

<span data-ttu-id="cb6dd-111">Bu komut, yakınlık Yerleşim grubunu alır</span><span class="sxs-lookup"><span data-stu-id="cb6dd-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="cb6dd-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="cb6dd-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="cb6dd-113">Bu komut, verilen kaynak grubunun altındaki tüm yakınlık Yerleşim gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="cb6dd-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="cb6dd-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="cb6dd-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="cb6dd-115">Bu komut aboneliğin altındaki tüm yakınlık Yerleşim gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="cb6dd-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="cb6dd-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb6dd-116">PARAMETERS</span></span>

### <span data-ttu-id="cb6dd-117">-Kolombiya Cationstatus</span><span class="sxs-lookup"><span data-stu-id="cb6dd-117">-ColocationStatus</span></span>
<span data-ttu-id="cb6dd-118">Yakınlık yerleşimi grubundaki bir kaynağın ayırma durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="cb6dd-118">Shows the colocation status of a resource in the proximity placement group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb6dd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb6dd-119">-DefaultProfile</span></span>
<span data-ttu-id="cb6dd-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb6dd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb6dd-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="cb6dd-121">-Name</span></span>
<span data-ttu-id="cb6dd-122">Yakınlık Yerleşim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="cb6dd-122">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: ProximityPlacementGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="cb6dd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb6dd-123">-ResourceGroupName</span></span>
<span data-ttu-id="cb6dd-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="cb6dd-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="cb6dd-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cb6dd-125">-ResourceId</span></span>
<span data-ttu-id="cb6dd-126">Yakınlık Yerleşim grubu için kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="cb6dd-126">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="cb6dd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb6dd-127">CommonParameters</span></span>
<span data-ttu-id="cb6dd-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb6dd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb6dd-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cb6dd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb6dd-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb6dd-130">INPUTS</span></span>

### <span data-ttu-id="cb6dd-131">System. String</span><span class="sxs-lookup"><span data-stu-id="cb6dd-131">System.String</span></span>

## <span data-ttu-id="cb6dd-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb6dd-132">OUTPUTS</span></span>

### <span data-ttu-id="cb6dd-133">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="cb6dd-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="cb6dd-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb6dd-134">NOTES</span></span>

## <span data-ttu-id="cb6dd-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb6dd-135">RELATED LINKS</span></span>
