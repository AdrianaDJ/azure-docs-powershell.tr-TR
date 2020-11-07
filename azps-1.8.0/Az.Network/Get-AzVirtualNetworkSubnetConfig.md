---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: e5b881547f84714e238f541948602569c773c9c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760466"
---
# <span data-ttu-id="a08bf-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a08bf-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="a08bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a08bf-102">SYNOPSIS</span></span>
<span data-ttu-id="a08bf-103">Sanal ağdaki bir alt ağı alır.</span><span class="sxs-lookup"><span data-stu-id="a08bf-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="a08bf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a08bf-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a08bf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a08bf-105">DESCRIPTION</span></span>
<span data-ttu-id="a08bf-106">**Get-AzVirtualNetworkSubnetConfig** cmdlet 'i, bir Azure sanal ağında bir veya daha fazla alt ağ yapılandırması alır.</span><span class="sxs-lookup"><span data-stu-id="a08bf-106">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="a08bf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a08bf-107">EXAMPLES</span></span>

### <span data-ttu-id="a08bf-108">1: Sanal ağda alt ağ edinme</span><span class="sxs-lookup"><span data-stu-id="a08bf-108">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="a08bf-109">Bu örnek, kaynak grubunda tek alt ağı olan bir kaynak grubu ve sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a08bf-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="a08bf-110">Bu alt ağla ilgili verileri alır.</span><span class="sxs-lookup"><span data-stu-id="a08bf-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="a08bf-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a08bf-111">PARAMETERS</span></span>

### <span data-ttu-id="a08bf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a08bf-112">-DefaultProfile</span></span>
<span data-ttu-id="a08bf-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a08bf-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a08bf-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="a08bf-114">-Name</span></span>
<span data-ttu-id="a08bf-115">Bu cmdlet 'in aldığı alt ağ yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a08bf-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a08bf-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a08bf-116">-VirtualNetwork</span></span>
<span data-ttu-id="a08bf-117">Bu cmdlet 'in aldığı alt ağ yapılandırmasını içeren **VirtualNetwork** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a08bf-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a08bf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a08bf-118">CommonParameters</span></span>
<span data-ttu-id="a08bf-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a08bf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a08bf-120">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a08bf-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a08bf-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a08bf-121">INPUTS</span></span>

### <span data-ttu-id="a08bf-122">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a08bf-122">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="a08bf-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a08bf-123">OUTPUTS</span></span>

### <span data-ttu-id="a08bf-124">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="a08bf-124">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="a08bf-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a08bf-125">NOTES</span></span>

## <span data-ttu-id="a08bf-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a08bf-126">RELATED LINKS</span></span>

[<span data-ttu-id="a08bf-127">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a08bf-127">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a08bf-128">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a08bf-128">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a08bf-129">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a08bf-129">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a08bf-130">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a08bf-130">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


