---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 2ffd1d0a0ab3542636a2deec134d5bd233fd8ffa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918344"
---
# <span data-ttu-id="20936-101">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="20936-101">New-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="20936-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20936-102">SYNOPSIS</span></span>
<span data-ttu-id="20936-103">Uygulama ağ geçidi için ön uç IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="20936-103">Creates a front-end IP configuration for an application gateway.</span></span>

## <span data-ttu-id="20936-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="20936-104">SYNTAX</span></span>

### <span data-ttu-id="20936-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="20936-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20936-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="20936-106">SetByResource</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20936-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="20936-107">DESCRIPTION</span></span>
<span data-ttu-id="20936-108">**Yeni-Azapplicationgatewayfrontendıconfıg** cmdlet 'i, bir Azure Application Gateway için ön uç IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="20936-108">The **New-AzApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuration for an Azure application gateway.</span></span>
<span data-ttu-id="20936-109">Uygulama ağ geçidi iki tür ön uç IP yapılandırmasını destekler:</span><span class="sxs-lookup"><span data-stu-id="20936-109">An application gateway supports two types of front-end IP configuration:</span></span> 
- <span data-ttu-id="20936-110">Genel IP adresleri--iç Yük Dengelemesi (ıLB) kullanan özel IP adresleri.</span><span class="sxs-lookup"><span data-stu-id="20936-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>
 <span data-ttu-id="20936-111">Uygulama ağ geçidi en çok bir genel IP adresi ve bir özel IP adresi içerebilir.</span><span class="sxs-lookup"><span data-stu-id="20936-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="20936-112">Genel IP adresi ve özel IP adresi, ön uç IP adresleri olarak ayrı ayrı eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="20936-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="20936-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="20936-113">EXAMPLES</span></span>

### <span data-ttu-id="20936-114">Örnek 1: genel IP kaynak nesnesini kullanarak ön uç IP yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="20936-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="20936-115">İlk komut ortak IP kaynak nesnesi oluşturur ve $PublicIP değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="20936-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="20936-116">İkinci komut, FrontEndIP01 adlı yeni bir ön uç IP yapılandırması oluşturmak için $PublicIP kullanır ve $FrontEnd değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="20936-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="20936-117">Örnek 2: ön uç IP adresi olarak statik özel bir IP oluşturma</span><span class="sxs-lookup"><span data-stu-id="20936-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="20936-118">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki bir sanal ağı alır ve $VNet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="20936-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="20936-119">İkinci komut, ilk komuttan $VNet kullanarak Subnet01 adlı bir alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="20936-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="20936-120">Üçüncü komut, $Subnet ikinci komuttan ve özel IP adresi 10.0.1.1 kullanarak FrontEndIP02 adlı ön uç IP yapılandırması oluşturur ve $FrontEnd değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="20936-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="20936-121">Örnek 3: ön uç IP adresi olarak dinamik özel IP oluşturma</span><span class="sxs-lookup"><span data-stu-id="20936-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="20936-122">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki bir sanal ağı alır ve $VNet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="20936-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="20936-123">İkinci komut, ilk komuttan $VNet kullanarak Subnet01 adlı bir alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="20936-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="20936-124">Üçüncü komut, ikinci komuttan $Subnet kullanarak FrontEndIP03 adlı ön uç IP yapılandırması oluşturur ve bunu $FrontEnd değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="20936-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="20936-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="20936-125">PARAMETERS</span></span>

### <span data-ttu-id="20936-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20936-126">-DefaultProfile</span></span>
<span data-ttu-id="20936-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="20936-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20936-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="20936-128">-Name</span></span>
<span data-ttu-id="20936-129">Bu cmdlet 'in oluşturduğu ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="20936-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="20936-130">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="20936-130">-PrivateIPAddress</span></span>
<span data-ttu-id="20936-131">Bu cmdlet 'in uygulama ağ geçidinin ön uç IP adresiyle ilişki kurduğu özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="20936-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="20936-132">Bu, yalnızca alt ağ belirtilmişse belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="20936-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="20936-133">Bu IP, alt ağdan statik olarak ayrılır.</span><span class="sxs-lookup"><span data-stu-id="20936-133">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="20936-134">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="20936-134">-PublicIPAddress</span></span>
<span data-ttu-id="20936-135">Bu cmdlet 'in uygulama ağ geçidinin ön uç IP adresiyle ilişki kurduğu ortak IP adresi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="20936-135">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="20936-136">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="20936-136">-PublicIPAddressId</span></span>
<span data-ttu-id="20936-137">Bu cmdlet 'in uygulama ağ geçidinin ön uç IP ile ilişki kurduğu genel IP adresi KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="20936-137">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

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

### <span data-ttu-id="20936-138">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="20936-138">-Subnet</span></span>
<span data-ttu-id="20936-139">Bu cmdlet 'in uygulama ağ geçidinin ön uç IP adresiyle ilişki kurduğu alt ağ nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="20936-139">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="20936-140">Bu parametreyi belirtirseniz, ağ geçidinin özel bir IP adresi kullandığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="20936-140">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="20936-141">*Privateıpaddress* parametresi belirtilmişse, bu parametrenin belirttiği alt ağa ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="20936-141">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="20936-142">*Privateıpaddress* belirtilmemişse, bu alt ağdaki IP adreslerinden biri, uygulama ağ geçidinin ön uç IP adresi olarak dinamik olarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="20936-142">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="20936-143">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="20936-143">-SubnetId</span></span>
<span data-ttu-id="20936-144">Bu cmdlet 'in uygulama ağ geçidinin ön uç IP yapılandırmasıyla ilişki kurduğu alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="20936-144">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="20936-145">*Alt ağ* parametresini belirtirseniz, ağ geçidinin özel bir IP adresi kullandığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="20936-145">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="20936-146">*Privateıpaddress* parametresi belirtilmişse *alt ağ* tarafından belirtilen alt ağa ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="20936-146">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="20936-147">*Privateıpaddress* belirtilmemişse, bu alt ağdaki IP adreslerinden biri, uygulama ağ geçidinin ön uç IP adresi olarak dinamik olarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="20936-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="20936-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20936-148">CommonParameters</span></span>
<span data-ttu-id="20936-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="20936-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20936-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20936-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20936-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="20936-151">INPUTS</span></span>

### <span data-ttu-id="20936-152">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="20936-152">None</span></span>

## <span data-ttu-id="20936-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="20936-153">OUTPUTS</span></span>

### <span data-ttu-id="20936-154">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="20936-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="20936-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="20936-155">NOTES</span></span>

## <span data-ttu-id="20936-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="20936-156">RELATED LINKS</span></span>

[<span data-ttu-id="20936-157">Add-Azapplicationgatewayfrontendıconfıg yapılandırması</span><span class="sxs-lookup"><span data-stu-id="20936-157">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="20936-158">Get-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="20936-158">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="20936-159">Remove-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="20936-159">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="20936-160">Set-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="20936-160">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)

