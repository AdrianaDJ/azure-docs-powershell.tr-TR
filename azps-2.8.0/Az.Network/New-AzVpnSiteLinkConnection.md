---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelinkconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
ms.openlocfilehash: e62e697deec0d7e3894e7eaf787790f64d72641b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932323"
---
# <span data-ttu-id="ea7b9-101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="ea7b9-101">New-AzVpnSiteLinkConnection</span></span>

## <span data-ttu-id="ea7b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea7b9-102">SYNOPSIS</span></span>
<span data-ttu-id="ea7b9-103">Azure VpnSiteLinkConnection nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea7b9-103">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="ea7b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea7b9-104">SYNTAX</span></span>

```
New-AzVpnSiteLinkConnection -Name <String> -VpnSiteLink <PSVpnSiteLink> [-SharedKey <SecureString>]
 [-ConnectionBandwidth <UInt32>] [-RoutingWeight <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea7b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea7b9-105">DESCRIPTION</span></span>
<span data-ttu-id="ea7b9-106">Azure VpnSiteLinkConnection nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea7b9-106">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="ea7b9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea7b9-107">EXAMPLES</span></span>

### <span data-ttu-id="ea7b9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ea7b9-108">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)


PS C:\> $vpnSiteLinkConnection = New-AzVpnSiteLinkConnection -Name "testLinkConnection1" -VpnSiteLink $vpnSite.VpnSiteLinks[0] -ConnectionBandwidth 100

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -VpnSiteLinkConnection @($vpnSiteLinkConnection)
```

<span data-ttu-id="ea7b9-109">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'deki 1 VpnSiteLinks 'e sahip bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea7b9-109">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="ea7b9-110">Sanal hub 'da bir VPN ağ geçidi oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="ea7b9-110">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="ea7b9-111">Ağ Geçidi oluşturulduktan sonra, vpnsite için 1 VpnSiteLinkConnections ile New-AzVpnConnection komutu ile VpnSite 'e bağlanır.</span><span class="sxs-lookup"><span data-stu-id="ea7b9-111">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="ea7b9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea7b9-112">PARAMETERS</span></span>

### <span data-ttu-id="ea7b9-113">-ConnectionBandwidth</span><span class="sxs-lookup"><span data-stu-id="ea7b9-113">-ConnectionBandwidth</span></span>
<span data-ttu-id="ea7b9-114">Bu bağlantı tarafından, Mbps 'de işlenmesi gereken bant genişliği.</span><span class="sxs-lookup"><span data-stu-id="ea7b9-114">The bandwidth that needs to be handled by this link connection in mbps.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea7b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea7b9-115">-DefaultProfile</span></span>
<span data-ttu-id="ea7b9-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ea7b9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea7b9-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="ea7b9-117">-EnableBgp</span></span>
<span data-ttu-id="ea7b9-118">Bu bağlantı için BGP 'yi etkinleştir</span><span class="sxs-lookup"><span data-stu-id="ea7b9-118">Enable BGP for this link connection</span></span>

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

### <span data-ttu-id="ea7b9-119">-Ipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="ea7b9-119">-IpSecPolicy</span></span>
<span data-ttu-id="ea7b9-120">Bu bağlantı için değerlendirilecek IPSec Ilkesi.</span><span class="sxs-lookup"><span data-stu-id="ea7b9-120">IpSec Policy to be considered for this link connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea7b9-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="ea7b9-121">-Name</span></span>
<span data-ttu-id="ea7b9-122">Adlandır</span><span class="sxs-lookup"><span data-stu-id="ea7b9-122">Name</span></span>

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

### <span data-ttu-id="ea7b9-123">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="ea7b9-123">-RoutingWeight</span></span>
<span data-ttu-id="ea7b9-124">Üretim akışı ağırlığı</span><span class="sxs-lookup"><span data-stu-id="ea7b9-124">Routing Weight</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea7b9-125">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="ea7b9-125">-SharedKey</span></span>
<span data-ttu-id="ea7b9-126">Bu bağlantı bağlantısını ayarlamak için gereken paylaşılan anahtar.</span><span class="sxs-lookup"><span data-stu-id="ea7b9-126">The shared key required to set this link connection up.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea7b9-127">-Uselocalazureıpaddress</span><span class="sxs-lookup"><span data-stu-id="ea7b9-127">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="ea7b9-128">Bu bağlantı için kaynak IP olarak yerel Azure IP adresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ea7b9-128">Use local azure ip address as source ip for this link connection.</span></span>

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

### <span data-ttu-id="ea7b9-129">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="ea7b9-129">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="ea7b9-130">Bu bağlantı için ilkeye dayalı trafik seçicileri kullanın.</span><span class="sxs-lookup"><span data-stu-id="ea7b9-130">Use policy based traffic selectors for this link connection.</span></span>

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

### <span data-ttu-id="ea7b9-131">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="ea7b9-131">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="ea7b9-132">Ağ Geçidi bağlantı protokolü: IKEv1/Ikev2</span><span class="sxs-lookup"><span data-stu-id="ea7b9-132">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea7b9-133">-Vpnsite</span><span class="sxs-lookup"><span data-stu-id="ea7b9-133">-VpnSiteLink</span></span>
<span data-ttu-id="ea7b9-134">Bağlanılacak VPN sitesi bağlantı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ea7b9-134">The vpn site link object to connect to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea7b9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea7b9-135">CommonParameters</span></span>
<span data-ttu-id="ea7b9-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea7b9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea7b9-137">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ea7b9-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea7b9-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea7b9-138">INPUTS</span></span>

### <span data-ttu-id="ea7b9-139">Microsoft. Azure. Commands. Network. model. Psvpnsite</span><span class="sxs-lookup"><span data-stu-id="ea7b9-139">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="ea7b9-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea7b9-140">OUTPUTS</span></span>

### <span data-ttu-id="ea7b9-141">Microsoft. Azure. Commands. Network. model. PSVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="ea7b9-141">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span></span>

## <span data-ttu-id="ea7b9-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea7b9-142">NOTES</span></span>

## <span data-ttu-id="ea7b9-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea7b9-143">RELATED LINKS</span></span>

[<span data-ttu-id="ea7b9-144">Yeni-Azvpnbağlantısı</span><span class="sxs-lookup"><span data-stu-id="ea7b9-144">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)