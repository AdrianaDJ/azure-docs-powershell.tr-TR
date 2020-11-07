---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 9369e44cb126eda5bad60b543f431be0fe494d21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932116"
---
# <span data-ttu-id="66df1-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="66df1-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="66df1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66df1-102">SYNOPSIS</span></span>
<span data-ttu-id="66df1-103">Uygulama ağ geçidine IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="66df1-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="66df1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66df1-104">SYNTAX</span></span>

### <span data-ttu-id="66df1-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="66df1-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66df1-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="66df1-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66df1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="66df1-107">DESCRIPTION</span></span>
<span data-ttu-id="66df1-108">**Add-Azapplicationgatewayıpconfiguration** cmdlet 'i, uygulama ağ GEÇIDINE bir IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="66df1-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="66df1-109">IP yapılandırmaları, uygulama ağ geçidinin dağıtıldığı alt ağı içerir.</span><span class="sxs-lookup"><span data-stu-id="66df1-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="66df1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66df1-110">EXAMPLES</span></span>

### <span data-ttu-id="66df1-111">Örnek 1: uygulama ağ geçidine sanal ağ yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="66df1-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="66df1-112">İlk komut sanal bir ağ alır.</span><span class="sxs-lookup"><span data-stu-id="66df1-112">The first command gets a virtual network.</span></span>
<span data-ttu-id="66df1-113">İkinci komut, önceden oluşturulmuş sanal ağı kullanan bir alt ağ alır.</span><span class="sxs-lookup"><span data-stu-id="66df1-113">The second command gets a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="66df1-114">Üçüncü komut, uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="66df1-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="66df1-115">Dördüncü komut, $AppGw depolanan uygulama ağ geçidine IP yapılandırmasını ekler.</span><span class="sxs-lookup"><span data-stu-id="66df1-115">The fourth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="66df1-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66df1-116">PARAMETERS</span></span>

### <span data-ttu-id="66df1-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="66df1-117">-ApplicationGateway</span></span>
<span data-ttu-id="66df1-118">Bu cmdlet 'in IP yapılandırması eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="66df1-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="66df1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66df1-119">-DefaultProfile</span></span>
<span data-ttu-id="66df1-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="66df1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66df1-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="66df1-121">-Name</span></span>
<span data-ttu-id="66df1-122">Eklenecek IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="66df1-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="66df1-123">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="66df1-123">-Subnet</span></span>
<span data-ttu-id="66df1-124">Alt ağ belirtir.</span><span class="sxs-lookup"><span data-stu-id="66df1-124">Specifies a subnet.</span></span>
<span data-ttu-id="66df1-125">Bu, uygulama ağ geçidinin dağıtıldığı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="66df1-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="66df1-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="66df1-126">-SubnetId</span></span>
<span data-ttu-id="66df1-127">Alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="66df1-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="66df1-128">Bu, uygulama ağ geçidinin dağıtıldığı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="66df1-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="66df1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66df1-129">CommonParameters</span></span>
<span data-ttu-id="66df1-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66df1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66df1-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66df1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66df1-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66df1-132">INPUTS</span></span>

### <span data-ttu-id="66df1-133">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="66df1-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="66df1-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66df1-134">OUTPUTS</span></span>

### <span data-ttu-id="66df1-135">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="66df1-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="66df1-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66df1-136">NOTES</span></span>

## <span data-ttu-id="66df1-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66df1-137">RELATED LINKS</span></span>

[<span data-ttu-id="66df1-138">Get-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="66df1-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="66df1-139">Yeni-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="66df1-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="66df1-140">Remove-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="66df1-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="66df1-141">Set-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="66df1-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


