---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: c0dad1f63f8a203a9f1b8aaeb75a2be13bfc61f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931933"
---
# <span data-ttu-id="32677-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="32677-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="32677-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32677-102">SYNOPSIS</span></span>
<span data-ttu-id="32677-103">Uygulama ağ geçidi için bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32677-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="32677-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="32677-104">SYNTAX</span></span>

### <span data-ttu-id="32677-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="32677-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32677-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="32677-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32677-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="32677-107">DESCRIPTION</span></span>
<span data-ttu-id="32677-108">**Yeni-Azapplicationgatewayıp** yapılandırması cmdlet 'i, uygulama ağ geçidi IÇIN bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32677-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="32677-109">IP yapılandırması, uygulama ağ geçidinin dağıtıldığı alt ağı içerir.</span><span class="sxs-lookup"><span data-stu-id="32677-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="32677-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="32677-110">EXAMPLES</span></span>

### <span data-ttu-id="32677-111">Örnek 1: uygulama ağ geçidi için IP yapılandırması oluşturma.</span><span class="sxs-lookup"><span data-stu-id="32677-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="32677-112">İlk komut, VNet01 adındaki kaynak grubuna ait olan bir sanal ağı alır.</span><span class="sxs-lookup"><span data-stu-id="32677-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="32677-113">İkinci komut, önceki komutun sanal ağının ait olduğu alt ağın alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="32677-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="32677-114">Üçüncü komut $Subnet kullanarak IP yapılandırmasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32677-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="32677-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="32677-115">PARAMETERS</span></span>

### <span data-ttu-id="32677-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32677-116">-DefaultProfile</span></span>
<span data-ttu-id="32677-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="32677-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32677-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="32677-118">-Name</span></span>
<span data-ttu-id="32677-119">Oluşturulacak IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32677-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="32677-120">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="32677-120">-Subnet</span></span>
<span data-ttu-id="32677-121">Alt ağ nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32677-121">Specifies the subnet object.</span></span>
<span data-ttu-id="32677-122">Bu, uygulama ağ geçidinin dağıtıldığı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="32677-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="32677-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="32677-123">-SubnetId</span></span>
<span data-ttu-id="32677-124">Alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="32677-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="32677-125">Bu, uygulama ağ geçidinin dağıtılacağı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="32677-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="32677-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32677-126">CommonParameters</span></span>
<span data-ttu-id="32677-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="32677-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32677-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32677-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32677-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="32677-129">INPUTS</span></span>

### <span data-ttu-id="32677-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="32677-130">None</span></span>

## <span data-ttu-id="32677-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="32677-131">OUTPUTS</span></span>

### <span data-ttu-id="32677-132">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="32677-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="32677-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="32677-133">NOTES</span></span>

## <span data-ttu-id="32677-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="32677-134">RELATED LINKS</span></span>

[<span data-ttu-id="32677-135">Add-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="32677-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="32677-136">Get-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="32677-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="32677-137">Remove-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="32677-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="32677-138">Set-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="32677-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


