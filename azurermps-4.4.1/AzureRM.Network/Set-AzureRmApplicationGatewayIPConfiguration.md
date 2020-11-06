---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: feeed9709833f56c42d4f3134794b96dda800ce5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594613"
---
# <span data-ttu-id="e4149-101">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4149-101">Set-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="e4149-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4149-102">SYNOPSIS</span></span>
<span data-ttu-id="e4149-103">Uygulama ağ geçidi için bir IP yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e4149-103">Modifies an IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4149-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4149-104">SYNTAX</span></span>

### <span data-ttu-id="e4149-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="e4149-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4149-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e4149-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4149-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4149-107">DESCRIPTION</span></span>
<span data-ttu-id="e4149-108">**Set-AzureRmApplicationGatewayIPConfiguration** cmdlet 'ı bir IP yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e4149-108">The **Set-AzureRmApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="e4149-109">IP yapılandırması, uygulama ağ geçidinin dağıtıldığı alt ağı içerir.</span><span class="sxs-lookup"><span data-stu-id="e4149-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="e4149-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4149-110">EXAMPLES</span></span>

### <span data-ttu-id="e4149-111">Örnek 1: IP yapılandırmasının hedef durumunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="e4149-111">Example 1: Set the goal state of an IP configuration</span></span>
```
PS C:\>$VNet = Get-AzureRmVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="e4149-112">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki sanal ağı alır ve $VNet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e4149-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>

<span data-ttu-id="e4149-113">İkinci komut $VNet kullanarak Subnet01 adındaki alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e4149-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="e4149-114">Üçüncü komut, ResourceGroup01 adındaki kaynak grubuna ait ApplicationGateway01 adındaki bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e4149-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="e4149-115">İleri komutu, $AppGw depolanan uygulama ağ geçidinin IP yapılandırmasını $Subnet depolanan alt ağ yapılandırmasına ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e4149-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="e4149-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4149-116">PARAMETERS</span></span>

### <span data-ttu-id="e4149-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4149-117">-ApplicationGateway</span></span>
<span data-ttu-id="e4149-118">Bu cmdlet 'in bir IP yapılandırmasını ilişkilendiren bir uygulama ağ geçidi nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4149-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="e4149-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="e4149-119">-Name</span></span>
<span data-ttu-id="e4149-120">IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4149-120">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="e4149-121">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="e4149-121">-Subnet</span></span>
<span data-ttu-id="e4149-122">Alt ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4149-122">Specifies the subnet.</span></span>
<span data-ttu-id="e4149-123">Bu, uygulama ağ geçidinin dağıtıldığı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="e4149-123">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="e4149-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e4149-124">-SubnetId</span></span>
<span data-ttu-id="e4149-125">Alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4149-125">Specifies the subnet ID.</span></span>
<span data-ttu-id="e4149-126">Bu, uygulama ağ geçidinin dağıtıldığı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="e4149-126">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="e4149-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4149-127">-DefaultProfile</span></span>
<span data-ttu-id="e4149-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e4149-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4149-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4149-129">CommonParameters</span></span>
<span data-ttu-id="e4149-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4149-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4149-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4149-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4149-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4149-132">INPUTS</span></span>

### <span data-ttu-id="e4149-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e4149-133">System.String</span></span>

## <span data-ttu-id="e4149-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4149-134">OUTPUTS</span></span>

### <span data-ttu-id="e4149-135">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4149-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e4149-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4149-136">NOTES</span></span>

## <span data-ttu-id="e4149-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4149-137">RELATED LINKS</span></span>

[<span data-ttu-id="e4149-138">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4149-138">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e4149-139">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4149-139">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e4149-140">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4149-140">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e4149-141">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4149-141">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e4149-142">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4149-142">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)


