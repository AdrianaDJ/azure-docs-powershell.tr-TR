---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 5655fafa866fbc3702a1c6bf017caddd21df6fab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594636"
---
# <span data-ttu-id="5bcce-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="5bcce-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="5bcce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bcce-102">SYNOPSIS</span></span>
<span data-ttu-id="5bcce-103">ExpressRoute devresi eşleme yapılandırmasını ekler.</span><span class="sxs-lookup"><span data-stu-id="5bcce-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bcce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5bcce-104">SYNTAX</span></span>

### <span data-ttu-id="5bcce-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5bcce-105">SetByResource (Default)</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5bcce-106">Microsoftpeeringconfigroutfilterıd</span><span class="sxs-lookup"><span data-stu-id="5bcce-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5bcce-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="5bcce-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bcce-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5bcce-108">DESCRIPTION</span></span>
<span data-ttu-id="5bcce-109">**Add-Azurermexpressroutedevresi Peeringconfig** cmdlet 'ı ExpressRoute devresi eşleme yapılandırmasını ekler.</span><span class="sxs-lookup"><span data-stu-id="5bcce-109">The **Add-AzureRmExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="5bcce-110">ExpressRoute devreler şirket içi ağınızı, ortak Internet yerine bir bağlantı sağlayıcısı kullanarak Microsoft bulut 'a bağlayın.</span><span class="sxs-lookup"><span data-stu-id="5bcce-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="5bcce-111">**Add-Azurermexpressroutedevresi Peeringconfig** 'i çalıştırdıktan sonra, yapılandırmayı etkinleştirmek için Set-AzureRmExpressRouteCircuit cmdlet 'ini çağırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5bcce-111">Note that, after running **Add-AzureRmExpressRouteCircuitPeeringConfig** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="5bcce-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5bcce-112">EXAMPLES</span></span>

### <span data-ttu-id="5bcce-113">Örnek 1: var olan ExpressRoute devresini eş ekleme</span><span class="sxs-lookup"><span data-stu-id="5bcce-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzureRmExpressRouteCircuitPeeringConfig @parameters
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="5bcce-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5bcce-114">PARAMETERS</span></span>

### <span data-ttu-id="5bcce-115">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="5bcce-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="5bcce-116">Değiştirilecek ExpressRoute devresi.</span><span class="sxs-lookup"><span data-stu-id="5bcce-116">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="5bcce-117">Bu, **Get-Azurermexpressroutedevresi** cmdlet 'i tarafından döndürülen Azure nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="5bcce-117">This is Azure object returned by the **Get-AzureRmExpressRouteCircuit** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bcce-118">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="5bcce-118">-LegacyMode</span></span>
<span data-ttu-id="5bcce-119">Eşin eski modu</span><span class="sxs-lookup"><span data-stu-id="5bcce-119">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="5bcce-120">-Microsoftconfigadvertisevseçpublicönekleri</span><span class="sxs-lookup"><span data-stu-id="5bcce-120">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="5bcce-121">Microsofteşlemedeki bir PeeringType için, BGP oturumu üzerinden duyurmak istediğiniz tüm öneklerin listesini sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5bcce-121">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="5bcce-122">Yalnızca genel IP adresi önekleri kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="5bcce-122">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="5bcce-123">Bir dizi önek göndermeyi düşünüyorsanız, virgülle ayrılmış bir liste gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5bcce-123">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="5bcce-124">Bu önekler size bir yönlendirme kayıt defteri adında (RıR/IÇ_VERIM_ORANı) kaydedilmelidir.</span><span class="sxs-lookup"><span data-stu-id="5bcce-124">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="5bcce-125">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="5bcce-125">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="5bcce-126">Eşleme numarası olarak kaydedilmemiş önekleri tanıtıcılarsa, kayıt edilen numara sayısını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5bcce-126">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="5bcce-127">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="5bcce-127">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="5bcce-128">AS numarası ve öneklerinin kaydedildiği yönlendirme kayıt defteri adı (RıR/IÇ_VERIM_ORANı).</span><span class="sxs-lookup"><span data-stu-id="5bcce-128">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="5bcce-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="5bcce-129">-Name</span></span>
<span data-ttu-id="5bcce-130">Eklenecek eşleme ilişkisinin adı.</span><span class="sxs-lookup"><span data-stu-id="5bcce-130">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="5bcce-131">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="5bcce-131">-PeerAddressType</span></span>
<span data-ttu-id="5bcce-132">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="5bcce-132">PeerAddressType</span></span>

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

### <span data-ttu-id="5bcce-133">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="5bcce-133">-PeerASN</span></span>
<span data-ttu-id="5bcce-134">ExpressRoute devrenin AS numarası.</span><span class="sxs-lookup"><span data-stu-id="5bcce-134">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="5bcce-135">Bu, PeeringType AzurePublicPeering olduğunda genel bir ASN olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5bcce-135">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="5bcce-136">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="5bcce-136">-PeeringType</span></span>
<span data-ttu-id="5bcce-137">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="5bcce-137">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="5bcce-138">-Eldeki sabit Adressprefıx</span><span class="sxs-lookup"><span data-stu-id="5bcce-138">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="5bcce-139">Bu, bu eşleme ilişkisinin birincil Yönlendirme yolunun IP adresi aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="5bcce-139">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="5bcce-140">Bu bir/30 CıDR alt ağı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5bcce-140">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="5bcce-141">Bu alt ağdaki ilk tek sayılı adres, yönlendirici arayüzüne atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5bcce-141">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="5bcce-142">Azure, sonraki çift numaralı adresi Azure yönlendirici arabirimine yapılandıracak.</span><span class="sxs-lookup"><span data-stu-id="5bcce-142">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="5bcce-143">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="5bcce-143">-RouteFilter</span></span>
<span data-ttu-id="5bcce-144">Bu, mevcut bir RouteFilter nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="5bcce-144">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="5bcce-145">-Routefilterıd</span><span class="sxs-lookup"><span data-stu-id="5bcce-145">-RouteFilterId</span></span>
<span data-ttu-id="5bcce-146">Bu, var olan bir RouteFilter nesnesinin kaynak kimliğidir.</span><span class="sxs-lookup"><span data-stu-id="5bcce-146">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="5bcce-147">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5bcce-147">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="5bcce-148">Bu, bu eşleme ilişkisinin ikincil Yönlendirme yolunun IP adresi aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="5bcce-148">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="5bcce-149">Bu bir/30 CıDR alt ağı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5bcce-149">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="5bcce-150">Bu alt ağdaki ilk tek sayılı adres, yönlendirici arayüzüne atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5bcce-150">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="5bcce-151">Azure, sonraki çift numaralı adresi Azure yönlendirici arabirimine yapılandıracak.</span><span class="sxs-lookup"><span data-stu-id="5bcce-151">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="5bcce-152">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="5bcce-152">-SharedKey</span></span>
<span data-ttu-id="5bcce-153">Bu, eşleme yapılandırması için önceden paylaşılan anahtar olarak kullanılan isteğe bağlı bir MD5 karmasıdır.</span><span class="sxs-lookup"><span data-stu-id="5bcce-153">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="5bcce-154">-Vlanıd</span><span class="sxs-lookup"><span data-stu-id="5bcce-154">-VlanId</span></span>
<span data-ttu-id="5bcce-155">Bu, bu eşleme için atanan VLAN 'ın kimlik numarasıdır.</span><span class="sxs-lookup"><span data-stu-id="5bcce-155">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="5bcce-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bcce-156">-DefaultProfile</span></span>
<span data-ttu-id="5bcce-157">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5bcce-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bcce-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bcce-158">CommonParameters</span></span>
<span data-ttu-id="5bcce-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5bcce-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bcce-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bcce-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bcce-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5bcce-161">INPUTS</span></span>

### <span data-ttu-id="5bcce-162">Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="5bcce-162">PSExpressRouteCircuit</span></span>
<span data-ttu-id="5bcce-163">' Expressroutedevresi ' parametresi, ardışık düzenin ' Psexpressroutedevresi ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="5bcce-163">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="5bcce-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5bcce-164">OUTPUTS</span></span>

### <span data-ttu-id="5bcce-165">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="5bcce-165">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="5bcce-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5bcce-166">NOTES</span></span>

## <span data-ttu-id="5bcce-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5bcce-167">RELATED LINKS</span></span>

[<span data-ttu-id="5bcce-168">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="5bcce-168">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="5bcce-169">New-Azurermexpressroutedevresi Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="5bcce-169">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="5bcce-170">Remove-Azurermexpressroutedevresi Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="5bcce-170">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="5bcce-171">Set-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="5bcce-171">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
