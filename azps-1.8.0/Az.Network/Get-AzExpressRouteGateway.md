---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: d5314453be4d2f9042fd5034cc864d94caf1dbd1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760578"
---
# <span data-ttu-id="76d47-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="76d47-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="76d47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76d47-102">SYNOPSIS</span></span>
<span data-ttu-id="76d47-103">ResourceGroupName ve GatewayName kullanarak bir ExpressRouteGateway kaynağı alır veya tüm ağ geçitlerini ResourceGroupName veya SubscriptionID tarafından listeler.</span><span class="sxs-lookup"><span data-stu-id="76d47-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="76d47-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76d47-104">SYNTAX</span></span>

### <span data-ttu-id="76d47-105">Listbysubscriptionıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="76d47-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76d47-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76d47-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76d47-107">Byexpressroutegatewayresourceıd</span><span class="sxs-lookup"><span data-stu-id="76d47-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76d47-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="76d47-108">DESCRIPTION</span></span>
<span data-ttu-id="76d47-109">ResourceGroupName ve GatewayName kullanarak bir ExpressRouteGateway kaynağı alır veya tüm ağ geçitlerini ResourceGroupName veya SubscriptionID tarafından listeler.</span><span class="sxs-lookup"><span data-stu-id="76d47-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="76d47-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76d47-110">EXAMPLES</span></span>

### <span data-ttu-id="76d47-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="76d47-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"

ResourceGroupName   : testRG
Name                : testExpressRoutegw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="76d47-112">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda, Batı merkezi 'nde ABD Merkezi</span><span class="sxs-lookup"><span data-stu-id="76d47-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="76d47-113">Daha sonra 2 ölçekli birim içeren sanal hub 'da bir ExpressRoute ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="76d47-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="76d47-114">Ardından, The resourceGroupName ve ağ geçidi adını kullanarak ExpressRouteGateway 'i alır.</span><span class="sxs-lookup"><span data-stu-id="76d47-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="76d47-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="76d47-115">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteGateway -Name test*

ResourceGroupName   : testRG
Name                : testExpressRoutegw1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw1
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : testExpressRoutegw2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw2
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="76d47-116">Bu komut, "test" ile başlayan tüm Expressroutegeçitleri alır</span><span class="sxs-lookup"><span data-stu-id="76d47-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="76d47-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76d47-117">PARAMETERS</span></span>

### <span data-ttu-id="76d47-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76d47-118">-DefaultProfile</span></span>
<span data-ttu-id="76d47-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="76d47-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76d47-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="76d47-120">-Name</span></span>
<span data-ttu-id="76d47-121">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="76d47-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, ExpressRouteGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="76d47-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76d47-122">-ResourceGroupName</span></span>
<span data-ttu-id="76d47-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="76d47-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="76d47-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="76d47-124">-ResourceId</span></span>
<span data-ttu-id="76d47-125">ExpressRouteGateway 'in silineceği Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="76d47-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: expressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76d47-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76d47-126">CommonParameters</span></span>
<span data-ttu-id="76d47-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76d47-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76d47-128">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="76d47-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76d47-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76d47-129">INPUTS</span></span>

### <span data-ttu-id="76d47-130">System. String</span><span class="sxs-lookup"><span data-stu-id="76d47-130">System.String</span></span>

## <span data-ttu-id="76d47-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76d47-131">OUTPUTS</span></span>

### <span data-ttu-id="76d47-132">Microsoft. Azure. Commands. Network. model. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="76d47-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="76d47-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76d47-133">NOTES</span></span>

## <span data-ttu-id="76d47-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76d47-134">RELATED LINKS</span></span>
