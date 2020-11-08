---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: ffc605a9376864a0576c4f7a6ae69f157ab9bacc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096820"
---
# <span data-ttu-id="11d58-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="11d58-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="11d58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11d58-102">SYNOPSIS</span></span>
<span data-ttu-id="11d58-103">Değiştirilmiş bir ExpressRoute eşleme yapılandırmasını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="11d58-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="11d58-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11d58-104">SYNTAX</span></span>

### <span data-ttu-id="11d58-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="11d58-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11d58-106">Microsoftpeeringconfigroutfilterıd</span><span class="sxs-lookup"><span data-stu-id="11d58-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11d58-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="11d58-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11d58-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="11d58-108">DESCRIPTION</span></span>
<span data-ttu-id="11d58-109">**Set-Azexpressroutedevresi Peeringconfig** cmdlet 'Leri değiştirilmiş ExpressRoute eşleme yapılandırmasını Azure 'a geri kaydeder.</span><span class="sxs-lookup"><span data-stu-id="11d58-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="11d58-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11d58-110">EXAMPLES</span></span>

### <span data-ttu-id="11d58-111">Örnek 1: varolan bir eşleme yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="11d58-111">Example 1: Change an existing peering configuration</span></span>
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

## <span data-ttu-id="11d58-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11d58-112">PARAMETERS</span></span>

### <span data-ttu-id="11d58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11d58-113">-DefaultProfile</span></span>
<span data-ttu-id="11d58-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="11d58-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11d58-115">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="11d58-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="11d58-116">Değiştirilecek eşleme yapılandırmasını içeren ExpressRoute devresi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="11d58-116">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="11d58-117">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="11d58-117">-LegacyMode</span></span>
<span data-ttu-id="11d58-118">Eşin eski modu</span><span class="sxs-lookup"><span data-stu-id="11d58-118">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="11d58-119">-Microsoftconfigadvertisevseçpublicönekleri</span><span class="sxs-lookup"><span data-stu-id="11d58-119">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="11d58-120">Microsofteşlemedeki bir PeeringType için, BGP oturumu üzerinden duyurmak istediğiniz tüm öneklerin listesini sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="11d58-120">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="11d58-121">Yalnızca genel IP adresi önekleri kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="11d58-121">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="11d58-122">Bir dizi önek göndermeyi düşünüyorsanız, virgülle ayrılmış bir liste gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11d58-122">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="11d58-123">Bu önekler size bir yönlendirme kayıt defteri adında (RıR/IÇ_VERIM_ORANı) kaydedilmelidir.</span><span class="sxs-lookup"><span data-stu-id="11d58-123">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="11d58-124">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="11d58-124">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="11d58-125">Eşleme numarası olarak kaydedilmemiş önekleri tanıtıcılarsa, kayıt edilen numara sayısını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11d58-125">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="11d58-126">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="11d58-126">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="11d58-127">AS numarası ve öneklerinin kaydedildiği yönlendirme kayıt defteri adı (RıR/IÇ_VERIM_ORANı).</span><span class="sxs-lookup"><span data-stu-id="11d58-127">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="11d58-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="11d58-128">-Name</span></span>
<span data-ttu-id="11d58-129">Değiştirilecek olan eşleme yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="11d58-129">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="11d58-130">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="11d58-130">-PeerAddressType</span></span>
<span data-ttu-id="11d58-131">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="11d58-131">PeerAddressType</span></span>

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

### <span data-ttu-id="11d58-132">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="11d58-132">-PeerASN</span></span>
<span data-ttu-id="11d58-133">ExpressRoute devrenin AS numarası.</span><span class="sxs-lookup"><span data-stu-id="11d58-133">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="11d58-134">Bu, PeeringType AzurePublicPeering olduğunda genel bir ASN olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="11d58-134">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="11d58-135">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="11d58-135">-PeeringType</span></span>
<span data-ttu-id="11d58-136">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="11d58-136">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="11d58-137">-Eldeki sabit Adressprefıx</span><span class="sxs-lookup"><span data-stu-id="11d58-137">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="11d58-138">Bu, bu eşleme ilişkisinin birincil Yönlendirme yolunun IP adresi aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="11d58-138">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="11d58-139">Bu bir/30 CıDR alt ağı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="11d58-139">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="11d58-140">Bu alt ağdaki ilk tek sayılı adres, yönlendirici arayüzüne atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="11d58-140">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="11d58-141">Azure, sonraki çift numaralı adresi Azure yönlendirici arabirimine yapılandıracak.</span><span class="sxs-lookup"><span data-stu-id="11d58-141">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="11d58-142">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="11d58-142">-RouteFilter</span></span>
<span data-ttu-id="11d58-143">Bu, mevcut bir RouteFilter nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="11d58-143">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="11d58-144">-Routefilterıd</span><span class="sxs-lookup"><span data-stu-id="11d58-144">-RouteFilterId</span></span>
<span data-ttu-id="11d58-145">Bu, var olan bir RouteFilter nesnesinin kaynak kimliğidir.</span><span class="sxs-lookup"><span data-stu-id="11d58-145">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="11d58-146">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="11d58-146">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="11d58-147">Bu, bu eşleme ilişkisinin ikincil Yönlendirme yolunun IP adresi aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="11d58-147">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="11d58-148">Bu bir/30 CıDR alt ağı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="11d58-148">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="11d58-149">Bu alt ağdaki ilk tek sayılı adres, yönlendirici arayüzüne atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="11d58-149">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="11d58-150">Azure, sonraki çift numaralı adresi Azure yönlendirici arabirimine yapılandıracak.</span><span class="sxs-lookup"><span data-stu-id="11d58-150">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="11d58-151">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="11d58-151">-SharedKey</span></span>
<span data-ttu-id="11d58-152">Bu, eşleme yapılandırması için önceden paylaşılan anahtar olarak kullanılan isteğe bağlı bir MD5 karmasıdır.</span><span class="sxs-lookup"><span data-stu-id="11d58-152">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="11d58-153">-Vlanıd</span><span class="sxs-lookup"><span data-stu-id="11d58-153">-VlanId</span></span>
<span data-ttu-id="11d58-154">Bu, bu eşleme için atanan VLAN 'ın kimlik numarasıdır.</span><span class="sxs-lookup"><span data-stu-id="11d58-154">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="11d58-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11d58-155">CommonParameters</span></span>
<span data-ttu-id="11d58-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11d58-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11d58-157">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11d58-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11d58-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11d58-158">INPUTS</span></span>

### <span data-ttu-id="11d58-159">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="11d58-159">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="11d58-160">System. String</span><span class="sxs-lookup"><span data-stu-id="11d58-160">System.String</span></span>

### <span data-ttu-id="11d58-161">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="11d58-161">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="11d58-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="11d58-162">System.Boolean</span></span>

## <span data-ttu-id="11d58-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11d58-163">OUTPUTS</span></span>

### <span data-ttu-id="11d58-164">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="11d58-164">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="11d58-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11d58-165">NOTES</span></span>

## <span data-ttu-id="11d58-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11d58-166">RELATED LINKS</span></span>

[<span data-ttu-id="11d58-167">Add-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="11d58-167">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="11d58-168">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="11d58-168">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="11d58-169">Yeni-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="11d58-169">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="11d58-170">Remove-Azexpressroutedevresi Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="11d58-170">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)