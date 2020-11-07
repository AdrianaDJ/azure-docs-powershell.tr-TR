---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 92740ce457c9e7c571f925e1813bc120a88a86a5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760718"
---
# <span data-ttu-id="cf612-101">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="cf612-101">Add-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="cf612-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf612-102">SYNOPSIS</span></span>
<span data-ttu-id="cf612-103">ExpressRoute çapraz bağlantısına eşleme yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="cf612-103">Adds a peering configuration to an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="cf612-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf612-104">SYNTAX</span></span>

```
Add-AzExpressRouteCrossConnectionPeering -Name <String>
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-Force] -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefix <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf612-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf612-105">DESCRIPTION</span></span>
<span data-ttu-id="cf612-106">**Add-Azexpressroutecrossconnectioneşlemecmdlet** 'ı ExpressRoute çapraz bağlantısına eşleme yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="cf612-106">The **Add-AzExpressRouteCrossConnectionPeering** cmdlet adds a peering configuration to an ExpressRoute cross connection.</span></span> <span data-ttu-id="cf612-107">**Add-Azexpressroutecrossconnectioneşlemeyi** çalıştırdıktan sonra, yapılandırmayı etkinleştirmek için Set-AzExpressRouteCrossConnection cmdlet 'ini çağırmanız gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="cf612-107">Note that, after running **Add-AzExpressRouteCrossConnectionPeering** , you must call the Set-AzExpressRouteCrossConnection cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="cf612-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf612-108">EXAMPLES</span></span>

### <span data-ttu-id="cf612-109">Örnek 1: var olan ExpressRoute çapraz bağlantısına eş ekleme</span><span class="sxs-lookup"><span data-stu-id="cf612-109">Example 1: Add a peer to an existing ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    CrossConnection = $cc
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCrossConnectionPeering @parameters
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="cf612-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf612-110">PARAMETERS</span></span>

### <span data-ttu-id="cf612-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf612-111">-DefaultProfile</span></span>
<span data-ttu-id="cf612-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cf612-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf612-113">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="cf612-113">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="cf612-114">ExpressRoute çapraz bağlantı.</span><span class="sxs-lookup"><span data-stu-id="cf612-114">The ExpressRoute cross connection being modified.</span></span> <span data-ttu-id="cf612-115">**Get-AzExpressRouteCrossConnection** cmdlet 'i tarafından döndürülen Azure nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="cf612-115">This is Azure object returned by the **Get-AzExpressRouteCrossConnection** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf612-116">-Force</span><span class="sxs-lookup"><span data-stu-id="cf612-116">-Force</span></span>
<span data-ttu-id="cf612-117">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="cf612-117">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf612-118">-Microsoftconfigadvertisevseçpublicprefix</span><span class="sxs-lookup"><span data-stu-id="cf612-118">-MicrosoftConfigAdvertisedPublicPrefix</span></span>
<span data-ttu-id="cf612-119">Microsofteşlemedeki bir PeeringType için, BGP oturumu üzerinden duyurmak istediğiniz tüm öneklerin listesini sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="cf612-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="cf612-120">Yalnızca genel IP adresi önekleri kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="cf612-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="cf612-121">Bir dizi önek göndermeyi düşünüyorsanız, virgülle ayrılmış bir liste gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cf612-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="cf612-122">Bu önekler size bir yönlendirme kayıt defteri adında (RıR/IÇ_VERIM_ORANı) kaydedilmelidir.</span><span class="sxs-lookup"><span data-stu-id="cf612-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="cf612-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="cf612-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="cf612-124">Eşleme numarası olarak kaydedilmemiş önekleri tanıtıcılarsa, kayıt edilen numara sayısını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cf612-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="cf612-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="cf612-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="cf612-126">AS numarası ve öneklerinin kaydedildiği yönlendirme kayıt defteri adı (RıR/IÇ_VERIM_ORANı).</span><span class="sxs-lookup"><span data-stu-id="cf612-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="cf612-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="cf612-127">-Name</span></span>
<span data-ttu-id="cf612-128">Eklenecek eşleme ilişkisinin adı.</span><span class="sxs-lookup"><span data-stu-id="cf612-128">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="cf612-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="cf612-129">-PeerAddressType</span></span>
<span data-ttu-id="cf612-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="cf612-130">PeerAddressType</span></span>

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

### <span data-ttu-id="cf612-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="cf612-131">-PeerASN</span></span>
<span data-ttu-id="cf612-132">ExpressRoute çapraz bağlantınızın AS numarası.</span><span class="sxs-lookup"><span data-stu-id="cf612-132">The AS number of your ExpressRoute cross connection.</span></span> <span data-ttu-id="cf612-133">Bu, PeeringType AzurePublicPeering olduğunda genel bir ASN olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="cf612-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="cf612-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="cf612-134">-PeeringType</span></span>
<span data-ttu-id="cf612-135">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="cf612-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="cf612-136">-Eldeki sabit Adressprefıx</span><span class="sxs-lookup"><span data-stu-id="cf612-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="cf612-137">Bu, bu eşleme ilişkisinin birincil Yönlendirme yolunun IP adresi aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="cf612-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="cf612-138">Bu bir/30 CıDR alt ağı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="cf612-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="cf612-139">Bu alt ağdaki ilk tek sayılı adres, yönlendirici arayüzüne atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="cf612-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="cf612-140">Azure, sonraki çift numaralı adresi Azure yönlendirici arabirimine yapılandıracak.</span><span class="sxs-lookup"><span data-stu-id="cf612-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="cf612-141">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="cf612-141">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="cf612-142">Bu, bu eşleme ilişkisinin ikincil Yönlendirme yolunun IP adresi aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="cf612-142">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="cf612-143">Bu bir/30 CıDR alt ağı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="cf612-143">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="cf612-144">Bu alt ağdaki ilk tek sayılı adres, yönlendirici arayüzüne atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="cf612-144">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="cf612-145">Azure, sonraki çift numaralı adresi Azure yönlendirici arabirimine yapılandıracak.</span><span class="sxs-lookup"><span data-stu-id="cf612-145">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="cf612-146">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="cf612-146">-SharedKey</span></span>
<span data-ttu-id="cf612-147">Bu, eşleme yapılandırması için önceden paylaşılan anahtar olarak kullanılan isteğe bağlı bir MD5 karmasıdır.</span><span class="sxs-lookup"><span data-stu-id="cf612-147">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="cf612-148">-Vlanıd</span><span class="sxs-lookup"><span data-stu-id="cf612-148">-VlanId</span></span>
<span data-ttu-id="cf612-149">Bu, bu eşleme için atanan VLAN 'ın kimlik numarasıdır.</span><span class="sxs-lookup"><span data-stu-id="cf612-149">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="cf612-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="cf612-150">-Confirm</span></span>
<span data-ttu-id="cf612-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cf612-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf612-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf612-152">-WhatIf</span></span>
<span data-ttu-id="cf612-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf612-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf612-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cf612-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf612-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf612-155">CommonParameters</span></span>
<span data-ttu-id="cf612-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf612-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf612-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf612-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf612-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf612-158">INPUTS</span></span>

### <span data-ttu-id="cf612-159">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="cf612-159">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="cf612-160">' ExpressRouteCrossConnection ' parametresi ardışık düzenin ' PSExpressRouteCrossConnection ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="cf612-160">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="cf612-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf612-161">OUTPUTS</span></span>

### <span data-ttu-id="cf612-162">Microsoft. Azure. Commands. Network. model. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="cf612-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="cf612-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf612-163">NOTES</span></span>

## <span data-ttu-id="cf612-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf612-164">RELATED LINKS</span></span>

[<span data-ttu-id="cf612-165">Get-azexpressroutecrossconnectioneşleme</span><span class="sxs-lookup"><span data-stu-id="cf612-165">Get-AzExpressRouteCrossConnectionPeering</span></span>](Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="cf612-166">Remove-azexpressroutecrossconnectioneşleme</span><span class="sxs-lookup"><span data-stu-id="cf612-166">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="cf612-167">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="cf612-167">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="cf612-168">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="cf612-168">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
