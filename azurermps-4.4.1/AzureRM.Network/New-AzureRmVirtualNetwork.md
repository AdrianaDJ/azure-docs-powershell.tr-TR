---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
ms.openlocfilehash: 7fccc6b16d44e9bd050d40a21a748dbd1d251a06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595144"
---
# <span data-ttu-id="2fbab-101">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2fbab-101">New-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="2fbab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fbab-102">SYNOPSIS</span></span>
<span data-ttu-id="2fbab-103">Sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2fbab-103">Creates a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fbab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2fbab-104">SYNTAX</span></span>

```
New-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-Subnet <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]>]
 [-Tag <Hashtable>] [-EnableDDoSProtection] [-EnableVmProtection] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fbab-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2fbab-105">DESCRIPTION</span></span>
<span data-ttu-id="2fbab-106">**New-AzureRmVirtualNetwork** cmdlet 'ı bir Azure sanal ağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2fbab-106">The **New-AzureRmVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="2fbab-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2fbab-107">EXAMPLES</span></span>

### <span data-ttu-id="2fbab-108">1: iki alt ağla sanal ağ oluşturma</span><span class="sxs-lookup"><span data-stu-id="2fbab-108">1:  Create a virtual network with two subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="2fbab-109">Bu örnek, iki alt ağ içeren bir sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2fbab-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="2fbab-110">İlk olarak, yeni kaynak grubu merkezileştirme bölgesinde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2fbab-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="2fbab-111">Ardından, örnekte iki alt ağın bellekteki gösterimler oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2fbab-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="2fbab-112">New-AzureRmVirtualNetworkSubnetConfig cmdlet 'i sunucu tarafında alt ağ oluşturmaz.</span><span class="sxs-lookup"><span data-stu-id="2fbab-112">The New-AzureRmVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="2fbab-113">Frontenvseçsubnet adındaki bir alt ağ ve backendSubnet adındaki bir alt ağ vardır.</span><span class="sxs-lookup"><span data-stu-id="2fbab-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="2fbab-114">New-AzureRmVirtualNetwork cmdlet 'i, adres öneki ve iki alt ağ olarak CıDR/16 kullanan bir sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2fbab-114">The New-AzureRmVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="2fbab-115">2: DNS ayarlarıyla sanal ağ oluşturma</span><span class="sxs-lookup"><span data-stu-id="2fbab-115">2:  Create a virtual network with DNS settings</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="2fbab-116">Bu örnekte, iki alt ağ ve iki DNS sunucusu içeren bir sanal ağ oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2fbab-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="2fbab-117">Sanal ağda DNS sunucularını belirtmekten dolayı, bu sanal ağa dağıtılan NIC 'Ler/VM 'Ler bu DNS sunucularını varsayılan olarak devralır.</span><span class="sxs-lookup"><span data-stu-id="2fbab-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="2fbab-118">Bu varsayılan değerler NIC düzeyinde bir ayar aracılığıyla NIC başına yazılır.</span><span class="sxs-lookup"><span data-stu-id="2fbab-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="2fbab-119">VNET üzerinde DNS sunucusu belirtilmemişse ve NIC 'ler üzerinde DNS sunucuları yoksa, DNS çözümlemesi için varsayılan Azure DNS sunucuları kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2fbab-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="2fbab-120">3: ağ güvenlik grubuna başvuran bir alt ağla sanal ağ oluşturma</span><span class="sxs-lookup"><span data-stu-id="2fbab-120">3: Create a virtual network with a subnet referencing a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="2fbab-121">Bu örnek, bir ağ güvenlik grubuna başvuran alt ağlar içeren bir sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2fbab-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="2fbab-122">İlk olarak, örnek oluşturulacak kaynaklar için kapsayıcı olarak bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2fbab-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="2fbab-123">Ardından, gelen RDP erişimine izin veren ancak varsayılan ağ güvenlik grubu kurallarını zorunlu kılan bir ağ güvenliği grubu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2fbab-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="2fbab-124">New-AzureRmVirtualNetworkSubnetConfig cmdlet 'i, hem oluşturulan ağ güvenlik grubuna başvuruda bulunan iki alt ağın bellek içi temsilleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2fbab-124">The New-AzureRmVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="2fbab-125">New-AzureRmVirtualNetwork komutu sanal ağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2fbab-125">The New-AzureRmVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="2fbab-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2fbab-126">PARAMETERS</span></span>

### <span data-ttu-id="2fbab-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2fbab-127">-AddressPrefix</span></span>
<span data-ttu-id="2fbab-128">Sanal ağın IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fbab-128">Specifies a range of IP addresses for a virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fbab-129">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="2fbab-129">-DnsServer</span></span>
<span data-ttu-id="2fbab-130">Alt ağın DNS sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fbab-130">Specifies the DNS server for a subnet.</span></span>

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

### <span data-ttu-id="2fbab-131">-EnableVmProtection</span><span class="sxs-lookup"><span data-stu-id="2fbab-131">-EnableVmProtection</span></span>
<span data-ttu-id="2fbab-132">VM korumasının etkinleştirilip etkinleştirilmediğini temsil eden bir switch parametresi.</span><span class="sxs-lookup"><span data-stu-id="2fbab-132">A switch parameter which represents if Vm protection is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fbab-133">-Force</span><span class="sxs-lookup"><span data-stu-id="2fbab-133">-Force</span></span>
<span data-ttu-id="2fbab-134">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="2fbab-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2fbab-135">-Konum</span><span class="sxs-lookup"><span data-stu-id="2fbab-135">-Location</span></span>
<span data-ttu-id="2fbab-136">Sanal ağın bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fbab-136">Specifies the region for the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fbab-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="2fbab-137">-Name</span></span>
<span data-ttu-id="2fbab-138">Bu cmdlet 'in oluşturduğu sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fbab-138">Specifies the name of the virtual network that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fbab-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fbab-139">-ResourceGroupName</span></span>
<span data-ttu-id="2fbab-140">Sanal ağı içerecek kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fbab-140">Specifies the name of a resource group to contain the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fbab-141">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="2fbab-141">-Subnet</span></span>
<span data-ttu-id="2fbab-142">Sanal Ağla ilişkilendirilecek alt ağların listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fbab-142">Specifies a list of subnets to associate with the virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fbab-143">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2fbab-143">-Tag</span></span>
<span data-ttu-id="2fbab-144">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="2fbab-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2fbab-145">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="2fbab-145">For example:</span></span>

<span data-ttu-id="2fbab-146">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="2fbab-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fbab-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="2fbab-147">-Confirm</span></span>
<span data-ttu-id="2fbab-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2fbab-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fbab-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fbab-149">-WhatIf</span></span>
<span data-ttu-id="2fbab-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2fbab-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fbab-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2fbab-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fbab-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fbab-152">-DefaultProfile</span></span>
<span data-ttu-id="2fbab-153">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2fbab-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fbab-154">-EnableDDoSProtection</span><span class="sxs-lookup"><span data-stu-id="2fbab-154">-EnableDDoSProtection</span></span>
<span data-ttu-id="2fbab-155">Vseçdos korumasının etkinleştirilip etkinleştirilmediğini temsil eden bir switch parametresi.</span><span class="sxs-lookup"><span data-stu-id="2fbab-155">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fbab-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fbab-156">CommonParameters</span></span>
<span data-ttu-id="2fbab-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2fbab-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fbab-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fbab-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fbab-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2fbab-159">INPUTS</span></span>

## <span data-ttu-id="2fbab-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2fbab-160">OUTPUTS</span></span>

### <span data-ttu-id="2fbab-161">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2fbab-161">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="2fbab-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2fbab-162">NOTES</span></span>

## <span data-ttu-id="2fbab-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2fbab-163">RELATED LINKS</span></span>

[<span data-ttu-id="2fbab-164">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2fbab-164">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="2fbab-165">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2fbab-165">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="2fbab-166">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2fbab-166">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)
