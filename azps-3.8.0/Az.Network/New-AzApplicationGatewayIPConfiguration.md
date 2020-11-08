---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e9e10eb151c6908e05047d80c5aed4aff3b9f613
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104802"
---
# <span data-ttu-id="c1fa0-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1fa0-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="c1fa0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1fa0-102">SYNOPSIS</span></span>
<span data-ttu-id="c1fa0-103">Uygulama ağ geçidi için bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="c1fa0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1fa0-104">SYNTAX</span></span>

### <span data-ttu-id="c1fa0-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="c1fa0-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1fa0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c1fa0-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1fa0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1fa0-107">DESCRIPTION</span></span>
<span data-ttu-id="c1fa0-108">**Yeni-Azapplicationgatewayıp** yapılandırması cmdlet 'i, uygulama ağ geçidi IÇIN bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="c1fa0-109">IP yapılandırması, uygulama ağ geçidinin dağıtıldığı alt ağı içerir.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="c1fa0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1fa0-110">EXAMPLES</span></span>

### <span data-ttu-id="c1fa0-111">Örnek 1: uygulama ağ geçidi için IP yapılandırması oluşturma.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="c1fa0-112">İlk komut, VNet01 adındaki kaynak grubuna ait olan bir sanal ağı alır.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="c1fa0-113">İkinci komut, önceki komutun sanal ağının ait olduğu alt ağın alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="c1fa0-114">Üçüncü komut $Subnet kullanarak IP yapılandırmasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="c1fa0-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1fa0-115">PARAMETERS</span></span>

### <span data-ttu-id="c1fa0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1fa0-116">-DefaultProfile</span></span>
<span data-ttu-id="c1fa0-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1fa0-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="c1fa0-118">-Name</span></span>
<span data-ttu-id="c1fa0-119">Oluşturulacak IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="c1fa0-120">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="c1fa0-120">-Subnet</span></span>
<span data-ttu-id="c1fa0-121">Alt ağ nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-121">Specifies the subnet object.</span></span>
<span data-ttu-id="c1fa0-122">Bu, uygulama ağ geçidinin dağıtıldığı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="c1fa0-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c1fa0-123">-SubnetId</span></span>
<span data-ttu-id="c1fa0-124">Alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="c1fa0-125">Bu, uygulama ağ geçidinin dağıtılacağı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="c1fa0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1fa0-126">CommonParameters</span></span>
<span data-ttu-id="c1fa0-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1fa0-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1fa0-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1fa0-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1fa0-129">INPUTS</span></span>

### <span data-ttu-id="c1fa0-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c1fa0-130">None</span></span>

## <span data-ttu-id="c1fa0-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1fa0-131">OUTPUTS</span></span>

### <span data-ttu-id="c1fa0-132">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1fa0-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="c1fa0-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1fa0-133">NOTES</span></span>

## <span data-ttu-id="c1fa0-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1fa0-134">RELATED LINKS</span></span>

[<span data-ttu-id="c1fa0-135">Add-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="c1fa0-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="c1fa0-136">Get-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="c1fa0-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="c1fa0-137">Remove-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="c1fa0-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="c1fa0-138">Set-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="c1fa0-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


