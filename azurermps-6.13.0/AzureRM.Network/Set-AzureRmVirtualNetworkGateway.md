---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 1884dd461c0433c4f6a68bf906f56653ca960e27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591933"
---
# <span data-ttu-id="c0aa4-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c0aa4-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="c0aa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="c0aa4-103">Sanal ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0aa4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0aa4-104">SYNTAX</span></span>

### <span data-ttu-id="c0aa4-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c0aa4-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0aa4-106">Radiusserveryapılandırması</span><span class="sxs-lookup"><span data-stu-id="c0aa4-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0aa4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0aa4-107">DESCRIPTION</span></span>
<span data-ttu-id="c0aa4-108">**Set-AzureRmVirtualNetworkGateway** cmdlet 'i sanal ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="c0aa4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0aa4-109">EXAMPLES</span></span>

### <span data-ttu-id="c0aa4-110">Örnek 1: hedef durumunu ayarlama sanal ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="c0aa4-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="c0aa4-111">İlk komut, Gateway01 adlı bir sanal ağ ağ geçidini kaynak grubuna ait ResourceGroup001 alır ve bu değişkeni $Gateway ikinci komut değişken $Gateway</span><span class="sxs-lookup"><span data-stu-id="c0aa4-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="c0aa4-112">Komut ayrıca ASN 'yi 1337 'e ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-112">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="c0aa4-113">Örnek 2: hedef durumunu ayarlama sanal ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="c0aa4-113">Example 2: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzureRmVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="c0aa4-114">İlk komut, Gateway01 adlı bir sanal ağ ağ geçidini kaynak grubuna ait ResourceGroup001 alır ve bu değeri $Gateway ikinci komut, belirtilen IPSec parametreleri için VPN IPSec ilke nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="c0aa4-115">Üçüncü komut, değişken $Gateway depolanan sanal ağ geçidi için hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-115">The third command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="c0aa4-116">Komut ayrıca sanal ağ geçidinde $vpnclientipsecpolicy nesnesinde belirtilen özel VPN IPSec ilkesini de ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-116">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

## <span data-ttu-id="c0aa4-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0aa4-117">PARAMETERS</span></span>

### <span data-ttu-id="c0aa4-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="c0aa4-118">-AsJob</span></span>
<span data-ttu-id="c0aa4-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c0aa4-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0aa4-120">-ASN</span><span class="sxs-lookup"><span data-stu-id="c0aa4-120">-Asn</span></span>
<span data-ttu-id="c0aa4-121">IPSec tünellerinin içindeki Sınır Ağ Geçidi Protokolü (BGP) oturumlarını ayarlamak için kullanılan sanal ağ geçidi otonom sistem numarasını (ASN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-121">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0aa4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0aa4-122">-DefaultProfile</span></span>
<span data-ttu-id="c0aa4-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0aa4-124">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="c0aa4-124">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="c0aa4-125">Etkin özelliği devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-125">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="c0aa4-126">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="c0aa4-126">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="c0aa4-127">Etkin özelliği etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-127">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="c0aa4-128">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="c0aa4-128">-GatewayDefaultSite</span></span>
<span data-ttu-id="c0aa4-129">Zorla tünel için kullanılacak varsayılan siteyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-129">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="c0aa4-130">Varsayılan bir site belirtilmişse, ağ geçidinin sanal özel ağından (VPN) tüm internet trafiği bu siteye yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-130">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0aa4-131">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="c0aa4-131">-GatewaySku</span></span>
<span data-ttu-id="c0aa4-132">Sanal ağ geçidi 'nin hisse senedi birimini (SKU) belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-132">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="c0aa4-133">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c0aa4-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c0aa4-134">Ana</span><span class="sxs-lookup"><span data-stu-id="c0aa4-134">Basic</span></span>
- <span data-ttu-id="c0aa4-135">Ardından</span><span class="sxs-lookup"><span data-stu-id="c0aa4-135">Standard</span></span>
- <span data-ttu-id="c0aa4-136">Üst performans</span><span class="sxs-lookup"><span data-stu-id="c0aa4-136">HighPerformance</span></span>
- <span data-ttu-id="c0aa4-137">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="c0aa4-137">VpnGw1</span></span>
- <span data-ttu-id="c0aa4-138">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="c0aa4-138">VpnGw2</span></span>
- <span data-ttu-id="c0aa4-139">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="c0aa4-139">VpnGw3</span></span>
- <span data-ttu-id="c0aa4-140">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="c0aa4-140">VpnGw1AZ</span></span>
- <span data-ttu-id="c0aa4-141">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="c0aa4-141">VpnGw2AZ</span></span>
- <span data-ttu-id="c0aa4-142">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="c0aa4-142">VpnGw3AZ</span></span>
- <span data-ttu-id="c0aa4-143">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="c0aa4-143">ErGw1AZ</span></span>
- <span data-ttu-id="c0aa4-144">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="c0aa4-144">ErGw2AZ</span></span>
- <span data-ttu-id="c0aa4-145">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="c0aa4-145">ErGw3AZ</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0aa4-146">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="c0aa4-146">-PeerWeight</span></span>
<span data-ttu-id="c0aa4-147">Bu sanal ağ ağ geçidinden BGP üzerinden öğrenilen yollara eklenecek ağırlığı belirtir</span><span class="sxs-lookup"><span data-stu-id="c0aa4-147">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0aa4-148">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="c0aa4-148">-RadiusServerAddress</span></span>
<span data-ttu-id="c0aa4-149">P2S dış RADIUS sunucusu adresi.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-149">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0aa4-150">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="c0aa4-150">-RadiusServerSecret</span></span>
<span data-ttu-id="c0aa4-151">Dış RADIUS sunucusu gizliliğini P2S.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-151">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0aa4-152">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c0aa4-152">-VirtualNetworkGateway</span></span>
<span data-ttu-id="c0aa4-153">Değişikliklerin temel aldığı sanal ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-153">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="c0aa4-154">Sanal ağ geçidi nesnesini almak için Get-AzureRmVirtualNetworkGateway cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-154">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0aa4-155">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="c0aa4-155">-VpnClientAddressPool</span></span>
<span data-ttu-id="c0aa4-156">Bu cmdlet 'in VPN istemci IP adreslerini ayırmak için kullandığı adres alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-156">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="c0aa4-157">Bu, sanal ağ veya şirket içi aralıklardaki çakışmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-157">This should not overlap with virtual network or on-premise ranges.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0aa4-158">-Vpnclientıpsecpolicy</span><span class="sxs-lookup"><span data-stu-id="c0aa4-158">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="c0aa4-159">P2S VPN istemcisi tünel protokollerinin IPSec ilkelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-159">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0aa4-160">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="c0aa4-160">-VpnClientProtocol</span></span>
<span data-ttu-id="c0aa4-161">P2S VPN istemci tünel protokollerinin listesi</span><span class="sxs-lookup"><span data-stu-id="c0aa4-161">A list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0aa4-162">-Vpnclientiptal sertifikaları</span><span class="sxs-lookup"><span data-stu-id="c0aa4-162">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="c0aa4-163">İptal edilen VPN istemci sertifikalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-163">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="c0aa4-164">Bunlardan biriyle eşleşen bir sertifika sunan VPN istemcisi kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-164">A VPN client presenting a certificate that matches one of these is removed.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0aa4-165">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="c0aa4-165">-VpnClientRootCertificates</span></span>
<span data-ttu-id="c0aa4-166">VPN istemci kimlik doğrulaması için kullanılacak VPN istemcisi kök sertifikalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-166">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="c0aa4-167">VPN istemcilerinin bağlanması, bu kök sertifikalardan birinden üretilmiş sertifikaları sunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-167">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0aa4-168">-Onay</span><span class="sxs-lookup"><span data-stu-id="c0aa4-168">-Confirm</span></span>
<span data-ttu-id="c0aa4-169">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0aa4-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0aa4-170">-WhatIf</span></span>
<span data-ttu-id="c0aa4-171">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0aa4-172">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0aa4-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0aa4-173">CommonParameters</span></span>
<span data-ttu-id="c0aa4-174">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0aa4-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0aa4-175">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0aa4-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0aa4-176">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0aa4-176">INPUTS</span></span>

### <span data-ttu-id="c0aa4-177">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c0aa4-177">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="c0aa4-178">Parametreler: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c0aa4-178">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="c0aa4-179">System. String</span><span class="sxs-lookup"><span data-stu-id="c0aa4-179">System.String</span></span>

### <span data-ttu-id="c0aa4-180">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c0aa4-180">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="c0aa4-181">System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c0aa4-181">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="c0aa4-182">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSVpnClientRootCertificate, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c0aa4-182">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c0aa4-183">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. Psvpnclientınneutral, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c0aa4-183">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c0aa4-184">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSIpsecPolicy, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c0aa4-184">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c0aa4-185">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="c0aa4-185">System.UInt32</span></span>

### <span data-ttu-id="c0aa4-186">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c0aa4-186">System.Int32</span></span>

### <span data-ttu-id="c0aa4-187">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="c0aa4-187">System.Security.SecureString</span></span>

## <span data-ttu-id="c0aa4-188">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0aa4-188">OUTPUTS</span></span>

### <span data-ttu-id="c0aa4-189">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c0aa4-189">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="c0aa4-190">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0aa4-190">NOTES</span></span>
* <span data-ttu-id="c0aa4-191">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="c0aa4-191">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c0aa4-192">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0aa4-192">RELATED LINKS</span></span>

[<span data-ttu-id="c0aa4-193">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c0aa4-193">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="c0aa4-194">Yeni-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c0aa4-194">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="c0aa4-195">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c0aa4-195">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="c0aa4-196">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c0aa4-196">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="c0aa4-197">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c0aa4-197">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


