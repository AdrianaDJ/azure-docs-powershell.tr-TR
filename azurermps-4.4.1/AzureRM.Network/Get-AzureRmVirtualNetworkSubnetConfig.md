---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 494c496a9f01b41fde2df07f804f9f0c851c5f61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594619"
---
# <span data-ttu-id="608aa-101">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="608aa-101">Get-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="608aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="608aa-102">SYNOPSIS</span></span>
<span data-ttu-id="608aa-103">Sanal ağdaki bir alt ağı alır.</span><span class="sxs-lookup"><span data-stu-id="608aa-103">Gets a subnet in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="608aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="608aa-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="608aa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="608aa-105">DESCRIPTION</span></span>
<span data-ttu-id="608aa-106">**Get-AzureRmVirtualNetworkSubnetConfig** cmdlet 'i, bir Azure sanal ağında bir veya daha fazla alt ağ yapılandırması alır.</span><span class="sxs-lookup"><span data-stu-id="608aa-106">The **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="608aa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="608aa-107">EXAMPLES</span></span>

### <span data-ttu-id="608aa-108">1: Sanal ağda alt ağ edinme</span><span class="sxs-lookup"><span data-stu-id="608aa-108">1: Get a subnet in a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="608aa-109">Bu örnek, kaynak grubunda tek alt ağı olan bir kaynak grubu ve sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="608aa-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="608aa-110">Bu alt ağla ilgili verileri alır.</span><span class="sxs-lookup"><span data-stu-id="608aa-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="608aa-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="608aa-111">PARAMETERS</span></span>

### <span data-ttu-id="608aa-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="608aa-112">-Name</span></span>
<span data-ttu-id="608aa-113">Bu cmdlet 'in aldığı alt ağ yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="608aa-113">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="608aa-114">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="608aa-114">-VirtualNetwork</span></span>
<span data-ttu-id="608aa-115">Bu cmdlet 'in aldığı alt ağ yapılandırmasını içeren **VirtualNetwork** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="608aa-115">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="608aa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="608aa-116">-DefaultProfile</span></span>
<span data-ttu-id="608aa-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="608aa-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="608aa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="608aa-118">CommonParameters</span></span>
<span data-ttu-id="608aa-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="608aa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="608aa-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="608aa-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="608aa-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="608aa-121">INPUTS</span></span>

### <span data-ttu-id="608aa-122">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="608aa-122">PSVirtualNetwork</span></span>
<span data-ttu-id="608aa-123">' VirtualNetwork ' parametresi ardışık düzen için ' PSVirtualNetwork ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="608aa-123">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="608aa-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="608aa-124">OUTPUTS</span></span>

### <span data-ttu-id="608aa-125">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="608aa-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="608aa-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="608aa-126">NOTES</span></span>

## <span data-ttu-id="608aa-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="608aa-127">RELATED LINKS</span></span>

[<span data-ttu-id="608aa-128">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="608aa-128">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="608aa-129">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="608aa-129">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="608aa-130">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="608aa-130">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="608aa-131">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="608aa-131">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


