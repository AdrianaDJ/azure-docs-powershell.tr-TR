---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 6e041efe4d0ee9ce19522dad0faa8abd2974c9b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760747"
---
# <span data-ttu-id="30ddb-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="30ddb-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="30ddb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30ddb-102">SYNOPSIS</span></span>
<span data-ttu-id="30ddb-103">Uygulama ağ geçidine ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="30ddb-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="30ddb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30ddb-104">SYNTAX</span></span>

### <span data-ttu-id="30ddb-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="30ddb-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30ddb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="30ddb-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30ddb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="30ddb-107">DESCRIPTION</span></span>
<span data-ttu-id="30ddb-108">**Add-Azapplicationgatewayfrontendıconfıg** cmdlet 'i, uygulama ağ geçidine ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="30ddb-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="30ddb-109">Uygulama ağ geçidi iki tür ön uç IP yapılandırmasını destekler:</span><span class="sxs-lookup"><span data-stu-id="30ddb-109">An application gateway supports two types of front-end IP configurations:</span></span> 
- <span data-ttu-id="30ddb-110">Genel IP adresleri</span><span class="sxs-lookup"><span data-stu-id="30ddb-110">Public IP addresses</span></span>
- <span data-ttu-id="30ddb-111">İç Yük Dengelemesi (ıLB) kullanan özel IP adresleri uygulama ağ geçidi 'nin en çok bir genel IP ve bir özel IP adresi olabilir.</span><span class="sxs-lookup"><span data-stu-id="30ddb-111">Private IP addresses using internal load-balancing (ILB) An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="30ddb-112">Genel IP adresini ve özel IP adresini ayrı ön uç IP 'Ler olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="30ddb-112">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="30ddb-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30ddb-113">EXAMPLES</span></span>

### <span data-ttu-id="30ddb-114">Örnek 1: ön uç IP adresi olarak ortak bir IP ekleme</span><span class="sxs-lookup"><span data-stu-id="30ddb-114">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="30ddb-115">İlk komut ortak IP adresi nesnesi oluşturur ve $PublicIp değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="30ddb-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="30ddb-116">İkinci komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="30ddb-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="30ddb-117">Üçüncü komut, $PublicIp depolanan adresi kullanarak $AppGw ağ geçidi için FrontEndIp01 adlı ön uç IP yapılandırmasını ekler.</span><span class="sxs-lookup"><span data-stu-id="30ddb-117">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="30ddb-118">Örnek 2: ön uç IP adresi olarak statik özel bir IP ekleme</span><span class="sxs-lookup"><span data-stu-id="30ddb-118">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="30ddb-119">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki bir sanal ağı alır ve $VNet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="30ddb-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="30ddb-120">İkinci komut, ilk komuttan $VNet kullanarak Subnet01 adlı bir alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="30ddb-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="30ddb-121">Üçüncü komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="30ddb-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="30ddb-122">Dördüncü komut, $Subnet ikinci komuttan ve özel IP adresi 10.0.1.1 kullanarak FrontendIP02 adlı bir ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="30ddb-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="30ddb-123">Örnek 3: ön uç IP adresi olarak dinamik özel IP ekleme</span><span class="sxs-lookup"><span data-stu-id="30ddb-123">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="30ddb-124">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki bir sanal ağı alır ve $VNet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="30ddb-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="30ddb-125">İkinci komut, ilk komuttan $VNet kullanarak Subnet01 adlı bir alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="30ddb-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="30ddb-126">Üçüncü komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="30ddb-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="30ddb-127">Dördüncü komut, ikinci komuttan $Subnet kullanarak FrontendIP02 adlı bir ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="30ddb-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="30ddb-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30ddb-128">PARAMETERS</span></span>

### <span data-ttu-id="30ddb-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30ddb-129">-ApplicationGateway</span></span>
<span data-ttu-id="30ddb-130">Bu cmdlet 'in ön uç IP yapılandırması eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="30ddb-130">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="30ddb-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30ddb-131">-DefaultProfile</span></span>
<span data-ttu-id="30ddb-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="30ddb-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30ddb-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="30ddb-133">-Name</span></span>
<span data-ttu-id="30ddb-134">Eklenecek ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="30ddb-134">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="30ddb-135">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="30ddb-135">-PrivateIPAddress</span></span>
<span data-ttu-id="30ddb-136">Uygulama ağ geçidi için ön uç IP olarak eklenecek özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="30ddb-136">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="30ddb-137">Belirtilmişse, bu IP alt ağdan statik olarak ayrılır.</span><span class="sxs-lookup"><span data-stu-id="30ddb-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="30ddb-138">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="30ddb-138">-PublicIPAddress</span></span>
<span data-ttu-id="30ddb-139">Bu cmdlet 'in uygulama ağ geçidi için ön uç IP adresi olarak eklediği genel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="30ddb-139">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="30ddb-140">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="30ddb-140">-PublicIPAddressId</span></span>
<span data-ttu-id="30ddb-141">Bu cmdlet 'in uygulama ağ geçidi için ön uç IP adresi olarak eklediği genel IP adresinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="30ddb-141">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="30ddb-142">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="30ddb-142">-Subnet</span></span>
<span data-ttu-id="30ddb-143">Bu cmdlet 'in ön uç IP yapılandırması olarak eklediği alt ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="30ddb-143">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="30ddb-144">Bu parametreyi belirtirseniz, uygulama ağ geçidinin özel bir IP tabanlı yapılandırmayı desteklediği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="30ddb-144">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="30ddb-145">*Privateıpaddress* parametresi belirtilmişse, bu alt ağa ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="30ddb-145">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="30ddb-146">*Privateıpaddress* belirtilmemişse, bu alt ağdaki IP adreslerinden biri, uygulama ağ geçidinin ön uç IP adresi olarak dinamik olarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="30ddb-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="30ddb-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="30ddb-147">-SubnetId</span></span>
<span data-ttu-id="30ddb-148">Bu cmdlet 'in ön uç IP yapılandırması olarak eklediği alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="30ddb-148">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="30ddb-149">Alt ağ, özel IP anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="30ddb-149">Passing subnet implies private IP.</span></span>
<span data-ttu-id="30ddb-150">*Privateıpaddresss* parametresi belirtilmişse, bu alt ağa ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="30ddb-150">If the *PrivateIPAddresss* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="30ddb-151">Aksi takdirde, bu alt ağdaki IP 'den biri, uygulama ağ geçidinin ön uç IP 'si olarak dinamik olarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="30ddb-151">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="30ddb-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ddb-152">CommonParameters</span></span>
<span data-ttu-id="30ddb-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30ddb-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30ddb-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30ddb-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30ddb-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30ddb-155">INPUTS</span></span>

### <span data-ttu-id="30ddb-156">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30ddb-156">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="30ddb-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30ddb-157">OUTPUTS</span></span>

### <span data-ttu-id="30ddb-158">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30ddb-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="30ddb-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30ddb-159">NOTES</span></span>

## <span data-ttu-id="30ddb-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30ddb-160">RELATED LINKS</span></span>

[<span data-ttu-id="30ddb-161">Get-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="30ddb-161">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="30ddb-162">Yeni-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="30ddb-162">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="30ddb-163">Remove-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="30ddb-163">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="30ddb-164">Set-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="30ddb-164">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


