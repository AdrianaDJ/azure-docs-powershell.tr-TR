---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 013da22d02f091d49e9780585bb8648c9c895ad7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588872"
---
# <span data-ttu-id="bf3df-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bf3df-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="bf3df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf3df-102">SYNOPSIS</span></span>
<span data-ttu-id="bf3df-103">Sanal ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="bf3df-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf3df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf3df-104">SYNTAX</span></span>

### <span data-ttu-id="bf3df-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bf3df-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf3df-106">Radiusserveryapılandırması</span><span class="sxs-lookup"><span data-stu-id="bf3df-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf3df-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf3df-107">DESCRIPTION</span></span>
<span data-ttu-id="bf3df-108">**Set-AzureRmVirtualNetworkGateway** cmdlet 'i sanal ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="bf3df-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="bf3df-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf3df-109">EXAMPLES</span></span>

### <span data-ttu-id="bf3df-110">Örnek 1: hedef durumunu ayarlama sanal ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="bf3df-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="bf3df-111">İlk komut, Gateway01 adında, kaynak grubuna ait bir sanal ağ geçidi alır ve $Gateway adlı değişkeni depolar</span><span class="sxs-lookup"><span data-stu-id="bf3df-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway</span></span>

<span data-ttu-id="bf3df-112">İkinci komut, $Gateway değişkeninde depolanan sanal ağ geçidinin hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="bf3df-112">The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="bf3df-113">Komut ayrıca ASN 'yi 1337 'e ayarlar.</span><span class="sxs-lookup"><span data-stu-id="bf3df-113">The command also sets the ASN to 1337.</span></span>

## <span data-ttu-id="bf3df-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf3df-114">PARAMETERS</span></span>

### <span data-ttu-id="bf3df-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="bf3df-115">-AsJob</span></span>
<span data-ttu-id="bf3df-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="bf3df-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf3df-117">-ASN</span><span class="sxs-lookup"><span data-stu-id="bf3df-117">-Asn</span></span>
<span data-ttu-id="bf3df-118">IPSec tünellerinin içindeki Sınır Ağ Geçidi Protokolü (BGP) oturumlarını ayarlamak için kullanılan sanal ağ geçidi otonom sistem numarasını (ASN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf3df-118">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3df-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf3df-119">-DefaultProfile</span></span>
<span data-ttu-id="bf3df-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bf3df-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="bf3df-121">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="bf3df-121">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="bf3df-122">Etkin özelliği devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="bf3df-122">Disables the active-active feature.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf3df-123">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="bf3df-123">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="bf3df-124">Etkin özelliği etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="bf3df-124">Enables the active-active feature.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf3df-125">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="bf3df-125">-GatewayDefaultSite</span></span>
<span data-ttu-id="bf3df-126">Zorla tünel için kullanılacak varsayılan siteyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf3df-126">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="bf3df-127">Varsayılan bir site belirtilmişse, ağ geçidinin sanal özel ağından (VPN) tüm internet trafiği bu siteye yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="bf3df-127">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3df-128">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="bf3df-128">-GatewaySku</span></span>
<span data-ttu-id="bf3df-129">Sanal ağ geçidi 'nin hisse senedi birimini (SKU) belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf3df-129">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="bf3df-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bf3df-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bf3df-131">Ana</span><span class="sxs-lookup"><span data-stu-id="bf3df-131">Basic</span></span>
- <span data-ttu-id="bf3df-132">Ardından</span><span class="sxs-lookup"><span data-stu-id="bf3df-132">Standard</span></span>
- <span data-ttu-id="bf3df-133">Üst performans</span><span class="sxs-lookup"><span data-stu-id="bf3df-133">HighPerformance</span></span>
- <span data-ttu-id="bf3df-134">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="bf3df-134">VpnGw1</span></span>
- <span data-ttu-id="bf3df-135">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="bf3df-135">VpnGw2</span></span>
- <span data-ttu-id="bf3df-136">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="bf3df-136">VpnGw3</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3df-137">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="bf3df-137">-PeerWeight</span></span>
<span data-ttu-id="bf3df-138">Bu sanal ağ ağ geçidinden BGP üzerinden öğrenilen yollara eklenecek ağırlığı belirtir</span><span class="sxs-lookup"><span data-stu-id="bf3df-138">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3df-139">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="bf3df-139">-RadiusServerAddress</span></span>
<span data-ttu-id="bf3df-140">P2S dış RADIUS sunucusu adresi.</span><span class="sxs-lookup"><span data-stu-id="bf3df-140">P2S External Radius server address.</span></span>
```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3df-141">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="bf3df-141">-RadiusServerSecret</span></span>
<span data-ttu-id="bf3df-142">Dış RADIUS sunucusu gizliliğini P2S.</span><span class="sxs-lookup"><span data-stu-id="bf3df-142">P2S External Radius server secret.</span></span>
```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3df-143">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bf3df-143">-VirtualNetworkGateway</span></span>
<span data-ttu-id="bf3df-144">Değişikliklerin temel aldığı sanal ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf3df-144">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="bf3df-145">Sanal ağ geçidi nesnesini almak için Get-AzureRmVirtualNetworkGateway cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bf3df-145">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3df-146">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="bf3df-146">-VpnClientAddressPool</span></span>
<span data-ttu-id="bf3df-147">Bu cmdlet 'in VPN istemci IP adreslerini ayırmak için kullandığı adres alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf3df-147">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="bf3df-148">Bu, sanal ağ veya şirket içi aralıklardaki çakışmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="bf3df-148">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="bf3df-149">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="bf3df-149">-VpnClientProtocol</span></span>
<span data-ttu-id="bf3df-150">P2S VPN istemci tünel protokollerinin listesi</span><span class="sxs-lookup"><span data-stu-id="bf3df-150">A list of P2S VPN client tunneling protocols</span></span>
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

### <span data-ttu-id="bf3df-151">-Vpnclientiptal sertifikaları</span><span class="sxs-lookup"><span data-stu-id="bf3df-151">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="bf3df-152">İptal edilen VPN istemci sertifikalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf3df-152">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="bf3df-153">Bunlardan biriyle eşleşen bir sertifika sunan VPN istemcisi kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="bf3df-153">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="bf3df-154">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="bf3df-154">-VpnClientRootCertificates</span></span>
<span data-ttu-id="bf3df-155">VPN istemci kimlik doğrulaması için kullanılacak VPN istemcisi kök sertifikalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf3df-155">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="bf3df-156">VPN istemcilerinin bağlanması, bu kök sertifikalardan birinden üretilmiş sertifikaları sunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bf3df-156">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="bf3df-157">-Onay</span><span class="sxs-lookup"><span data-stu-id="bf3df-157">-Confirm</span></span>
<span data-ttu-id="bf3df-158">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bf3df-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf3df-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf3df-159">-WhatIf</span></span>
<span data-ttu-id="bf3df-160">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bf3df-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf3df-161">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bf3df-161">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf3df-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf3df-162">CommonParameters</span></span>
<span data-ttu-id="bf3df-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf3df-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf3df-164">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf3df-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf3df-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf3df-165">INPUTS</span></span>

### <span data-ttu-id="bf3df-166">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bf3df-166">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="bf3df-167">' VirtualNetworkGateway ' parametresi ardışık düzenin ' PSVirtualNetworkGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="bf3df-167">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="bf3df-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf3df-168">OUTPUTS</span></span>

### <span data-ttu-id="bf3df-169">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bf3df-169">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="bf3df-170">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf3df-170">NOTES</span></span>
* <span data-ttu-id="bf3df-171">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="bf3df-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bf3df-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf3df-172">RELATED LINKS</span></span>

[<span data-ttu-id="bf3df-173">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bf3df-173">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="bf3df-174">Yeni-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bf3df-174">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="bf3df-175">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bf3df-175">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="bf3df-176">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bf3df-176">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="bf3df-177">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bf3df-177">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


