---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: ecbd0d101db979d5982891bbfbd4ad1e3083ee8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760023"
---
# <span data-ttu-id="d87fc-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="d87fc-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="d87fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d87fc-102">SYNOPSIS</span></span>
<span data-ttu-id="d87fc-103">Değiştirilmiş bir ExpressRoute eşleme yapılandırmasını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d87fc-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="d87fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d87fc-104">SYNTAX</span></span>

### <span data-ttu-id="d87fc-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d87fc-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d87fc-106">Microsoftpeeringconfigroutfilterıd</span><span class="sxs-lookup"><span data-stu-id="d87fc-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d87fc-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="d87fc-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d87fc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d87fc-108">DESCRIPTION</span></span>
<span data-ttu-id="d87fc-109">**Set-Azexpressroutedevresi Peeringconfig** cmdlet 'Leri değiştirilmiş ExpressRoute eşleme yapılandırmasını Azure 'a geri kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d87fc-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="d87fc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d87fc-110">EXAMPLES</span></span>

### <span data-ttu-id="d87fc-111">Örnek 1: varolan bir eşleme yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="d87fc-111">Example 1: Change an existing peering configuration</span></span>
```
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

## <span data-ttu-id="d87fc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d87fc-112">PARAMETERS</span></span>

### <span data-ttu-id="d87fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d87fc-113">-DefaultProfile</span></span>
<span data-ttu-id="d87fc-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d87fc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d87fc-115">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="d87fc-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="d87fc-116">Değiştirilecek eşleme yapılandırmasını içeren ExpressRoute devresi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d87fc-116">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="d87fc-117">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="d87fc-117">-LegacyMode</span></span>
<span data-ttu-id="d87fc-118">Eşin eski modu</span><span class="sxs-lookup"><span data-stu-id="d87fc-118">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="d87fc-119">-Microsoftconfigadvertisevseçpublicönekleri</span><span class="sxs-lookup"><span data-stu-id="d87fc-119">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="d87fc-120">Microsofteşlemedeki bir PeeringType için, BGP oturumu üzerinden duyurmak istediğiniz tüm öneklerin listesini sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d87fc-120">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="d87fc-121">Yalnızca genel IP adresi önekleri kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="d87fc-121">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="d87fc-122">Bir dizi önek göndermeyi düşünüyorsanız, virgülle ayrılmış bir liste gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d87fc-122">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="d87fc-123">Bu önekler size bir yönlendirme kayıt defteri adında (RıR/IÇ_VERIM_ORANı) kaydedilmelidir.</span><span class="sxs-lookup"><span data-stu-id="d87fc-123">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="d87fc-124">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="d87fc-124">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="d87fc-125">Eşleme numarası olarak kaydedilmemiş önekleri tanıtıcılarsa, kayıt edilen numara sayısını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d87fc-125">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="d87fc-126">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="d87fc-126">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="d87fc-127">AS numarası ve öneklerinin kaydedildiği yönlendirme kayıt defteri adı (RıR/IÇ_VERIM_ORANı).</span><span class="sxs-lookup"><span data-stu-id="d87fc-127">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="d87fc-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="d87fc-128">-Name</span></span>
<span data-ttu-id="d87fc-129">Değiştirilecek olan eşleme yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="d87fc-129">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="d87fc-130">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="d87fc-130">-PeerAddressType</span></span>
<span data-ttu-id="d87fc-131">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="d87fc-131">PeerAddressType</span></span>

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

### <span data-ttu-id="d87fc-132">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="d87fc-132">-PeerASN</span></span>
<span data-ttu-id="d87fc-133">ExpressRoute devrenin AS numarası.</span><span class="sxs-lookup"><span data-stu-id="d87fc-133">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="d87fc-134">Bu, PeeringType AzurePublicPeering olduğunda genel bir ASN olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d87fc-134">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="d87fc-135">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="d87fc-135">-PeeringType</span></span>
<span data-ttu-id="d87fc-136">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="d87fc-136">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="d87fc-137">-Eldeki sabit Adressprefıx</span><span class="sxs-lookup"><span data-stu-id="d87fc-137">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="d87fc-138">Bu, bu eşleme ilişkisinin birincil Yönlendirme yolunun IP adresi aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="d87fc-138">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="d87fc-139">Bu bir/30 CıDR alt ağı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d87fc-139">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="d87fc-140">Bu alt ağdaki ilk tek sayılı adres, yönlendirici arayüzüne atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d87fc-140">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="d87fc-141">Azure, sonraki çift numaralı adresi Azure yönlendirici arabirimine yapılandıracak.</span><span class="sxs-lookup"><span data-stu-id="d87fc-141">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="d87fc-142">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="d87fc-142">-RouteFilter</span></span>
<span data-ttu-id="d87fc-143">Bu, mevcut bir RouteFilter nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="d87fc-143">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="d87fc-144">-Routefilterıd</span><span class="sxs-lookup"><span data-stu-id="d87fc-144">-RouteFilterId</span></span>
<span data-ttu-id="d87fc-145">Bu, var olan bir RouteFilter nesnesinin kaynak kimliğidir.</span><span class="sxs-lookup"><span data-stu-id="d87fc-145">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="d87fc-146">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d87fc-146">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="d87fc-147">Bu, bu eşleme ilişkisinin ikincil Yönlendirme yolunun IP adresi aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="d87fc-147">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="d87fc-148">Bu bir/30 CıDR alt ağı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d87fc-148">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="d87fc-149">Bu alt ağdaki ilk tek sayılı adres, yönlendirici arayüzüne atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d87fc-149">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="d87fc-150">Azure, sonraki çift numaralı adresi Azure yönlendirici arabirimine yapılandıracak.</span><span class="sxs-lookup"><span data-stu-id="d87fc-150">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="d87fc-151">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="d87fc-151">-SharedKey</span></span>
<span data-ttu-id="d87fc-152">Bu, eşleme yapılandırması için önceden paylaşılan anahtar olarak kullanılan isteğe bağlı bir MD5 karmasıdır.</span><span class="sxs-lookup"><span data-stu-id="d87fc-152">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="d87fc-153">-Vlanıd</span><span class="sxs-lookup"><span data-stu-id="d87fc-153">-VlanId</span></span>
<span data-ttu-id="d87fc-154">Bu, bu eşleme için atanan VLAN 'ın kimlik numarasıdır.</span><span class="sxs-lookup"><span data-stu-id="d87fc-154">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="d87fc-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d87fc-155">CommonParameters</span></span>
<span data-ttu-id="d87fc-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d87fc-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d87fc-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d87fc-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d87fc-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d87fc-158">INPUTS</span></span>

### <span data-ttu-id="d87fc-159">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="d87fc-159">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="d87fc-160">System. String</span><span class="sxs-lookup"><span data-stu-id="d87fc-160">System.String</span></span>

### <span data-ttu-id="d87fc-161">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d87fc-161">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="d87fc-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d87fc-162">System.Boolean</span></span>

## <span data-ttu-id="d87fc-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d87fc-163">OUTPUTS</span></span>

### <span data-ttu-id="d87fc-164">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="d87fc-164">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="d87fc-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d87fc-165">NOTES</span></span>

## <span data-ttu-id="d87fc-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d87fc-166">RELATED LINKS</span></span>

[<span data-ttu-id="d87fc-167">Add-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="d87fc-167">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="d87fc-168">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="d87fc-168">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="d87fc-169">Yeni-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="d87fc-169">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="d87fc-170">Remove-Azexpressroutedevresi Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="d87fc-170">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)
