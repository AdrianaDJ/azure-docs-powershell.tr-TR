---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: abcf1665f6117d12ad99e48e8fd15d0a350c1d96
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940011"
---
# <span data-ttu-id="87680-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="87680-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="87680-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87680-102">SYNOPSIS</span></span>
<span data-ttu-id="87680-103">Ön uç IP adresi yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="87680-103">Modifies a front-end IP address configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87680-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87680-104">SYNTAX</span></span>

### <span data-ttu-id="87680-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="87680-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87680-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="87680-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87680-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="87680-107">DESCRIPTION</span></span>
<span data-ttu-id="87680-108">**Set-AzureRmApplicationGatewayFrontendIPConfig** cmdlet 'i ön uç IP yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="87680-108">The **Set-AzureRmApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>

<span data-ttu-id="87680-109">Uygulama ağ geçidi iki tür ön uç IP adresini destekler:</span><span class="sxs-lookup"><span data-stu-id="87680-109">An application gateway supports two types of front-end IP addresses:</span></span> 

- <span data-ttu-id="87680-110">Genel IP adresleri</span><span class="sxs-lookup"><span data-stu-id="87680-110">Public IP addresses</span></span>
- <span data-ttu-id="87680-111">Yapılandırmanın Iç yük dengelemesi kullandığı özel IP adresleri (ıLB)</span><span class="sxs-lookup"><span data-stu-id="87680-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB)</span></span>

<span data-ttu-id="87680-112">Uygulama ağ geçidi en çok bir genel IP adresi ve bir özel IP adresi içerebilir.</span><span class="sxs-lookup"><span data-stu-id="87680-112">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="87680-113">Genel bir IP adresi ve özel bir IP adresi, ön uç IP adresleri olarak ayrı ayrı eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="87680-113">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="87680-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87680-114">EXAMPLES</span></span>

### <span data-ttu-id="87680-115">Örnek 1: uygulama ağ geçidinin ön uç IP olarak ortak bir IP ayarlama</span><span class="sxs-lookup"><span data-stu-id="87680-115">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="87680-116">İlk komut ortak IP adresi nesnesi oluşturur ve $PublicIp değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="87680-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>

<span data-ttu-id="87680-117">İkinci komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="87680-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="87680-118">Üçüncü komut, $PublicIp depolanan adresi kullanarak $AppGw ağ geçidi için FrontEndIp01 adlı ön uç IP yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="87680-118">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="87680-119">Örnek 2: uygulama ağ geçidinin ön uç IP 'si olarak statik özel bir IP ayarlama</span><span class="sxs-lookup"><span data-stu-id="87680-119">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="87680-120">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki bir sanal ağı alır ve $VNet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="87680-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="87680-121">İkinci komut, ilk komuttan $VNet kullanarak Subnet01 adlı bir alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="87680-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="87680-122">Üçüncü komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="87680-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="87680-123">Dördüncü komut, $Subnet ikinci komuttan ve özel IP adresi 10.0.1.1 kullanarak FrontendIP02 adlı bir ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="87680-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="87680-124">Örnek 3: uygulama ağ geçidinin ön uç IP 'si olarak dinamik özel IP ayarlama</span><span class="sxs-lookup"><span data-stu-id="87680-124">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="87680-125">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki bir sanal ağı alır ve $VNet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="87680-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="87680-126">İkinci komut, ilk komuttan $VNet kullanarak Subnet01 adlı bir alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="87680-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="87680-127">Üçüncü komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="87680-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="87680-128">Dördüncü komut, ikinci komuttan $Subnet kullanarak FrontendIP02 adlı bir ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="87680-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="87680-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87680-129">PARAMETERS</span></span>

### <span data-ttu-id="87680-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="87680-130">-ApplicationGateway</span></span>
<span data-ttu-id="87680-131">Ön uç IP yapılandırmasının değiştirileceği bir uygulama ağ geçidi nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="87680-131">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="87680-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87680-132">-DefaultProfile</span></span>
<span data-ttu-id="87680-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="87680-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87680-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="87680-134">-Name</span></span>
<span data-ttu-id="87680-135">Bu cmdlet 'in değiştirdiği ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87680-135">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="87680-136">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="87680-136">-PrivateIPAddress</span></span>
<span data-ttu-id="87680-137">Özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87680-137">Specifies the private IP address.</span></span>
<span data-ttu-id="87680-138">Belirtilmişse, bu IP alt ağdan statik olarak ayrılır.</span><span class="sxs-lookup"><span data-stu-id="87680-138">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="87680-139">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="87680-139">-PublicIPAddress</span></span>
<span data-ttu-id="87680-140">Genel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87680-140">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="87680-141">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="87680-141">-PublicIPAddressId</span></span>
<span data-ttu-id="87680-142">Genel IP adresinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="87680-142">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="87680-143">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="87680-143">-Subnet</span></span>
<span data-ttu-id="87680-144">Uygulama ağ geçidinin kullandığı alt ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="87680-144">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="87680-145">Ağ Geçidi özel bir IP adresi kullanıyorsa bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="87680-145">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="87680-146">*Privateıpaddress* adresi belirtilmişse, bu alt ağa ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="87680-146">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="87680-147">*Privateıpaddress* belirtilmemişse, bu alt ağdaki IP adreslerinden biri, uygulama ağ geçidinin ön uç IP adresi olarak dinamik olarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="87680-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="87680-148">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="87680-148">-SubnetId</span></span>
<span data-ttu-id="87680-149">Alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="87680-149">Specifies the subnet ID.</span></span>
<span data-ttu-id="87680-150">Ağ Geçidi özel bir IP adresi kullanıyorsa bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="87680-150">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="87680-151">*Privateıpaddress* parametresi belirtilmişse, bu alt ağa ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="87680-151">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="87680-152">*Privateıpaddress* belirtilmemişse, bu alt ağdaki IP adreslerinden biri, uygulama ağ geçidinin ön uç IP adresi olarak dinamik olarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="87680-152">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="87680-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87680-153">CommonParameters</span></span>
<span data-ttu-id="87680-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87680-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87680-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87680-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87680-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87680-156">INPUTS</span></span>

### <span data-ttu-id="87680-157">System. String</span><span class="sxs-lookup"><span data-stu-id="87680-157">System.String</span></span>

## <span data-ttu-id="87680-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87680-158">OUTPUTS</span></span>

### <span data-ttu-id="87680-159">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="87680-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="87680-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87680-160">NOTES</span></span>

## <span data-ttu-id="87680-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87680-161">RELATED LINKS</span></span>

[<span data-ttu-id="87680-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="87680-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="87680-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="87680-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="87680-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="87680-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="87680-165">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="87680-165">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="87680-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="87680-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)


