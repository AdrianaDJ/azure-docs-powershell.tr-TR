---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 4b0fd2fd55b255a9734a0c6b0c325f7ac113b4e9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935663"
---
# <span data-ttu-id="839bc-101">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="839bc-101">Add-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="839bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="839bc-102">SYNOPSIS</span></span>
<span data-ttu-id="839bc-103">Uygulama ağ geçidine ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="839bc-103">Adds a front-end IP configuration to an application gateway.</span></span>

## <span data-ttu-id="839bc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="839bc-104">SYNTAX</span></span>

### <span data-ttu-id="839bc-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="839bc-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="839bc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="839bc-106">SetByResource</span></span>
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="839bc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="839bc-107">DESCRIPTION</span></span>
<span data-ttu-id="839bc-108">**Add-Azapplicationgatewayfrontendıconfıg** cmdlet 'i, uygulama ağ geçidine ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="839bc-108">The **Add-AzApplicationGatewayFrontendIPConfig** cmdlet adds a front-end IP configuration to an application gateway.</span></span>
<span data-ttu-id="839bc-109">Uygulama ağ geçidi iki tür ön uç IP yapılandırmasını destekler:</span><span class="sxs-lookup"><span data-stu-id="839bc-109">An application gateway supports two types of front-end IP configurations:</span></span> 

- <span data-ttu-id="839bc-110">Genel IP adresleri</span><span class="sxs-lookup"><span data-stu-id="839bc-110">Public IP addresses</span></span>
- <span data-ttu-id="839bc-111">İç Yük Dengelemesi (ıLB) kullanan özel IP adresleri</span><span class="sxs-lookup"><span data-stu-id="839bc-111">Private IP addresses using internal load-balancing (ILB)</span></span>

<span data-ttu-id="839bc-112">Uygulama ağ geçidi en çok bir genel IP ve bir özel IP olabilir.</span><span class="sxs-lookup"><span data-stu-id="839bc-112">An application gateway can have at most one public IP and one private IP.</span></span>
<span data-ttu-id="839bc-113">Genel IP adresini ve özel IP adresini ayrı ön uç IP 'Ler olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="839bc-113">Add the public IP address and private IP address as separate front-end IPs.</span></span>

## <span data-ttu-id="839bc-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="839bc-114">EXAMPLES</span></span>

### <span data-ttu-id="839bc-115">Örnek 1: ön uç IP adresi olarak ortak bir IP ekleme</span><span class="sxs-lookup"><span data-stu-id="839bc-115">Example 1: Add a public IP as the front-end IP address</span></span>
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="839bc-116">İlk komut ortak IP adresi nesnesi oluşturur ve $PublicIp değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="839bc-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>
<span data-ttu-id="839bc-117">İkinci komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="839bc-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="839bc-118">Üçüncü komut, $PublicIp depolanan adresi kullanarak $AppGw ağ geçidi için FrontEndIp01 adlı ön uç IP yapılandırmasını ekler.</span><span class="sxs-lookup"><span data-stu-id="839bc-118">The third command adds the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="839bc-119">Örnek 2: ön uç IP adresi olarak statik özel bir IP ekleme</span><span class="sxs-lookup"><span data-stu-id="839bc-119">Example 2: Add a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="839bc-120">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki bir sanal ağı alır ve $VNet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="839bc-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="839bc-121">İkinci komut, ilk komuttan $VNet kullanarak Subnet01 adlı bir alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="839bc-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="839bc-122">Üçüncü komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="839bc-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="839bc-123">Dördüncü komut, $Subnet ikinci komuttan ve özel IP adresi 10.0.1.1 kullanarak FrontendIP02 adlı bir ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="839bc-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="839bc-124">Örnek 3: ön uç IP adresi olarak dinamik özel IP ekleme</span><span class="sxs-lookup"><span data-stu-id="839bc-124">Example 3: Add a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="839bc-125">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki bir sanal ağı alır ve $VNet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="839bc-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="839bc-126">İkinci komut, ilk komuttan $VNet kullanarak Subnet01 adlı bir alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="839bc-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="839bc-127">Üçüncü komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="839bc-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="839bc-128">Dördüncü komut, ikinci komuttan $Subnet kullanarak FrontendIP02 adlı bir ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="839bc-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="839bc-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="839bc-129">PARAMETERS</span></span>

### <span data-ttu-id="839bc-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="839bc-130">-ApplicationGateway</span></span>
<span data-ttu-id="839bc-131">Bu cmdlet 'in ön uç IP yapılandırması eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="839bc-131">Specifies the application gateway to which this cmdlet adds a front-end IP configuration.</span></span>

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

### <span data-ttu-id="839bc-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="839bc-132">-DefaultProfile</span></span>
<span data-ttu-id="839bc-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="839bc-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="839bc-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="839bc-134">-Name</span></span>
<span data-ttu-id="839bc-135">Eklenecek ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="839bc-135">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="839bc-136">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="839bc-136">-PrivateIPAddress</span></span>
<span data-ttu-id="839bc-137">Uygulama ağ geçidi için ön uç IP olarak eklenecek özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="839bc-137">Specifies the private IP address to add as a front-end IP for the application gateway.</span></span>
<span data-ttu-id="839bc-138">Belirtilmişse, bu IP alt ağdan statik olarak ayrılır.</span><span class="sxs-lookup"><span data-stu-id="839bc-138">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="839bc-139">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="839bc-139">-PublicIPAddress</span></span>
<span data-ttu-id="839bc-140">Bu cmdlet 'in uygulama ağ geçidi için ön uç IP adresi olarak eklediği genel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="839bc-140">Specifies the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="839bc-141">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="839bc-141">-PublicIPAddressId</span></span>
<span data-ttu-id="839bc-142">Bu cmdlet 'in uygulama ağ geçidi için ön uç IP adresi olarak eklediği genel IP adresinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="839bc-142">Specifies the ID of the public IP address which this cmdlet adds as a front-end IP address for the application gateway.</span></span>

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

### <span data-ttu-id="839bc-143">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="839bc-143">-Subnet</span></span>
<span data-ttu-id="839bc-144">Bu cmdlet 'in ön uç IP yapılandırması olarak eklediği alt ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="839bc-144">Specifies the subnet which this cmdlet adds as front-end IP configuration.</span></span>
<span data-ttu-id="839bc-145">Bu parametreyi belirtirseniz, uygulama ağ geçidinin özel bir IP tabanlı yapılandırmayı desteklediği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="839bc-145">If you specify this parameter, it implies that the application gateway supports a private IP based-configuration.</span></span>
<span data-ttu-id="839bc-146">*Privateıpaddress* parametresi belirtilmişse, bu alt ağa ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="839bc-146">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="839bc-147">*Privateıpaddress* belirtilmemişse, bu alt ağdaki IP adreslerinden biri, uygulama ağ geçidinin ön uç IP adresi olarak dinamik olarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="839bc-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="839bc-148">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="839bc-148">-SubnetId</span></span>
<span data-ttu-id="839bc-149">Bu cmdlet 'in ön uç IP yapılandırması olarak eklediği alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="839bc-149">Specifies the subnet ID which this cmdlet adds as the front-end IP configuration.</span></span>
<span data-ttu-id="839bc-150">Alt ağ, özel IP anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="839bc-150">Passing subnet implies private IP.</span></span>
<span data-ttu-id="839bc-151">*Privateıpaddresss* parametresi belirtilmişse, bu alt ağa ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="839bc-151">If the *PrivateIPAddresss* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="839bc-152">Aksi takdirde, bu alt ağdaki IP 'den biri, uygulama ağ geçidinin ön uç IP 'si olarak dinamik olarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="839bc-152">Otherwise, one of the IP from this subnet is dynamically picked up as the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="839bc-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="839bc-153">CommonParameters</span></span>
<span data-ttu-id="839bc-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="839bc-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="839bc-155">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="839bc-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="839bc-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="839bc-156">INPUTS</span></span>

### <span data-ttu-id="839bc-157">System. String</span><span class="sxs-lookup"><span data-stu-id="839bc-157">System.String</span></span>

## <span data-ttu-id="839bc-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="839bc-158">OUTPUTS</span></span>

### <span data-ttu-id="839bc-159">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="839bc-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="839bc-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="839bc-160">NOTES</span></span>

## <span data-ttu-id="839bc-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="839bc-161">RELATED LINKS</span></span>

[<span data-ttu-id="839bc-162">Get-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="839bc-162">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="839bc-163">Yeni-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="839bc-163">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="839bc-164">Remove-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="839bc-164">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="839bc-165">Set-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="839bc-165">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


