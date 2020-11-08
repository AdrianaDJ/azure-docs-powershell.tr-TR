---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: b41e7a0d6da67134cc1dd8842e0bd34c73128f58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274325"
---
# <span data-ttu-id="9d4d6-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="9d4d6-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="9d4d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d4d6-102">SYNOPSIS</span></span>
<span data-ttu-id="9d4d6-103">Değiştirilmiş bir ExpressRoute eşleme yapılandırmasını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="9d4d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9d4d6-104">SYNTAX</span></span>

### <span data-ttu-id="9d4d6-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9d4d6-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d4d6-106">Microsoftpeeringconfigroutfilterıd</span><span class="sxs-lookup"><span data-stu-id="9d4d6-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d4d6-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="9d4d6-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d4d6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9d4d6-108">DESCRIPTION</span></span>
<span data-ttu-id="9d4d6-109">**Set-Azexpressroutedevresi Peeringconfig** cmdlet 'Leri değiştirilmiş ExpressRoute eşleme yapılandırmasını Azure 'a geri kaydeder.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="9d4d6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9d4d6-110">EXAMPLES</span></span>

### <span data-ttu-id="9d4d6-111">Örnek 1: varolan bir eşleme yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="9d4d6-111">Example 1: Change an existing peering configuration</span></span>
```powershell
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 201
}
Set-AzExpressRouteCircuitPeeringConfig @parameters
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

### <span data-ttu-id="9d4d6-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9d4d6-112">Example 2</span></span>

<span data-ttu-id="9d4d6-113">Değiştirilmiş bir ExpressRoute eşleme yapılandırmasını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-113">Saves a modified ExpressRoute peering configuration.</span></span> <span data-ttu-id="9d4d6-114">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="9d4d6-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzExpressRouteCircuitPeeringConfig -ExpressRouteCircuit <PSExpressRouteCircuit> -Name 'cert01' -PeerASN 100 -PeerAddressType IPv4 -PeeringType AzurePrivatePeering -PrimaryPeerAddressPrefix '123.0.0.0/30' -SecondaryPeerAddressPrefix '123.0.0.4/30' -VlanId 300
```

## <span data-ttu-id="9d4d6-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9d4d6-115">PARAMETERS</span></span>

### <span data-ttu-id="9d4d6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d4d6-116">-DefaultProfile</span></span>
<span data-ttu-id="9d4d6-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d4d6-118">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="9d4d6-118">-ExpressRouteCircuit</span></span>
<span data-ttu-id="9d4d6-119">Değiştirilecek eşleme yapılandırmasını içeren ExpressRoute devresi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-119">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="9d4d6-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="9d4d6-120">-LegacyMode</span></span>
<span data-ttu-id="9d4d6-121">Eşin eski modu</span><span class="sxs-lookup"><span data-stu-id="9d4d6-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="9d4d6-122">-Microsoftconfigadvertisevseçpublicönekleri</span><span class="sxs-lookup"><span data-stu-id="9d4d6-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="9d4d6-123">Microsofteşlemedeki bir PeeringType için, BGP oturumu üzerinden duyurmak istediğiniz tüm öneklerin listesini sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="9d4d6-124">Yalnızca genel IP adresi önekleri kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="9d4d6-125">Bir dizi önek göndermeyi düşünüyorsanız, virgülle ayrılmış bir liste gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="9d4d6-126">Bu önekler size bir yönlendirme kayıt defteri adında (RıR/IÇ_VERIM_ORANı) kaydedilmelidir.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="9d4d6-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="9d4d6-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="9d4d6-128">Eşleme numarası olarak kaydedilmemiş önekleri tanıtıcılarsa, kayıt edilen numara sayısını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="9d4d6-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="9d4d6-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="9d4d6-130">AS numarası ve öneklerinin kaydedildiği yönlendirme kayıt defteri adı (RıR/IÇ_VERIM_ORANı).</span><span class="sxs-lookup"><span data-stu-id="9d4d6-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="9d4d6-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="9d4d6-131">-Name</span></span>
<span data-ttu-id="9d4d6-132">Değiştirilecek olan eşleme yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-132">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="9d4d6-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="9d4d6-133">-PeerAddressType</span></span>
<span data-ttu-id="9d4d6-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="9d4d6-134">PeerAddressType</span></span>

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

### <span data-ttu-id="9d4d6-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="9d4d6-135">-PeerASN</span></span>
<span data-ttu-id="9d4d6-136">ExpressRoute devrenin AS numarası.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="9d4d6-137">Bu, PeeringType AzurePublicPeering olduğunda genel bir ASN olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="9d4d6-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="9d4d6-138">-PeeringType</span></span>
<span data-ttu-id="9d4d6-139">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="9d4d6-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="9d4d6-140">-Eldeki sabit Adressprefıx</span><span class="sxs-lookup"><span data-stu-id="9d4d6-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="9d4d6-141">Bu, bu eşleme ilişkisinin birincil Yönlendirme yolunun IP adresi aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="9d4d6-142">Bu bir/30 CıDR alt ağı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="9d4d6-143">Bu alt ağdaki ilk tek sayılı adres, yönlendirici arayüzüne atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="9d4d6-144">Azure, sonraki çift numaralı adresi Azure yönlendirici arabirimine yapılandıracak.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="9d4d6-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="9d4d6-145">-RouteFilter</span></span>
<span data-ttu-id="9d4d6-146">Bu, mevcut bir RouteFilter nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="9d4d6-147">-Routefilterıd</span><span class="sxs-lookup"><span data-stu-id="9d4d6-147">-RouteFilterId</span></span>
<span data-ttu-id="9d4d6-148">Bu, var olan bir RouteFilter nesnesinin kaynak kimliğidir.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="9d4d6-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9d4d6-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="9d4d6-150">Bu, bu eşleme ilişkisinin ikincil Yönlendirme yolunun IP adresi aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="9d4d6-151">Bu bir/30 CıDR alt ağı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="9d4d6-152">Bu alt ağdaki ilk tek sayılı adres, yönlendirici arayüzüne atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="9d4d6-153">Azure, sonraki çift numaralı adresi Azure yönlendirici arabirimine yapılandıracak.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="9d4d6-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="9d4d6-154">-SharedKey</span></span>
<span data-ttu-id="9d4d6-155">Bu, eşleme yapılandırması için önceden paylaşılan anahtar olarak kullanılan isteğe bağlı bir MD5 karmasıdır.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="9d4d6-156">-Vlanıd</span><span class="sxs-lookup"><span data-stu-id="9d4d6-156">-VlanId</span></span>
<span data-ttu-id="9d4d6-157">Bu, bu eşleme için atanan VLAN 'ın kimlik numarasıdır.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="9d4d6-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d4d6-158">CommonParameters</span></span>
<span data-ttu-id="9d4d6-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d4d6-160">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d4d6-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d4d6-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9d4d6-161">INPUTS</span></span>

### <span data-ttu-id="9d4d6-162">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="9d4d6-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="9d4d6-163">System. String</span><span class="sxs-lookup"><span data-stu-id="9d4d6-163">System.String</span></span>

### <span data-ttu-id="9d4d6-164">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9d4d6-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="9d4d6-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9d4d6-165">System.Boolean</span></span>

## <span data-ttu-id="9d4d6-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9d4d6-166">OUTPUTS</span></span>

### <span data-ttu-id="9d4d6-167">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="9d4d6-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="9d4d6-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9d4d6-168">NOTES</span></span>

## <span data-ttu-id="9d4d6-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9d4d6-169">RELATED LINKS</span></span>

[<span data-ttu-id="9d4d6-170">Add-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="9d4d6-170">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="9d4d6-171">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="9d4d6-171">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="9d4d6-172">Yeni-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="9d4d6-172">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="9d4d6-173">Remove-Azexpressroutedevresi Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="9d4d6-173">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)
