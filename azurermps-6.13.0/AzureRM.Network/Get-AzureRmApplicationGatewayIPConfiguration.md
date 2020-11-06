---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 8995c91484bba1c11944bf9d2a6e3dbc8ff5738d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594385"
---
# <span data-ttu-id="278c5-101">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="278c5-101">Get-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="278c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="278c5-102">SYNOPSIS</span></span>
<span data-ttu-id="278c5-103">Uygulama ağ geçidinin IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="278c5-103">Gets the IP configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="278c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="278c5-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="278c5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="278c5-105">DESCRIPTION</span></span>
<span data-ttu-id="278c5-106">**Get-AzureRmApplicationGatewayIPConfiguration** cmdlet 'i bir uygulama ağ geçidinin IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="278c5-106">The **Get-AzureRmApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="278c5-107">IP yapılandırması, uygulama ağ geçidinin dağıtıldığı alt ağı içerir.</span><span class="sxs-lookup"><span data-stu-id="278c5-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="278c5-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="278c5-108">EXAMPLES</span></span>

### <span data-ttu-id="278c5-109">Örnek 1: belirli bir IP yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="278c5-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzureRmApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="278c5-110">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar. İkinci komut, $AppGw depolanan ağ geçidinden GateSubnet01 adlı bir IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="278c5-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="278c5-111">Örnek 2: IP yapılandırmalarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="278c5-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="278c5-112">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar. İkinci komut, tüm IP yapılandırmalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="278c5-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="278c5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="278c5-113">PARAMETERS</span></span>

### <span data-ttu-id="278c5-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="278c5-114">-ApplicationGateway</span></span>
<span data-ttu-id="278c5-115">IP yapılandırmasını içeren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="278c5-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="278c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="278c5-116">-DefaultProfile</span></span>
<span data-ttu-id="278c5-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="278c5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="278c5-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="278c5-118">-Name</span></span>
<span data-ttu-id="278c5-119">Bu cmdlet 'in aldığı IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="278c5-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="278c5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="278c5-120">CommonParameters</span></span>
<span data-ttu-id="278c5-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="278c5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="278c5-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="278c5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="278c5-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="278c5-123">INPUTS</span></span>

### <span data-ttu-id="278c5-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="278c5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="278c5-125">Parametreler: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="278c5-125">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="278c5-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="278c5-126">OUTPUTS</span></span>

### <span data-ttu-id="278c5-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="278c5-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="278c5-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="278c5-128">NOTES</span></span>

## <span data-ttu-id="278c5-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="278c5-129">RELATED LINKS</span></span>

[<span data-ttu-id="278c5-130">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="278c5-130">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="278c5-131">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="278c5-131">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="278c5-132">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="278c5-132">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="278c5-133">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="278c5-133">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


