---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayipconfiguration
schema: 2.0.0
ms.openlocfilehash: 09986be8ccc8dce8eaec522c501fe3f98ff03c56
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940098"
---
# <span data-ttu-id="82151-101">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="82151-101">Get-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="82151-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82151-102">SYNOPSIS</span></span>
<span data-ttu-id="82151-103">Uygulama ağ geçidinin IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="82151-103">Gets the IP configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82151-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="82151-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82151-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="82151-105">DESCRIPTION</span></span>
<span data-ttu-id="82151-106">**Get-AzureRmApplicationGatewayIPConfiguration** cmdlet 'i bir uygulama ağ geçidinin IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="82151-106">The **Get-AzureRmApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="82151-107">IP yapılandırması, uygulama ağ geçidinin dağıtıldığı alt ağı içerir.</span><span class="sxs-lookup"><span data-stu-id="82151-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="82151-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="82151-108">EXAMPLES</span></span>

### <span data-ttu-id="82151-109">Örnek 1: belirli bir IP yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="82151-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzureRmApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="82151-110">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar. İkinci komut, $AppGw depolanan ağ geçidinden GateSubnet01 adlı bir IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="82151-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="82151-111">Örnek 2: IP yapılandırmalarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="82151-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="82151-112">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar. İkinci komut, tüm IP yapılandırmalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="82151-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="82151-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="82151-113">PARAMETERS</span></span>

### <span data-ttu-id="82151-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82151-114">-ApplicationGateway</span></span>
<span data-ttu-id="82151-115">IP yapılandırmasını içeren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="82151-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="82151-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82151-116">-DefaultProfile</span></span>
<span data-ttu-id="82151-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="82151-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82151-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="82151-118">-Name</span></span>
<span data-ttu-id="82151-119">Bu cmdlet 'in aldığı IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="82151-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82151-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82151-120">CommonParameters</span></span>
<span data-ttu-id="82151-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="82151-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82151-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82151-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82151-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="82151-123">INPUTS</span></span>

### <span data-ttu-id="82151-124">System. String</span><span class="sxs-lookup"><span data-stu-id="82151-124">System.String</span></span>

## <span data-ttu-id="82151-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="82151-125">OUTPUTS</span></span>

### <span data-ttu-id="82151-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="82151-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="82151-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="82151-127">NOTES</span></span>

## <span data-ttu-id="82151-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="82151-128">RELATED LINKS</span></span>

[<span data-ttu-id="82151-129">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="82151-129">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="82151-130">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="82151-130">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="82151-131">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="82151-131">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="82151-132">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="82151-132">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


