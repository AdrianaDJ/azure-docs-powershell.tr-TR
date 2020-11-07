---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 80324e1d6fa87959edb0da8e7aa72f3b2a42a3b6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935638"
---
# <span data-ttu-id="99d4e-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="99d4e-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="99d4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99d4e-102">SYNOPSIS</span></span>
<span data-ttu-id="99d4e-103">Bir yük dengeleyicisine ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="99d4e-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="99d4e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99d4e-104">SYNTAX</span></span>

### <span data-ttu-id="99d4e-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="99d4e-105">SetByResourceSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99d4e-106">Setbyresourceıdsubnet</span><span class="sxs-lookup"><span data-stu-id="99d4e-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99d4e-107">Setbyresourceidpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="99d4e-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99d4e-108">Setbyresourcepublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="99d4e-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99d4e-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="99d4e-109">DESCRIPTION</span></span>
<span data-ttu-id="99d4e-110">**Add-AzLoadBalancerFrontendIpConifg** cmdlet 'ı bir Azure yük dengeleyicisine ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="99d4e-110">The **Add-AzLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="99d4e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99d4e-111">EXAMPLES</span></span>

### <span data-ttu-id="99d4e-112">Örnek 1 dinamik IP adresi olan ön uç IP yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="99d4e-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="99d4e-113">İlk komut MyVnet adlı Azure sanal ağını alır ve MySubnet adlı alt ağı almak için ardışık düzeni **Get-AzVirtualNetworkSubnetConfig** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="99d4e-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="99d4e-114">Bu komut, sonucu $Subnet adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="99d4e-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="99d4e-115">İkinci komut MyLB adındaki yük dengeleyiciyi alır ve sonucu, $MySubnet adlı değişkende depolanan alt ağdan dinamik bir IP adresi içeren bir ön uç IP yapılandırması olan **Add-Azloadbalancerfrontendıconfıg** cmdlet 'ine iletir.</span><span class="sxs-lookup"><span data-stu-id="99d4e-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="99d4e-116">Örnek 2 statik IP adresi olan ön uç IP yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="99d4e-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="99d4e-117">İlk komut MyVnet adlı Azure sanal ağını alır ve MySubnet adlı alt ağı almak için ardışık düzeni **Get-AzVirtualNetworkSubnetConfig** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="99d4e-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="99d4e-118">Bu komut, sonucu $Subnet adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="99d4e-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="99d4e-119">İkinci komut MyLB adındaki yük dengeleyiciyi alır ve sonucu, $Subnet adlı değişkende depolanan alt ağdan statik özel IP adresi olan bir ön uç IP **yapılandırması ekleyerek yük** dengeleyicisine geçirir.</span><span class="sxs-lookup"><span data-stu-id="99d4e-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="99d4e-120">Örnek 3 genel IP adresiyle ön uç IP yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="99d4e-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="99d4e-121">İlk komut, MyPub adlı Azure genel IP adresini alır ve sonucu $PublicIp adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="99d4e-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="99d4e-122">İkinci komut MyLB adındaki yük dengeleyiciyi alır ve sonucu $PublicIp adlı değişkende depolanan genel IP adresiyle yük dengeleyicisine ön uç IP yapılandırması ekleyen **Add-Azloadbalancerfrontendıconfıg** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="99d4e-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="99d4e-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99d4e-123">PARAMETERS</span></span>

### <span data-ttu-id="99d4e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d4e-124">-DefaultProfile</span></span>
<span data-ttu-id="99d4e-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="99d4e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99d4e-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99d4e-126">-LoadBalancer</span></span>
<span data-ttu-id="99d4e-127">**LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="99d4e-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="99d4e-128">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicisine ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="99d4e-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99d4e-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="99d4e-129">-Name</span></span>
<span data-ttu-id="99d4e-130">Eklenecek ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99d4e-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="99d4e-131">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="99d4e-131">-PrivateIpAddress</span></span>
<span data-ttu-id="99d4e-132">Ön uç IP yapılandırmasıyla ilişkilendirilecek özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="99d4e-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d4e-133">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="99d4e-133">-PublicIpAddress</span></span>
<span data-ttu-id="99d4e-134">Ön uç IP yapılandırmasıyla ilişkilendirilecek ortak IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="99d4e-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d4e-135">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="99d4e-135">-PublicIpAddressId</span></span>
<span data-ttu-id="99d4e-136">Ön uç IP yapılandırmasının ekleneceği genel IP adresinin KIMLIĞINI verir.</span><span class="sxs-lookup"><span data-stu-id="99d4e-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d4e-137">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="99d4e-137">-Subnet</span></span>
<span data-ttu-id="99d4e-138">Ön uç IP yapılandırmasının ekleneceği alt ağ nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="99d4e-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d4e-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="99d4e-139">-SubnetId</span></span>
<span data-ttu-id="99d4e-140">Ön uç IP yapılandırmasının ekleneceği alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="99d4e-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d4e-141">-Bölge</span><span class="sxs-lookup"><span data-stu-id="99d4e-141">-Zone</span></span>
<span data-ttu-id="99d4e-142">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="99d4e-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="99d4e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d4e-143">CommonParameters</span></span>
<span data-ttu-id="99d4e-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99d4e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d4e-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99d4e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d4e-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99d4e-146">INPUTS</span></span>

### <span data-ttu-id="99d4e-147">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99d4e-147">PSLoadBalancer</span></span>
<span data-ttu-id="99d4e-148">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="99d4e-148">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="99d4e-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99d4e-149">OUTPUTS</span></span>

### <span data-ttu-id="99d4e-150">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99d4e-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="99d4e-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99d4e-151">NOTES</span></span>

## <span data-ttu-id="99d4e-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99d4e-152">RELATED LINKS</span></span>

[<span data-ttu-id="99d4e-153">Get-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="99d4e-153">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="99d4e-154">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99d4e-154">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="99d4e-155">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="99d4e-155">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="99d4e-156">Yeni-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="99d4e-156">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="99d4e-157">Remove-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="99d4e-157">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="99d4e-158">Set-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="99d4e-158">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


