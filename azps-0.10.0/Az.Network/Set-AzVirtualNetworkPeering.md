---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
ms.openlocfilehash: 9ad6d0ef43913bc7b182a37a9bca4b9cccae1918
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936494"
---
# <span data-ttu-id="4a128-101">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="4a128-101">Set-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="4a128-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a128-102">SYNOPSIS</span></span>
<span data-ttu-id="4a128-103">Sanal ağ eşliğini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="4a128-103">Configures a virtual network peering.</span></span>

## <span data-ttu-id="4a128-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a128-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a128-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a128-105">DESCRIPTION</span></span>
<span data-ttu-id="4a128-106">**Set-Azvirtualnetworkeşlemecmdlet** 'i sanal ağ eşliğini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="4a128-106">The **Set-AzVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="4a128-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a128-107">EXAMPLES</span></span>

### <span data-ttu-id="4a128-108">Örnek 1: sanal ağ eşliğini iletilen trafik yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="4a128-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="4a128-109">Örnek 2: sanal ağ eşliğini sanal ağ erişimi 'ni değiştirme</span><span class="sxs-lookup"><span data-stu-id="4a128-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="4a128-110">Örnek 3: sanal ağ eşliğini ağ geçidi Aktarım özelliği yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="4a128-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="4a128-111">Örnek 4: sanal ağ eşliğini kullanarak uzak ağ geçitleri kullanın</span><span class="sxs-lookup"><span data-stu-id="4a128-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $LinkToVNet2
```

<span data-ttu-id="4a128-112">Bu özelliği $True olarak değiştirerek, eşin VNet ağ geçidi kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4a128-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="4a128-113">Bununla birlikte, eşin VNet için ağ geçidi yapılandırılmış olmalıdır ve **Allowgatewayın** değeri $true olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4a128-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>

<span data-ttu-id="4a128-114">Ağ Geçidi zaten yapılandırılmışsa bu özellik kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="4a128-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="4a128-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a128-115">PARAMETERS</span></span>

### <span data-ttu-id="4a128-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="4a128-116">-AsJob</span></span>
<span data-ttu-id="4a128-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4a128-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a128-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a128-118">-DefaultProfile</span></span>
<span data-ttu-id="4a128-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4a128-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a128-120">-Virtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="4a128-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="4a128-121">Sanal ağ eşliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a128-121">Specifies the virtual network peering.</span></span>

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

### <span data-ttu-id="4a128-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a128-122">CommonParameters</span></span>
<span data-ttu-id="4a128-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a128-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a128-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a128-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a128-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a128-125">INPUTS</span></span>

### <span data-ttu-id="4a128-126">Psvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="4a128-126">PSVirtualNetworkPeering</span></span>
<span data-ttu-id="4a128-127">' Virtualnetworkeşleme ' parametresi ardışık düzenin ' Psvirtualnetworkeşleme ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4a128-127">Parameter 'VirtualNetworkPeering' accepts value of type 'PSVirtualNetworkPeering' from the pipeline</span></span>

## <span data-ttu-id="4a128-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a128-128">OUTPUTS</span></span>

### <span data-ttu-id="4a128-129">Microsoft. Azure. Commands. Network. model. psvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="4a128-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="4a128-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a128-130">NOTES</span></span>

## <span data-ttu-id="4a128-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a128-131">RELATED LINKS</span></span>

[<span data-ttu-id="4a128-132">Add-azvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="4a128-132">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="4a128-133">Get-azvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="4a128-133">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="4a128-134">Remove-azvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="4a128-134">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

