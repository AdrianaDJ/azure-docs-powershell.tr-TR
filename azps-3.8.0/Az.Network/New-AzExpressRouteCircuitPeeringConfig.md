---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: c4c3abf1eeb387c700bb456b50887fdc9dd41c74
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104749"
---
# <span data-ttu-id="e5c13-101">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e5c13-101">New-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="e5c13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5c13-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c13-103">ExpressRoute devresi 'e eklenecek yeni bir eşleme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e5c13-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="e5c13-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5c13-104">SYNTAX</span></span>

### <span data-ttu-id="e5c13-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e5c13-105">SetByResource (Default)</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5c13-106">Microsoftpeeringconfigroutfilterıd</span><span class="sxs-lookup"><span data-stu-id="e5c13-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5c13-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="e5c13-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5c13-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5c13-108">DESCRIPTION</span></span>
<span data-ttu-id="e5c13-109">**Yeni-Azexpressroute, Peeringconfig** cmdlet 'ı ExpressRoute devresi eşleme yapılandırmasını ekler.</span><span class="sxs-lookup"><span data-stu-id="e5c13-109">The **New-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="e5c13-110">ExpressRoute devreler şirket içi ağınızı, ortak Internet yerine bir bağlantı sağlayıcısı kullanarak Microsoft bulut 'a bağlayın.</span><span class="sxs-lookup"><span data-stu-id="e5c13-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="e5c13-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5c13-111">EXAMPLES</span></span>

### <span data-ttu-id="e5c13-112">Örnek 1: eşleme yapılandırması ile yeni bir ExpressRoute devresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e5c13-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
```
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
$PeerConfig = New-AzExpressRouteCircuitPeeringConfig @parameters

$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ServiceProviderName='Equinix'
    Peering=$PeerConfig
    PeeringLocation='Silicon Valley'
    BandwidthInMbps=200
}
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="e5c13-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5c13-113">PARAMETERS</span></span>

### <span data-ttu-id="e5c13-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c13-114">-DefaultProfile</span></span>
<span data-ttu-id="e5c13-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e5c13-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5c13-116">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="e5c13-116">-LegacyMode</span></span>
<span data-ttu-id="e5c13-117">Eşin eski modu</span><span class="sxs-lookup"><span data-stu-id="e5c13-117">The legacy mode of the Peering</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c13-118">-Microsoftconfigadvertisevseçpublicönekleri</span><span class="sxs-lookup"><span data-stu-id="e5c13-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="e5c13-119">Microsofteşlemedeki bir PeeringType için, BGP oturumu üzerinden duyurmak istediğiniz tüm öneklerin listesini sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e5c13-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="e5c13-120">Yalnızca genel IP adresi önekleri kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="e5c13-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="e5c13-121">Bir dizi önek göndermeyi düşünüyorsanız, virgülle ayrılmış bir liste gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5c13-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="e5c13-122">Bu önekler size bir yönlendirme kayıt defteri adında (RıR/IÇ_VERIM_ORANı) kaydedilmelidir.</span><span class="sxs-lookup"><span data-stu-id="e5c13-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c13-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="e5c13-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="e5c13-124">Eşleme numarası olarak kaydedilmemiş önekleri tanıtıcılarsa, kayıt edilen numara sayısını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5c13-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c13-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="e5c13-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="e5c13-126">AS numarası ve öneklerinin kaydedildiği yönlendirme kayıt defteri adı (RıR/IÇ_VERIM_ORANı).</span><span class="sxs-lookup"><span data-stu-id="e5c13-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="e5c13-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="e5c13-127">-Name</span></span>
<span data-ttu-id="e5c13-128">Oluşturulacak eşleme yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="e5c13-128">The name of the peering configuration to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c13-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="e5c13-129">-PeerAddressType</span></span>
<span data-ttu-id="e5c13-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="e5c13-130">PeerAddressType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c13-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="e5c13-131">-PeerASN</span></span>
<span data-ttu-id="e5c13-132">ExpressRoute devrenin AS numarası.</span><span class="sxs-lookup"><span data-stu-id="e5c13-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="e5c13-133">Bu, PeeringType AzurePublicPeering olduğunda genel bir ASN olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e5c13-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c13-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="e5c13-134">-PeeringType</span></span>
<span data-ttu-id="e5c13-135">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="e5c13-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c13-136">-Eldeki sabit Adressprefıx</span><span class="sxs-lookup"><span data-stu-id="e5c13-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="e5c13-137">Bu, bu eşleme ilişkisinin birincil Yönlendirme yolunun IP adresi aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="e5c13-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="e5c13-138">Bu bir/30 CıDR alt ağı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e5c13-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="e5c13-139">Bu alt ağdaki ilk tek sayılı adres, yönlendirici arayüzüne atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e5c13-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="e5c13-140">Azure, sonraki çift numaralı adresi Azure yönlendirici arabirimine yapılandıracak.</span><span class="sxs-lookup"><span data-stu-id="e5c13-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c13-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="e5c13-141">-RouteFilter</span></span>
<span data-ttu-id="e5c13-142">Bu, mevcut bir RouteFilter nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="e5c13-142">This is an existing RouteFilter object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: MicrosoftPeeringConfigRoutFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c13-143">-Routefilterıd</span><span class="sxs-lookup"><span data-stu-id="e5c13-143">-RouteFilterId</span></span>
<span data-ttu-id="e5c13-144">Bu, var olan bir RouteFilter nesnesinin kaynak kimliğidir.</span><span class="sxs-lookup"><span data-stu-id="e5c13-144">This is the resource Id of an existing RouteFilter object.</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftPeeringConfigRoutFilterId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c13-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e5c13-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="e5c13-146">Bu, bu eşleme ilişkisinin ikincil Yönlendirme yolunun IP adresi aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="e5c13-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="e5c13-147">Bu bir/30 CıDR alt ağı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e5c13-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="e5c13-148">Bu alt ağdaki ilk tek sayılı adres, yönlendirici arayüzüne atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e5c13-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="e5c13-149">Azure, sonraki çift numaralı adresi Azure yönlendirici arabirimine yapılandıracak.</span><span class="sxs-lookup"><span data-stu-id="e5c13-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c13-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="e5c13-150">-SharedKey</span></span>
<span data-ttu-id="e5c13-151">Bu, eşleme yapılandırması için önceden paylaşılan anahtar olarak kullanılan isteğe bağlı bir MD5 karmasıdır.</span><span class="sxs-lookup"><span data-stu-id="e5c13-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="e5c13-152">-Vlanıd</span><span class="sxs-lookup"><span data-stu-id="e5c13-152">-VlanId</span></span>
<span data-ttu-id="e5c13-153">Bu, bu eşleme için atanan VLAN 'ın kimlik numarasıdır.</span><span class="sxs-lookup"><span data-stu-id="e5c13-153">This is the Id number of the VLAN assigned for this peering.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c13-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c13-154">CommonParameters</span></span>
<span data-ttu-id="e5c13-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5c13-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c13-156">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5c13-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c13-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5c13-157">INPUTS</span></span>

### <span data-ttu-id="e5c13-158">System. String</span><span class="sxs-lookup"><span data-stu-id="e5c13-158">System.String</span></span>

### <span data-ttu-id="e5c13-159">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e5c13-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="e5c13-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e5c13-160">System.Boolean</span></span>

## <span data-ttu-id="e5c13-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5c13-161">OUTPUTS</span></span>

### <span data-ttu-id="e5c13-162">Microsoft. Azure. Commands. Network. model. pspe,</span><span class="sxs-lookup"><span data-stu-id="e5c13-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="e5c13-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5c13-163">NOTES</span></span>

## <span data-ttu-id="e5c13-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5c13-164">RELATED LINKS</span></span>

[<span data-ttu-id="e5c13-165">Add-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="e5c13-165">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="e5c13-166">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="e5c13-166">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="e5c13-167">Remove-Azexpressroutedevresi Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="e5c13-167">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="e5c13-168">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="e5c13-168">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
