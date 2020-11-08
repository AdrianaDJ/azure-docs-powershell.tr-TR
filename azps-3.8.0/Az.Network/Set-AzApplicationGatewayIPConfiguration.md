---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 4b3a3303e8ade93b5c6945dae7650f7a9d16bbff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096827"
---
# <span data-ttu-id="8b458-101">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b458-101">Set-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="8b458-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b458-102">SYNOPSIS</span></span>
<span data-ttu-id="8b458-103">Uygulama ağ geçidi için bir IP yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8b458-103">Modifies an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="8b458-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b458-104">SYNTAX</span></span>

### <span data-ttu-id="8b458-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="8b458-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b458-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8b458-106">SetByResource</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b458-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b458-107">DESCRIPTION</span></span>
<span data-ttu-id="8b458-108">**Set-Azapplicationgatewayıp** yapılandırması cmdlet 'ı, IP yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8b458-108">The **Set-AzApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="8b458-109">IP yapılandırması, uygulama ağ geçidinin dağıtıldığı alt ağı içerir.</span><span class="sxs-lookup"><span data-stu-id="8b458-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="8b458-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b458-110">EXAMPLES</span></span>

### <span data-ttu-id="8b458-111">Örnek 1: uygulama ağ geçidi için IP yapılandırmasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="8b458-111">Example 1: Update an IP configuration for an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="8b458-112">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki sanal ağı alır ve $VNet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8b458-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>
<span data-ttu-id="8b458-113">İkinci komut $VNet kullanarak Subnet01 adındaki alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8b458-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="8b458-114">Üçüncü komut, ResourceGroup01 adındaki kaynak grubuna ait ApplicationGateway01 adındaki bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8b458-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8b458-115">İleri komutu, $AppGw depolanan uygulama ağ geçidinin IP yapılandırmasını $Subnet depolanan alt ağ yapılandırmasına ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8b458-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="8b458-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b458-116">PARAMETERS</span></span>

### <span data-ttu-id="8b458-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b458-117">-ApplicationGateway</span></span>
<span data-ttu-id="8b458-118">Bu cmdlet 'in bir IP yapılandırmasını ilişkilendiren bir uygulama ağ geçidi nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b458-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="8b458-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b458-119">-DefaultProfile</span></span>
<span data-ttu-id="8b458-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8b458-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b458-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="8b458-121">-Name</span></span>
<span data-ttu-id="8b458-122">IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b458-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="8b458-123">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="8b458-123">-Subnet</span></span>
<span data-ttu-id="8b458-124">Alt ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b458-124">Specifies the subnet.</span></span>
<span data-ttu-id="8b458-125">Bu, uygulama ağ geçidinin dağıtıldığı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="8b458-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="8b458-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8b458-126">-SubnetId</span></span>
<span data-ttu-id="8b458-127">Alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b458-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="8b458-128">Bu, uygulama ağ geçidinin dağıtıldığı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="8b458-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="8b458-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b458-129">CommonParameters</span></span>
<span data-ttu-id="8b458-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b458-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b458-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b458-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b458-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b458-132">INPUTS</span></span>

### <span data-ttu-id="8b458-133">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b458-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8b458-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b458-134">OUTPUTS</span></span>

### <span data-ttu-id="8b458-135">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b458-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8b458-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b458-136">NOTES</span></span>

## <span data-ttu-id="8b458-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b458-137">RELATED LINKS</span></span>

[<span data-ttu-id="8b458-138">Add-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="8b458-138">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8b458-139">Add-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="8b458-139">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8b458-140">Get-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="8b458-140">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8b458-141">Yeni-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="8b458-141">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8b458-142">Remove-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="8b458-142">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)


