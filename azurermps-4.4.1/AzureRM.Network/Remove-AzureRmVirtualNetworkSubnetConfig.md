---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: f2e0bb88df867da0a110422debea4d6688ad3af0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593061"
---
# <span data-ttu-id="c477f-101">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c477f-101">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="c477f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c477f-102">SYNOPSIS</span></span>
<span data-ttu-id="c477f-103">Sanal ağdan alt ağ yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c477f-103">Removes a subnet configuration from a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c477f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c477f-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c477f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c477f-105">DESCRIPTION</span></span>
<span data-ttu-id="c477f-106">**Remove-AzureRmVirtualNetworkSubnetConfig** cmdlet 'i, bir Azure sanal ağından alt ağı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c477f-106">The **Remove-AzureRmVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="c477f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c477f-107">EXAMPLES</span></span>

### <span data-ttu-id="c477f-108">1: sanal ağdan bir alt ağı kaldırın ve sanal ağı güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="c477f-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
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

<span data-ttu-id="c477f-109">Bu örnek, iki alt ağı olan bir kaynak grubu ve sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c477f-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="c477f-110">Ardından, arka uç alt ağını sanal ağın bellekteki gösteriminden kaldırmak için Remove-AzureRmVirtualNetworkSubnetConfig komutunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="c477f-110">It then uses the Remove-AzureRmVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="c477f-111">Sunucu tarafındaki sanal ağı değiştirmek için Set-AzureRmVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="c477f-111">Set-AzureRmVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="c477f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c477f-112">PARAMETERS</span></span>

### <span data-ttu-id="c477f-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="c477f-113">-Name</span></span>
<span data-ttu-id="c477f-114">Kaldırılacak alt ağ yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c477f-114">Specifies the name of the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="c477f-115">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c477f-115">-VirtualNetwork</span></span>
<span data-ttu-id="c477f-116">Kaldırılacak alt ağ yapılandırmasını içeren **VirtualNetwork** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c477f-116">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="c477f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c477f-117">-DefaultProfile</span></span>
<span data-ttu-id="c477f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c477f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c477f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c477f-119">CommonParameters</span></span>
<span data-ttu-id="c477f-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c477f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c477f-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c477f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c477f-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c477f-122">INPUTS</span></span>

### <span data-ttu-id="c477f-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c477f-123">PSVirtualNetwork</span></span>
<span data-ttu-id="c477f-124">' VirtualNetwork ' parametresi ardışık düzen için ' PSVirtualNetwork ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c477f-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="c477f-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c477f-125">OUTPUTS</span></span>

### <span data-ttu-id="c477f-126">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c477f-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="c477f-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c477f-127">NOTES</span></span>

## <span data-ttu-id="c477f-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c477f-128">RELATED LINKS</span></span>

[<span data-ttu-id="c477f-129">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c477f-129">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c477f-130">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c477f-130">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c477f-131">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c477f-131">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c477f-132">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c477f-132">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


