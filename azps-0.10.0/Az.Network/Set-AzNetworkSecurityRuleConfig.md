---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 963dc6391ef5f500b26068e2a407eacd64ce6c16
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936525"
---
# <span data-ttu-id="b526e-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b526e-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="b526e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b526e-102">SYNOPSIS</span></span>
<span data-ttu-id="b526e-103">Ağ güvenlik kuralı yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b526e-103">Sets the goal state for a network security rule configuration.</span></span>

## <span data-ttu-id="b526e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b526e-104">SYNTAX</span></span>

### <span data-ttu-id="b526e-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b526e-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b526e-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="b526e-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b526e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b526e-107">DESCRIPTION</span></span>
<span data-ttu-id="b526e-108">**Set-Azağsecurityruleconfig** cmdlet 'i, bir Azure ağ güvenlik kuralı yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b526e-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet sets the goal state for an Azure network security rule configuration.</span></span>

## <span data-ttu-id="b526e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b526e-109">EXAMPLES</span></span>

### <span data-ttu-id="b526e-110">Örnek 1: ağ güvenlik kuralında erişim yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="b526e-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="b526e-111">İlk komut NSG-ön uç adlı ağ güvenlik grubunu alır ve bunu değişken $nsg depolar.</span><span class="sxs-lookup"><span data-stu-id="b526e-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>

<span data-ttu-id="b526e-112">İkinci komut, RDP kuralı adlı güvenlik kuralı yapılandırmasını alan ve Get-AzNetworkSecurityRuleConfig öğesine $nsg güvenlik grubuna geçirmek için ardışık düzen işlecini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b526e-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>

<span data-ttu-id="b526e-113">Üçüncü komut, RDP kuralının erişim yapılandırmasını reddedecek şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b526e-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="b526e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b526e-114">PARAMETERS</span></span>

### <span data-ttu-id="b526e-115">-Access</span><span class="sxs-lookup"><span data-stu-id="b526e-115">-Access</span></span>
<span data-ttu-id="b526e-116">Ağ trafiğine izin verilip verilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b526e-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="b526e-117">Bu parametre için kabul edilebilir değerler: Izin ver ve Reddet.</span><span class="sxs-lookup"><span data-stu-id="b526e-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b526e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b526e-118">-DefaultProfile</span></span>
<span data-ttu-id="b526e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b526e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b526e-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="b526e-120">-Description</span></span>
<span data-ttu-id="b526e-121">Kural yapılandırmasının açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b526e-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="b526e-122">Boyut üst sınırı 140 karakterdir.</span><span class="sxs-lookup"><span data-stu-id="b526e-122">The maximum size is 140 characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b526e-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b526e-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="b526e-124">Hedef adres önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b526e-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="b526e-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b526e-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b526e-126">Sınıfsız Etki alanları arası yönlendirme (CıDR) adresi</span><span class="sxs-lookup"><span data-stu-id="b526e-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="b526e-127">Hedef IP adresi aralığı</span><span class="sxs-lookup"><span data-stu-id="b526e-127">A destination IP address range</span></span> 
- <span data-ttu-id="b526e-128">Herhangi bir IP adresiyle eşleşen joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="b526e-128">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="b526e-129">VirtualNetwork, AzureLoadBalancer ve Internet gibi etiketleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b526e-129">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="b526e-130">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b526e-130">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="b526e-131">Kural için hedef olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="b526e-131">The application security group set as destination for the rule.</span></span> <span data-ttu-id="b526e-132">' DestinationAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="b526e-132">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="b526e-133">-Destinationapplicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="b526e-133">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="b526e-134">Kural için hedef olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="b526e-134">The application security group set as destination for the rule.</span></span> <span data-ttu-id="b526e-135">' DestinationAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="b526e-135">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="b526e-136">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="b526e-136">-DestinationPortRange</span></span>
<span data-ttu-id="b526e-137">Hedef bir bağlantı noktası veya aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="b526e-137">Specifies a destination port or range.</span></span>
<span data-ttu-id="b526e-138">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b526e-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b526e-139">Bir tamsayı</span><span class="sxs-lookup"><span data-stu-id="b526e-139">An integer</span></span> 
- <span data-ttu-id="b526e-140">0 ile 65535 arasında bir tamsayı aralığı</span><span class="sxs-lookup"><span data-stu-id="b526e-140">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="b526e-141">Herhangi bir bağlantı noktası ile eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="b526e-141">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="b526e-142">-Yön</span><span class="sxs-lookup"><span data-stu-id="b526e-142">-Direction</span></span>
<span data-ttu-id="b526e-143">Kuralın gelen veya giden trafik için değerlendirilip değerlendirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b526e-143">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="b526e-144">Bu parametre için kabul edilebilir değerler: gelen ve giden.</span><span class="sxs-lookup"><span data-stu-id="b526e-144">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b526e-145">-Ad</span><span class="sxs-lookup"><span data-stu-id="b526e-145">-Name</span></span>
<span data-ttu-id="b526e-146">Bu cmdlet 'in ayarladığı ağ güvenlik kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b526e-146">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b526e-147">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b526e-147">-NetworkSecurityGroup</span></span>
<span data-ttu-id="b526e-148">Ayarlanacak ağ güvenlik kuralı yapılandırmasını içeren **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b526e-148">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b526e-149">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="b526e-149">-Priority</span></span>
<span data-ttu-id="b526e-150">Kural yapılandırmasının önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b526e-150">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="b526e-151">Bu parametre için kabul edilebilir değerler şunlardır: 100 ile 4096 arasında bir tamsayı.</span><span class="sxs-lookup"><span data-stu-id="b526e-151">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>

<span data-ttu-id="b526e-152">Öncelikteki her kural için öncelik numarası benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b526e-152">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="b526e-153">Öncelik numarası düşükse, kuralın önceliği o kadar yüksek olur.</span><span class="sxs-lookup"><span data-stu-id="b526e-153">The lower the priority number, the higher the priority of the rule.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b526e-154">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="b526e-154">-Protocol</span></span>
<span data-ttu-id="b526e-155">Kural yapılandırmasının uygulandığı ağ protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b526e-155">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="b526e-156">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b526e-156">The acceptable values for this parameter are:</span></span>

 <span data-ttu-id="b526e-157">--TCP</span><span class="sxs-lookup"><span data-stu-id="b526e-157">--Tcp</span></span>
- <span data-ttu-id="b526e-158">UDP</span><span class="sxs-lookup"><span data-stu-id="b526e-158">Udp</span></span>
- <span data-ttu-id="b526e-159">Her ikisiyle eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="b526e-159">A wildcard character (\*) to match both</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b526e-160">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b526e-160">-SourceAddressPrefix</span></span>
<span data-ttu-id="b526e-161">Kaynak adres önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b526e-161">Specifies a source address prefix.</span></span>
<span data-ttu-id="b526e-162">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b526e-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b526e-163">CıDR</span><span class="sxs-lookup"><span data-stu-id="b526e-163">A CIDR</span></span>
- <span data-ttu-id="b526e-164">Kaynak IP aralığı</span><span class="sxs-lookup"><span data-stu-id="b526e-164">A source IP range</span></span>
- <span data-ttu-id="b526e-165">Herhangi bir IP adresiyle eşleşen joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="b526e-165">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="b526e-166">VirtualNetwork, AzureLoadBalancer ve Internet gibi etiketleri de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b526e-166">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="b526e-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b526e-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="b526e-168">Kural için kaynak olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="b526e-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="b526e-169">' SourceAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="b526e-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="b526e-170">-Sourceapplicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="b526e-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="b526e-171">Kural için kaynak olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="b526e-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="b526e-172">' SourceAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="b526e-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="b526e-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="b526e-173">-SourcePortRange</span></span>
<span data-ttu-id="b526e-174">Kaynak bağlantı noktasını veya aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b526e-174">Specifies the source port or range.</span></span>
<span data-ttu-id="b526e-175">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b526e-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b526e-176">Bir tamsayı</span><span class="sxs-lookup"><span data-stu-id="b526e-176">An integer</span></span>
- <span data-ttu-id="b526e-177">0 ile 65535 arasında bir tamsayı aralığı</span><span class="sxs-lookup"><span data-stu-id="b526e-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="b526e-178">Herhangi bir bağlantı noktası ile eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="b526e-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="b526e-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b526e-179">CommonParameters</span></span>
<span data-ttu-id="b526e-180">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b526e-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b526e-181">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b526e-181">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b526e-182">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b526e-182">INPUTS</span></span>

### <span data-ttu-id="b526e-183">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b526e-183">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="b526e-184">' NetworkSecurityGroup ' parametresi ardışık düzenin ' PSNetworkSecurityGroup ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b526e-184">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="b526e-185">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b526e-185">OUTPUTS</span></span>

### <span data-ttu-id="b526e-186">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b526e-186">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="b526e-187">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b526e-187">NOTES</span></span>

## <span data-ttu-id="b526e-188">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b526e-188">RELATED LINKS</span></span>

[<span data-ttu-id="b526e-189">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b526e-189">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b526e-190">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b526e-190">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b526e-191">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b526e-191">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b526e-192">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b526e-192">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


