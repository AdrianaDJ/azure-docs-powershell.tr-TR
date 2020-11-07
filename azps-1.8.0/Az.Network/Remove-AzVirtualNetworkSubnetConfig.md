---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 92550eb08fb6abf704d450f323e3fd0b724d9942
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760096"
---
# <span data-ttu-id="6695b-101">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6695b-101">Remove-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="6695b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6695b-102">SYNOPSIS</span></span>
<span data-ttu-id="6695b-103">Sanal ağdan alt ağ yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6695b-103">Removes a subnet configuration from a virtual network.</span></span>

## <span data-ttu-id="6695b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6695b-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6695b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6695b-105">DESCRIPTION</span></span>
<span data-ttu-id="6695b-106">**Remove-AzVirtualNetworkSubnetConfig** cmdlet 'i, bir Azure sanal ağından alt ağı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6695b-106">The **Remove-AzVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="6695b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6695b-107">EXAMPLES</span></span>

### <span data-ttu-id="6695b-108">1: sanal ağdan bir alt ağı kaldırın ve sanal ağı güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="6695b-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="6695b-109">Bu örnek, iki alt ağı olan bir kaynak grubu ve sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6695b-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="6695b-110">Ardından, arka uç alt ağını sanal ağın bellekteki gösteriminden kaldırmak için Remove-AzVirtualNetworkSubnetConfig komutunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="6695b-110">It then uses the Remove-AzVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="6695b-111">Sunucu tarafındaki sanal ağı değiştirmek için Set-AzVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="6695b-111">Set-AzVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="6695b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6695b-112">PARAMETERS</span></span>

### <span data-ttu-id="6695b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6695b-113">-DefaultProfile</span></span>
<span data-ttu-id="6695b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6695b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6695b-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="6695b-115">-Name</span></span>
<span data-ttu-id="6695b-116">Kaldırılacak alt ağ yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6695b-116">Specifies the name of the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="6695b-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6695b-117">-VirtualNetwork</span></span>
<span data-ttu-id="6695b-118">Kaldırılacak alt ağ yapılandırmasını içeren **VirtualNetwork** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6695b-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6695b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6695b-119">CommonParameters</span></span>
<span data-ttu-id="6695b-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6695b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6695b-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6695b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6695b-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6695b-122">INPUTS</span></span>

### <span data-ttu-id="6695b-123">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6695b-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="6695b-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6695b-124">OUTPUTS</span></span>

### <span data-ttu-id="6695b-125">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6695b-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="6695b-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6695b-126">NOTES</span></span>

## <span data-ttu-id="6695b-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6695b-127">RELATED LINKS</span></span>

[<span data-ttu-id="6695b-128">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6695b-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="6695b-129">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6695b-129">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="6695b-130">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6695b-130">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="6695b-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6695b-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)

