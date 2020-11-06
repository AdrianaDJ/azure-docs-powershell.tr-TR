---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: e5bbe82276cb356da1e5a66c45145c7daa1d8769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590126"
---
# <span data-ttu-id="31e32-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="31e32-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="31e32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31e32-102">SYNOPSIS</span></span>
<span data-ttu-id="31e32-103">Ön uç IP adresi yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="31e32-103">Modifies a front-end IP address configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31e32-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31e32-104">SYNTAX</span></span>

### <span data-ttu-id="31e32-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="31e32-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31e32-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="31e32-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31e32-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="31e32-107">DESCRIPTION</span></span>
<span data-ttu-id="31e32-108">**Set-AzureRmApplicationGatewayFrontendIPConfig** cmdlet 'i ön uç IP yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="31e32-108">The **Set-AzureRmApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>
<span data-ttu-id="31e32-109">Uygulama ağ geçidi iki tür ön uç IP adresini destekler:</span><span class="sxs-lookup"><span data-stu-id="31e32-109">An application gateway supports two types of front-end IP addresses:</span></span> 
- <span data-ttu-id="31e32-110">Genel IP adresleri</span><span class="sxs-lookup"><span data-stu-id="31e32-110">Public IP addresses</span></span>
- <span data-ttu-id="31e32-111">Yapılandırmanın Iç Yük Dengelemesi (ıLB) kullandığı özel IP adresleri, bir uygulama ağ geçidinin en çok bir genel IP adresi ve bir özel IP adresi olabilir.</span><span class="sxs-lookup"><span data-stu-id="31e32-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB) An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="31e32-112">Genel bir IP adresi ve özel bir IP adresi, ön uç IP adresleri olarak ayrı ayrı eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="31e32-112">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="31e32-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31e32-113">EXAMPLES</span></span>

### <span data-ttu-id="31e32-114">Örnek 1: uygulama ağ geçidinin ön uç IP olarak ortak bir IP ayarlama</span><span class="sxs-lookup"><span data-stu-id="31e32-114">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="31e32-115">İlk komut ortak IP adresi nesnesi oluşturur ve $PublicIp değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="31e32-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="31e32-116">İkinci komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="31e32-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="31e32-117">Üçüncü komut, $PublicIp depolanan adresi kullanarak $AppGw ağ geçidi için FrontEndIp01 adlı ön uç IP yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="31e32-117">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="31e32-118">Örnek 2: uygulama ağ geçidinin ön uç IP 'si olarak statik özel bir IP ayarlama</span><span class="sxs-lookup"><span data-stu-id="31e32-118">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="31e32-119">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki bir sanal ağı alır ve $VNet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="31e32-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="31e32-120">İkinci komut, ilk komuttan $VNet kullanarak Subnet01 adlı bir alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="31e32-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="31e32-121">Üçüncü komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="31e32-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="31e32-122">Dördüncü komut, $Subnet ikinci komuttan ve özel IP adresi 10.0.1.1 kullanarak FrontendIP02 adlı bir ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="31e32-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="31e32-123">Örnek 3: uygulama ağ geçidinin ön uç IP 'si olarak dinamik özel IP ayarlama</span><span class="sxs-lookup"><span data-stu-id="31e32-123">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="31e32-124">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki bir sanal ağı alır ve $VNet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="31e32-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="31e32-125">İkinci komut, ilk komuttan $VNet kullanarak Subnet01 adlı bir alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="31e32-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="31e32-126">Üçüncü komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="31e32-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="31e32-127">Dördüncü komut, ikinci komuttan $Subnet kullanarak FrontendIP02 adlı bir ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="31e32-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="31e32-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31e32-128">PARAMETERS</span></span>

### <span data-ttu-id="31e32-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31e32-129">-ApplicationGateway</span></span>
<span data-ttu-id="31e32-130">Ön uç IP yapılandırmasının değiştirileceği bir uygulama ağ geçidi nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="31e32-130">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

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

### <span data-ttu-id="31e32-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e32-131">-DefaultProfile</span></span>
<span data-ttu-id="31e32-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="31e32-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31e32-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="31e32-133">-Name</span></span>
<span data-ttu-id="31e32-134">Bu cmdlet 'in değiştirdiği ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31e32-134">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="31e32-135">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="31e32-135">-PrivateIPAddress</span></span>
<span data-ttu-id="31e32-136">Özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="31e32-136">Specifies the private IP address.</span></span>
<span data-ttu-id="31e32-137">Belirtilmişse, bu IP alt ağdan statik olarak ayrılır.</span><span class="sxs-lookup"><span data-stu-id="31e32-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="31e32-138">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="31e32-138">-PublicIPAddress</span></span>
<span data-ttu-id="31e32-139">Genel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="31e32-139">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="31e32-140">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="31e32-140">-PublicIPAddressId</span></span>
<span data-ttu-id="31e32-141">Genel IP adresinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="31e32-141">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="31e32-142">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="31e32-142">-Subnet</span></span>
<span data-ttu-id="31e32-143">Uygulama ağ geçidinin kullandığı alt ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="31e32-143">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="31e32-144">Ağ Geçidi özel bir IP adresi kullanıyorsa bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="31e32-144">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="31e32-145">*Privateıpaddress* adresi belirtilmişse, bu alt ağa ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="31e32-145">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="31e32-146">*Privateıpaddress* belirtilmemişse, bu alt ağdaki IP adreslerinden biri, uygulama ağ geçidinin ön uç IP adresi olarak dinamik olarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="31e32-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="31e32-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="31e32-147">-SubnetId</span></span>
<span data-ttu-id="31e32-148">Alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="31e32-148">Specifies the subnet ID.</span></span>
<span data-ttu-id="31e32-149">Ağ Geçidi özel bir IP adresi kullanıyorsa bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="31e32-149">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="31e32-150">*Privateıpaddress* parametresi belirtilmişse, bu alt ağa ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="31e32-150">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="31e32-151">*Privateıpaddress* belirtilmemişse, bu alt ağdaki IP adreslerinden biri, uygulama ağ geçidinin ön uç IP adresi olarak dinamik olarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="31e32-151">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="31e32-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e32-152">CommonParameters</span></span>
<span data-ttu-id="31e32-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31e32-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e32-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31e32-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e32-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31e32-155">INPUTS</span></span>

### <span data-ttu-id="31e32-156">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31e32-156">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="31e32-157">Parametreler: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="31e32-157">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="31e32-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31e32-158">OUTPUTS</span></span>

### <span data-ttu-id="31e32-159">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31e32-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="31e32-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31e32-160">NOTES</span></span>

## <span data-ttu-id="31e32-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31e32-161">RELATED LINKS</span></span>

[<span data-ttu-id="31e32-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="31e32-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="31e32-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="31e32-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="31e32-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="31e32-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="31e32-165">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="31e32-165">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="31e32-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="31e32-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)


