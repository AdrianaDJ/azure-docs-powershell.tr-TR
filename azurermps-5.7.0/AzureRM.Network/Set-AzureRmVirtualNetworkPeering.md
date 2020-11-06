---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: a8af220313d0e6bbd03d35aa60d235651b19704c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588860"
---
# <span data-ttu-id="3c551-101">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="3c551-101">Set-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="3c551-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c551-102">SYNOPSIS</span></span>
<span data-ttu-id="3c551-103">Sanal ağ eşliğini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="3c551-103">Configures a virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c551-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c551-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c551-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c551-105">DESCRIPTION</span></span>
<span data-ttu-id="3c551-106">**Set-Azurermvirtualnetworkeşlemecmdlet** 'i sanal ağ eşliğini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="3c551-106">The **Set-AzureRmVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="3c551-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c551-107">EXAMPLES</span></span>

### <span data-ttu-id="3c551-108">Örnek 1: sanal ağ eşliğini iletilen trafik yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="3c551-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="3c551-109">Örnek 2: sanal ağ eşliğini sanal ağ erişimi 'ni değiştirme</span><span class="sxs-lookup"><span data-stu-id="3c551-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="3c551-110">Örnek 3: sanal ağ eşliğini ağ geçidi Aktarım özelliği yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="3c551-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="3c551-111">Örnek 4: sanal ağ eşliğini kullanarak uzak ağ geçitleri kullanın</span><span class="sxs-lookup"><span data-stu-id="3c551-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $LinkToVNet2
```

<span data-ttu-id="3c551-112">Bu özelliği $True olarak değiştirerek, eşin VNet ağ geçidi kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="3c551-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="3c551-113">Bununla birlikte, eşin VNet için ağ geçidi yapılandırılmış olmalıdır ve **Allowgatewayın** değeri $true olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3c551-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>

<span data-ttu-id="3c551-114">Ağ Geçidi zaten yapılandırılmışsa bu özellik kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="3c551-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="3c551-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c551-115">PARAMETERS</span></span>

### <span data-ttu-id="3c551-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="3c551-116">-AsJob</span></span>
<span data-ttu-id="3c551-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3c551-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c551-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c551-118">-DefaultProfile</span></span>
<span data-ttu-id="3c551-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3c551-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c551-120">-Virtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="3c551-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="3c551-121">Sanal ağ eşliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c551-121">Specifies the virtual network peering.</span></span>

```yaml
Type: PSVirtualNetworkPeering
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c551-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c551-122">CommonParameters</span></span>
<span data-ttu-id="3c551-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c551-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c551-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c551-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c551-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c551-125">INPUTS</span></span>

### <span data-ttu-id="3c551-126">Psvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="3c551-126">PSVirtualNetworkPeering</span></span>
<span data-ttu-id="3c551-127">' Virtualnetworkeşleme ' parametresi ardışık düzenin ' Psvirtualnetworkeşleme ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3c551-127">Parameter 'VirtualNetworkPeering' accepts value of type 'PSVirtualNetworkPeering' from the pipeline</span></span>

## <span data-ttu-id="3c551-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c551-128">OUTPUTS</span></span>

### <span data-ttu-id="3c551-129">Microsoft. Azure. Commands. Network. model. psvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="3c551-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="3c551-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c551-130">NOTES</span></span>

## <span data-ttu-id="3c551-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c551-131">RELATED LINKS</span></span>

[<span data-ttu-id="3c551-132">Add-azurermvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="3c551-132">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="3c551-133">Get-azurermvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="3c551-133">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="3c551-134">Remove-azurermvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="3c551-134">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)


