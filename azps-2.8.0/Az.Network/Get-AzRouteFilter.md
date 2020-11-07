---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 26fb3e9a7b4b097e79fdb328d79a82fc423ac675
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931978"
---
# <span data-ttu-id="e2306-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e2306-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="e2306-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2306-102">SYNOPSIS</span></span>
<span data-ttu-id="e2306-103">Bir yol filtresi alır.</span><span class="sxs-lookup"><span data-stu-id="e2306-103">Gets a route filter.</span></span>

## <span data-ttu-id="e2306-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2306-104">SYNTAX</span></span>

### <span data-ttu-id="e2306-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="e2306-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2306-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="e2306-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2306-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2306-107">DESCRIPTION</span></span>
<span data-ttu-id="e2306-108">**Get-AzRouteFilter** cmdlet 'i bir yol filtresi alır.</span><span class="sxs-lookup"><span data-stu-id="e2306-108">The **Get-AzRouteFilter** cmdlet gets a route filter.</span></span>

## <span data-ttu-id="e2306-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2306-109">EXAMPLES</span></span>

### <span data-ttu-id="e2306-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e2306-110">Example 1</span></span>
```powershell
PS C:\> Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"

Name              : RouteFilter01
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter01
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []
```

<span data-ttu-id="e2306-111">Bu komut, ResourceGroup01 adındaki kaynak grubuna ait olan RouteFilter01 adındaki yol filtresini alır.</span><span class="sxs-lookup"><span data-stu-id="e2306-111">This command gets the route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="e2306-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e2306-112">Example 2</span></span>
```powershell
PS C:\> Get-AzRouteFilter -Name "RouteFilter*"

Name              : RouteFilter01
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter01
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []

Name              : RouteFilter02
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter02
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []
```

<span data-ttu-id="e2306-113">Bu komut, "RouteFilter" ile başlayan tüm yol filtrelerini alır.</span><span class="sxs-lookup"><span data-stu-id="e2306-113">This command gets all route filters that start with "RouteFilter".</span></span>

## <span data-ttu-id="e2306-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2306-114">PARAMETERS</span></span>

### <span data-ttu-id="e2306-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2306-115">-DefaultProfile</span></span>
<span data-ttu-id="e2306-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e2306-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2306-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="e2306-117">-ExpandResource</span></span>
<span data-ttu-id="e2306-118">Genişletilecek kaynak başvurusu.</span><span class="sxs-lookup"><span data-stu-id="e2306-118">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2306-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="e2306-119">-Name</span></span>
<span data-ttu-id="e2306-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="e2306-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e2306-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2306-121">-ResourceGroupName</span></span>
<span data-ttu-id="e2306-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e2306-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e2306-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2306-123">CommonParameters</span></span>
<span data-ttu-id="e2306-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2306-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2306-125">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e2306-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2306-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2306-126">INPUTS</span></span>

### <span data-ttu-id="e2306-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e2306-127">System.String</span></span>

## <span data-ttu-id="e2306-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2306-128">OUTPUTS</span></span>

### <span data-ttu-id="e2306-129">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e2306-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="e2306-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2306-130">NOTES</span></span>

## <span data-ttu-id="e2306-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2306-131">RELATED LINKS</span></span>

[<span data-ttu-id="e2306-132">Yeni-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e2306-132">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="e2306-133">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e2306-133">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="e2306-134">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e2306-134">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="e2306-135">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2306-135">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="e2306-136">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2306-136">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="e2306-137">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2306-137">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="e2306-138">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2306-138">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="e2306-139">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2306-139">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
