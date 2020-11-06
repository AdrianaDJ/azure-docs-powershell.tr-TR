---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: fa1416d7bd65236d3a4e1198d6f70efb1a860985
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589229"
---
# <span data-ttu-id="96608-101">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="96608-101">Set-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="96608-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96608-102">SYNOPSIS</span></span>
<span data-ttu-id="96608-103">Ağ güvenlik kuralı yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="96608-103">Sets the goal state for a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96608-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="96608-104">SYNTAX</span></span>

### <span data-ttu-id="96608-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="96608-105">SetByResource (Default)</span></span>
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

### <span data-ttu-id="96608-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="96608-106">SetByResourceId</span></span>
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

## <span data-ttu-id="96608-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="96608-107">DESCRIPTION</span></span>
<span data-ttu-id="96608-108">**Set-AzureRmNetworkSecurityRuleConfig** cmdlet 'i, bir Azure ağ güvenlik kuralı yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="96608-108">The **Set-AzureRmNetworkSecurityRuleConfig** cmdlet sets the goal state for an Azure network security rule configuration.</span></span>

## <span data-ttu-id="96608-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="96608-109">EXAMPLES</span></span>

### <span data-ttu-id="96608-110">Örnek 1: ağ güvenlik kuralında erişim yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="96608-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="96608-111">İlk komut NSG-ön uç adlı ağ güvenlik grubunu alır ve bunu değişken $nsg depolar.</span><span class="sxs-lookup"><span data-stu-id="96608-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>

<span data-ttu-id="96608-112">İkinci $nsg komut, RDP kuralı adlı güvenlik kuralı yapılandırmasını alan,-AzureRmNetworkSecurityRuleConfig 'i almak</span><span class="sxs-lookup"><span data-stu-id="96608-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzureRmNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>

<span data-ttu-id="96608-113">Üçüncü komut, RDP kuralının erişim yapılandırmasını reddedecek şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="96608-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="96608-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="96608-114">PARAMETERS</span></span>

### <span data-ttu-id="96608-115">-Access</span><span class="sxs-lookup"><span data-stu-id="96608-115">-Access</span></span>
<span data-ttu-id="96608-116">Ağ trafiğine izin verilip verilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="96608-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="96608-117">Bu parametre için kabul edilebilir değerler: Izin ver ve Reddet.</span><span class="sxs-lookup"><span data-stu-id="96608-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="96608-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96608-118">-DefaultProfile</span></span>
<span data-ttu-id="96608-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="96608-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96608-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="96608-120">-Description</span></span>
<span data-ttu-id="96608-121">Kural yapılandırmasının açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="96608-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="96608-122">Boyut üst sınırı 140 karakterdir.</span><span class="sxs-lookup"><span data-stu-id="96608-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="96608-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="96608-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="96608-124">Hedef adres önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="96608-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="96608-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="96608-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="96608-126">Sınıfsız Etki alanları arası yönlendirme (CıDR) adresi</span><span class="sxs-lookup"><span data-stu-id="96608-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="96608-127">Hedef IP adresi aralığı</span><span class="sxs-lookup"><span data-stu-id="96608-127">A destination IP address range</span></span> 
- <span data-ttu-id="96608-128">Herhangi bir IP adresiyle eşleşen joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="96608-128">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="96608-129">VirtualNetwork, AzureLoadBalancer ve Internet gibi etiketleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="96608-129">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="96608-130">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="96608-130">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="96608-131">Kural için hedef olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="96608-131">The application security group set as destination for the rule.</span></span> <span data-ttu-id="96608-132">' DestinationAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="96608-132">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="96608-133">-Destinationapplicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="96608-133">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="96608-134">Kural için hedef olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="96608-134">The application security group set as destination for the rule.</span></span> <span data-ttu-id="96608-135">' DestinationAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="96608-135">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="96608-136">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="96608-136">-DestinationPortRange</span></span>
<span data-ttu-id="96608-137">Hedef bir bağlantı noktası veya aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="96608-137">Specifies a destination port or range.</span></span>
<span data-ttu-id="96608-138">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="96608-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="96608-139">Bir tamsayı</span><span class="sxs-lookup"><span data-stu-id="96608-139">An integer</span></span> 
- <span data-ttu-id="96608-140">0 ile 65535 arasında bir tamsayı aralığı</span><span class="sxs-lookup"><span data-stu-id="96608-140">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="96608-141">Herhangi bir bağlantı noktası ile eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="96608-141">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="96608-142">-Yön</span><span class="sxs-lookup"><span data-stu-id="96608-142">-Direction</span></span>
<span data-ttu-id="96608-143">Kuralın gelen veya giden trafik için değerlendirilip değerlendirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="96608-143">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="96608-144">Bu parametre için kabul edilebilir değerler: gelen ve giden.</span><span class="sxs-lookup"><span data-stu-id="96608-144">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="96608-145">-Ad</span><span class="sxs-lookup"><span data-stu-id="96608-145">-Name</span></span>
<span data-ttu-id="96608-146">Bu cmdlet 'in ayarladığı ağ güvenlik kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="96608-146">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="96608-147">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="96608-147">-NetworkSecurityGroup</span></span>
<span data-ttu-id="96608-148">Ayarlanacak ağ güvenlik kuralı yapılandırmasını içeren **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="96608-148">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="96608-149">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="96608-149">-Priority</span></span>
<span data-ttu-id="96608-150">Kural yapılandırmasının önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="96608-150">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="96608-151">Bu parametre için kabul edilebilir değerler şunlardır: 100 ile 4096 arasında bir tamsayı.</span><span class="sxs-lookup"><span data-stu-id="96608-151">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>

<span data-ttu-id="96608-152">Öncelikteki her kural için öncelik numarası benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="96608-152">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="96608-153">Öncelik numarası düşükse, kuralın önceliği o kadar yüksek olur.</span><span class="sxs-lookup"><span data-stu-id="96608-153">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="96608-154">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="96608-154">-Protocol</span></span>
<span data-ttu-id="96608-155">Kural yapılandırmasının uygulandığı ağ protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="96608-155">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="96608-156">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="96608-156">The acceptable values for this parameter are:</span></span>

 <span data-ttu-id="96608-157">--TCP</span><span class="sxs-lookup"><span data-stu-id="96608-157">--Tcp</span></span>
- <span data-ttu-id="96608-158">UDP</span><span class="sxs-lookup"><span data-stu-id="96608-158">Udp</span></span>
- <span data-ttu-id="96608-159">Her ikisiyle eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="96608-159">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="96608-160">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="96608-160">-SourceAddressPrefix</span></span>
<span data-ttu-id="96608-161">Kaynak adres önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="96608-161">Specifies a source address prefix.</span></span>
<span data-ttu-id="96608-162">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="96608-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="96608-163">CıDR</span><span class="sxs-lookup"><span data-stu-id="96608-163">A CIDR</span></span>
- <span data-ttu-id="96608-164">Kaynak IP aralığı</span><span class="sxs-lookup"><span data-stu-id="96608-164">A source IP range</span></span>
- <span data-ttu-id="96608-165">Herhangi bir IP adresiyle eşleşen joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="96608-165">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="96608-166">VirtualNetwork, AzureLoadBalancer ve Internet gibi etiketleri de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="96608-166">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="96608-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="96608-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="96608-168">Kural için kaynak olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="96608-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="96608-169">' SourceAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="96608-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="96608-170">-Sourceapplicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="96608-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="96608-171">Kural için kaynak olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="96608-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="96608-172">' SourceAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="96608-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="96608-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="96608-173">-SourcePortRange</span></span>
<span data-ttu-id="96608-174">Kaynak bağlantı noktasını veya aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="96608-174">Specifies the source port or range.</span></span>
<span data-ttu-id="96608-175">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="96608-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="96608-176">Bir tamsayı</span><span class="sxs-lookup"><span data-stu-id="96608-176">An integer</span></span>
- <span data-ttu-id="96608-177">0 ile 65535 arasında bir tamsayı aralığı</span><span class="sxs-lookup"><span data-stu-id="96608-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="96608-178">Herhangi bir bağlantı noktası ile eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="96608-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="96608-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96608-179">CommonParameters</span></span>
<span data-ttu-id="96608-180">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="96608-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96608-181">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96608-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96608-182">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="96608-182">INPUTS</span></span>

### <span data-ttu-id="96608-183">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="96608-183">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="96608-184">' NetworkSecurityGroup ' parametresi ardışık düzenin ' PSNetworkSecurityGroup ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="96608-184">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="96608-185">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="96608-185">OUTPUTS</span></span>

### <span data-ttu-id="96608-186">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="96608-186">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="96608-187">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="96608-187">NOTES</span></span>

## <span data-ttu-id="96608-188">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="96608-188">RELATED LINKS</span></span>

[<span data-ttu-id="96608-189">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="96608-189">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="96608-190">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="96608-190">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="96608-191">Yeni-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="96608-191">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="96608-192">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="96608-192">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)


