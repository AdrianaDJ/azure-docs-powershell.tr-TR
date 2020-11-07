---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 99fac74f920c0137224c9c0f5c123e6c8ef28610
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93595220"
---
# <span data-ttu-id="cd6ee-101">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd6ee-101">Set-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="cd6ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd6ee-102">SYNOPSIS</span></span>
<span data-ttu-id="cd6ee-103">Uygulama ağ geçidi için bir IP yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cd6ee-103">Modifies an IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd6ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd6ee-104">SYNTAX</span></span>

### <span data-ttu-id="cd6ee-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="cd6ee-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd6ee-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="cd6ee-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd6ee-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd6ee-107">DESCRIPTION</span></span>
<span data-ttu-id="cd6ee-108">**Set-AzureRmApplicationGatewayIPConfiguration** cmdlet 'ı bir IP yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cd6ee-108">The **Set-AzureRmApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="cd6ee-109">IP yapılandırması, uygulama ağ geçidinin dağıtıldığı alt ağı içerir.</span><span class="sxs-lookup"><span data-stu-id="cd6ee-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="cd6ee-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd6ee-110">EXAMPLES</span></span>

### <span data-ttu-id="cd6ee-111">Örnek 1: IP yapılandırmasının hedef durumunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="cd6ee-111">Example 1: Set the goal state of an IP configuration</span></span>
```
PS C:\>$VNet = Get-AzureRmVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="cd6ee-112">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki sanal ağı alır ve $VNet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cd6ee-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>

<span data-ttu-id="cd6ee-113">İkinci komut $VNet kullanarak Subnet01 adındaki alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cd6ee-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="cd6ee-114">Üçüncü komut, ResourceGroup01 adındaki kaynak grubuna ait ApplicationGateway01 adındaki bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cd6ee-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="cd6ee-115">İleri komutu, $AppGw depolanan uygulama ağ geçidinin IP yapılandırmasını $Subnet depolanan alt ağ yapılandırmasına ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cd6ee-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="cd6ee-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd6ee-116">PARAMETERS</span></span>

### <span data-ttu-id="cd6ee-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cd6ee-117">-ApplicationGateway</span></span>
<span data-ttu-id="cd6ee-118">Bu cmdlet 'in bir IP yapılandırmasını ilişkilendiren bir uygulama ağ geçidi nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd6ee-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="cd6ee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd6ee-119">-DefaultProfile</span></span>
<span data-ttu-id="cd6ee-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cd6ee-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd6ee-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="cd6ee-121">-Name</span></span>
<span data-ttu-id="cd6ee-122">IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd6ee-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="cd6ee-123">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="cd6ee-123">-Subnet</span></span>
<span data-ttu-id="cd6ee-124">Alt ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd6ee-124">Specifies the subnet.</span></span>
<span data-ttu-id="cd6ee-125">Bu, uygulama ağ geçidinin dağıtıldığı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="cd6ee-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="cd6ee-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="cd6ee-126">-SubnetId</span></span>
<span data-ttu-id="cd6ee-127">Alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd6ee-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="cd6ee-128">Bu, uygulama ağ geçidinin dağıtıldığı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="cd6ee-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="cd6ee-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd6ee-129">CommonParameters</span></span>
<span data-ttu-id="cd6ee-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd6ee-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd6ee-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd6ee-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd6ee-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd6ee-132">INPUTS</span></span>

### <span data-ttu-id="cd6ee-133">System. String</span><span class="sxs-lookup"><span data-stu-id="cd6ee-133">System.String</span></span>

## <span data-ttu-id="cd6ee-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd6ee-134">OUTPUTS</span></span>

### <span data-ttu-id="cd6ee-135">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cd6ee-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cd6ee-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd6ee-136">NOTES</span></span>

## <span data-ttu-id="cd6ee-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd6ee-137">RELATED LINKS</span></span>

[<span data-ttu-id="cd6ee-138">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd6ee-138">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="cd6ee-139">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd6ee-139">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="cd6ee-140">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd6ee-140">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="cd6ee-141">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd6ee-141">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="cd6ee-142">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd6ee-142">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

