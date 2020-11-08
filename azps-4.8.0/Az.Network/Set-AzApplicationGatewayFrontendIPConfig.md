---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: b72b072307ee4d8ae304888e2d1b3db4a36be3aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268454"
---
# <span data-ttu-id="16f95-101">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="16f95-101">Set-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="16f95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16f95-102">SYNOPSIS</span></span>
<span data-ttu-id="16f95-103">Ön uç IP adresi yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="16f95-103">Modifies a front-end IP address configuration.</span></span>

## <span data-ttu-id="16f95-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16f95-104">SYNTAX</span></span>

### <span data-ttu-id="16f95-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="16f95-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16f95-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="16f95-106">SetByResource</span></span>
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16f95-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="16f95-107">DESCRIPTION</span></span>
<span data-ttu-id="16f95-108">**Set-Azapplicationgatewayfrontendıconfıg** cmdlet 'i ön uç IP yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="16f95-108">The **Set-AzApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="16f95-109">Uygulama ağ geçidi iki tür ön uç IP adresini destekler:</span><span class="sxs-lookup"><span data-stu-id="16f95-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="16f95-110">Genel IP adresleri</span><span class="sxs-lookup"><span data-stu-id="16f95-110">Public IP addresses</span></span>
- <span data-ttu-id="16f95-111">Yapılandırmanın Iç Yük Dengelemesi (ıLB) kullandığı özel IP adresleri, bir uygulama ağ geçidinin en çok bir genel IP adresi ve bir özel IP adresi olabilir.</span><span class="sxs-lookup"><span data-stu-id="16f95-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="16f95-112">Genel bir IP adresi ve özel bir IP adresi, ön uç IP adresleri olarak ayrı ayrı eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="16f95-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="16f95-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16f95-113">EXAMPLES</span></span>

### <span data-ttu-id="16f95-114">Örnek 1: uygulama ağ geçidinin ön uç IP olarak ortak bir IP ayarlama</span><span class="sxs-lookup"><span data-stu-id="16f95-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="16f95-115">İlk komut ortak IP adresi nesnesi oluşturur ve $PublicIp değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="16f95-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="16f95-116">İkinci komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="16f95-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="16f95-117">Üçüncü komut, $PublicIp depolanan adresi kullanarak $AppGw ağ geçidi için FrontEndIp01 adlı ön uç IP yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="16f95-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="16f95-118">Örnek 2: uygulama ağ geçidinin ön uç IP 'si olarak statik özel bir IP ayarlama</span><span class="sxs-lookup"><span data-stu-id="16f95-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="16f95-119">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki bir sanal ağı alır ve $VNet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="16f95-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="16f95-120">İkinci komut, ilk komuttan $VNet kullanarak Subnet01 adlı bir alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="16f95-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="16f95-121">Üçüncü komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="16f95-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="16f95-122">Dördüncü komut, $Subnet ikinci komuttan ve özel IP adresi 10.0.1.1 kullanarak FrontendIP02 adlı bir ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="16f95-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="16f95-123">Örnek 3: uygulama ağ geçidinin ön uç IP 'si olarak dinamik özel IP ayarlama</span><span class="sxs-lookup"><span data-stu-id="16f95-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="16f95-124">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki bir sanal ağı alır ve $VNet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="16f95-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="16f95-125">İkinci komut, ilk komuttan $VNet kullanarak Subnet01 adlı bir alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="16f95-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="16f95-126">Üçüncü komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="16f95-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="16f95-127">Dördüncü komut, ikinci komuttan $Subnet kullanarak FrontendIP02 adlı bir ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="16f95-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="16f95-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16f95-128">PARAMETERS</span></span>

### <span data-ttu-id="16f95-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16f95-129">-ApplicationGateway</span></span>
<span data-ttu-id="16f95-130">Ön uç IP yapılandırmasının değiştirileceği bir uygulama ağ geçidi nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="16f95-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16f95-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16f95-131">-DefaultProfile</span></span>
<span data-ttu-id="16f95-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="16f95-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f95-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="16f95-133">-Name</span></span>
<span data-ttu-id="16f95-134">Bu cmdlet 'in değiştirdiği ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16f95-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="16f95-135">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="16f95-135">-PrivateIPAddress</span></span>
<span data-ttu-id="16f95-136">Özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="16f95-136">Specifies the private IP address.</span></span>
<span data-ttu-id="16f95-137">Belirtilmişse, bu IP alt ağdan statik olarak ayrılır.</span><span class="sxs-lookup"><span data-stu-id="16f95-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="16f95-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="16f95-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="16f95-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="16f95-139">PrivateLinkConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f95-140">-Privatelinkconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="16f95-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="16f95-141">Privatelinkconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="16f95-141">PrivateLinkConfigurationId</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f95-142">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="16f95-142">-PublicIPAddress</span></span>
<span data-ttu-id="16f95-143">Genel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="16f95-143">Specifies the public IP address.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f95-144">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="16f95-144">-PublicIPAddressId</span></span>
<span data-ttu-id="16f95-145">Genel IP adresinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="16f95-145">Specifies the ID of the public IP address.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f95-146">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="16f95-146">-Subnet</span></span>
<span data-ttu-id="16f95-147">Uygulama ağ geçidinin kullandığı alt ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="16f95-147">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="16f95-148">Ağ Geçidi özel bir IP adresi kullanıyorsa bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="16f95-148">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="16f95-149">*Privateıpaddress* adresi belirtilmişse, bu alt ağa ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="16f95-149">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="16f95-150">*Privateıpaddress* belirtilmemişse, bu alt ağdaki IP adreslerinden biri, uygulama ağ geçidinin ön uç IP adresi olarak dinamik olarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="16f95-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f95-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="16f95-151">-SubnetId</span></span>
<span data-ttu-id="16f95-152">Alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="16f95-152">Specifies the subnet ID.</span></span>
<span data-ttu-id="16f95-153">Ağ Geçidi özel bir IP adresi kullanıyorsa bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="16f95-153">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="16f95-154">*Privateıpaddress* parametresi belirtilmişse, bu alt ağa ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="16f95-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="16f95-155">*Privateıpaddress* belirtilmemişse, bu alt ağdaki IP adreslerinden biri, uygulama ağ geçidinin ön uç IP adresi olarak dinamik olarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="16f95-155">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f95-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16f95-156">CommonParameters</span></span>
<span data-ttu-id="16f95-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16f95-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16f95-158">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="16f95-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16f95-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16f95-159">INPUTS</span></span>

### <span data-ttu-id="16f95-160">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16f95-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="16f95-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16f95-161">OUTPUTS</span></span>

### <span data-ttu-id="16f95-162">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16f95-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="16f95-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16f95-163">NOTES</span></span>

## <span data-ttu-id="16f95-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16f95-164">RELATED LINKS</span></span>

[<span data-ttu-id="16f95-165">Add-Azapplicationgatewayfrontendıconfıg yapılandırması</span><span class="sxs-lookup"><span data-stu-id="16f95-165">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="16f95-166">Add-Azapplicationgatewayfrontendıconfıg yapılandırması</span><span class="sxs-lookup"><span data-stu-id="16f95-166">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="16f95-167">Get-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="16f95-167">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="16f95-168">Yeni-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="16f95-168">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="16f95-169">Remove-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="16f95-169">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)


