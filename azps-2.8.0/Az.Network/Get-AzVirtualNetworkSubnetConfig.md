---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 350b084ee9a7de03e447520dae0cc584bcfacde9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918416"
---
# <span data-ttu-id="b4b0f-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b4b0f-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="b4b0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4b0f-102">SYNOPSIS</span></span>
<span data-ttu-id="b4b0f-103">Sanal ağdaki bir alt ağı alır.</span><span class="sxs-lookup"><span data-stu-id="b4b0f-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="b4b0f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4b0f-104">SYNTAX</span></span>

### <span data-ttu-id="b4b0f-105">GetByVirtualNetwork (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4b0f-105">GetByVirtualNetwork (Default)</span></span>
```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4b0f-106">Getbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="b4b0f-106">GetByResourceId</span></span>
```
Get-AzVirtualNetworkSubnetConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4b0f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4b0f-107">DESCRIPTION</span></span>
<span data-ttu-id="b4b0f-108">**Get-AzVirtualNetworkSubnetConfig** cmdlet 'i, bir Azure sanal ağında bir veya daha fazla alt ağ yapılandırması alır.</span><span class="sxs-lookup"><span data-stu-id="b4b0f-108">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="b4b0f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4b0f-109">EXAMPLES</span></span>

### <span data-ttu-id="b4b0f-110">1: Sanal ağda alt ağ edinme</span><span class="sxs-lookup"><span data-stu-id="b4b0f-110">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="b4b0f-111">Bu örnek, kaynak grubunda tek alt ağı olan bir kaynak grubu ve sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4b0f-111">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="b4b0f-112">Bu alt ağla ilgili verileri alır.</span><span class="sxs-lookup"><span data-stu-id="b4b0f-112">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="b4b0f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4b0f-113">PARAMETERS</span></span>

### <span data-ttu-id="b4b0f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4b0f-114">-DefaultProfile</span></span>
<span data-ttu-id="b4b0f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4b0f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4b0f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="b4b0f-116">-Name</span></span>
<span data-ttu-id="b4b0f-117">Bu cmdlet 'in aldığı alt ağ yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4b0f-117">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4b0f-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b4b0f-118">-ResourceId</span></span>
<span data-ttu-id="b4b0f-119">Bu cmdlet 'in aldığı alt ağın kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4b0f-119">Specifies the resource id of the subnet that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4b0f-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b4b0f-120">-VirtualNetwork</span></span>
<span data-ttu-id="b4b0f-121">Bu cmdlet 'in aldığı alt ağ yapılandırmasını içeren **VirtualNetwork** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4b0f-121">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4b0f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4b0f-122">CommonParameters</span></span>
<span data-ttu-id="b4b0f-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4b0f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4b0f-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4b0f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4b0f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4b0f-125">INPUTS</span></span>

### <span data-ttu-id="b4b0f-126">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b4b0f-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="b4b0f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b4b0f-127">System.String</span></span>

## <span data-ttu-id="b4b0f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4b0f-128">OUTPUTS</span></span>

### <span data-ttu-id="b4b0f-129">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="b4b0f-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="b4b0f-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4b0f-130">NOTES</span></span>

## <span data-ttu-id="b4b0f-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4b0f-131">RELATED LINKS</span></span>

[<span data-ttu-id="b4b0f-132">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b4b0f-132">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b4b0f-133">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b4b0f-133">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b4b0f-134">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b4b0f-134">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b4b0f-135">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b4b0f-135">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
