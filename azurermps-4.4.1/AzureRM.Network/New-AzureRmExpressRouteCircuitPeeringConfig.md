---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 7008ec07c4ed8800d5817e6dbf306a1540d89a04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762566"
---
# <span data-ttu-id="2befd-101">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="2befd-101">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="2befd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2befd-102">SYNOPSIS</span></span>
<span data-ttu-id="2befd-103">ExpressRoute devresi 'e eklenecek yeni bir eşleme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2befd-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2befd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2befd-104">SYNTAX</span></span>

### <span data-ttu-id="2befd-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2befd-105">SetByResource (Default)</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <Int32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2befd-106">Microsoftpeeringconfigroutfilterıd</span><span class="sxs-lookup"><span data-stu-id="2befd-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <Int32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2befd-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="2befd-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <Int32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2befd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2befd-108">DESCRIPTION</span></span>
<span data-ttu-id="2befd-109">**Yeni-Azurermexpressroutedevresi Peeringconfig** cmdlet 'ı ExpressRoute devresi eşleme yapılandırmasını ekler.</span><span class="sxs-lookup"><span data-stu-id="2befd-109">The **New-AzureRmExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="2befd-110">ExpressRoute devreler şirket içi ağınızı, ortak Internet yerine bir bağlantı sağlayıcısı kullanarak Microsoft bulut 'a bağlayın.</span><span class="sxs-lookup"><span data-stu-id="2befd-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="2befd-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2befd-111">EXAMPLES</span></span>

### <span data-ttu-id="2befd-112">Örnek 1: eşleme yapılandırması ile yeni bir ExpressRoute devresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2befd-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
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
$PeerConfig = New-AzureRmExpressRouteCircuitPeeringConfig @parameters

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
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="2befd-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2befd-113">PARAMETERS</span></span>

### <span data-ttu-id="2befd-114">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="2befd-114">-LegacyMode</span></span>
<span data-ttu-id="2befd-115">Eşin eski modu</span><span class="sxs-lookup"><span data-stu-id="2befd-115">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="2befd-116">-Microsoftconfigadvertisevseçpublicönekleri</span><span class="sxs-lookup"><span data-stu-id="2befd-116">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="2befd-117">Microsofteşlemedeki bir PeeringType için, BGP oturumu üzerinden duyurmak istediğiniz tüm öneklerin listesini sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2befd-117">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="2befd-118">Yalnızca genel IP adresi önekleri kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="2befd-118">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="2befd-119">Bir dizi önek göndermeyi düşünüyorsanız, virgülle ayrılmış bir liste gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2befd-119">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="2befd-120">Bu önekler size bir yönlendirme kayıt defteri adında (RıR/IÇ_VERIM_ORANı) kaydedilmelidir.</span><span class="sxs-lookup"><span data-stu-id="2befd-120">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2befd-121">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="2befd-121">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="2befd-122">Eşleme numarası olarak kaydedilmemiş önekleri tanıtıcılarsa, kayıt edilen numara sayısını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2befd-122">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="2befd-123">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="2befd-123">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="2befd-124">AS numarası ve öneklerinin kaydedildiği yönlendirme kayıt defteri adı (RıR/IÇ_VERIM_ORANı).</span><span class="sxs-lookup"><span data-stu-id="2befd-124">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="2befd-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="2befd-125">-Name</span></span>
<span data-ttu-id="2befd-126">Oluşturulacak eşleme yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="2befd-126">The name of the peering configuration to be created.</span></span>

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

### <span data-ttu-id="2befd-127">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="2befd-127">-PeerAddressType</span></span>
<span data-ttu-id="2befd-128">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="2befd-128">PeerAddressType</span></span>

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

### <span data-ttu-id="2befd-129">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="2befd-129">-PeerASN</span></span>
<span data-ttu-id="2befd-130">ExpressRoute devrenin AS numarası.</span><span class="sxs-lookup"><span data-stu-id="2befd-130">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="2befd-131">Bu, PeeringType AzurePublicPeering olduğunda genel bir ASN olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2befd-131">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="2befd-132">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="2befd-132">-PeeringType</span></span>
<span data-ttu-id="2befd-133">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="2befd-133">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="2befd-134">-Eldeki sabit Adressprefıx</span><span class="sxs-lookup"><span data-stu-id="2befd-134">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="2befd-135">Bu, bu eşleme ilişkisinin birincil Yönlendirme yolunun IP adresi aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="2befd-135">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="2befd-136">Bu bir/30 CıDR alt ağı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2befd-136">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="2befd-137">Bu alt ağdaki ilk tek sayılı adres, yönlendirici arayüzüne atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2befd-137">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="2befd-138">Azure, sonraki çift numaralı adresi Azure yönlendirici arabirimine yapılandıracak.</span><span class="sxs-lookup"><span data-stu-id="2befd-138">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="2befd-139">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="2befd-139">-RouteFilter</span></span>
<span data-ttu-id="2befd-140">Bu, mevcut bir RouteFilter nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="2befd-140">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="2befd-141">-Routefilterıd</span><span class="sxs-lookup"><span data-stu-id="2befd-141">-RouteFilterId</span></span>
<span data-ttu-id="2befd-142">Bu, var olan bir RouteFilter nesnesinin kaynak kimliğidir.</span><span class="sxs-lookup"><span data-stu-id="2befd-142">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="2befd-143">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2befd-143">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="2befd-144">Bu, bu eşleme ilişkisinin ikincil Yönlendirme yolunun IP adresi aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="2befd-144">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="2befd-145">Bu bir/30 CıDR alt ağı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2befd-145">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="2befd-146">Bu alt ağdaki ilk tek sayılı adres, yönlendirici arayüzüne atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2befd-146">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="2befd-147">Azure, sonraki çift numaralı adresi Azure yönlendirici arabirimine yapılandıracak.</span><span class="sxs-lookup"><span data-stu-id="2befd-147">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="2befd-148">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="2befd-148">-SharedKey</span></span>
<span data-ttu-id="2befd-149">Bu, eşleme yapılandırması için önceden paylaşılan anahtar olarak kullanılan isteğe bağlı bir MD5 karmasıdır.</span><span class="sxs-lookup"><span data-stu-id="2befd-149">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="2befd-150">-Vlanıd</span><span class="sxs-lookup"><span data-stu-id="2befd-150">-VlanId</span></span>
<span data-ttu-id="2befd-151">Bu, bu eşleme için atanan VLAN 'ın kimlik numarasıdır.</span><span class="sxs-lookup"><span data-stu-id="2befd-151">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="2befd-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2befd-152">-DefaultProfile</span></span>
<span data-ttu-id="2befd-153">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2befd-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2befd-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2befd-154">CommonParameters</span></span>
<span data-ttu-id="2befd-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2befd-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2befd-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2befd-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2befd-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2befd-157">INPUTS</span></span>

## <span data-ttu-id="2befd-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2befd-158">OUTPUTS</span></span>

### <span data-ttu-id="2befd-159">Microsoft. Azure. Commands. Network. model. pspe,</span><span class="sxs-lookup"><span data-stu-id="2befd-159">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="2befd-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2befd-160">NOTES</span></span>

## <span data-ttu-id="2befd-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2befd-161">RELATED LINKS</span></span>

[<span data-ttu-id="2befd-162">Add-Azurermexpressroutedevresi Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="2befd-162">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="2befd-163">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="2befd-163">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="2befd-164">Remove-Azurermexpressroutedevresi Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="2befd-164">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="2befd-165">Set-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="2befd-165">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
