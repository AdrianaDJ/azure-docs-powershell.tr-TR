---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 3e11b1ca7b83a4f01ce2d344874f4da02b399221
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760697"
---
# <span data-ttu-id="9fbe3-101">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9fbe3-101">Add-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="9fbe3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fbe3-102">SYNOPSIS</span></span>
<span data-ttu-id="9fbe3-103">Ağ güvenlik grubuna ağ güvenlik kuralı yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-103">Adds a network security rule configuration to a network security group.</span></span>

## <span data-ttu-id="9fbe3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9fbe3-104">SYNTAX</span></span>

### <span data-ttu-id="9fbe3-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9fbe3-105">SetByResource (Default)</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fbe3-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="9fbe3-106">SetByResourceId</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9fbe3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9fbe3-107">DESCRIPTION</span></span>
<span data-ttu-id="9fbe3-108">**Add-AzNetworkSecurityRuleConfig** cmdlet 'ı bir Azure ağ güvenlik grubuna ağ güvenlik kuralı yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-108">The **Add-AzNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="9fbe3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9fbe3-109">EXAMPLES</span></span>

### <span data-ttu-id="9fbe3-110">1: ağ güvenlik grubu ekleme</span><span class="sxs-lookup"><span data-stu-id="9fbe3-110">1: Adding a network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

<span data-ttu-id="9fbe3-111">İlk komut, "RG1" kaynak grubundan "nsg1" adlı bir Azure ağ güvenlik grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="9fbe3-112">İkinci komut "RDP-Rule" adlı bir ağ güvenlik kuralı ekler; bağlantı 3389 noktası</span><span class="sxs-lookup"><span data-stu-id="9fbe3-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="9fbe3-113">Değiştirilmiş Azure Network Security grubunu devam ettirir.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="9fbe3-114">2: uygulama güvenlik gruplarıyla yeni bir güvenlik kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="9fbe3-114">2: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

<span data-ttu-id="9fbe3-115">İlk olarak iki yeni uygulama güvenlik grubu oluşturduk.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-115">First, we create two new application security groups.</span></span> <span data-ttu-id="9fbe3-116">Ardından, "RG1" kaynak grubundan "nsg1" adlı bir Azure ağ güvenlik grubunu aldık.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="9fbe3-117">ve buna "RDP-Rule" adlı bir ağ güvenliği kuralı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="9fbe3-118">Kural, "srcAsg" uygulama güvenlik grubundaki tüm IP yapılandırmalarından gelen trafiğe, bağlantı noktası 3389 "destAsg" uygulamasındaki tüm IP yapılandırmalarına izin verir.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="9fbe3-119">Kuralı ekledikten sonra, değiştirilmiş Azure ağ güvenlik grubunu devam ediyoruz.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="9fbe3-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9fbe3-120">PARAMETERS</span></span>

### <span data-ttu-id="9fbe3-121">-Access</span><span class="sxs-lookup"><span data-stu-id="9fbe3-121">-Access</span></span>
<span data-ttu-id="9fbe3-122">Ağ trafiğine izin verilip verilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="9fbe3-123">Bu parametre için kabul edilebilir değerler: Izin ver ve Reddet.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="9fbe3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fbe3-124">-DefaultProfile</span></span>
<span data-ttu-id="9fbe3-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fbe3-126">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="9fbe3-126">-Description</span></span>
<span data-ttu-id="9fbe3-127">Ağ güvenlik kuralı yapılandırmasının açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-127">Specifies a description of a network security rule configuration.</span></span>

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

### <span data-ttu-id="9fbe3-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9fbe3-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="9fbe3-129">Hedef adres önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="9fbe3-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9fbe3-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9fbe3-131">Sınıfsız Etki alanları arası yönlendirme (CıDR) adresi</span><span class="sxs-lookup"><span data-stu-id="9fbe3-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="9fbe3-132">Hedef IP adresi aralığı</span><span class="sxs-lookup"><span data-stu-id="9fbe3-132">A destination IP address range</span></span>
- <span data-ttu-id="9fbe3-133">Herhangi bir IP adresiyle eşleşen bir joker karakter (\*), VirtualNetwork, AzureLoadBalancer ve Internet gibi etiketleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="9fbe3-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9fbe3-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="9fbe3-135">Kural için hedef olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="9fbe3-136">' DestinationAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="9fbe3-137">-Destinationapplicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="9fbe3-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="9fbe3-138">Kural için hedef olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="9fbe3-139">' DestinationAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="9fbe3-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="9fbe3-140">-DestinationPortRange</span></span>
<span data-ttu-id="9fbe3-141">Hedef bir bağlantı noktası veya aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="9fbe3-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9fbe3-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9fbe3-143">Bir tamsayı</span><span class="sxs-lookup"><span data-stu-id="9fbe3-143">An integer</span></span>
- <span data-ttu-id="9fbe3-144">0 ile 65535 arasında bir tamsayı aralığı</span><span class="sxs-lookup"><span data-stu-id="9fbe3-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="9fbe3-145">Herhangi bir bağlantı noktası ile eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="9fbe3-145">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="9fbe3-146">-Yön</span><span class="sxs-lookup"><span data-stu-id="9fbe3-146">-Direction</span></span>
<span data-ttu-id="9fbe3-147">Kuralın gelen veya giden trafikte değerlendirilip değerlendirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-147">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="9fbe3-148">Bu parametre için kabul edilebilir değerler: gelen ve giden.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="9fbe3-149">-Ad</span><span class="sxs-lookup"><span data-stu-id="9fbe3-149">-Name</span></span>
<span data-ttu-id="9fbe3-150">Ağ güvenlik kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-150">Specifies the name of a network security rule configuration.</span></span>

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

### <span data-ttu-id="9fbe3-151">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9fbe3-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="9fbe3-152">Bir **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-152">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="9fbe3-153">Bu cmdlet, bu parametrenin belirttiği nesneye ağ güvenlik kuralı yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-153">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="9fbe3-154">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="9fbe3-154">-Priority</span></span>
<span data-ttu-id="9fbe3-155">Kural yapılandırmasının önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-155">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="9fbe3-156">Bu parametre için kabul edilebilir değerler şunlardır: 100 ile 4096 arasında bir tamsayı.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-156">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="9fbe3-157">Öncelikteki her kural için öncelik numarası benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-157">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="9fbe3-158">Öncelik numarası düşükse, kuralın önceliği o kadar yüksek olur.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-158">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="9fbe3-159">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="9fbe3-159">-Protocol</span></span>
<span data-ttu-id="9fbe3-160">Kural yapılandırmasının uygulandığı ağ protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-160">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="9fbe3-161">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9fbe3-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9fbe3-162">TC</span><span class="sxs-lookup"><span data-stu-id="9fbe3-162">Tcp</span></span>
- <span data-ttu-id="9fbe3-163">UDP</span><span class="sxs-lookup"><span data-stu-id="9fbe3-163">Udp</span></span>
- <span data-ttu-id="9fbe3-164">İkisi ile eşleşen joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="9fbe3-164">Wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="9fbe3-165">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9fbe3-165">-SourceAddressPrefix</span></span>
<span data-ttu-id="9fbe3-166">Kaynak adres önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-166">Specifies a source address prefix.</span></span>
<span data-ttu-id="9fbe3-167">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9fbe3-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9fbe3-168">CıDR</span><span class="sxs-lookup"><span data-stu-id="9fbe3-168">A CIDR</span></span>
- <span data-ttu-id="9fbe3-169">Kaynak IP aralığı</span><span class="sxs-lookup"><span data-stu-id="9fbe3-169">A source IP range</span></span>
- <span data-ttu-id="9fbe3-170">Herhangi bir IP adresiyle eşleşen joker karakter (\*).</span><span class="sxs-lookup"><span data-stu-id="9fbe3-170">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="9fbe3-171">VirtualNetwork, AzureLoadBalancer ve Internet gibi etiketleri de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-171">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="9fbe3-172">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9fbe3-172">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="9fbe3-173">Kural için kaynak olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="9fbe3-174">' SourceAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="9fbe3-175">-Sourceapplicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="9fbe3-175">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="9fbe3-176">Kural için kaynak olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-176">The application security group set as source for the rule.</span></span> <span data-ttu-id="9fbe3-177">' SourceAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-177">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="9fbe3-178">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="9fbe3-178">-SourcePortRange</span></span>
<span data-ttu-id="9fbe3-179">Kaynak bağlantı noktası veya aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-179">Specifies a source port or range.</span></span>
<span data-ttu-id="9fbe3-180">Bu değer bir tamsayı olarak, 0 ile 65535 arasındaki bir Aralık veya herhangi bir kaynak bağlantı noktası ile eşleşen bir joker karakter (\*) olarak ifade edilir.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-180">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

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

### <span data-ttu-id="9fbe3-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fbe3-181">CommonParameters</span></span>
<span data-ttu-id="9fbe3-182">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9fbe3-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fbe3-183">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fbe3-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fbe3-184">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9fbe3-184">INPUTS</span></span>

### <span data-ttu-id="9fbe3-185">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9fbe3-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="9fbe3-186">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9fbe3-186">OUTPUTS</span></span>

### <span data-ttu-id="9fbe3-187">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9fbe3-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="9fbe3-188">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9fbe3-188">NOTES</span></span>

## <span data-ttu-id="9fbe3-189">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9fbe3-189">RELATED LINKS</span></span>

[<span data-ttu-id="9fbe3-190">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9fbe3-190">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9fbe3-191">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9fbe3-191">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9fbe3-192">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9fbe3-192">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9fbe3-193">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9fbe3-193">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

