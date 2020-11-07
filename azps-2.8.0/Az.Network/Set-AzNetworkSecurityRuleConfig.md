---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 4293f044a270a43f12c7b4d74a410a324d0284dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917880"
---
# <span data-ttu-id="84313-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="84313-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="84313-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84313-102">SYNOPSIS</span></span>
<span data-ttu-id="84313-103">Ağ güvenlik grubu için ağ güvenliği kuralı yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="84313-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="84313-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="84313-104">SYNTAX</span></span>

### <span data-ttu-id="84313-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="84313-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84313-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="84313-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84313-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="84313-107">DESCRIPTION</span></span>
<span data-ttu-id="84313-108">**Set-Azağsecurityruleconfig** cmdlet 'i, ağ güvenlik grubu için bir ağ güvenliği kuralı yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="84313-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="84313-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="84313-109">EXAMPLES</span></span>

### <span data-ttu-id="84313-110">Örnek 1: ağ güvenlik kuralında erişim yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="84313-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="84313-111">İlk komut NSG-ön uç adlı ağ güvenlik grubunu alır ve bunu değişken $nsg depolar.</span><span class="sxs-lookup"><span data-stu-id="84313-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="84313-112">İkinci komut, RDP kuralı adlı güvenlik kuralı yapılandırmasını alan ve Get-AzNetworkSecurityRuleConfig öğesine $nsg güvenlik grubuna geçirmek için ardışık düzen işlecini kullanır.</span><span class="sxs-lookup"><span data-stu-id="84313-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="84313-113">Üçüncü komut, RDP kuralının erişim yapılandırmasını reddedecek şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="84313-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="84313-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="84313-114">PARAMETERS</span></span>

### <span data-ttu-id="84313-115">-Access</span><span class="sxs-lookup"><span data-stu-id="84313-115">-Access</span></span>
<span data-ttu-id="84313-116">Ağ trafiğine izin verilip verilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="84313-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="84313-117">Bu parametre için kabul edilebilir değerler: Izin ver ve Reddet.</span><span class="sxs-lookup"><span data-stu-id="84313-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84313-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84313-118">-DefaultProfile</span></span>
<span data-ttu-id="84313-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="84313-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84313-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="84313-120">-Description</span></span>
<span data-ttu-id="84313-121">Kural yapılandırmasının açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="84313-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="84313-122">Boyut üst sınırı 140 karakterdir.</span><span class="sxs-lookup"><span data-stu-id="84313-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="84313-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="84313-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="84313-124">Hedef adres önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="84313-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="84313-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="84313-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="84313-126">Sınıfsız Etki alanları arası yönlendirme (CıDR) adresi</span><span class="sxs-lookup"><span data-stu-id="84313-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="84313-127">Hedef IP adresi aralığı</span><span class="sxs-lookup"><span data-stu-id="84313-127">A destination IP address range</span></span> 
- <span data-ttu-id="84313-128">Herhangi bir IP adresiyle eşleşen bir joker karakter (\*), VirtualNetwork, AzureLoadBalancer ve Internet gibi etiketleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="84313-128">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="84313-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="84313-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="84313-130">Kural için hedef olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="84313-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="84313-131">' DestinationAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="84313-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84313-132">-Destinationapplicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="84313-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="84313-133">Kural için hedef olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="84313-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="84313-134">' DestinationAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="84313-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84313-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="84313-135">-DestinationPortRange</span></span>
<span data-ttu-id="84313-136">Hedef bir bağlantı noktası veya aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="84313-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="84313-137">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="84313-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="84313-138">Bir tamsayı</span><span class="sxs-lookup"><span data-stu-id="84313-138">An integer</span></span> 
- <span data-ttu-id="84313-139">0 ile 65535 arasında bir tamsayı aralığı</span><span class="sxs-lookup"><span data-stu-id="84313-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="84313-140">Herhangi bir bağlantı noktası ile eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="84313-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="84313-141">-Yön</span><span class="sxs-lookup"><span data-stu-id="84313-141">-Direction</span></span>
<span data-ttu-id="84313-142">Kuralın gelen veya giden trafik için değerlendirilip değerlendirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="84313-142">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="84313-143">Bu parametre için kabul edilebilir değerler: gelen ve giden.</span><span class="sxs-lookup"><span data-stu-id="84313-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84313-144">-Ad</span><span class="sxs-lookup"><span data-stu-id="84313-144">-Name</span></span>
<span data-ttu-id="84313-145">Bu cmdlet 'in ayarladığı ağ güvenlik kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="84313-145">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="84313-146">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="84313-146">-NetworkSecurityGroup</span></span>
<span data-ttu-id="84313-147">Ayarlanacak ağ güvenlik kuralı yapılandırmasını içeren **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="84313-147">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84313-148">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="84313-148">-Priority</span></span>
<span data-ttu-id="84313-149">Kural yapılandırmasının önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="84313-149">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="84313-150">Bu parametre için kabul edilebilir değerler şunlardır: 100 ile 4096 arasında bir tamsayı.</span><span class="sxs-lookup"><span data-stu-id="84313-150">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="84313-151">Öncelikteki her kural için öncelik numarası benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="84313-151">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="84313-152">Öncelik numarası düşükse, kuralın önceliği o kadar yüksek olur.</span><span class="sxs-lookup"><span data-stu-id="84313-152">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="84313-153">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="84313-153">-Protocol</span></span>
<span data-ttu-id="84313-154">Kural yapılandırmasının uygulandığı ağ protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="84313-154">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="84313-155">Bu parametre için kabul edilebilir değerler şunlardır:-TCP</span><span class="sxs-lookup"><span data-stu-id="84313-155">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="84313-156">UDP</span><span class="sxs-lookup"><span data-stu-id="84313-156">Udp</span></span>
- <span data-ttu-id="84313-157">Her ikisiyle eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="84313-157">A wildcard character (\*) to match both</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84313-158">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="84313-158">-SourceAddressPrefix</span></span>
<span data-ttu-id="84313-159">Kaynak adres önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="84313-159">Specifies a source address prefix.</span></span>
<span data-ttu-id="84313-160">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="84313-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="84313-161">CıDR</span><span class="sxs-lookup"><span data-stu-id="84313-161">A CIDR</span></span>
- <span data-ttu-id="84313-162">Kaynak IP aralığı</span><span class="sxs-lookup"><span data-stu-id="84313-162">A source IP range</span></span>
- <span data-ttu-id="84313-163">Herhangi bir IP adresiyle eşleşen bir joker karakter (\*), VirtualNetwork, AzureLoadBalancer ve Internet gibi etiketleri de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="84313-163">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="84313-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="84313-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="84313-165">Kural için kaynak olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="84313-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="84313-166">' SourceAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="84313-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84313-167">-Sourceapplicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="84313-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="84313-168">Kural için kaynak olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="84313-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="84313-169">' SourceAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="84313-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84313-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="84313-170">-SourcePortRange</span></span>
<span data-ttu-id="84313-171">Kaynak bağlantı noktasını veya aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="84313-171">Specifies the source port or range.</span></span>
<span data-ttu-id="84313-172">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="84313-172">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="84313-173">Bir tamsayı</span><span class="sxs-lookup"><span data-stu-id="84313-173">An integer</span></span>
- <span data-ttu-id="84313-174">0 ile 65535 arasında bir tamsayı aralığı</span><span class="sxs-lookup"><span data-stu-id="84313-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="84313-175">Herhangi bir bağlantı noktası ile eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="84313-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="84313-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84313-176">CommonParameters</span></span>
<span data-ttu-id="84313-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="84313-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84313-178">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84313-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84313-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="84313-179">INPUTS</span></span>

### <span data-ttu-id="84313-180">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="84313-180">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="84313-181">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="84313-181">OUTPUTS</span></span>

### <span data-ttu-id="84313-182">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="84313-182">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="84313-183">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="84313-183">NOTES</span></span>

## <span data-ttu-id="84313-184">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="84313-184">RELATED LINKS</span></span>

[<span data-ttu-id="84313-185">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="84313-185">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="84313-186">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="84313-186">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="84313-187">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="84313-187">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="84313-188">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="84313-188">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


