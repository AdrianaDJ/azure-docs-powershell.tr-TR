---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 1abb59c6f610182e14bdf9483610cdb9bbbb66bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765142"
---
# <span data-ttu-id="99045-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="99045-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="99045-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99045-102">SYNOPSIS</span></span>
<span data-ttu-id="99045-103">Ön uç IP adresi yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="99045-103">Modifies a front-end IP address configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99045-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99045-104">SYNTAX</span></span>

### <span data-ttu-id="99045-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="99045-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99045-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="99045-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99045-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="99045-107">DESCRIPTION</span></span>
<span data-ttu-id="99045-108">**Set-AzureRmApplicationGatewayFrontendIPConfig** cmdlet 'i ön uç IP yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="99045-108">The **Set-AzureRmApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>

<span data-ttu-id="99045-109">Uygulama ağ geçidi iki tür ön uç IP adresini destekler:</span><span class="sxs-lookup"><span data-stu-id="99045-109">An application gateway supports two types of front-end IP addresses:</span></span> 

- <span data-ttu-id="99045-110">Genel IP adresleri</span><span class="sxs-lookup"><span data-stu-id="99045-110">Public IP addresses</span></span>
- <span data-ttu-id="99045-111">Yapılandırmanın Iç yük dengelemesi kullandığı özel IP adresleri (ıLB)</span><span class="sxs-lookup"><span data-stu-id="99045-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB)</span></span>

<span data-ttu-id="99045-112">Uygulama ağ geçidi en çok bir genel IP adresi ve bir özel IP adresi içerebilir.</span><span class="sxs-lookup"><span data-stu-id="99045-112">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="99045-113">Genel bir IP adresi ve özel bir IP adresi, ön uç IP adresleri olarak ayrı ayrı eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="99045-113">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="99045-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99045-114">EXAMPLES</span></span>

### <span data-ttu-id="99045-115">Örnek 1: uygulama ağ geçidinin ön uç IP olarak ortak bir IP ayarlama</span><span class="sxs-lookup"><span data-stu-id="99045-115">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="99045-116">İlk komut ortak IP adresi nesnesi oluşturur ve $PublicIp değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="99045-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>

<span data-ttu-id="99045-117">İkinci komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="99045-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="99045-118">Üçüncü komut, $PublicIp depolanan adresi kullanarak $AppGw ağ geçidi için FrontEndIp01 adlı ön uç IP yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="99045-118">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="99045-119">Örnek 2: uygulama ağ geçidinin ön uç IP 'si olarak statik özel bir IP ayarlama</span><span class="sxs-lookup"><span data-stu-id="99045-119">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="99045-120">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki bir sanal ağı alır ve $VNet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="99045-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="99045-121">İkinci komut, ilk komuttan $VNet kullanarak Subnet01 adlı bir alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="99045-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="99045-122">Üçüncü komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="99045-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="99045-123">Dördüncü komut, $Subnet ikinci komuttan ve özel IP adresi 10.0.1.1 kullanarak FrontendIP02 adlı bir ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="99045-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="99045-124">Örnek 3: uygulama ağ geçidinin ön uç IP 'si olarak dinamik özel IP ayarlama</span><span class="sxs-lookup"><span data-stu-id="99045-124">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="99045-125">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki bir sanal ağı alır ve $VNet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="99045-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="99045-126">İkinci komut, ilk komuttan $VNet kullanarak Subnet01 adlı bir alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="99045-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="99045-127">Üçüncü komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="99045-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="99045-128">Dördüncü komut, ikinci komuttan $Subnet kullanarak FrontendIP02 adlı bir ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="99045-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="99045-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99045-129">PARAMETERS</span></span>

### <span data-ttu-id="99045-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99045-130">-ApplicationGateway</span></span>
<span data-ttu-id="99045-131">Ön uç IP yapılandırmasının değiştirileceği bir uygulama ağ geçidi nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="99045-131">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99045-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="99045-132">-Name</span></span>
<span data-ttu-id="99045-133">Bu cmdlet 'in değiştirdiği ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99045-133">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="99045-134">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="99045-134">-PrivateIPAddress</span></span>
<span data-ttu-id="99045-135">Özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="99045-135">Specifies the private IP address.</span></span>
<span data-ttu-id="99045-136">Belirtilmişse, bu IP alt ağdan statik olarak ayrılır.</span><span class="sxs-lookup"><span data-stu-id="99045-136">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="99045-137">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="99045-137">-PublicIPAddress</span></span>
<span data-ttu-id="99045-138">Genel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="99045-138">Specifies the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99045-139">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="99045-139">-PublicIPAddressId</span></span>
<span data-ttu-id="99045-140">Genel IP adresinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="99045-140">Specifies the ID of the public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99045-141">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="99045-141">-Subnet</span></span>
<span data-ttu-id="99045-142">Uygulama ağ geçidinin kullandığı alt ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="99045-142">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="99045-143">Ağ Geçidi özel bir IP adresi kullanıyorsa bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="99045-143">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="99045-144">*Privateıpaddress* adresi belirtilmişse, bu alt ağa ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="99045-144">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="99045-145">*Privateıpaddress* belirtilmemişse, bu alt ağdaki IP adreslerinden biri, uygulama ağ geçidinin ön uç IP adresi olarak dinamik olarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="99045-145">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99045-146">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="99045-146">-SubnetId</span></span>
<span data-ttu-id="99045-147">Alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="99045-147">Specifies the subnet ID.</span></span>
<span data-ttu-id="99045-148">Ağ Geçidi özel bir IP adresi kullanıyorsa bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="99045-148">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="99045-149">*Privateıpaddress* parametresi belirtilmişse, bu alt ağa ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="99045-149">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="99045-150">*Privateıpaddress* belirtilmemişse, bu alt ağdaki IP adreslerinden biri, uygulama ağ geçidinin ön uç IP adresi olarak dinamik olarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="99045-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99045-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99045-151">-DefaultProfile</span></span>
<span data-ttu-id="99045-152">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="99045-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99045-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99045-153">CommonParameters</span></span>
<span data-ttu-id="99045-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99045-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99045-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99045-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99045-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99045-156">INPUTS</span></span>

### <span data-ttu-id="99045-157">System. String</span><span class="sxs-lookup"><span data-stu-id="99045-157">System.String</span></span>

## <span data-ttu-id="99045-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99045-158">OUTPUTS</span></span>

### <span data-ttu-id="99045-159">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99045-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="99045-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99045-160">NOTES</span></span>

## <span data-ttu-id="99045-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99045-161">RELATED LINKS</span></span>

[<span data-ttu-id="99045-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="99045-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="99045-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="99045-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="99045-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="99045-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="99045-165">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="99045-165">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="99045-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="99045-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)


