---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 076965d0f63a8c28742cf9853068b9e020403a66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593535"
---
# <span data-ttu-id="42d75-101">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="42d75-101">New-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="42d75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42d75-102">SYNOPSIS</span></span>
<span data-ttu-id="42d75-103">Uygulama ağ geçidi için bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="42d75-103">Creates an IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42d75-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42d75-104">SYNTAX</span></span>

### <span data-ttu-id="42d75-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="42d75-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42d75-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="42d75-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42d75-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="42d75-107">DESCRIPTION</span></span>
<span data-ttu-id="42d75-108">**New-AzureRmApplicationGatewayIPConfiguration** cmdlet 'i, uygulama ağ geçidi IÇIN bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="42d75-108">The **New-AzureRmApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="42d75-109">IP yapılandırması, uygulama ağ geçidinin dağıtıldığı alt ağı içerir.</span><span class="sxs-lookup"><span data-stu-id="42d75-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="42d75-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42d75-110">EXAMPLES</span></span>

### <span data-ttu-id="42d75-111">Örnek 1: uygulama ağ geçidi için IP yapılandırması oluşturma.</span><span class="sxs-lookup"><span data-stu-id="42d75-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzureRmApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="42d75-112">İlk komut, VNet01 adındaki kaynak grubuna ait olan bir sanal ağı alır.</span><span class="sxs-lookup"><span data-stu-id="42d75-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>

<span data-ttu-id="42d75-113">İkinci komut, önceki komutun sanal ağının ait olduğu alt ağın alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="42d75-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="42d75-114">Üçüncü komut $Subnet kullanarak IP yapılandırmasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="42d75-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="42d75-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42d75-115">PARAMETERS</span></span>

### <span data-ttu-id="42d75-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="42d75-116">-Name</span></span>
<span data-ttu-id="42d75-117">Oluşturulacak IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42d75-117">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="42d75-118">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="42d75-118">-Subnet</span></span>
<span data-ttu-id="42d75-119">Alt ağ nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="42d75-119">Specifies the subnet object.</span></span>
<span data-ttu-id="42d75-120">Bu, uygulama ağ geçidinin dağıtıldığı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="42d75-120">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="42d75-121">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="42d75-121">-SubnetId</span></span>
<span data-ttu-id="42d75-122">Alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="42d75-122">Specifies the subnet ID.</span></span>
<span data-ttu-id="42d75-123">Bu, uygulama ağ geçidinin dağıtılacağı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="42d75-123">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="42d75-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d75-124">-DefaultProfile</span></span>
<span data-ttu-id="42d75-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="42d75-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42d75-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d75-126">CommonParameters</span></span>
<span data-ttu-id="42d75-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42d75-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d75-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42d75-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d75-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42d75-129">INPUTS</span></span>

### <span data-ttu-id="42d75-130">System. String</span><span class="sxs-lookup"><span data-stu-id="42d75-130">System.String</span></span>

## <span data-ttu-id="42d75-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42d75-131">OUTPUTS</span></span>

### <span data-ttu-id="42d75-132">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="42d75-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="42d75-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42d75-133">NOTES</span></span>

## <span data-ttu-id="42d75-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42d75-134">RELATED LINKS</span></span>

[<span data-ttu-id="42d75-135">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="42d75-135">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="42d75-136">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="42d75-136">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="42d75-137">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="42d75-137">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="42d75-138">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="42d75-138">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


