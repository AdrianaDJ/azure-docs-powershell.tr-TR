---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 93b7c79544f79a528fc09203fdae77f8ee76474a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935462"
---
# <span data-ttu-id="019fa-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="019fa-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="019fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="019fa-102">SYNOPSIS</span></span>
<span data-ttu-id="019fa-103">Sanal ağdaki bir alt ağı alır.</span><span class="sxs-lookup"><span data-stu-id="019fa-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="019fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="019fa-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="019fa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="019fa-105">DESCRIPTION</span></span>
<span data-ttu-id="019fa-106">**Get-AzVirtualNetworkSubnetConfig** cmdlet 'i, bir Azure sanal ağında bir veya daha fazla alt ağ yapılandırması alır.</span><span class="sxs-lookup"><span data-stu-id="019fa-106">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="019fa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="019fa-107">EXAMPLES</span></span>

### <span data-ttu-id="019fa-108">1: Sanal ağda alt ağ edinme</span><span class="sxs-lookup"><span data-stu-id="019fa-108">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="019fa-109">Bu örnek, kaynak grubunda tek alt ağı olan bir kaynak grubu ve sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="019fa-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="019fa-110">Bu alt ağla ilgili verileri alır.</span><span class="sxs-lookup"><span data-stu-id="019fa-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="019fa-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="019fa-111">PARAMETERS</span></span>

### <span data-ttu-id="019fa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="019fa-112">-DefaultProfile</span></span>
<span data-ttu-id="019fa-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="019fa-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="019fa-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="019fa-114">-Name</span></span>
<span data-ttu-id="019fa-115">Bu cmdlet 'in aldığı alt ağ yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="019fa-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="019fa-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="019fa-116">-VirtualNetwork</span></span>
<span data-ttu-id="019fa-117">Bu cmdlet 'in aldığı alt ağ yapılandırmasını içeren **VirtualNetwork** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="019fa-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="019fa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="019fa-118">CommonParameters</span></span>
<span data-ttu-id="019fa-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="019fa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="019fa-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="019fa-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="019fa-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="019fa-121">INPUTS</span></span>

### <span data-ttu-id="019fa-122">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="019fa-122">PSVirtualNetwork</span></span>
<span data-ttu-id="019fa-123">' VirtualNetwork ' parametresi ardışık düzen için ' PSVirtualNetwork ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="019fa-123">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="019fa-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="019fa-124">OUTPUTS</span></span>

### <span data-ttu-id="019fa-125">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="019fa-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="019fa-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="019fa-126">NOTES</span></span>

## <span data-ttu-id="019fa-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="019fa-127">RELATED LINKS</span></span>

[<span data-ttu-id="019fa-128">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="019fa-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="019fa-129">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="019fa-129">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="019fa-130">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="019fa-130">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="019fa-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="019fa-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


