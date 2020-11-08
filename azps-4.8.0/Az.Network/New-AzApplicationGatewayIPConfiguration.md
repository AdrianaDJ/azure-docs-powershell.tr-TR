---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e9e10eb151c6908e05047d80c5aed4aff3b9f613
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268504"
---
# <span data-ttu-id="2082c-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2082c-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="2082c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2082c-102">SYNOPSIS</span></span>
<span data-ttu-id="2082c-103">Uygulama ağ geçidi için bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2082c-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="2082c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2082c-104">SYNTAX</span></span>

### <span data-ttu-id="2082c-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="2082c-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2082c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2082c-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2082c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2082c-107">DESCRIPTION</span></span>
<span data-ttu-id="2082c-108">**Yeni-Azapplicationgatewayıp** yapılandırması cmdlet 'i, uygulama ağ geçidi IÇIN bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2082c-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="2082c-109">IP yapılandırması, uygulama ağ geçidinin dağıtıldığı alt ağı içerir.</span><span class="sxs-lookup"><span data-stu-id="2082c-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="2082c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2082c-110">EXAMPLES</span></span>

### <span data-ttu-id="2082c-111">Örnek 1: uygulama ağ geçidi için IP yapılandırması oluşturma.</span><span class="sxs-lookup"><span data-stu-id="2082c-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="2082c-112">İlk komut, VNet01 adındaki kaynak grubuna ait olan bir sanal ağı alır.</span><span class="sxs-lookup"><span data-stu-id="2082c-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="2082c-113">İkinci komut, önceki komutun sanal ağının ait olduğu alt ağın alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2082c-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="2082c-114">Üçüncü komut $Subnet kullanarak IP yapılandırmasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2082c-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="2082c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2082c-115">PARAMETERS</span></span>

### <span data-ttu-id="2082c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2082c-116">-DefaultProfile</span></span>
<span data-ttu-id="2082c-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2082c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2082c-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="2082c-118">-Name</span></span>
<span data-ttu-id="2082c-119">Oluşturulacak IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2082c-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="2082c-120">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="2082c-120">-Subnet</span></span>
<span data-ttu-id="2082c-121">Alt ağ nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2082c-121">Specifies the subnet object.</span></span>
<span data-ttu-id="2082c-122">Bu, uygulama ağ geçidinin dağıtıldığı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="2082c-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="2082c-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="2082c-123">-SubnetId</span></span>
<span data-ttu-id="2082c-124">Alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2082c-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="2082c-125">Bu, uygulama ağ geçidinin dağıtılacağı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="2082c-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="2082c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2082c-126">CommonParameters</span></span>
<span data-ttu-id="2082c-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2082c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2082c-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2082c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2082c-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2082c-129">INPUTS</span></span>

### <span data-ttu-id="2082c-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2082c-130">None</span></span>

## <span data-ttu-id="2082c-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2082c-131">OUTPUTS</span></span>

### <span data-ttu-id="2082c-132">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2082c-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="2082c-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2082c-133">NOTES</span></span>

## <span data-ttu-id="2082c-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2082c-134">RELATED LINKS</span></span>

[<span data-ttu-id="2082c-135">Add-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="2082c-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2082c-136">Get-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="2082c-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2082c-137">Remove-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="2082c-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2082c-138">Set-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="2082c-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


