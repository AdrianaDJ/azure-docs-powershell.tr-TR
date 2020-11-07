---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 1a27b43a7767fab6fee7cc89098ef045dde8529c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762260"
---
# <span data-ttu-id="fea99-101">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fea99-101">Add-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="fea99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fea99-102">SYNOPSIS</span></span>
<span data-ttu-id="fea99-103">İki sanal ağ arasında bir eşleme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fea99-103">Creates a peering between two virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fea99-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fea99-104">SYNTAX</span></span>

```
Add-AzureRmVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -RemoteVirtualNetworkId <String> [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit]
 [-UseRemoteGateways] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fea99-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fea99-105">DESCRIPTION</span></span>
<span data-ttu-id="fea99-106">**Add-Azurermvirtualnetworkeşlemecmdlet** 'i iki sanal ağ arasında bir eşleme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fea99-106">The **Add-AzureRmVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="fea99-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fea99-107">EXAMPLES</span></span>

### <span data-ttu-id="fea99-108">Örnek 1: aynı bölgedeki iki sanal ağ arasında eşleme oluşturma</span><span class="sxs-lookup"><span data-stu-id="fea99-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'
$location='eastus'

# Create a resource group.
New-AzureRmResourceGroup -Name $rgName  -Location $location

# Create virtual network 1.
$vnet1 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location $location

# Create virtual network 2.
$vnet2 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location $location

# Peer VNet1 to VNet2.
Add-AzureRmVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzureRmVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="fea99-109">Eşün çalışması için, vnet1 'den vnet2 'e bir eşleme bağlantısı oluşturulması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="fea99-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="fea99-110">Örnek 2: farklı bölgelerde iki sanal ağ arasında eşleme oluşturma</span><span class="sxs-lookup"><span data-stu-id="fea99-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzureRmResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location candacentral

# Peer VNet1 to VNet2.
Add-AzureRmVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzureRmVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="fea99-111">"MyVnet1" US Batı merkezi 'nde, Kanada Merkezi 'nde ' myVnet2 ' ile birlikte.</span><span class="sxs-lookup"><span data-stu-id="fea99-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="fea99-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fea99-112">PARAMETERS</span></span>

### <span data-ttu-id="fea99-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="fea99-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="fea99-114">Bu cmdlet 'in uzak sanal ağdaki sanal makinelerden iletilen trafiğe izin verdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="fea99-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="fea99-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="fea99-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="fea99-116">Uzak sanal ağın bu sanal ağa bağlantısında gatewayLinks 'in kullanılmasına izin ver bayrağı</span><span class="sxs-lookup"><span data-stu-id="fea99-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: AlloowGatewayTransit

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fea99-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="fea99-117">-AsJob</span></span>
<span data-ttu-id="fea99-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="fea99-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fea99-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="fea99-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="fea99-120">Bu cmdlet 'in, yerel sanal ağ alanındaki tüm sanal makinelere erişmek için bağlantılı sanal ağ alanındaki sanal makineleri engellediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="fea99-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="fea99-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fea99-121">-DefaultProfile</span></span>
<span data-ttu-id="fea99-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fea99-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fea99-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="fea99-123">-Name</span></span>
<span data-ttu-id="fea99-124">Sanal ağ eşliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fea99-124">Specifies the name of the virtual network peering.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fea99-125">-Remotevirtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="fea99-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="fea99-126">Uzak sanal ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fea99-126">Specifies the ID of the remote virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fea99-127">-Useremotegeçitleri</span><span class="sxs-lookup"><span data-stu-id="fea99-127">-UseRemoteGateways</span></span>
<span data-ttu-id="fea99-128">Bu cmdlet 'in bu sanal ağda uzak ağ geçitlerine izin verdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="fea99-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="fea99-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fea99-129">-VirtualNetwork</span></span>
<span data-ttu-id="fea99-130">Üst sanal ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="fea99-130">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="fea99-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea99-131">CommonParameters</span></span>
<span data-ttu-id="fea99-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fea99-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea99-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fea99-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea99-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fea99-134">INPUTS</span></span>

### <span data-ttu-id="fea99-135">Dizisi</span><span class="sxs-lookup"><span data-stu-id="fea99-135">String</span></span>
<span data-ttu-id="fea99-136">' Remotevirtualnetworkıd ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="fea99-136">Parameter 'RemoteVirtualNetworkId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="fea99-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fea99-137">PSVirtualNetwork</span></span>
<span data-ttu-id="fea99-138">' VirtualNetwork ' parametresi ardışık düzen için ' PSVirtualNetwork ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="fea99-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="fea99-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fea99-139">OUTPUTS</span></span>

### <span data-ttu-id="fea99-140">Microsoft. Azure. Commands. Network. model. psvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="fea99-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="fea99-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fea99-141">NOTES</span></span>

## <span data-ttu-id="fea99-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fea99-142">RELATED LINKS</span></span>

[<span data-ttu-id="fea99-143">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fea99-143">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="fea99-144">Get-azurermvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="fea99-144">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="fea99-145">Remove-azurermvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="fea99-145">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="fea99-146">Set-azurermvirtualnetworkeşleme</span><span class="sxs-lookup"><span data-stu-id="fea99-146">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


