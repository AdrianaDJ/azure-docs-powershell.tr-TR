---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: c1febd5d39e99ef52e940c590fcd43c24b19affd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593723"
---
# <span data-ttu-id="64f16-101">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64f16-101">Set-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="64f16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64f16-102">SYNOPSIS</span></span>
<span data-ttu-id="64f16-103">Ağ güvenlik kuralı yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="64f16-103">Sets the goal state for a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64f16-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="64f16-104">SYNTAX</span></span>

### <span data-ttu-id="64f16-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="64f16-105">SetByResource (Default)</span></span>
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

### <span data-ttu-id="64f16-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="64f16-106">SetByResourceId</span></span>
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

## <span data-ttu-id="64f16-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="64f16-107">DESCRIPTION</span></span>
<span data-ttu-id="64f16-108">**Set-AzureRmNetworkSecurityRuleConfig** cmdlet 'i, bir Azure ağ güvenlik kuralı yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="64f16-108">The **Set-AzureRmNetworkSecurityRuleConfig** cmdlet sets the goal state for an Azure network security rule configuration.</span></span>

## <span data-ttu-id="64f16-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="64f16-109">EXAMPLES</span></span>

### <span data-ttu-id="64f16-110">Örnek 1: ağ güvenlik kuralında erişim yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="64f16-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="64f16-111">İlk komut NSG-ön uç adlı ağ güvenlik grubunu alır ve bunu değişken $nsg depolar.</span><span class="sxs-lookup"><span data-stu-id="64f16-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>

<span data-ttu-id="64f16-112">İkinci $nsg komut, RDP kuralı adlı güvenlik kuralı yapılandırmasını alan,-AzureRmNetworkSecurityRuleConfig 'i almak</span><span class="sxs-lookup"><span data-stu-id="64f16-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzureRmNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>

<span data-ttu-id="64f16-113">Üçüncü komut, RDP kuralının erişim yapılandırmasını reddedecek şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="64f16-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="64f16-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="64f16-114">PARAMETERS</span></span>

### <span data-ttu-id="64f16-115">-Access</span><span class="sxs-lookup"><span data-stu-id="64f16-115">-Access</span></span>
<span data-ttu-id="64f16-116">Ağ trafiğine izin verilip verilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="64f16-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="64f16-117">Bu parametre için kabul edilebilir değerler: Izin ver ve Reddet.</span><span class="sxs-lookup"><span data-stu-id="64f16-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="64f16-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64f16-118">-DefaultProfile</span></span>
<span data-ttu-id="64f16-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="64f16-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64f16-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="64f16-120">-Description</span></span>
<span data-ttu-id="64f16-121">Kural yapılandırmasının açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64f16-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="64f16-122">Boyut üst sınırı 140 karakterdir.</span><span class="sxs-lookup"><span data-stu-id="64f16-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="64f16-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="64f16-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="64f16-124">Hedef adres önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="64f16-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="64f16-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="64f16-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64f16-126">Sınıfsız Etki alanları arası yönlendirme (CıDR) adresi</span><span class="sxs-lookup"><span data-stu-id="64f16-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="64f16-127">Hedef IP adresi aralığı</span><span class="sxs-lookup"><span data-stu-id="64f16-127">A destination IP address range</span></span> 
- <span data-ttu-id="64f16-128">Herhangi bir IP adresiyle eşleşen joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="64f16-128">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="64f16-129">VirtualNetwork, AzureLoadBalancer ve Internet gibi etiketleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64f16-129">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="64f16-130">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="64f16-130">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="64f16-131">Kural için hedef olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="64f16-131">The application security group set as destination for the rule.</span></span> <span data-ttu-id="64f16-132">' DestinationAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="64f16-132">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="64f16-133">-Destinationapplicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="64f16-133">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="64f16-134">Kural için hedef olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="64f16-134">The application security group set as destination for the rule.</span></span> <span data-ttu-id="64f16-135">' DestinationAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="64f16-135">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="64f16-136">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="64f16-136">-DestinationPortRange</span></span>
<span data-ttu-id="64f16-137">Hedef bir bağlantı noktası veya aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="64f16-137">Specifies a destination port or range.</span></span>
<span data-ttu-id="64f16-138">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="64f16-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64f16-139">Bir tamsayı</span><span class="sxs-lookup"><span data-stu-id="64f16-139">An integer</span></span> 
- <span data-ttu-id="64f16-140">0 ile 65535 arasında bir tamsayı aralığı</span><span class="sxs-lookup"><span data-stu-id="64f16-140">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="64f16-141">Herhangi bir bağlantı noktası ile eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="64f16-141">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="64f16-142">-Yön</span><span class="sxs-lookup"><span data-stu-id="64f16-142">-Direction</span></span>
<span data-ttu-id="64f16-143">Kuralın gelen veya giden trafik için değerlendirilip değerlendirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="64f16-143">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="64f16-144">Bu parametre için kabul edilebilir değerler: gelen ve giden.</span><span class="sxs-lookup"><span data-stu-id="64f16-144">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="64f16-145">-Ad</span><span class="sxs-lookup"><span data-stu-id="64f16-145">-Name</span></span>
<span data-ttu-id="64f16-146">Bu cmdlet 'in ayarladığı ağ güvenlik kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64f16-146">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="64f16-147">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="64f16-147">-NetworkSecurityGroup</span></span>
<span data-ttu-id="64f16-148">Ayarlanacak ağ güvenlik kuralı yapılandırmasını içeren **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="64f16-148">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="64f16-149">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="64f16-149">-Priority</span></span>
<span data-ttu-id="64f16-150">Kural yapılandırmasının önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="64f16-150">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="64f16-151">Bu parametre için kabul edilebilir değerler şunlardır: 100 ile 4096 arasında bir tamsayı.</span><span class="sxs-lookup"><span data-stu-id="64f16-151">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>

<span data-ttu-id="64f16-152">Öncelikteki her kural için öncelik numarası benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="64f16-152">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="64f16-153">Öncelik numarası düşükse, kuralın önceliği o kadar yüksek olur.</span><span class="sxs-lookup"><span data-stu-id="64f16-153">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="64f16-154">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="64f16-154">-Protocol</span></span>
<span data-ttu-id="64f16-155">Kural yapılandırmasının uygulandığı ağ protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="64f16-155">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="64f16-156">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="64f16-156">The acceptable values for this parameter are:</span></span>

 <span data-ttu-id="64f16-157">--TCP</span><span class="sxs-lookup"><span data-stu-id="64f16-157">--Tcp</span></span>
- <span data-ttu-id="64f16-158">UDP</span><span class="sxs-lookup"><span data-stu-id="64f16-158">Udp</span></span>
- <span data-ttu-id="64f16-159">Her ikisiyle eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="64f16-159">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="64f16-160">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="64f16-160">-SourceAddressPrefix</span></span>
<span data-ttu-id="64f16-161">Kaynak adres önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="64f16-161">Specifies a source address prefix.</span></span>
<span data-ttu-id="64f16-162">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="64f16-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64f16-163">CıDR</span><span class="sxs-lookup"><span data-stu-id="64f16-163">A CIDR</span></span>
- <span data-ttu-id="64f16-164">Kaynak IP aralığı</span><span class="sxs-lookup"><span data-stu-id="64f16-164">A source IP range</span></span>
- <span data-ttu-id="64f16-165">Herhangi bir IP adresiyle eşleşen joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="64f16-165">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="64f16-166">VirtualNetwork, AzureLoadBalancer ve Internet gibi etiketleri de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64f16-166">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="64f16-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="64f16-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="64f16-168">Kural için kaynak olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="64f16-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="64f16-169">' SourceAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="64f16-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="64f16-170">-Sourceapplicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="64f16-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="64f16-171">Kural için kaynak olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="64f16-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="64f16-172">' SourceAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="64f16-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="64f16-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="64f16-173">-SourcePortRange</span></span>
<span data-ttu-id="64f16-174">Kaynak bağlantı noktasını veya aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64f16-174">Specifies the source port or range.</span></span>
<span data-ttu-id="64f16-175">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="64f16-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64f16-176">Bir tamsayı</span><span class="sxs-lookup"><span data-stu-id="64f16-176">An integer</span></span>
- <span data-ttu-id="64f16-177">0 ile 65535 arasında bir tamsayı aralığı</span><span class="sxs-lookup"><span data-stu-id="64f16-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="64f16-178">Herhangi bir bağlantı noktası ile eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="64f16-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="64f16-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64f16-179">CommonParameters</span></span>
<span data-ttu-id="64f16-180">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="64f16-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64f16-181">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64f16-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64f16-182">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="64f16-182">INPUTS</span></span>

### <span data-ttu-id="64f16-183">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="64f16-183">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="64f16-184">' NetworkSecurityGroup ' parametresi ardışık düzenin ' PSNetworkSecurityGroup ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="64f16-184">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="64f16-185">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="64f16-185">OUTPUTS</span></span>

### <span data-ttu-id="64f16-186">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="64f16-186">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="64f16-187">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="64f16-187">NOTES</span></span>

## <span data-ttu-id="64f16-188">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="64f16-188">RELATED LINKS</span></span>

[<span data-ttu-id="64f16-189">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64f16-189">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="64f16-190">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64f16-190">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="64f16-191">Yeni-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64f16-191">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="64f16-192">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64f16-192">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)


