---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: c1a8381bd7f8172d972092e0a95bf2b50c6bd585
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935356"
---
# <span data-ttu-id="1f10c-101">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1f10c-101">New-AzVirtualNetwork</span></span>

## <span data-ttu-id="1f10c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f10c-102">SYNOPSIS</span></span>
<span data-ttu-id="1f10c-103">Sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1f10c-103">Creates a virtual network.</span></span>

## <span data-ttu-id="1f10c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f10c-104">SYNTAX</span></span>

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-Subnet <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]>]
 [-Tag <Hashtable>] [-EnableDDoSProtection] [-EnableVmProtection] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f10c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f10c-105">DESCRIPTION</span></span>
<span data-ttu-id="1f10c-106">**New-AzVirtualNetwork** cmdlet 'ı bir Azure sanal ağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1f10c-106">The **New-AzVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="1f10c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f10c-107">EXAMPLES</span></span>

### <span data-ttu-id="1f10c-108">1: iki alt ağla sanal ağ oluşturma</span><span class="sxs-lookup"><span data-stu-id="1f10c-108">1:  Create a virtual network with two subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="1f10c-109">Bu örnek, iki alt ağ içeren bir sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1f10c-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="1f10c-110">İlk olarak, yeni kaynak grubu merkezileştirme bölgesinde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1f10c-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="1f10c-111">Ardından, örnekte iki alt ağın bellekteki gösterimler oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1f10c-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="1f10c-112">New-AzVirtualNetworkSubnetConfig cmdlet 'i sunucu tarafında alt ağ oluşturmaz.</span><span class="sxs-lookup"><span data-stu-id="1f10c-112">The New-AzVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="1f10c-113">Frontenvseçsubnet adındaki bir alt ağ ve backendSubnet adındaki bir alt ağ vardır.</span><span class="sxs-lookup"><span data-stu-id="1f10c-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="1f10c-114">New-AzVirtualNetwork cmdlet 'i, adres öneki ve iki alt ağ olarak CıDR/16 kullanan bir sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1f10c-114">The New-AzVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="1f10c-115">2: DNS ayarlarıyla sanal ağ oluşturma</span><span class="sxs-lookup"><span data-stu-id="1f10c-115">2:  Create a virtual network with DNS settings</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="1f10c-116">Bu örnekte, iki alt ağ ve iki DNS sunucusu içeren bir sanal ağ oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1f10c-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="1f10c-117">Sanal ağda DNS sunucularını belirtmekten dolayı, bu sanal ağa dağıtılan NIC 'Ler/VM 'Ler bu DNS sunucularını varsayılan olarak devralır.</span><span class="sxs-lookup"><span data-stu-id="1f10c-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="1f10c-118">Bu varsayılan değerler NIC düzeyinde bir ayar aracılığıyla NIC başına yazılır.</span><span class="sxs-lookup"><span data-stu-id="1f10c-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="1f10c-119">VNET üzerinde DNS sunucusu belirtilmemişse ve NIC 'ler üzerinde DNS sunucuları yoksa, DNS çözümlemesi için varsayılan Azure DNS sunucuları kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1f10c-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="1f10c-120">3: ağ güvenlik grubuna başvuran bir alt ağla sanal ağ oluşturma</span><span class="sxs-lookup"><span data-stu-id="1f10c-120">3: Create a virtual network with a subnet referencing a network security group</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="1f10c-121">Bu örnek, bir ağ güvenlik grubuna başvuran alt ağlar içeren bir sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1f10c-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="1f10c-122">İlk olarak, örnek oluşturulacak kaynaklar için kapsayıcı olarak bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1f10c-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="1f10c-123">Ardından, gelen RDP erişimine izin veren ancak varsayılan ağ güvenlik grubu kurallarını zorunlu kılan bir ağ güvenliği grubu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1f10c-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="1f10c-124">New-AzVirtualNetworkSubnetConfig cmdlet 'i, hem oluşturulan ağ güvenlik grubuna başvuruda bulunan iki alt ağın bellek içi temsilleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1f10c-124">The New-AzVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="1f10c-125">New-AzVirtualNetwork komutu sanal ağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1f10c-125">The New-AzVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="1f10c-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f10c-126">PARAMETERS</span></span>

### <span data-ttu-id="1f10c-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1f10c-127">-AddressPrefix</span></span>
<span data-ttu-id="1f10c-128">Sanal ağın IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f10c-128">Specifies a range of IP addresses for a virtual network.</span></span>

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

### <span data-ttu-id="1f10c-129">-Iş</span><span class="sxs-lookup"><span data-stu-id="1f10c-129">-AsJob</span></span>
<span data-ttu-id="1f10c-130">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1f10c-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f10c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f10c-131">-DefaultProfile</span></span>
<span data-ttu-id="1f10c-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1f10c-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f10c-133">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="1f10c-133">-DnsServer</span></span>
<span data-ttu-id="1f10c-134">Alt ağın DNS sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f10c-134">Specifies the DNS server for a subnet.</span></span>

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

### <span data-ttu-id="1f10c-135">-EnableDDoSProtection</span><span class="sxs-lookup"><span data-stu-id="1f10c-135">-EnableDDoSProtection</span></span>
<span data-ttu-id="1f10c-136">Vseçdos korumasının etkinleştirilip etkinleştirilmediğini temsil eden bir switch parametresi.</span><span class="sxs-lookup"><span data-stu-id="1f10c-136">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f10c-137">-EnableVmProtection</span><span class="sxs-lookup"><span data-stu-id="1f10c-137">-EnableVmProtection</span></span>
<span data-ttu-id="1f10c-138">VM korumasının etkinleştirilip etkinleştirilmediğini temsil eden bir switch parametresi.</span><span class="sxs-lookup"><span data-stu-id="1f10c-138">A switch parameter which represents if Vm protection is enabled or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f10c-139">-Force</span><span class="sxs-lookup"><span data-stu-id="1f10c-139">-Force</span></span>
<span data-ttu-id="1f10c-140">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="1f10c-140">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1f10c-141">-Konum</span><span class="sxs-lookup"><span data-stu-id="1f10c-141">-Location</span></span>
<span data-ttu-id="1f10c-142">Sanal ağın bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f10c-142">Specifies the region for the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f10c-143">-Ad</span><span class="sxs-lookup"><span data-stu-id="1f10c-143">-Name</span></span>
<span data-ttu-id="1f10c-144">Bu cmdlet 'in oluşturduğu sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f10c-144">Specifies the name of the virtual network that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f10c-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f10c-145">-ResourceGroupName</span></span>
<span data-ttu-id="1f10c-146">Sanal ağı içerecek kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f10c-146">Specifies the name of a resource group to contain the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f10c-147">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="1f10c-147">-Subnet</span></span>
<span data-ttu-id="1f10c-148">Sanal Ağla ilişkilendirilecek alt ağların listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f10c-148">Specifies a list of subnets to associate with the virtual network.</span></span>

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

### <span data-ttu-id="1f10c-149">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1f10c-149">-Tag</span></span>
<span data-ttu-id="1f10c-150">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="1f10c-150">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1f10c-151">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="1f10c-151">For example:</span></span>

<span data-ttu-id="1f10c-152">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="1f10c-152">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f10c-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="1f10c-153">-Confirm</span></span>
<span data-ttu-id="1f10c-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1f10c-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f10c-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f10c-155">-WhatIf</span></span>
<span data-ttu-id="1f10c-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1f10c-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f10c-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1f10c-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f10c-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f10c-158">CommonParameters</span></span>
<span data-ttu-id="1f10c-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f10c-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f10c-160">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f10c-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f10c-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f10c-161">INPUTS</span></span>

## <span data-ttu-id="1f10c-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f10c-162">OUTPUTS</span></span>

### <span data-ttu-id="1f10c-163">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1f10c-163">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="1f10c-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f10c-164">NOTES</span></span>

## <span data-ttu-id="1f10c-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f10c-165">RELATED LINKS</span></span>

[<span data-ttu-id="1f10c-166">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1f10c-166">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="1f10c-167">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1f10c-167">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="1f10c-168">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1f10c-168">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)
