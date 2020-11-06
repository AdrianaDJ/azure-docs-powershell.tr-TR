---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 41c94d0dd8401399f360af89f1744cc10e900e1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590718"
---
# <span data-ttu-id="1ab49-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ab49-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="1ab49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ab49-102">SYNOPSIS</span></span>
<span data-ttu-id="1ab49-103">Sanal ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1ab49-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ab49-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ab49-104">SYNTAX</span></span>

### <span data-ttu-id="1ab49-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1ab49-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ab49-106">Radiusserveryapılandırması</span><span class="sxs-lookup"><span data-stu-id="1ab49-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ab49-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ab49-107">DESCRIPTION</span></span>
<span data-ttu-id="1ab49-108">**Set-AzureRmVirtualNetworkGateway** cmdlet 'i sanal ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1ab49-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="1ab49-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ab49-109">EXAMPLES</span></span>

### <span data-ttu-id="1ab49-110">Örnek 1: hedef durumunu ayarlama sanal ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="1ab49-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="1ab49-111">İlk komut, Gateway01 adında, kaynak grubuna ait bir sanal ağ geçidi alır ve $Gateway adlı değişkeni depolar</span><span class="sxs-lookup"><span data-stu-id="1ab49-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway</span></span>

<span data-ttu-id="1ab49-112">İkinci komut, $Gateway değişkeninde depolanan sanal ağ geçidinin hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1ab49-112">The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="1ab49-113">Komut ayrıca ASN 'yi 1337 'e ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1ab49-113">The command also sets the ASN to 1337.</span></span>

## <span data-ttu-id="1ab49-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ab49-114">PARAMETERS</span></span>

### <span data-ttu-id="1ab49-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="1ab49-115">-Asn</span></span>
<span data-ttu-id="1ab49-116">IPSec tünellerinin içindeki Sınır Ağ Geçidi Protokolü (BGP) oturumlarını ayarlamak için kullanılan sanal ağ geçidi otonom sistem numarasını (ASN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ab49-116">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="1ab49-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ab49-117">-DefaultProfile</span></span>
<span data-ttu-id="1ab49-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1ab49-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="1ab49-119">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="1ab49-119">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="1ab49-120">Etkin özelliği devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="1ab49-120">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="1ab49-121">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="1ab49-121">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="1ab49-122">Etkin özelliği etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="1ab49-122">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="1ab49-123">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="1ab49-123">-GatewayDefaultSite</span></span>
<span data-ttu-id="1ab49-124">Zorla tünel için kullanılacak varsayılan siteyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ab49-124">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="1ab49-125">Varsayılan bir site belirtilmişse, ağ geçidinin sanal özel ağından (VPN) tüm internet trafiği bu siteye yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="1ab49-125">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="1ab49-126">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="1ab49-126">-GatewaySku</span></span>
<span data-ttu-id="1ab49-127">Sanal ağ geçidi 'nin hisse senedi birimini (SKU) belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ab49-127">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="1ab49-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1ab49-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1ab49-129">Ana</span><span class="sxs-lookup"><span data-stu-id="1ab49-129">Basic</span></span>
- <span data-ttu-id="1ab49-130">Ardından</span><span class="sxs-lookup"><span data-stu-id="1ab49-130">Standard</span></span>
- <span data-ttu-id="1ab49-131">Üst performans</span><span class="sxs-lookup"><span data-stu-id="1ab49-131">HighPerformance</span></span>
- <span data-ttu-id="1ab49-132">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="1ab49-132">VpnGw1</span></span>
- <span data-ttu-id="1ab49-133">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="1ab49-133">VpnGw2</span></span>
- <span data-ttu-id="1ab49-134">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="1ab49-134">VpnGw3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ab49-135">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="1ab49-135">-PeerWeight</span></span>
<span data-ttu-id="1ab49-136">Bu sanal ağ ağ geçidinden BGP üzerinden öğrenilen yollara eklenecek ağırlığı belirtir</span><span class="sxs-lookup"><span data-stu-id="1ab49-136">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="1ab49-137">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="1ab49-137">-RadiusServerAddress</span></span>
<span data-ttu-id="1ab49-138">P2S dış RADIUS sunucusu adresi.</span><span class="sxs-lookup"><span data-stu-id="1ab49-138">P2S External Radius server address.</span></span>
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

### <span data-ttu-id="1ab49-139">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="1ab49-139">-RadiusServerSecret</span></span>
<span data-ttu-id="1ab49-140">Dış RADIUS sunucusu gizliliğini P2S.</span><span class="sxs-lookup"><span data-stu-id="1ab49-140">P2S External Radius server secret.</span></span>
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

### <span data-ttu-id="1ab49-141">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ab49-141">-VirtualNetworkGateway</span></span>
<span data-ttu-id="1ab49-142">Değişikliklerin temel aldığı sanal ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ab49-142">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="1ab49-143">Sanal ağ geçidi nesnesini almak için Get-AzureRmVirtualNetworkGateway cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ab49-143">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="1ab49-144">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="1ab49-144">-VpnClientAddressPool</span></span>
<span data-ttu-id="1ab49-145">Bu cmdlet 'in VPN istemci IP adreslerini ayırmak için kullandığı adres alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ab49-145">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="1ab49-146">Bu, sanal ağ veya şirket içi aralıklardaki çakışmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="1ab49-146">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="1ab49-147">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="1ab49-147">-VpnClientProtocol</span></span>
<span data-ttu-id="1ab49-148">P2S VPN istemci tünel protokollerinin listesi</span><span class="sxs-lookup"><span data-stu-id="1ab49-148">A list of P2S VPN client tunneling protocols</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: SSTP, IkeV2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ab49-149">-Vpnclientiptal sertifikaları</span><span class="sxs-lookup"><span data-stu-id="1ab49-149">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="1ab49-150">İptal edilen VPN istemci sertifikalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ab49-150">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="1ab49-151">Bunlardan biriyle eşleşen bir sertifika sunan VPN istemcisi kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="1ab49-151">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="1ab49-152">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="1ab49-152">-VpnClientRootCertificates</span></span>
<span data-ttu-id="1ab49-153">VPN istemci kimlik doğrulaması için kullanılacak VPN istemcisi kök sertifikalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ab49-153">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="1ab49-154">VPN istemcilerinin bağlanması, bu kök sertifikalardan birinden üretilmiş sertifikaları sunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1ab49-154">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="1ab49-155">-Onay</span><span class="sxs-lookup"><span data-stu-id="1ab49-155">-Confirm</span></span>
<span data-ttu-id="1ab49-156">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1ab49-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ab49-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ab49-157">-WhatIf</span></span>
<span data-ttu-id="1ab49-158">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ab49-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ab49-159">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1ab49-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ab49-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ab49-160">CommonParameters</span></span>
<span data-ttu-id="1ab49-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ab49-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ab49-162">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ab49-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ab49-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ab49-163">INPUTS</span></span>

### <span data-ttu-id="1ab49-164">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ab49-164">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="1ab49-165">' VirtualNetworkGateway ' parametresi ardışık düzenin ' PSVirtualNetworkGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1ab49-165">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="1ab49-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ab49-166">OUTPUTS</span></span>

### <span data-ttu-id="1ab49-167">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ab49-167">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="1ab49-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ab49-168">NOTES</span></span>
* <span data-ttu-id="1ab49-169">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="1ab49-169">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1ab49-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ab49-170">RELATED LINKS</span></span>

[<span data-ttu-id="1ab49-171">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ab49-171">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="1ab49-172">Yeni-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ab49-172">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="1ab49-173">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ab49-173">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="1ab49-174">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ab49-174">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="1ab49-175">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ab49-175">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


