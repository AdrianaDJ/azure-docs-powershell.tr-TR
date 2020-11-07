---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecurityruleconfig
schema: 2.0.0
ms.openlocfilehash: 8a1e4cb97f151843f92697a2a230bd2721a56f29
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939691"
---
# <span data-ttu-id="93c1f-101">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="93c1f-101">Set-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="93c1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="93c1f-103">Ağ güvenlik kuralı yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="93c1f-103">Sets the goal state for a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93c1f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="93c1f-104">SYNTAX</span></span>

### <span data-ttu-id="93c1f-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="93c1f-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
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

### <span data-ttu-id="93c1f-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="93c1f-106">SetByResourceId</span></span>
```
Set-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93c1f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="93c1f-107">DESCRIPTION</span></span>
<span data-ttu-id="93c1f-108">**Set-AzureRmNetworkSecurityRuleConfig** cmdlet 'i, bir Azure ağ güvenlik kuralı yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="93c1f-108">The **Set-AzureRmNetworkSecurityRuleConfig** cmdlet sets the goal state for an Azure network security rule configuration.</span></span>

## <span data-ttu-id="93c1f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="93c1f-109">EXAMPLES</span></span>

### <span data-ttu-id="93c1f-110">Örnek 1: ağ güvenlik kuralında erişim yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="93c1f-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="93c1f-111">İlk komut NSG-ön uç adlı ağ güvenlik grubunu alır ve bunu değişken $nsg depolar.</span><span class="sxs-lookup"><span data-stu-id="93c1f-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>

<span data-ttu-id="93c1f-112">İkinci $nsg komut, RDP kuralı adlı güvenlik kuralı yapılandırmasını alan,-AzureRmNetworkSecurityRuleConfig 'i almak</span><span class="sxs-lookup"><span data-stu-id="93c1f-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzureRmNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>

<span data-ttu-id="93c1f-113">Üçüncü komut, RDP kuralının erişim yapılandırmasını reddedecek şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="93c1f-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="93c1f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="93c1f-114">PARAMETERS</span></span>

### <span data-ttu-id="93c1f-115">-Access</span><span class="sxs-lookup"><span data-stu-id="93c1f-115">-Access</span></span>
<span data-ttu-id="93c1f-116">Ağ trafiğine izin verilip verilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="93c1f-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="93c1f-117">Bu parametre için kabul edilebilir değerler: Izin ver ve Reddet.</span><span class="sxs-lookup"><span data-stu-id="93c1f-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="93c1f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93c1f-118">-DefaultProfile</span></span>
<span data-ttu-id="93c1f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="93c1f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93c1f-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="93c1f-120">-Description</span></span>
<span data-ttu-id="93c1f-121">Kural yapılandırmasının açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93c1f-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="93c1f-122">Boyut üst sınırı 140 karakterdir.</span><span class="sxs-lookup"><span data-stu-id="93c1f-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="93c1f-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="93c1f-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="93c1f-124">Hedef adres önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="93c1f-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="93c1f-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="93c1f-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="93c1f-126">Sınıfsız Etki alanları arası yönlendirme (CıDR) adresi</span><span class="sxs-lookup"><span data-stu-id="93c1f-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="93c1f-127">Hedef IP adresi aralığı</span><span class="sxs-lookup"><span data-stu-id="93c1f-127">A destination IP address range</span></span> 
- <span data-ttu-id="93c1f-128">Herhangi bir IP adresiyle eşleşen joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="93c1f-128">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="93c1f-129">VirtualNetwork, AzureLoadBalancer ve Internet gibi etiketleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="93c1f-129">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="93c1f-130">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="93c1f-130">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="93c1f-131">Kural için hedef olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="93c1f-131">The application security group set as destination for the rule.</span></span> <span data-ttu-id="93c1f-132">' DestinationAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="93c1f-132">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="93c1f-133">-Destinationapplicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="93c1f-133">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="93c1f-134">Kural için hedef olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="93c1f-134">The application security group set as destination for the rule.</span></span> <span data-ttu-id="93c1f-135">' DestinationAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="93c1f-135">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="93c1f-136">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="93c1f-136">-DestinationPortRange</span></span>
<span data-ttu-id="93c1f-137">Hedef bir bağlantı noktası veya aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="93c1f-137">Specifies a destination port or range.</span></span>
<span data-ttu-id="93c1f-138">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="93c1f-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="93c1f-139">Bir tamsayı</span><span class="sxs-lookup"><span data-stu-id="93c1f-139">An integer</span></span> 
- <span data-ttu-id="93c1f-140">0 ile 65535 arasında bir tamsayı aralığı</span><span class="sxs-lookup"><span data-stu-id="93c1f-140">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="93c1f-141">Herhangi bir bağlantı noktası ile eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="93c1f-141">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="93c1f-142">-Yön</span><span class="sxs-lookup"><span data-stu-id="93c1f-142">-Direction</span></span>
<span data-ttu-id="93c1f-143">Kuralın gelen veya giden trafik için değerlendirilip değerlendirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="93c1f-143">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="93c1f-144">Bu parametre için kabul edilebilir değerler: gelen ve giden.</span><span class="sxs-lookup"><span data-stu-id="93c1f-144">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="93c1f-145">-Ad</span><span class="sxs-lookup"><span data-stu-id="93c1f-145">-Name</span></span>
<span data-ttu-id="93c1f-146">Bu cmdlet 'in ayarladığı ağ güvenlik kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93c1f-146">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="93c1f-147">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="93c1f-147">-NetworkSecurityGroup</span></span>
<span data-ttu-id="93c1f-148">Ayarlanacak ağ güvenlik kuralı yapılandırmasını içeren **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="93c1f-148">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="93c1f-149">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="93c1f-149">-Priority</span></span>
<span data-ttu-id="93c1f-150">Kural yapılandırmasının önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="93c1f-150">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="93c1f-151">Bu parametre için kabul edilebilir değerler şunlardır: 100 ile 4096 arasında bir tamsayı.</span><span class="sxs-lookup"><span data-stu-id="93c1f-151">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>

<span data-ttu-id="93c1f-152">Öncelikteki her kural için öncelik numarası benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="93c1f-152">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="93c1f-153">Öncelik numarası düşükse, kuralın önceliği o kadar yüksek olur.</span><span class="sxs-lookup"><span data-stu-id="93c1f-153">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="93c1f-154">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="93c1f-154">-Protocol</span></span>
<span data-ttu-id="93c1f-155">Kural yapılandırmasının uygulandığı ağ protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="93c1f-155">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="93c1f-156">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="93c1f-156">The acceptable values for this parameter are:</span></span>

 <span data-ttu-id="93c1f-157">--TCP</span><span class="sxs-lookup"><span data-stu-id="93c1f-157">--Tcp</span></span>
- <span data-ttu-id="93c1f-158">UDP</span><span class="sxs-lookup"><span data-stu-id="93c1f-158">Udp</span></span>
- <span data-ttu-id="93c1f-159">Her ikisiyle eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="93c1f-159">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="93c1f-160">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="93c1f-160">-SourceAddressPrefix</span></span>
<span data-ttu-id="93c1f-161">Kaynak adres önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="93c1f-161">Specifies a source address prefix.</span></span>
<span data-ttu-id="93c1f-162">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="93c1f-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="93c1f-163">CıDR</span><span class="sxs-lookup"><span data-stu-id="93c1f-163">A CIDR</span></span>
- <span data-ttu-id="93c1f-164">Kaynak IP aralığı</span><span class="sxs-lookup"><span data-stu-id="93c1f-164">A source IP range</span></span>
- <span data-ttu-id="93c1f-165">Herhangi bir IP adresiyle eşleşen joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="93c1f-165">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="93c1f-166">VirtualNetwork, AzureLoadBalancer ve Internet gibi etiketleri de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="93c1f-166">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="93c1f-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="93c1f-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="93c1f-168">Kural için kaynak olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="93c1f-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="93c1f-169">' SourceAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="93c1f-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="93c1f-170">-Sourceapplicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="93c1f-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="93c1f-171">Kural için kaynak olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="93c1f-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="93c1f-172">' SourceAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="93c1f-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="93c1f-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="93c1f-173">-SourcePortRange</span></span>
<span data-ttu-id="93c1f-174">Kaynak bağlantı noktasını veya aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93c1f-174">Specifies the source port or range.</span></span>
<span data-ttu-id="93c1f-175">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="93c1f-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="93c1f-176">Bir tamsayı</span><span class="sxs-lookup"><span data-stu-id="93c1f-176">An integer</span></span>
- <span data-ttu-id="93c1f-177">0 ile 65535 arasında bir tamsayı aralığı</span><span class="sxs-lookup"><span data-stu-id="93c1f-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="93c1f-178">Herhangi bir bağlantı noktası ile eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="93c1f-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="93c1f-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93c1f-179">CommonParameters</span></span>
<span data-ttu-id="93c1f-180">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="93c1f-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93c1f-181">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93c1f-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93c1f-182">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="93c1f-182">INPUTS</span></span>

### <span data-ttu-id="93c1f-183">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="93c1f-183">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="93c1f-184">' NetworkSecurityGroup ' parametresi ardışık düzenin ' PSNetworkSecurityGroup ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="93c1f-184">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="93c1f-185">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="93c1f-185">OUTPUTS</span></span>

### <span data-ttu-id="93c1f-186">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="93c1f-186">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="93c1f-187">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="93c1f-187">NOTES</span></span>

## <span data-ttu-id="93c1f-188">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="93c1f-188">RELATED LINKS</span></span>

[<span data-ttu-id="93c1f-189">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="93c1f-189">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="93c1f-190">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="93c1f-190">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="93c1f-191">Yeni-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="93c1f-191">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="93c1f-192">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="93c1f-192">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)


