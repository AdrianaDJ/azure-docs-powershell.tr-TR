---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: 9ec2760ba50d4ed97ebf36f5bab7c02d110d77ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752946"
---
# <span data-ttu-id="7e11f-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="7e11f-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="7e11f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e11f-102">SYNOPSIS</span></span>
<span data-ttu-id="7e11f-103">Yakınlık Yerleşim grubu kaynakları alın veya listeleyin.</span><span class="sxs-lookup"><span data-stu-id="7e11f-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="7e11f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e11f-104">SYNTAX</span></span>

### <span data-ttu-id="7e11f-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7e11f-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e11f-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="7e11f-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e11f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e11f-107">DESCRIPTION</span></span>
<span data-ttu-id="7e11f-108">Bu cmdlet, yakınlık Yerleşim grubu kaynakları 'nı alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="7e11f-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="7e11f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e11f-109">EXAMPLES</span></span>

### <span data-ttu-id="7e11f-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7e11f-110">Example 1</span></span>
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

<span data-ttu-id="7e11f-111">Bu komut, yakınlık Yerleşim grubunu alır</span><span class="sxs-lookup"><span data-stu-id="7e11f-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="7e11f-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7e11f-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="7e11f-113">Bu komut, verilen kaynak grubunun altındaki tüm yakınlık Yerleşim gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="7e11f-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="7e11f-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="7e11f-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="7e11f-115">Bu komut aboneliğin altındaki tüm yakınlık Yerleşim gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="7e11f-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="7e11f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e11f-116">PARAMETERS</span></span>

### <span data-ttu-id="7e11f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e11f-117">-DefaultProfile</span></span>
<span data-ttu-id="7e11f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7e11f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e11f-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="7e11f-119">-Name</span></span>
<span data-ttu-id="7e11f-120">Yakınlık Yerleşim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7e11f-120">The name of the proximity placement group.</span></span>

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

### <span data-ttu-id="7e11f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e11f-121">-ResourceGroupName</span></span>
<span data-ttu-id="7e11f-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7e11f-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="7e11f-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7e11f-123">-ResourceId</span></span>
<span data-ttu-id="7e11f-124">Yakınlık Yerleşim grubu için kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="7e11f-124">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="7e11f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e11f-125">CommonParameters</span></span>
<span data-ttu-id="7e11f-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e11f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e11f-127">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7e11f-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e11f-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e11f-128">INPUTS</span></span>

### <span data-ttu-id="7e11f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7e11f-129">System.String</span></span>

## <span data-ttu-id="7e11f-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e11f-130">OUTPUTS</span></span>

### <span data-ttu-id="7e11f-131">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="7e11f-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="7e11f-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e11f-132">NOTES</span></span>

## <span data-ttu-id="7e11f-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e11f-133">RELATED LINKS</span></span>
