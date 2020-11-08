---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 42f92e7f90e5349c116f8a6ed948ed7a29a35ad2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276736"
---
# <span data-ttu-id="aeb24-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aeb24-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="aeb24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aeb24-102">SYNOPSIS</span></span>
<span data-ttu-id="aeb24-103">Ağ güvenlik grubu için ağ güvenliği kuralı yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="aeb24-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="aeb24-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aeb24-104">SYNTAX</span></span>

### <span data-ttu-id="aeb24-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aeb24-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aeb24-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="aeb24-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aeb24-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="aeb24-107">DESCRIPTION</span></span>
<span data-ttu-id="aeb24-108">**Set-Azağsecurityruleconfig** cmdlet 'i, ağ güvenlik grubu için bir ağ güvenliği kuralı yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="aeb24-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="aeb24-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aeb24-109">EXAMPLES</span></span>

### <span data-ttu-id="aeb24-110">Örnek 1: ağ güvenlik kuralında erişim yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="aeb24-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="aeb24-111">İlk komut NSG-ön uç adlı ağ güvenlik grubunu alır ve bunu değişken $nsg depolar.</span><span class="sxs-lookup"><span data-stu-id="aeb24-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="aeb24-112">İkinci komut, RDP kuralı adlı güvenlik kuralı yapılandırmasını alan ve Get-AzNetworkSecurityRuleConfig öğesine $nsg güvenlik grubuna geçirmek için ardışık düzen işlecini kullanır.</span><span class="sxs-lookup"><span data-stu-id="aeb24-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="aeb24-113">Üçüncü komut, RDP kuralının erişim yapılandırmasını reddedecek şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="aeb24-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

### <span data-ttu-id="aeb24-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="aeb24-114">Example 2</span></span>

<span data-ttu-id="aeb24-115">Ağ güvenlik grubu için ağ güvenliği kuralı yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="aeb24-115">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="aeb24-116">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="aeb24-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="aeb24-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aeb24-117">PARAMETERS</span></span>

### <span data-ttu-id="aeb24-118">-Access</span><span class="sxs-lookup"><span data-stu-id="aeb24-118">-Access</span></span>
<span data-ttu-id="aeb24-119">Ağ trafiğine izin verilip verilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb24-119">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="aeb24-120">Bu parametre için kabul edilebilir değerler: Izin ver ve Reddet.</span><span class="sxs-lookup"><span data-stu-id="aeb24-120">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="aeb24-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeb24-121">-DefaultProfile</span></span>
<span data-ttu-id="aeb24-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aeb24-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aeb24-123">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="aeb24-123">-Description</span></span>
<span data-ttu-id="aeb24-124">Kural yapılandırmasının açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb24-124">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="aeb24-125">Boyut üst sınırı 140 karakterdir.</span><span class="sxs-lookup"><span data-stu-id="aeb24-125">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="aeb24-126">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="aeb24-126">-DestinationAddressPrefix</span></span>
<span data-ttu-id="aeb24-127">Hedef adres önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb24-127">Specifies a destination address prefix.</span></span>
<span data-ttu-id="aeb24-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="aeb24-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aeb24-129">Sınıfsız Etki alanları arası yönlendirme (CıDR) adresi</span><span class="sxs-lookup"><span data-stu-id="aeb24-129">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="aeb24-130">Hedef IP adresi aralığı</span><span class="sxs-lookup"><span data-stu-id="aeb24-130">A destination IP address range</span></span> 
- <span data-ttu-id="aeb24-131">Herhangi bir IP adresiyle eşleşen bir joker karakter (\*), VirtualNetwork, AzureLoadBalancer ve Internet gibi etiketleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aeb24-131">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="aeb24-132">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aeb24-132">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="aeb24-133">Kural için hedef olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="aeb24-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="aeb24-134">' DestinationAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="aeb24-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="aeb24-135">-Destinationapplicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="aeb24-135">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="aeb24-136">Kural için hedef olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="aeb24-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="aeb24-137">' DestinationAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="aeb24-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="aeb24-138">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="aeb24-138">-DestinationPortRange</span></span>
<span data-ttu-id="aeb24-139">Hedef bir bağlantı noktası veya aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb24-139">Specifies a destination port or range.</span></span>
<span data-ttu-id="aeb24-140">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="aeb24-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aeb24-141">Bir tamsayı</span><span class="sxs-lookup"><span data-stu-id="aeb24-141">An integer</span></span> 
- <span data-ttu-id="aeb24-142">0 ile 65535 arasında bir tamsayı aralığı</span><span class="sxs-lookup"><span data-stu-id="aeb24-142">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="aeb24-143">Herhangi bir bağlantı noktası ile eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="aeb24-143">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="aeb24-144">-Yön</span><span class="sxs-lookup"><span data-stu-id="aeb24-144">-Direction</span></span>
<span data-ttu-id="aeb24-145">Kuralın gelen veya giden trafik için değerlendirilip değerlendirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb24-145">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="aeb24-146">Bu parametre için kabul edilebilir değerler: gelen ve giden.</span><span class="sxs-lookup"><span data-stu-id="aeb24-146">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="aeb24-147">-Ad</span><span class="sxs-lookup"><span data-stu-id="aeb24-147">-Name</span></span>
<span data-ttu-id="aeb24-148">Bu cmdlet 'in ayarladığı ağ güvenlik kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb24-148">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="aeb24-149">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aeb24-149">-NetworkSecurityGroup</span></span>
<span data-ttu-id="aeb24-150">Ayarlanacak ağ güvenlik kuralı yapılandırmasını içeren **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb24-150">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="aeb24-151">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="aeb24-151">-Priority</span></span>
<span data-ttu-id="aeb24-152">Kural yapılandırmasının önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb24-152">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="aeb24-153">Bu parametre için kabul edilebilir değerler şunlardır: 100 ile 4096 arasında bir tamsayı.</span><span class="sxs-lookup"><span data-stu-id="aeb24-153">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="aeb24-154">Öncelikteki her kural için öncelik numarası benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="aeb24-154">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="aeb24-155">Öncelik numarası düşükse, kuralın önceliği o kadar yüksek olur.</span><span class="sxs-lookup"><span data-stu-id="aeb24-155">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="aeb24-156">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="aeb24-156">-Protocol</span></span>
<span data-ttu-id="aeb24-157">Kural yapılandırmasının uygulandığı ağ protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb24-157">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="aeb24-158">Bu parametre için kabul edilebilir değerler şunlardır:-TCP</span><span class="sxs-lookup"><span data-stu-id="aeb24-158">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="aeb24-159">UDP</span><span class="sxs-lookup"><span data-stu-id="aeb24-159">Udp</span></span>
- <span data-ttu-id="aeb24-160">Her ikisiyle eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="aeb24-160">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="aeb24-161">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="aeb24-161">-SourceAddressPrefix</span></span>
<span data-ttu-id="aeb24-162">Kaynak adres önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb24-162">Specifies a source address prefix.</span></span>
<span data-ttu-id="aeb24-163">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="aeb24-163">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aeb24-164">CıDR</span><span class="sxs-lookup"><span data-stu-id="aeb24-164">A CIDR</span></span>
- <span data-ttu-id="aeb24-165">Kaynak IP aralığı</span><span class="sxs-lookup"><span data-stu-id="aeb24-165">A source IP range</span></span>
- <span data-ttu-id="aeb24-166">Herhangi bir IP adresiyle eşleşen bir joker karakter (\*), VirtualNetwork, AzureLoadBalancer ve Internet gibi etiketleri de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aeb24-166">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="aeb24-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aeb24-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="aeb24-168">Kural için kaynak olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="aeb24-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="aeb24-169">' SourceAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="aeb24-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="aeb24-170">-Sourceapplicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="aeb24-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="aeb24-171">Kural için kaynak olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="aeb24-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="aeb24-172">' SourceAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="aeb24-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="aeb24-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="aeb24-173">-SourcePortRange</span></span>
<span data-ttu-id="aeb24-174">Kaynak bağlantı noktasını veya aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb24-174">Specifies the source port or range.</span></span>
<span data-ttu-id="aeb24-175">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="aeb24-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aeb24-176">Bir tamsayı</span><span class="sxs-lookup"><span data-stu-id="aeb24-176">An integer</span></span>
- <span data-ttu-id="aeb24-177">0 ile 65535 arasında bir tamsayı aralığı</span><span class="sxs-lookup"><span data-stu-id="aeb24-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="aeb24-178">Herhangi bir bağlantı noktası ile eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="aeb24-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="aeb24-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeb24-179">CommonParameters</span></span>
<span data-ttu-id="aeb24-180">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aeb24-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeb24-181">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeb24-181">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeb24-182">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aeb24-182">INPUTS</span></span>

### <span data-ttu-id="aeb24-183">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aeb24-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="aeb24-184">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aeb24-184">OUTPUTS</span></span>

### <span data-ttu-id="aeb24-185">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aeb24-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="aeb24-186">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aeb24-186">NOTES</span></span>

## <span data-ttu-id="aeb24-187">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aeb24-187">RELATED LINKS</span></span>

[<span data-ttu-id="aeb24-188">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aeb24-188">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="aeb24-189">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aeb24-189">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="aeb24-190">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aeb24-190">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="aeb24-191">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aeb24-191">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


