---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 2ce0cb130e6c4d25d4b076d06224364011ced2b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593988"
---
# <span data-ttu-id="9f31f-101">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f31f-101">Add-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="9f31f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f31f-102">SYNOPSIS</span></span>
<span data-ttu-id="9f31f-103">Uygulama ağ geçidine IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="9f31f-103">Adds an IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f31f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f31f-104">SYNTAX</span></span>

### <span data-ttu-id="9f31f-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="9f31f-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f31f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9f31f-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f31f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f31f-107">DESCRIPTION</span></span>
<span data-ttu-id="9f31f-108">**Add-AzureRmApplicationGatewayIPConfiguration** cmdlet 'i bir uygulama ağ geçidine IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="9f31f-108">The **Add-AzureRmApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="9f31f-109">IP yapılandırmaları, uygulama ağ geçidinin dağıtıldığı alt ağı içerir.</span><span class="sxs-lookup"><span data-stu-id="9f31f-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="9f31f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f31f-110">EXAMPLES</span></span>

### <span data-ttu-id="9f31f-111">Örnek 1: uygulama ağ geçidine sanal ağ yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="9f31f-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzureRmVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="9f31f-112">İlk komut sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9f31f-112">The first command creates a virtual network.</span></span>
<span data-ttu-id="9f31f-113">İkinci komut, önceden oluşturulmuş sanal ağı kullanarak bir alt ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9f31f-113">The second command creates a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="9f31f-114">Üçüncü komut, uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9f31f-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9f31f-115">Fouth komutu, IP yapılandırmasını $AppGw depolanan uygulama ağ geçidine ekler.</span><span class="sxs-lookup"><span data-stu-id="9f31f-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="9f31f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f31f-116">PARAMETERS</span></span>

### <span data-ttu-id="9f31f-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f31f-117">-ApplicationGateway</span></span>
<span data-ttu-id="9f31f-118">Bu cmdlet 'in IP yapılandırması eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f31f-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="9f31f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f31f-119">-DefaultProfile</span></span>
<span data-ttu-id="9f31f-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9f31f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f31f-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="9f31f-121">-Name</span></span>
<span data-ttu-id="9f31f-122">Eklenecek IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f31f-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="9f31f-123">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="9f31f-123">-Subnet</span></span>
<span data-ttu-id="9f31f-124">Alt ağ belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f31f-124">Specifies a subnet.</span></span>
<span data-ttu-id="9f31f-125">Bu, uygulama ağ geçidinin dağıtıldığı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="9f31f-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="9f31f-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9f31f-126">-SubnetId</span></span>
<span data-ttu-id="9f31f-127">Alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f31f-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="9f31f-128">Bu, uygulama ağ geçidinin dağıtıldığı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="9f31f-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="9f31f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f31f-129">CommonParameters</span></span>
<span data-ttu-id="9f31f-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f31f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f31f-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f31f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f31f-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f31f-132">INPUTS</span></span>

### <span data-ttu-id="9f31f-133">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f31f-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="9f31f-134">Parametreler: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9f31f-134">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="9f31f-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f31f-135">OUTPUTS</span></span>

### <span data-ttu-id="9f31f-136">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f31f-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9f31f-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f31f-137">NOTES</span></span>

## <span data-ttu-id="9f31f-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f31f-138">RELATED LINKS</span></span>

[<span data-ttu-id="9f31f-139">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f31f-139">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9f31f-140">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f31f-140">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9f31f-141">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f31f-141">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9f31f-142">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f31f-142">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


