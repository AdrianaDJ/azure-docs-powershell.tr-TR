---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: a97379fb3cf59658c3f0822fc08fa65c0614021d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760245"
---
# <span data-ttu-id="9f5f6-101">New-AzVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="9f5f6-101">New-AzVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="9f5f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f5f6-102">SYNOPSIS</span></span>
<span data-ttu-id="9f5f6-103">Bu komut, kullanıcıların, VPN ağ geçidinde ayarlanan ıpsecencryption, ıpsecıntegrity, ıkeencryption, ıkeıntegrity, DhGroup gibi bir değer veya tüm değerleri belirten VPN IPSec ilkesi nesnesini oluşturmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="9f5f6-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="9f5f6-104">Bu komut, çıkış nesnesinin hem yeni, hem de mevcut ağ geçidi için VPN IPSec ilkesini ayarlamak üzere kullanılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="9f5f6-104">This command let output object is used to set vpn ipsec policy for both new / exisitng gateway.</span></span>

## <span data-ttu-id="9f5f6-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f5f6-105">SYNTAX</span></span>

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f5f6-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f5f6-106">DESCRIPTION</span></span>
<span data-ttu-id="9f5f6-107">Bu komut, kullanıcıların, VPN ağ geçidinde ayarlanan ıpsecencryption, ıpsecıntegrity, ıkeencryption, ıkeıntegrity, DhGroup gibi bir değer veya tüm değerleri belirten VPN IPSec ilkesi nesnesini oluşturmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="9f5f6-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="9f5f6-108">Bu komut, çıkış nesnesinin hem yeni, hem de mevcut ağ geçidi için VPN IPSec ilkesini ayarlamak üzere kullanılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="9f5f6-108">This command let output object is used to set vpn ipsec policy for both new / exisitng gateway.</span></span>

## <span data-ttu-id="9f5f6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f5f6-109">EXAMPLES</span></span>

### <span data-ttu-id="9f5f6-110">VPN IPSec ilkesi nesnesini tanımla:</span><span class="sxs-lookup"><span data-stu-id="9f5f6-110">Define vpn ipsec policy object:</span></span>
```
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="9f5f6-111">Bu cmdlet, geçen bir veya tüm parametrelerin parametre değerlerini kullanarak VPN IPSec ilkesi nesnesini oluşturmak için kullanılır: Set-AzVirtualNetworkGateway _Resourcegroup: VpnClientIpsecPolicy 'in PS komut 'si New-AzVirtualNetworkGateway komut 'si:</span><span class="sxs-lookup"><span data-stu-id="9f5f6-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzVirtualNetworkGateway (New VPN Gateway creation) / Set-AzVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="9f5f6-112">VPN özel IPSec ilkesini ayarlamak için yeni sanal ağ ağ geçidi oluşturma:</span><span class="sxs-lookup"><span data-stu-id="9f5f6-112">Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="9f5f6-113">Bu cmdlet, oluşturulduktan sonra sanal ağ geçidi nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="9f5f6-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="9f5f6-114">Mevcut sanal ağ ağ geçidinde VPN özel IPSec ilkesini ayarlama:</span><span class="sxs-lookup"><span data-stu-id="9f5f6-114">Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="9f5f6-115">Bu cmdlet, VPN özel IPSec ilkesini ayarladıktan sonra sanal ağ geçidi nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="9f5f6-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="9f5f6-116">VPN özel ilkesinin doğru ayarlanıp ayarlanmadıysa sanal ağ geçidi 'ni alın:</span><span class="sxs-lookup"><span data-stu-id="9f5f6-116">Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="9f5f6-117">Bu cmdlet sanal ağ geçidi nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="9f5f6-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="9f5f6-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f5f6-118">PARAMETERS</span></span>

### <span data-ttu-id="9f5f6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f5f6-119">-DefaultProfile</span></span>
<span data-ttu-id="9f5f6-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9f5f6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f5f6-121">-Dhgrup</span><span class="sxs-lookup"><span data-stu-id="9f5f6-121">-DhGroup</span></span>
<span data-ttu-id="9f5f6-122">İlk SA için ıKE Aşama 1 ' de kullanılan vpnclient DH grupları</span><span class="sxs-lookup"><span data-stu-id="9f5f6-122">The Vpnclient DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5f6-123">-Ikeencryption</span><span class="sxs-lookup"><span data-stu-id="9f5f6-123">-IkeEncryption</span></span>
<span data-ttu-id="9f5f6-124">Vpnclient ıKE şifreleme algoritması (ıKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="9f5f6-124">The Vpnclient IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5f6-125">-Ikeıntegrity</span><span class="sxs-lookup"><span data-stu-id="9f5f6-125">-IkeIntegrity</span></span>
<span data-ttu-id="9f5f6-126">Vpnclient ıKE bütünlük algoritması (ıKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="9f5f6-126">The Vpnclient IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5f6-127">-Ipsecencryption</span><span class="sxs-lookup"><span data-stu-id="9f5f6-127">-IpsecEncryption</span></span>
<span data-ttu-id="9f5f6-128">Vpnclient IPSec şifreleme algoritması (ıKE Aşama 1)</span><span class="sxs-lookup"><span data-stu-id="9f5f6-128">The Vpnclient IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5f6-129">-Ipsecıntegrity</span><span class="sxs-lookup"><span data-stu-id="9f5f6-129">-IpsecIntegrity</span></span>
<span data-ttu-id="9f5f6-130">Vpnclient IPSec bütünlük algoritması (ıKE Aşama 1)</span><span class="sxs-lookup"><span data-stu-id="9f5f6-130">The Vpnclient IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5f6-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="9f5f6-131">-PfsGroup</span></span>
<span data-ttu-id="9f5f6-132">Yeni alt SA için ıKE Phase 2 ' de kullanılan vpnclient PFS grupları</span><span class="sxs-lookup"><span data-stu-id="9f5f6-132">The Vpnclient PFS Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5f6-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="9f5f6-133">-SADataSize</span></span>
<span data-ttu-id="9f5f6-134">KB cinsinden vpnclient IPSec güvenlik Ilişkisi (hızlı mod veya Aşama 2 SA) yük boyutu</span><span class="sxs-lookup"><span data-stu-id="9f5f6-134">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="9f5f6-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="9f5f6-135">-SALifeTime</span></span>
<span data-ttu-id="9f5f6-136">Saniye cinsinden vpnclient IPSec güvenlik Ilişkisi (hızlı mod veya Aşama 2 SA) ömrü</span><span class="sxs-lookup"><span data-stu-id="9f5f6-136">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="9f5f6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f5f6-137">CommonParameters</span></span>
<span data-ttu-id="9f5f6-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f5f6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f5f6-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f5f6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f5f6-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f5f6-140">INPUTS</span></span>

### <span data-ttu-id="9f5f6-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9f5f6-141">None</span></span>

## <span data-ttu-id="9f5f6-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f5f6-142">OUTPUTS</span></span>

### <span data-ttu-id="9f5f6-143">Microsoft. Azure. Commands. Network. model. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="9f5f6-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="9f5f6-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f5f6-144">NOTES</span></span>

## <span data-ttu-id="9f5f6-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f5f6-145">RELATED LINKS</span></span>
