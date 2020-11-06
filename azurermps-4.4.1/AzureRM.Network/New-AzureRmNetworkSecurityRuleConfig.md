---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: e30a03f82d0bcf719ffc4dc5640e3fbf9b3bb99f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593064"
---
# <span data-ttu-id="8125f-101">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8125f-101">New-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="8125f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8125f-102">SYNOPSIS</span></span>
<span data-ttu-id="8125f-103">Ağ güvenlik kuralı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8125f-103">Creates a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8125f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8125f-104">SYNTAX</span></span>

### <span data-ttu-id="8125f-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8125f-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8125f-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="8125f-106">SetByResourceId</span></span>
```
New-AzureRmNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8125f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8125f-107">DESCRIPTION</span></span>
<span data-ttu-id="8125f-108">**Yeni-AzureRmNetworkSecurityRuleConfig** cmdlet 'i, bir ağ güvenlik grubu Için bir Azure ağ güvenlik kuralı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8125f-108">The **New-AzureRmNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="8125f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8125f-109">EXAMPLES</span></span>

### <span data-ttu-id="8125f-110">1: RDP 'ye izin veren ağ güvenlik kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="8125f-110">1: Create a network security rule to allow RDP</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="8125f-111">Bu komut Internet 'ten bağlantı noktası 3389 'e erişim izni veren bir güvenlik kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="8125f-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="8125f-112">2: HTTP 'ye izin veren ağ güvenlik kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="8125f-112">2: Create a network security rule that allows HTTP</span></span>
```
$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="8125f-113">Bu komut Internet 'ten bağlantı noktası 80 'e erişim izni veren bir güvenlik kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="8125f-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="8125f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8125f-114">PARAMETERS</span></span>

### <span data-ttu-id="8125f-115">-Access</span><span class="sxs-lookup"><span data-stu-id="8125f-115">-Access</span></span>
<span data-ttu-id="8125f-116">Ağ trafiğine izin verilip verilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8125f-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="8125f-117">Bu parametre için kabul edilebilir değerler: Izin ver ve Reddet.</span><span class="sxs-lookup"><span data-stu-id="8125f-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="8125f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8125f-118">-DefaultProfile</span></span>
<span data-ttu-id="8125f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8125f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8125f-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="8125f-120">-Description</span></span>
<span data-ttu-id="8125f-121">Oluşturulacak ağ güvenliği kuralı yapılandırmasının açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8125f-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="8125f-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8125f-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="8125f-123">Hedef adres önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8125f-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="8125f-124">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8125f-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8125f-125">Sınıfsız Etki alanları arası yönlendirme (CıDR) adresi</span><span class="sxs-lookup"><span data-stu-id="8125f-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="8125f-126">Hedef IP adresi aralığı</span><span class="sxs-lookup"><span data-stu-id="8125f-126">A destination IP address range</span></span> 
- <span data-ttu-id="8125f-127">Herhangi bir IP adresiyle eşleşen joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="8125f-127">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="8125f-128">VirtualNetwork, AzureLoadBalancer ve Internet gibi etiketleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8125f-128">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="8125f-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8125f-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="8125f-130">Kural için hedef olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="8125f-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="8125f-131">' DestinationAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="8125f-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8125f-132">-Destinationapplicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="8125f-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="8125f-133">Kural için hedef olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="8125f-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="8125f-134">' DestinationAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="8125f-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8125f-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="8125f-135">-DestinationPortRange</span></span>
<span data-ttu-id="8125f-136">Hedef bir bağlantı noktası veya aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8125f-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="8125f-137">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8125f-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8125f-138">Bir tamsayı</span><span class="sxs-lookup"><span data-stu-id="8125f-138">An integer</span></span>
- <span data-ttu-id="8125f-139">0 ile 65535 arasında bir tamsayı aralığı</span><span class="sxs-lookup"><span data-stu-id="8125f-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="8125f-140">Herhangi bir bağlantı noktası ile eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="8125f-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="8125f-141">-Yön</span><span class="sxs-lookup"><span data-stu-id="8125f-141">-Direction</span></span>
<span data-ttu-id="8125f-142">Kuralın gelen veya giden trafikte değerlendirilip değerlendirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8125f-142">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="8125f-143">Bu parametre için kabul edilebilir değerler: gelen ve giden.</span><span class="sxs-lookup"><span data-stu-id="8125f-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="8125f-144">-Ad</span><span class="sxs-lookup"><span data-stu-id="8125f-144">-Name</span></span>
<span data-ttu-id="8125f-145">Bu cmdlet 'in oluşturduğu ağ güvenlik kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8125f-145">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8125f-146">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="8125f-146">-Priority</span></span>
<span data-ttu-id="8125f-147">Kural yapılandırmasının önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8125f-147">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="8125f-148">Bu parametre için kabul edilebilir değerler şunlardır: 100 ile 4096 arasında bir tamsayı.</span><span class="sxs-lookup"><span data-stu-id="8125f-148">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="8125f-149">Öncelikteki her kural için öncelik numarası benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8125f-149">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="8125f-150">Öncelik numarası düşükse, kuralın önceliği o kadar yüksek olur.</span><span class="sxs-lookup"><span data-stu-id="8125f-150">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="8125f-151">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="8125f-151">-Protocol</span></span>
<span data-ttu-id="8125f-152">Yeni bir kural yapılandırmasının uygulandığı ağ protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8125f-152">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="8125f-153">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8125f-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8125f-154">TC</span><span class="sxs-lookup"><span data-stu-id="8125f-154">Tcp</span></span>
- <span data-ttu-id="8125f-155">UDP</span><span class="sxs-lookup"><span data-stu-id="8125f-155">Udp</span></span>
- <span data-ttu-id="8125f-156">joker karakter (\*) ile eşleşir.</span><span class="sxs-lookup"><span data-stu-id="8125f-156">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="8125f-157">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8125f-157">-SourceAddressPrefix</span></span>
<span data-ttu-id="8125f-158">Kaynak adres önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8125f-158">Specifies a source address prefix.</span></span>
<span data-ttu-id="8125f-159">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8125f-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8125f-160">CıDR</span><span class="sxs-lookup"><span data-stu-id="8125f-160">A CIDR</span></span>
- <span data-ttu-id="8125f-161">Kaynak IP aralığı</span><span class="sxs-lookup"><span data-stu-id="8125f-161">A source IP range</span></span>
- <span data-ttu-id="8125f-162">Herhangi bir IP adresiyle eşleşen joker karakter (\*).</span><span class="sxs-lookup"><span data-stu-id="8125f-162">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="8125f-163">VirtualNetwork, AzureLoadBalancer ve Internet gibi etiketleri de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8125f-163">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="8125f-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8125f-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="8125f-165">Kural için kaynak olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="8125f-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="8125f-166">' SourceAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="8125f-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8125f-167">-Sourceapplicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="8125f-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="8125f-168">Kural için kaynak olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="8125f-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="8125f-169">' SourceAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="8125f-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8125f-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="8125f-170">-SourcePortRange</span></span>
<span data-ttu-id="8125f-171">Kaynak bağlantı noktasını veya aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8125f-171">Specifies the source port or range.</span></span>
<span data-ttu-id="8125f-172">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8125f-172">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8125f-173">Bir tamsayı</span><span class="sxs-lookup"><span data-stu-id="8125f-173">An integer</span></span>
- <span data-ttu-id="8125f-174">0 ile 65535 arasında bir tamsayı aralığı</span><span class="sxs-lookup"><span data-stu-id="8125f-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="8125f-175">Herhangi bir bağlantı noktası ile eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="8125f-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="8125f-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8125f-176">CommonParameters</span></span>
<span data-ttu-id="8125f-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8125f-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8125f-178">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8125f-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8125f-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8125f-179">INPUTS</span></span>

## <span data-ttu-id="8125f-180">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8125f-180">OUTPUTS</span></span>

### <span data-ttu-id="8125f-181">Microsoft. Azure. Commands. Network. modeller. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="8125f-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="8125f-182">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8125f-182">NOTES</span></span>

## <span data-ttu-id="8125f-183">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8125f-183">RELATED LINKS</span></span>

[<span data-ttu-id="8125f-184">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8125f-184">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8125f-185">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8125f-185">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8125f-186">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8125f-186">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8125f-187">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8125f-187">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


