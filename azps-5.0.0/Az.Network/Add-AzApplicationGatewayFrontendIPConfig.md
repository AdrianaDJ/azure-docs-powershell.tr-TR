---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: dadb58348305434294a9a435a136733f0b6ef1e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277278"
---
# <span data-ttu-id="99316-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="99316-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="99316-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99316-102">SYNOPSIS</span></span>
<span data-ttu-id="99316-103">Uygulama ağ geçidine ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="99316-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="99316-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99316-104">SYNTAX</span></span>

### <span data-ttu-id="99316-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="99316-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99316-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="99316-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99316-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="99316-107">DESCRIPTION</span></span>
<span data-ttu-id="99316-108">**Add-Azapplicationgatewayfrontendıconfıg** cmdlet 'i, uygulama ağ geçidine ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="99316-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="99316-109">Uygulama ağ geçidi iki tür ön uç IP yapılandırmasını destekler:</span><span class="sxs-lookup"><span data-stu-id="99316-109">An application gateway supports two types of front-end IP configurations:</span></span> 
- <span data-ttu-id="99316-110">Genel IP adresleri</span><span class="sxs-lookup"><span data-stu-id="99316-110">Public IP addresses</span></span>
- <span data-ttu-id="99316-111">İç Yük Dengelemesi (ıLB) kullanan özel IP adresleri uygulama ağ geçidi 'nin en çok bir genel IP ve bir özel IP adresi olabilir.</span><span class="sxs-lookup"><span data-stu-id="99316-111">Private IP addresses using internal load-balancing (ILB) An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="99316-112">Genel IP adresini ve özel IP adresini ayrı ön uç IP 'Ler olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="99316-112">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="99316-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99316-113">EXAMPLES</span></span>

### <span data-ttu-id="99316-114">Örnek 1: ön uç IP adresi olarak ortak bir IP ekleme</span><span class="sxs-lookup"><span data-stu-id="99316-114">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="99316-115">İlk komut ortak IP adresi nesnesi oluşturur ve $PublicIp değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="99316-115">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="99316-116">İkinci komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="99316-116">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="99316-117">Üçüncü komut, $PublicIp depolanan adresi kullanarak $AppGw ağ geçidi için FrontEndIp01 adlı ön uç IP yapılandırmasını ekler.</span><span class="sxs-lookup"><span data-stu-id="99316-117">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="99316-118">Örnek 2: ön uç IP adresi olarak statik özel bir IP ekleme</span><span class="sxs-lookup"><span data-stu-id="99316-118">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="99316-119">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki bir sanal ağı alır ve $VNet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="99316-119">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="99316-120">İkinci komut, ilk komuttan $VNet kullanarak Subnet01 adlı bir alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="99316-120">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="99316-121">Üçüncü komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="99316-121">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="99316-122">Dördüncü komut, $Subnet ikinci komuttan ve özel IP adresi 10.0.1.1 kullanarak FrontendIP02 adlı bir ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="99316-122">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="99316-123">Örnek 3: ön uç IP adresi olarak dinamik özel IP ekleme</span><span class="sxs-lookup"><span data-stu-id="99316-123">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="99316-124">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki bir sanal ağı alır ve $VNet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="99316-124">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="99316-125">İkinci komut, ilk komuttan $VNet kullanarak Subnet01 adlı bir alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="99316-125">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="99316-126">Üçüncü komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="99316-126">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="99316-127">Dördüncü komut, ikinci komuttan $Subnet kullanarak FrontendIP02 adlı bir ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="99316-127">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="99316-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99316-128">PARAMETERS</span></span>

### <span data-ttu-id="99316-129">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99316-129">-ApplicationGateway</span></span>
<span data-ttu-id="99316-130">Bu cmdlet 'in ön uç IP yapılandırması eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="99316-130">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="99316-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99316-131">-DefaultProfile</span></span>
<span data-ttu-id="99316-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="99316-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99316-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="99316-133">-Name</span></span>
<span data-ttu-id="99316-134">Eklenecek ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99316-134">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="99316-135">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="99316-135">-PrivateIPAddress</span></span>
<span data-ttu-id="99316-136">Uygulama ağ geçidi için ön uç IP olarak eklenecek özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="99316-136">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="99316-137">Belirtilmişse, bu IP alt ağdan statik olarak ayrılır.</span><span class="sxs-lookup"><span data-stu-id="99316-137">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="99316-138">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="99316-138">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="99316-139">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="99316-139">PrivateLinkConfiguration</span></span>

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

### <span data-ttu-id="99316-140">-Privatelinkconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="99316-140">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="99316-141">Privatelinkconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="99316-141">PrivateLinkConfigurationId</span></span>

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

### <span data-ttu-id="99316-142">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="99316-142">-PublicIPAddress</span></span>
<span data-ttu-id="99316-143">Bu cmdlet 'in uygulama ağ geçidi için ön uç IP adresi olarak eklediği genel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="99316-143">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="99316-144">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="99316-144">-PublicIPAddressId</span></span>
<span data-ttu-id="99316-145">Bu cmdlet 'in uygulama ağ geçidi için ön uç IP adresi olarak eklediği genel IP adresinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="99316-145">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="99316-146">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="99316-146">-Subnet</span></span>
<span data-ttu-id="99316-147">Bu cmdlet 'in ön uç IP yapılandırması olarak eklediği alt ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="99316-147">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="99316-148">Bu parametreyi belirtirseniz, uygulama ağ geçidinin özel bir IP tabanlı yapılandırmayı desteklediği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="99316-148">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="99316-149">*Privateıpaddress* parametresi belirtilmişse, bu alt ağa ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="99316-149">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="99316-150">*Privateıpaddress* belirtilmemişse, bu alt ağdaki IP adreslerinden biri, uygulama ağ geçidinin ön uç IP adresi olarak dinamik olarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="99316-150">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="99316-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="99316-151">-SubnetId</span></span>
<span data-ttu-id="99316-152">Bu cmdlet 'in ön uç IP yapılandırması olarak eklediği alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="99316-152">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="99316-153">Alt ağ, özel IP anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="99316-153">Passing subnet implies private IP.</span></span>
<span data-ttu-id="99316-154">*Privateıpaddress* parametresi belirtilmişse, bu alt ağa ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="99316-154">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="99316-155">Aksi takdirde, bu alt ağdaki IP 'den biri, uygulama ağ geçidinin ön uç IP 'si olarak dinamik olarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="99316-155">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="99316-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99316-156">CommonParameters</span></span>
<span data-ttu-id="99316-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99316-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99316-158">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="99316-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99316-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99316-159">INPUTS</span></span>

### <span data-ttu-id="99316-160">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99316-160">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="99316-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99316-161">OUTPUTS</span></span>

### <span data-ttu-id="99316-162">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99316-162">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="99316-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99316-163">NOTES</span></span>

## <span data-ttu-id="99316-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99316-164">RELATED LINKS</span></span>

[<span data-ttu-id="99316-165">Get-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="99316-165">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="99316-166">Yeni-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="99316-166">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="99316-167">Remove-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="99316-167">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="99316-168">Set-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="99316-168">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


