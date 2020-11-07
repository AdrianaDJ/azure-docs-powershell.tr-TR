---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 026e9a5bcad55312156be4a14eea238c063b9caa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763358"
---
# <span data-ttu-id="1ce81-101">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1ce81-101">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="1ce81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ce81-102">SYNOPSIS</span></span>
<span data-ttu-id="1ce81-103">Bir yük dengeleyicisine ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="1ce81-103">Adds a front-end IP configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ce81-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ce81-104">SYNTAX</span></span>

### <span data-ttu-id="1ce81-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="1ce81-105">SetByResourceSubnet</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ce81-106">Setbyresourceıdsubnet</span><span class="sxs-lookup"><span data-stu-id="1ce81-106">SetByResourceIdSubnet</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ce81-107">Setbyresourceidpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="1ce81-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ce81-108">Setbyresourcepublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="1ce81-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ce81-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ce81-109">DESCRIPTION</span></span>
<span data-ttu-id="1ce81-110">**Add-AzureRmLoadBalancerFrontendIpConifg** cmdlet 'ı bir Azure yük dengeleyicisine ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="1ce81-110">The **Add-AzureRmLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="1ce81-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ce81-111">EXAMPLES</span></span>

### <span data-ttu-id="1ce81-112">Örnek 1 dinamik IP adresi olan ön uç IP yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="1ce81-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzureRmLoadBalancer
```

<span data-ttu-id="1ce81-113">İlk komut MyVnet adlı Azure sanal ağını alır ve MySubnet adlı alt ağı almak için kanalı kullanarak **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet 'ine geçer.</span><span class="sxs-lookup"><span data-stu-id="1ce81-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="1ce81-114">Bu komut, sonucu $Subnet adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="1ce81-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="1ce81-115">İkinci komut MyLB adındaki yük dengeleyiciyi alır ve sonucu, $MySubnet adlı değişkende depolanan alt ağdan dinamik özel IP adresiyle yük dengeleyiciden bir ön uç IP yapılandırması ekleyen **Add-Azurermloadbalancerfrontendıconfıg** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="1ce81-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="1ce81-116">Örnek 2 statik IP adresi olan ön uç IP yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="1ce81-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="1ce81-117">İlk komut MyVnet adlı Azure sanal ağını alır ve MySubnet adlı alt ağı almak için kanalı kullanarak **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet 'ine geçer.</span><span class="sxs-lookup"><span data-stu-id="1ce81-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="1ce81-118">Bu komut, sonucu $Subnet adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="1ce81-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="1ce81-119">İkinci komut MyLB adındaki yük dengeleyiciyi alır ve sonucu, $Subnet adlı değişkende depolanan alt ağdan statik özel IP adresiyle yük dengeleyiciden bir ön uç IP yapılandırması ekleyen **Add-Azurermloadbalancerfrontendıconfıg** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="1ce81-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="1ce81-120">Örnek 3 genel IP adresiyle ön uç IP yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="1ce81-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzureRmPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzureRmLoadBalancer
```

<span data-ttu-id="1ce81-121">İlk komut, MyPub adlı Azure genel IP adresini alır ve sonucu $PublicIp adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="1ce81-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="1ce81-122">İkinci komut MyLB adındaki yük dengeleyiciyi alır ve sonucu $PublicIp adlı değişkende depolanan genel IP adresiyle yük dengeleyicisine ön uç IP yapılandırması ekleyen **Add-Azurermloadbalancerfrontendıconfıg** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="1ce81-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="1ce81-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ce81-123">PARAMETERS</span></span>

### <span data-ttu-id="1ce81-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ce81-124">-DefaultProfile</span></span>
<span data-ttu-id="1ce81-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1ce81-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ce81-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1ce81-126">-LoadBalancer</span></span>
<span data-ttu-id="1ce81-127">**LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ce81-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="1ce81-128">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicisine ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="1ce81-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce81-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="1ce81-129">-Name</span></span>
<span data-ttu-id="1ce81-130">Eklenecek ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ce81-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="1ce81-131">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="1ce81-131">-PrivateIpAddress</span></span>
<span data-ttu-id="1ce81-132">Ön uç IP yapılandırmasıyla ilişkilendirilecek özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ce81-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ce81-133">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="1ce81-133">-PublicIpAddress</span></span>
<span data-ttu-id="1ce81-134">Ön uç IP yapılandırmasıyla ilişkilendirilecek ortak IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ce81-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ce81-135">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="1ce81-135">-PublicIpAddressId</span></span>
<span data-ttu-id="1ce81-136">Ön uç IP yapılandırmasının ekleneceği genel IP adresinin KIMLIĞINI verir.</span><span class="sxs-lookup"><span data-stu-id="1ce81-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ce81-137">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="1ce81-137">-Subnet</span></span>
<span data-ttu-id="1ce81-138">Ön uç IP yapılandırmasının ekleneceği alt ağ nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ce81-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ce81-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1ce81-139">-SubnetId</span></span>
<span data-ttu-id="1ce81-140">Ön uç IP yapılandırmasının ekleneceği alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ce81-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ce81-141">-Bölge</span><span class="sxs-lookup"><span data-stu-id="1ce81-141">-Zone</span></span>
<span data-ttu-id="1ce81-142">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="1ce81-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="1ce81-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ce81-143">CommonParameters</span></span>
<span data-ttu-id="1ce81-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ce81-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ce81-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ce81-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ce81-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ce81-146">INPUTS</span></span>

### <span data-ttu-id="1ce81-147">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1ce81-147">PSLoadBalancer</span></span>
<span data-ttu-id="1ce81-148">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1ce81-148">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="1ce81-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ce81-149">OUTPUTS</span></span>

### <span data-ttu-id="1ce81-150">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1ce81-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1ce81-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ce81-151">NOTES</span></span>

## <span data-ttu-id="1ce81-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ce81-152">RELATED LINKS</span></span>

[<span data-ttu-id="1ce81-153">Get-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="1ce81-153">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1ce81-154">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1ce81-154">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="1ce81-155">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1ce81-155">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="1ce81-156">Yeni-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="1ce81-156">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1ce81-157">Remove-Azurermloadbalancerfrontendıconfig</span><span class="sxs-lookup"><span data-stu-id="1ce81-157">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1ce81-158">Set-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="1ce81-158">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


