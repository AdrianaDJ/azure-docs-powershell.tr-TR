---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 822b982b2c1714e2c0331cc9b64fe2c1753044f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277579"
---
# <span data-ttu-id="5cbc3-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5cbc3-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="5cbc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cbc3-102">SYNOPSIS</span></span>
<span data-ttu-id="5cbc3-103">Sanal ağı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5cbc3-103">Updates a virtual network.</span></span>

## <span data-ttu-id="5cbc3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5cbc3-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5cbc3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5cbc3-105">DESCRIPTION</span></span>
<span data-ttu-id="5cbc3-106">**Set-AzVirtualNetwork** cmdlet 'i sanal ağı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5cbc3-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="5cbc3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5cbc3-107">EXAMPLES</span></span>

### <span data-ttu-id="5cbc3-108">1: sanal ağ oluşturur ve alt ağlarından birini kaldırır</span><span class="sxs-lookup"><span data-stu-id="5cbc3-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="5cbc3-109">Bu örnek iki alt ağı olan TestResourceGroup adlı sanal bir ağ oluşturur: Frontenvseçsubnet ve backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="5cbc3-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="5cbc3-110">Ardından, sanal ağın bellekteki gösteriminden backendSubnet alt ağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5cbc3-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="5cbc3-111">Ardından, hizmet tarafında değiştirilmiş sanal ağ durumunu yazmak için Set-AzVirtualNetwork cmdlet 'i kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5cbc3-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="5cbc3-112">Set-AzVirtualNetwork cmdlet 'i yürütüldüğünde backendSubnet öğesi kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="5cbc3-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="5cbc3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5cbc3-113">PARAMETERS</span></span>

### <span data-ttu-id="5cbc3-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="5cbc3-114">-AsJob</span></span>
<span data-ttu-id="5cbc3-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5cbc3-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbc3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cbc3-116">-DefaultProfile</span></span>
<span data-ttu-id="5cbc3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5cbc3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cbc3-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5cbc3-118">-VirtualNetwork</span></span>
<span data-ttu-id="5cbc3-119">Sanal ağın ayarlanması gereken durumu temsil eden sanal ağ nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cbc3-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

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

### <span data-ttu-id="5cbc3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cbc3-120">CommonParameters</span></span>
<span data-ttu-id="5cbc3-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5cbc3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cbc3-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cbc3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cbc3-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5cbc3-123">INPUTS</span></span>

### <span data-ttu-id="5cbc3-124">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5cbc3-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="5cbc3-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5cbc3-125">OUTPUTS</span></span>

### <span data-ttu-id="5cbc3-126">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5cbc3-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="5cbc3-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5cbc3-127">NOTES</span></span>

## <span data-ttu-id="5cbc3-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5cbc3-128">RELATED LINKS</span></span>

[<span data-ttu-id="5cbc3-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5cbc3-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="5cbc3-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5cbc3-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="5cbc3-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5cbc3-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="5cbc3-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5cbc3-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


