---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
ms.openlocfilehash: fa91ce991a109c91b27560b0b969d1af0f4342d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760445"
---
# <span data-ttu-id="aa526-101">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="aa526-101">Get-AzVpnGateway</span></span>

## <span data-ttu-id="aa526-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa526-102">SYNOPSIS</span></span>
<span data-ttu-id="aa526-103">ResourceGroupName ve GatewayName kullanarak VpnGateway kaynağını alır veya tüm ağ geçitlerini ResourceGroupName veya SubscriptionID tarafından listeler.</span><span class="sxs-lookup"><span data-stu-id="aa526-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="aa526-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aa526-104">SYNTAX</span></span>

### <span data-ttu-id="aa526-105">Listbysubscriptionıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aa526-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa526-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa526-106">ListByResourceGroupName</span></span>
```
Get-AzVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa526-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="aa526-107">DESCRIPTION</span></span>
<span data-ttu-id="aa526-108">ResourceGroupName ve GatewayName kullanarak VpnGateway kaynağını alır veya tüm ağ geçitlerini ResourceGroupName veya SubscriptionID tarafından listeler.</span><span class="sxs-lookup"><span data-stu-id="aa526-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="aa526-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aa526-109">EXAMPLES</span></span>

### <span data-ttu-id="aa526-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="aa526-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="aa526-111">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda bir kaynak grubu, sanal WAN, sanal ağ, Batı ABD 'deki sanal hub 'ı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aa526-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="aa526-112">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="aa526-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="aa526-113">Ardından, resourceGroupName ve ağ geçidi adını kullanarak VpnGateway 'i alır.</span><span class="sxs-lookup"><span data-stu-id="aa526-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="aa526-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="aa526-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnGateway -Name test*

ResourceGroupName   : testRG
Name                : test1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test1
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : test2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test2
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="aa526-115">Bu cmdlet, "test" ile başlayan tüm ağ geçitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="aa526-115">This cmdlet gets all Gateways that start with "test".</span></span>

## <span data-ttu-id="aa526-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aa526-116">PARAMETERS</span></span>

### <span data-ttu-id="aa526-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa526-117">-DefaultProfile</span></span>
<span data-ttu-id="aa526-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aa526-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa526-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="aa526-119">-Name</span></span>
<span data-ttu-id="aa526-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="aa526-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="aa526-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa526-121">-ResourceGroupName</span></span>
<span data-ttu-id="aa526-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="aa526-122">The resource group name.</span></span>

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

### <span data-ttu-id="aa526-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa526-123">CommonParameters</span></span>
<span data-ttu-id="aa526-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aa526-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa526-125">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="aa526-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa526-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aa526-126">INPUTS</span></span>

### <span data-ttu-id="aa526-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="aa526-127">None</span></span>

## <span data-ttu-id="aa526-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aa526-128">OUTPUTS</span></span>

### <span data-ttu-id="aa526-129">Microsoft. Azure. Commands. Network. model. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="aa526-129">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="aa526-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aa526-130">NOTES</span></span>

## <span data-ttu-id="aa526-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aa526-131">RELATED LINKS</span></span>

[<span data-ttu-id="aa526-132">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="aa526-132">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="aa526-133">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="aa526-133">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="aa526-134">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="aa526-134">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)