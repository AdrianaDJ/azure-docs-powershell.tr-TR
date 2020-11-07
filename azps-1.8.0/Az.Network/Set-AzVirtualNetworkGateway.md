---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 6576cedfa49d2ba2215d72b7f31ea85288f5cbda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759962"
---
# <span data-ttu-id="4a858-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4a858-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="4a858-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a858-102">SYNOPSIS</span></span>
<span data-ttu-id="4a858-103">Sanal ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4a858-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="4a858-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a858-104">SYNTAX</span></span>

### <span data-ttu-id="4a858-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4a858-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a858-106">Radiusserveryapılandırması</span><span class="sxs-lookup"><span data-stu-id="4a858-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a858-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a858-107">DESCRIPTION</span></span>
<span data-ttu-id="4a858-108">**Set-AzVirtualNetworkGateway** cmdlet 'i sanal ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4a858-108">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="4a858-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a858-109">EXAMPLES</span></span>

### <span data-ttu-id="4a858-110">Örnek 1: sanal ağ geçidinin ASN 'yi güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="4a858-110">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="4a858-111">İlk komut, Gateway01 adlı bir sanal ağ ağ geçidini kaynak grubuna ait ResourceGroup001 alır $Gateway ve ikinci komut $Gateway değişken bir şekilde depolanan sanal ağ ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4a858-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="4a858-112">Komut ayrıca ASN 'yi 1337 'e ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4a858-112">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="4a858-113">Örnek 2: sanal ağ ağ geçidine IPSec ilkesi ekleme</span><span class="sxs-lookup"><span data-stu-id="4a858-113">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="4a858-114">İlk komut, Gateway01 adlı bir sanal ağ ağ geçidini kaynak grubuna ait ResourceGroup001 alır ve bu değeri $Gateway ikinci komut, belirtilen IPSec parametreleri için VPN IPSec ilke nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4a858-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="4a858-115">Üçüncü komut, $Gateway değişkeninde depolanan sanal ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4a858-115">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="4a858-116">Komut ayrıca sanal ağ geçidinde $vpnclientipsecpolicy nesnesinde belirtilen özel VPN IPSec ilkesini de ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4a858-116">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

## <span data-ttu-id="4a858-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a858-117">PARAMETERS</span></span>

### <span data-ttu-id="4a858-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="4a858-118">-AsJob</span></span>
<span data-ttu-id="4a858-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4a858-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a858-120">-ASN</span><span class="sxs-lookup"><span data-stu-id="4a858-120">-Asn</span></span>
<span data-ttu-id="4a858-121">IPSec tünellerinin içindeki Sınır Ağ Geçidi Protokolü (BGP) oturumlarını ayarlamak için kullanılan sanal ağ geçidi otonom sistem numarasını (ASN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a858-121">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="4a858-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a858-122">-DefaultProfile</span></span>
<span data-ttu-id="4a858-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4a858-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a858-124">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="4a858-124">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="4a858-125">Etkin özelliği devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="4a858-125">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="4a858-126">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="4a858-126">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="4a858-127">Etkin özelliği etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="4a858-127">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="4a858-128">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="4a858-128">-GatewayDefaultSite</span></span>
<span data-ttu-id="4a858-129">Zorla tünel için kullanılacak varsayılan siteyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a858-129">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="4a858-130">Varsayılan bir site belirtilmişse, ağ geçidinin sanal özel ağından (VPN) tüm internet trafiği bu siteye yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="4a858-130">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="4a858-131">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="4a858-131">-GatewaySku</span></span>
<span data-ttu-id="4a858-132">Sanal ağ geçidi 'nin hisse senedi birimini (SKU) belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a858-132">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="4a858-133">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4a858-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4a858-134">Ana</span><span class="sxs-lookup"><span data-stu-id="4a858-134">Basic</span></span>
- <span data-ttu-id="4a858-135">Ardından</span><span class="sxs-lookup"><span data-stu-id="4a858-135">Standard</span></span>
- <span data-ttu-id="4a858-136">Üst performans</span><span class="sxs-lookup"><span data-stu-id="4a858-136">HighPerformance</span></span>
- <span data-ttu-id="4a858-137">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="4a858-137">VpnGw1</span></span>
- <span data-ttu-id="4a858-138">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="4a858-138">VpnGw2</span></span>
- <span data-ttu-id="4a858-139">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="4a858-139">VpnGw3</span></span>
- <span data-ttu-id="4a858-140">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="4a858-140">VpnGw1AZ</span></span>
- <span data-ttu-id="4a858-141">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="4a858-141">VpnGw2AZ</span></span>
- <span data-ttu-id="4a858-142">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="4a858-142">VpnGw3AZ</span></span>
- <span data-ttu-id="4a858-143">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="4a858-143">ErGw1AZ</span></span>
- <span data-ttu-id="4a858-144">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="4a858-144">ErGw2AZ</span></span>
- <span data-ttu-id="4a858-145">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="4a858-145">ErGw3AZ</span></span>

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

### <span data-ttu-id="4a858-146">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="4a858-146">-PeerWeight</span></span>
<span data-ttu-id="4a858-147">Bu sanal ağ ağ geçidinden BGP üzerinden öğrenilen yollara eklenecek ağırlığı belirtir</span><span class="sxs-lookup"><span data-stu-id="4a858-147">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="4a858-148">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="4a858-148">-RadiusServerAddress</span></span>
<span data-ttu-id="4a858-149">P2S dış RADIUS sunucusu adresi.</span><span class="sxs-lookup"><span data-stu-id="4a858-149">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="4a858-150">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="4a858-150">-RadiusServerSecret</span></span>
<span data-ttu-id="4a858-151">Dış RADIUS sunucusu gizliliğini P2S.</span><span class="sxs-lookup"><span data-stu-id="4a858-151">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="4a858-152">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4a858-152">-VirtualNetworkGateway</span></span>
<span data-ttu-id="4a858-153">Değişikliklerin temel aldığı sanal ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a858-153">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="4a858-154">Sanal ağ geçidi nesnesini almak için Get-AzVirtualNetworkGateway cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a858-154">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="4a858-155">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="4a858-155">-VpnClientAddressPool</span></span>
<span data-ttu-id="4a858-156">Bu cmdlet 'in VPN istemci IP adreslerini ayırmak için kullandığı adres alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a858-156">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="4a858-157">Bu, sanal ağ veya şirket içi aralıklardaki çakışmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="4a858-157">This should not overlap with virtual network or on-premise ranges.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a858-158">-Vpnclientıpsecpolicy</span><span class="sxs-lookup"><span data-stu-id="4a858-158">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="4a858-159">P2S VPN istemcisi tünel protokollerinin IPSec ilkelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="4a858-159">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a858-160">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="4a858-160">-VpnClientProtocol</span></span>
<span data-ttu-id="4a858-161">P2S VPN istemci tünel protokollerinin listesi</span><span class="sxs-lookup"><span data-stu-id="4a858-161">A list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a858-162">-Vpnclientiptal sertifikaları</span><span class="sxs-lookup"><span data-stu-id="4a858-162">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="4a858-163">İptal edilen VPN istemci sertifikalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a858-163">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="4a858-164">Bunlardan biriyle eşleşen bir sertifika sunan VPN istemcisi kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="4a858-164">A VPN client presenting a certificate that matches one of these is removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a858-165">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="4a858-165">-VpnClientRootCertificates</span></span>
<span data-ttu-id="4a858-166">VPN istemci kimlik doğrulaması için kullanılacak VPN istemcisi kök sertifikalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a858-166">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="4a858-167">VPN istemcilerinin bağlanması, bu kök sertifikalardan birinden üretilmiş sertifikaları sunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4a858-167">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a858-168">-Onay</span><span class="sxs-lookup"><span data-stu-id="4a858-168">-Confirm</span></span>
<span data-ttu-id="4a858-169">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4a858-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a858-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a858-170">-WhatIf</span></span>
<span data-ttu-id="4a858-171">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4a858-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a858-172">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4a858-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a858-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a858-173">CommonParameters</span></span>
<span data-ttu-id="4a858-174">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a858-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a858-175">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a858-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a858-176">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a858-176">INPUTS</span></span>

### <span data-ttu-id="4a858-177">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4a858-177">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="4a858-178">System. String</span><span class="sxs-lookup"><span data-stu-id="4a858-178">System.String</span></span>

### <span data-ttu-id="4a858-179">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4a858-179">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="4a858-180">System. String []</span><span class="sxs-lookup"><span data-stu-id="4a858-180">System.String[]</span></span>

### <span data-ttu-id="4a858-181">Microsoft. Azure. Commands. Network. model. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="4a858-181">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="4a858-182">Microsoft. Azure. Commands. Network. model. Psvpnclientiptal edilmiş sertifika []</span><span class="sxs-lookup"><span data-stu-id="4a858-182">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="4a858-183">Microsoft. Azure. Commands. Network. model. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="4a858-183">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="4a858-184">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="4a858-184">System.UInt32</span></span>

### <span data-ttu-id="4a858-185">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4a858-185">System.Int32</span></span>

### <span data-ttu-id="4a858-186">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="4a858-186">System.Security.SecureString</span></span>

## <span data-ttu-id="4a858-187">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a858-187">OUTPUTS</span></span>

### <span data-ttu-id="4a858-188">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4a858-188">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="4a858-189">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a858-189">NOTES</span></span>
* <span data-ttu-id="4a858-190">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="4a858-190">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4a858-191">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a858-191">RELATED LINKS</span></span>

[<span data-ttu-id="4a858-192">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4a858-192">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="4a858-193">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4a858-193">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="4a858-194">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4a858-194">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="4a858-195">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4a858-195">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="4a858-196">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4a858-196">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)
