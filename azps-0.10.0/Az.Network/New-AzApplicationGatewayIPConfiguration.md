---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 67cf5adb8d8cc0bef914f0623f66ee0e871302d8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935429"
---
# <span data-ttu-id="911f6-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="911f6-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="911f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="911f6-102">SYNOPSIS</span></span>
<span data-ttu-id="911f6-103">Uygulama ağ geçidi için bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="911f6-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="911f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="911f6-104">SYNTAX</span></span>

### <span data-ttu-id="911f6-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="911f6-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="911f6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="911f6-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="911f6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="911f6-107">DESCRIPTION</span></span>
<span data-ttu-id="911f6-108">**Yeni-Azapplicationgatewayıp** yapılandırması cmdlet 'i, uygulama ağ geçidi IÇIN bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="911f6-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="911f6-109">IP yapılandırması, uygulama ağ geçidinin dağıtıldığı alt ağı içerir.</span><span class="sxs-lookup"><span data-stu-id="911f6-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="911f6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="911f6-110">EXAMPLES</span></span>

### <span data-ttu-id="911f6-111">Örnek 1: uygulama ağ geçidi için IP yapılandırması oluşturma.</span><span class="sxs-lookup"><span data-stu-id="911f6-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="911f6-112">İlk komut, VNet01 adındaki kaynak grubuna ait olan bir sanal ağı alır.</span><span class="sxs-lookup"><span data-stu-id="911f6-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>

<span data-ttu-id="911f6-113">İkinci komut, önceki komutun sanal ağının ait olduğu alt ağın alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="911f6-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="911f6-114">Üçüncü komut $Subnet kullanarak IP yapılandırmasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="911f6-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="911f6-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="911f6-115">PARAMETERS</span></span>

### <span data-ttu-id="911f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="911f6-116">-DefaultProfile</span></span>
<span data-ttu-id="911f6-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="911f6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="911f6-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="911f6-118">-Name</span></span>
<span data-ttu-id="911f6-119">Oluşturulacak IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="911f6-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="911f6-120">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="911f6-120">-Subnet</span></span>
<span data-ttu-id="911f6-121">Alt ağ nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="911f6-121">Specifies the subnet object.</span></span>
<span data-ttu-id="911f6-122">Bu, uygulama ağ geçidinin dağıtıldığı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="911f6-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="911f6-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="911f6-123">-SubnetId</span></span>
<span data-ttu-id="911f6-124">Alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="911f6-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="911f6-125">Bu, uygulama ağ geçidinin dağıtılacağı alt ağdır.</span><span class="sxs-lookup"><span data-stu-id="911f6-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="911f6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="911f6-126">CommonParameters</span></span>
<span data-ttu-id="911f6-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="911f6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="911f6-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="911f6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="911f6-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="911f6-129">INPUTS</span></span>

### <span data-ttu-id="911f6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="911f6-130">System.String</span></span>

## <span data-ttu-id="911f6-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="911f6-131">OUTPUTS</span></span>

### <span data-ttu-id="911f6-132">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="911f6-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="911f6-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="911f6-133">NOTES</span></span>

## <span data-ttu-id="911f6-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="911f6-134">RELATED LINKS</span></span>

[<span data-ttu-id="911f6-135">Add-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="911f6-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="911f6-136">Get-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="911f6-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="911f6-137">Remove-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="911f6-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="911f6-138">Set-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="911f6-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)

