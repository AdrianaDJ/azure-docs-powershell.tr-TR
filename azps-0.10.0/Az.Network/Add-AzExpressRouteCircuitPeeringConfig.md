---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 95c361199e813d5a79bd8f49858ad8d924bd02f3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935644"
---
# <span data-ttu-id="e694b-101">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e694b-101">Add-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="e694b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e694b-102">SYNOPSIS</span></span>
<span data-ttu-id="e694b-103">ExpressRoute devresi eşleme yapılandırmasını ekler.</span><span class="sxs-lookup"><span data-stu-id="e694b-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="e694b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e694b-104">SYNTAX</span></span>

### <span data-ttu-id="e694b-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e694b-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e694b-106">Microsoftpeeringconfigroutfilterıd</span><span class="sxs-lookup"><span data-stu-id="e694b-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e694b-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="e694b-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e694b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e694b-108">DESCRIPTION</span></span>
<span data-ttu-id="e694b-109">**Add-Azexpressroute, Peeringconfig** cmdlet 'ı ExpressRoute devresi eşleme yapılandırmasını ekler.</span><span class="sxs-lookup"><span data-stu-id="e694b-109">The **Add-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="e694b-110">ExpressRoute devreler şirket içi ağınızı, ortak Internet yerine bir bağlantı sağlayıcısı kullanarak Microsoft bulut 'a bağlayın.</span><span class="sxs-lookup"><span data-stu-id="e694b-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="e694b-111">**Add-Azexpressroute, Peeringconfig** 'i çalıştırdıktan sonra, yapılandırmayı etkinleştirmek için Set-AzExpressRouteCircuit cmdlet 'ini çağırmanız gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="e694b-111">Note that, after running **Add-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="e694b-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e694b-112">EXAMPLES</span></span>

### <span data-ttu-id="e694b-113">Örnek 1: var olan ExpressRoute devresini eş ekleme</span><span class="sxs-lookup"><span data-stu-id="e694b-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCircuitPeeringConfig @parameters
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="e694b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e694b-114">PARAMETERS</span></span>

### <span data-ttu-id="e694b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e694b-115">-DefaultProfile</span></span>
<span data-ttu-id="e694b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e694b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e694b-117">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="e694b-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="e694b-118">Değiştirilecek ExpressRoute devresi.</span><span class="sxs-lookup"><span data-stu-id="e694b-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="e694b-119">**Get-Azexpressroute, Get-Azexpressroutedevdevile** döndürülen Azure nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="e694b-119">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e694b-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="e694b-120">-LegacyMode</span></span>
<span data-ttu-id="e694b-121">Eşin eski modu</span><span class="sxs-lookup"><span data-stu-id="e694b-121">The legacy mode of the Peering</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e694b-122">-Microsoftconfigadvertisevseçpublicönekleri</span><span class="sxs-lookup"><span data-stu-id="e694b-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="e694b-123">Microsofteşlemedeki bir PeeringType için, BGP oturumu üzerinden duyurmak istediğiniz tüm öneklerin listesini sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e694b-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="e694b-124">Yalnızca genel IP adresi önekleri kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="e694b-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="e694b-125">Bir dizi önek göndermeyi düşünüyorsanız, virgülle ayrılmış bir liste gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e694b-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="e694b-126">Bu önekler size bir yönlendirme kayıt defteri adında (RıR/IÇ_VERIM_ORANı) kaydedilmelidir.</span><span class="sxs-lookup"><span data-stu-id="e694b-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="e694b-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="e694b-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="e694b-128">Eşleme numarası olarak kaydedilmemiş önekleri tanıtıcılarsa, kayıt edilen numara sayısını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e694b-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e694b-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="e694b-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="e694b-130">AS numarası ve öneklerinin kaydedildiği yönlendirme kayıt defteri adı (RıR/IÇ_VERIM_ORANı).</span><span class="sxs-lookup"><span data-stu-id="e694b-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e694b-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="e694b-131">-Name</span></span>
<span data-ttu-id="e694b-132">Eklenecek eşleme ilişkisinin adı.</span><span class="sxs-lookup"><span data-stu-id="e694b-132">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="e694b-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="e694b-133">-PeerAddressType</span></span>
<span data-ttu-id="e694b-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="e694b-134">PeerAddressType</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e694b-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="e694b-135">-PeerASN</span></span>
<span data-ttu-id="e694b-136">ExpressRoute devrenin AS numarası.</span><span class="sxs-lookup"><span data-stu-id="e694b-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="e694b-137">Bu, PeeringType AzurePublicPeering olduğunda genel bir ASN olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e694b-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e694b-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="e694b-138">-PeeringType</span></span>
<span data-ttu-id="e694b-139">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="e694b-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e694b-140">-Eldeki sabit Adressprefıx</span><span class="sxs-lookup"><span data-stu-id="e694b-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="e694b-141">Bu, bu eşleme ilişkisinin birincil Yönlendirme yolunun IP adresi aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="e694b-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="e694b-142">Bu bir/30 CıDR alt ağı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e694b-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="e694b-143">Bu alt ağdaki ilk tek sayılı adres, yönlendirici arayüzüne atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e694b-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="e694b-144">Azure, sonraki çift numaralı adresi Azure yönlendirici arabirimine yapılandıracak.</span><span class="sxs-lookup"><span data-stu-id="e694b-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="e694b-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="e694b-145">-RouteFilter</span></span>
<span data-ttu-id="e694b-146">Bu, mevcut bir RouteFilter nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="e694b-146">This is an existing RouteFilter object.</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: MicrosoftPeeringConfigRoutFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e694b-147">-Routefilterıd</span><span class="sxs-lookup"><span data-stu-id="e694b-147">-RouteFilterId</span></span>
<span data-ttu-id="e694b-148">Bu, var olan bir RouteFilter nesnesinin kaynak kimliğidir.</span><span class="sxs-lookup"><span data-stu-id="e694b-148">This is the resource Id of an existing RouteFilter object.</span></span>

```yaml
Type: String
Parameter Sets: MicrosoftPeeringConfigRoutFilterId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e694b-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e694b-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="e694b-150">Bu, bu eşleme ilişkisinin ikincil Yönlendirme yolunun IP adresi aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="e694b-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="e694b-151">Bu bir/30 CıDR alt ağı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e694b-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="e694b-152">Bu alt ağdaki ilk tek sayılı adres, yönlendirici arayüzüne atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e694b-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="e694b-153">Azure, sonraki çift numaralı adresi Azure yönlendirici arabirimine yapılandıracak.</span><span class="sxs-lookup"><span data-stu-id="e694b-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="e694b-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="e694b-154">-SharedKey</span></span>
<span data-ttu-id="e694b-155">Bu, eşleme yapılandırması için önceden paylaşılan anahtar olarak kullanılan isteğe bağlı bir MD5 karmasıdır.</span><span class="sxs-lookup"><span data-stu-id="e694b-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e694b-156">-Vlanıd</span><span class="sxs-lookup"><span data-stu-id="e694b-156">-VlanId</span></span>
<span data-ttu-id="e694b-157">Bu, bu eşleme için atanan VLAN 'ın kimlik numarasıdır.</span><span class="sxs-lookup"><span data-stu-id="e694b-157">This is the Id number of the VLAN assigned for this peering.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e694b-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e694b-158">CommonParameters</span></span>
<span data-ttu-id="e694b-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e694b-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e694b-160">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e694b-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e694b-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e694b-161">INPUTS</span></span>

### <span data-ttu-id="e694b-162">Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="e694b-162">PSExpressRouteCircuit</span></span>
<span data-ttu-id="e694b-163">' Expressroutedevresi ' parametresi, ardışık düzenin ' Psexpressroutedevresi ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e694b-163">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="e694b-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e694b-164">OUTPUTS</span></span>

### <span data-ttu-id="e694b-165">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="e694b-165">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e694b-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e694b-166">NOTES</span></span>

## <span data-ttu-id="e694b-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e694b-167">RELATED LINKS</span></span>

[<span data-ttu-id="e694b-168">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="e694b-168">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="e694b-169">Yeni-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="e694b-169">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="e694b-170">Remove-Azexpressroutedevresi Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="e694b-170">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="e694b-171">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="e694b-171">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
