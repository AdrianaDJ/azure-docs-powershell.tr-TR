---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
ms.openlocfilehash: cf8c4867fcc623065cce73fa392cb78d513200fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096930"
---
# <span data-ttu-id="d37fa-101">New-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d37fa-101">New-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="d37fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d37fa-102">SYNOPSIS</span></span>
<span data-ttu-id="d37fa-103">Yakınlık Yerleşim grubu kaynağı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d37fa-103">Create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="d37fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d37fa-104">SYNTAX</span></span>

```
New-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-ProximityPlacementGroupType <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d37fa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d37fa-105">DESCRIPTION</span></span>
<span data-ttu-id="d37fa-106">Bu cmdlet, yakınlık Yerleşim grubu kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d37fa-106">This cmdlet will create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="d37fa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d37fa-107">EXAMPLES</span></span>

### <span data-ttu-id="d37fa-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d37fa-108">Example 1</span></span>
```
PS C:\> New-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = "val1"}

ResourceGroupName           : rg0
ProximityPlacementGroupType : Standard
Id                          : /subscriptions/5393f919-a68a-43d0-9063-4b2bda6bffdf/resourceGroups/rg0/providers/Microsoft.Compute/proximityPlacementGroups/ppg0
Name                        : ppg0
Type                        : Microsoft.Compute/proximityPlacementGroups
Location                    : westcentralus
Tags                        : {"key1":"val1"}
```

<span data-ttu-id="d37fa-109">Bu komut, verilen konumda bir yakınlık grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d37fa-109">This command creates a proximity place group in the given location.</span></span>

## <span data-ttu-id="d37fa-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d37fa-110">PARAMETERS</span></span>

### <span data-ttu-id="d37fa-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="d37fa-111">-AsJob</span></span>
<span data-ttu-id="d37fa-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d37fa-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d37fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37fa-113">-DefaultProfile</span></span>
<span data-ttu-id="d37fa-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d37fa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d37fa-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="d37fa-115">-Location</span></span>
<span data-ttu-id="d37fa-116">Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="d37fa-116">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37fa-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="d37fa-117">-Name</span></span>
<span data-ttu-id="d37fa-118">Yakınlık Yerleşim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d37fa-118">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProximityPlacementGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d37fa-119">-ProximityPlacementGroupType</span><span class="sxs-lookup"><span data-stu-id="d37fa-119">-ProximityPlacementGroupType</span></span>
<span data-ttu-id="d37fa-120">Yakınlık Yerleşim grubunun türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d37fa-120">Specifies the type of the proximity placement group.</span></span>  <span data-ttu-id="d37fa-121">Olası değerler: Standart veya ultra</span><span class="sxs-lookup"><span data-stu-id="d37fa-121">Possible values are: Standard or Ultra</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37fa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d37fa-122">-ResourceGroupName</span></span>
<span data-ttu-id="d37fa-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d37fa-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="d37fa-124">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d37fa-124">-Tag</span></span>
<span data-ttu-id="d37fa-125">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="d37fa-125">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37fa-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="d37fa-126">-Confirm</span></span>
<span data-ttu-id="d37fa-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d37fa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d37fa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d37fa-128">-WhatIf</span></span>
<span data-ttu-id="d37fa-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d37fa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d37fa-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d37fa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d37fa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37fa-131">CommonParameters</span></span>
<span data-ttu-id="d37fa-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d37fa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37fa-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d37fa-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37fa-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d37fa-134">INPUTS</span></span>

### <span data-ttu-id="d37fa-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d37fa-135">System.String</span></span>

## <span data-ttu-id="d37fa-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d37fa-136">OUTPUTS</span></span>

### <span data-ttu-id="d37fa-137">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d37fa-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="d37fa-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d37fa-138">NOTES</span></span>

## <span data-ttu-id="d37fa-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d37fa-139">RELATED LINKS</span></span>
