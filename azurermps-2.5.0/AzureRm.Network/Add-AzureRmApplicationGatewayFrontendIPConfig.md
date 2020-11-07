---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: 646aaa2ec5d39089627caa97e74990ac3ce43b5c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939539"
---
# <span data-ttu-id="521c4-101">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="521c4-101">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="521c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="521c4-102">SYNOPSIS</span></span>
<span data-ttu-id="521c4-103">Uygulama ağ geçidine ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="521c4-103">Adds a front-end IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="521c4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="521c4-104">SYNTAX</span></span>

### <span data-ttu-id="521c4-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="521c4-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="521c4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="521c4-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="521c4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="521c4-107">DESCRIPTION</span></span>
<span data-ttu-id="521c4-108">**Add-AzureRmApplicationGatewayFrontendIPConfig** cmdlet 'i uygulama ağ geçidine ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="521c4-108">The **Add-AzureRmApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="521c4-109">Uygulama ağ geçidi iki tür ön uç IP yapılandırmasını destekler:</span><span class="sxs-lookup"><span data-stu-id="521c4-109">An application gateway supports two types of front-end IP configurations:</span></span> 

- <span data-ttu-id="521c4-110">Genel IP adresleri</span><span class="sxs-lookup"><span data-stu-id="521c4-110">Public IP addresses</span></span>
- <span data-ttu-id="521c4-111">İç Yük Dengelemesi (ıLB) kullanan özel IP adresleri</span><span class="sxs-lookup"><span data-stu-id="521c4-111">Private IP addresses using internal load-balancing (ILB)</span></span>

<span data-ttu-id="521c4-112">Uygulama ağ geçidi en çok bir genel IP ve bir özel IP olabilir.</span><span class="sxs-lookup"><span data-stu-id="521c4-112">An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="521c4-113">Genel IP adresini ve özel IP adresini ayrı ön uç IP 'Ler olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="521c4-113">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="521c4-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="521c4-114">EXAMPLES</span></span>

### <span data-ttu-id="521c4-115">Örnek 1: ön uç IP adresi olarak ortak bir IP ekleme</span><span class="sxs-lookup"><span data-stu-id="521c4-115">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="521c4-116">İlk komut ortak IP adresi nesnesi oluşturur ve $PublicIp değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="521c4-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="521c4-117">İkinci komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="521c4-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="521c4-118">Üçüncü komut, $PublicIp depolanan adresi kullanarak $AppGw ağ geçidi için FrontEndIp01 adlı ön uç IP yapılandırmasını ekler.</span><span class="sxs-lookup"><span data-stu-id="521c4-118">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="521c4-119">Örnek 2: ön uç IP adresi olarak statik özel bir IP ekleme</span><span class="sxs-lookup"><span data-stu-id="521c4-119">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="521c4-120">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki bir sanal ağı alır ve $VNet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="521c4-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="521c4-121">İkinci komut, ilk komuttan $VNet kullanarak Subnet01 adlı bir alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="521c4-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="521c4-122">Üçüncü komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="521c4-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="521c4-123">Dördüncü komut, $Subnet ikinci komuttan ve özel IP adresi 10.0.1.1 kullanarak FrontendIP02 adlı bir ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="521c4-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="521c4-124">Örnek 3: ön uç IP adresi olarak dinamik özel IP ekleme</span><span class="sxs-lookup"><span data-stu-id="521c4-124">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="521c4-125">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki bir sanal ağı alır ve $VNet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="521c4-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="521c4-126">İkinci komut, ilk komuttan $VNet kullanarak Subnet01 adlı bir alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="521c4-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="521c4-127">Üçüncü komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="521c4-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="521c4-128">Dördüncü komut, ikinci komuttan $Subnet kullanarak FrontendIP02 adlı bir ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="521c4-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="521c4-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="521c4-129">PARAMETERS</span></span>

### <span data-ttu-id="521c4-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="521c4-130">-ApplicationGateway</span></span>
<span data-ttu-id="521c4-131">Bu cmdlet 'in ön uç IP yapılandırması eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="521c4-131">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="521c4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="521c4-132">-DefaultProfile</span></span>
<span data-ttu-id="521c4-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="521c4-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="521c4-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="521c4-134">-Name</span></span>
<span data-ttu-id="521c4-135">Eklenecek ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="521c4-135">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="521c4-136">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="521c4-136">-PrivateIPAddress</span></span>
<span data-ttu-id="521c4-137">Uygulama ağ geçidi için ön uç IP olarak eklenecek özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="521c4-137">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="521c4-138">Belirtilmişse, bu IP alt ağdan statik olarak ayrılır.</span><span class="sxs-lookup"><span data-stu-id="521c4-138">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="521c4-139">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="521c4-139">-PublicIPAddress</span></span>
<span data-ttu-id="521c4-140">Bu cmdlet 'in uygulama ağ geçidi için ön uç IP adresi olarak eklediği genel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="521c4-140">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="521c4-141">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="521c4-141">-PublicIPAddressId</span></span>
<span data-ttu-id="521c4-142">Bu cmdlet 'in uygulama ağ geçidi için ön uç IP adresi olarak eklediği genel IP adresinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="521c4-142">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="521c4-143">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="521c4-143">-Subnet</span></span>
<span data-ttu-id="521c4-144">Bu cmdlet 'in ön uç IP yapılandırması olarak eklediği alt ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="521c4-144">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="521c4-145">Bu parametreyi belirtirseniz, uygulama ağ geçidinin özel bir IP tabanlı yapılandırmayı desteklediği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="521c4-145">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="521c4-146">*Privateıpaddress* parametresi belirtilmişse, bu alt ağa ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="521c4-146">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="521c4-147">*Privateıpaddress* belirtilmemişse, bu alt ağdaki IP adreslerinden biri, uygulama ağ geçidinin ön uç IP adresi olarak dinamik olarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="521c4-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="521c4-148">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="521c4-148">-SubnetId</span></span>
<span data-ttu-id="521c4-149">Bu cmdlet 'in ön uç IP yapılandırması olarak eklediği alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="521c4-149">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="521c4-150">Alt ağ, özel IP anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="521c4-150">Passing subnet implies private IP.</span></span>
<span data-ttu-id="521c4-151">*Privateıpaddresss* parametresi belirtilmişse, bu alt ağa ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="521c4-151">If the *PrivateIPAddresss* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="521c4-152">Aksi takdirde, bu alt ağdaki IP 'den biri, uygulama ağ geçidinin ön uç IP 'si olarak dinamik olarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="521c4-152">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="521c4-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="521c4-153">CommonParameters</span></span>
<span data-ttu-id="521c4-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="521c4-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="521c4-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="521c4-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="521c4-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="521c4-156">INPUTS</span></span>

### <span data-ttu-id="521c4-157">System. String</span><span class="sxs-lookup"><span data-stu-id="521c4-157">System.String</span></span>

## <span data-ttu-id="521c4-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="521c4-158">OUTPUTS</span></span>

### <span data-ttu-id="521c4-159">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="521c4-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="521c4-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="521c4-160">NOTES</span></span>

## <span data-ttu-id="521c4-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="521c4-161">RELATED LINKS</span></span>

[<span data-ttu-id="521c4-162">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="521c4-162">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="521c4-163">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="521c4-163">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="521c4-164">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="521c4-164">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="521c4-165">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="521c4-165">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


