---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworksubnetconfig
schema: 2.0.0
ms.openlocfilehash: 4020f6aa32a7dda31f97831badf9f7916f3db10f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940028"
---
# <span data-ttu-id="4bd23-101">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4bd23-101">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="4bd23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bd23-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd23-103">Sanal ağdan alt ağ yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4bd23-103">Removes a subnet configuration from a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bd23-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4bd23-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bd23-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bd23-105">DESCRIPTION</span></span>
<span data-ttu-id="4bd23-106">**Remove-AzureRmVirtualNetworkSubnetConfig** cmdlet 'i, bir Azure sanal ağından alt ağı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4bd23-106">The **Remove-AzureRmVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="4bd23-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4bd23-107">EXAMPLES</span></span>

### <span data-ttu-id="4bd23-108">1: sanal ağdan bir alt ağı kaldırın ve sanal ağı güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="4bd23-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="4bd23-109">Bu örnek, iki alt ağı olan bir kaynak grubu ve sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4bd23-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="4bd23-110">Ardından, arka uç alt ağını sanal ağın bellekteki gösteriminden kaldırmak için Remove-AzureRmVirtualNetworkSubnetConfig komutunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="4bd23-110">It then uses the Remove-AzureRmVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="4bd23-111">Sunucu tarafındaki sanal ağı değiştirmek için Set-AzureRmVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="4bd23-111">Set-AzureRmVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="4bd23-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4bd23-112">PARAMETERS</span></span>

### <span data-ttu-id="4bd23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd23-113">-DefaultProfile</span></span>
<span data-ttu-id="4bd23-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4bd23-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd23-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="4bd23-115">-Name</span></span>
<span data-ttu-id="4bd23-116">Kaldırılacak alt ağ yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bd23-116">Specifies the name of the subnet configuration to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd23-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4bd23-117">-VirtualNetwork</span></span>
<span data-ttu-id="4bd23-118">Kaldırılacak alt ağ yapılandırmasını içeren **VirtualNetwork** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bd23-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd23-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd23-119">CommonParameters</span></span>
<span data-ttu-id="4bd23-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4bd23-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd23-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bd23-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd23-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4bd23-122">INPUTS</span></span>

### <span data-ttu-id="4bd23-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4bd23-123">PSVirtualNetwork</span></span>
<span data-ttu-id="4bd23-124">' VirtualNetwork ' parametresi ardışık düzen için ' PSVirtualNetwork ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4bd23-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="4bd23-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4bd23-125">OUTPUTS</span></span>

### <span data-ttu-id="4bd23-126">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4bd23-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="4bd23-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4bd23-127">NOTES</span></span>

## <span data-ttu-id="4bd23-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4bd23-128">RELATED LINKS</span></span>

[<span data-ttu-id="4bd23-129">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4bd23-129">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4bd23-130">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4bd23-130">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4bd23-131">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4bd23-131">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4bd23-132">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4bd23-132">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


