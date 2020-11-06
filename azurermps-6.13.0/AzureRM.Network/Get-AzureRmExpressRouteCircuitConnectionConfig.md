---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 4d9442ba87ba46704aaa93b31f41f111519c980b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594383"
---
# <span data-ttu-id="11732-101">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="11732-101">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="11732-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11732-102">SYNOPSIS</span></span>
<span data-ttu-id="11732-103">Expressroutedevresi özel eşiyle ilişkili bir ExpressRoute devre bağlantısı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="11732-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11732-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11732-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11732-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="11732-105">DESCRIPTION</span></span>
<span data-ttu-id="11732-106">**Get-Azurermexpressroutedevresi Connectionconfig** cmdlet 'ı ExpressRoute devresi Için özel eşiyle ilişkili bir devre bağlantısının yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="11732-106">The **Get-AzureRmExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="11732-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11732-107">EXAMPLES</span></span>

### <span data-ttu-id="11732-108">Örnek 1: ExpressRoute devresi için devre bağlantısı yapılandırmasını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="11732-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="11732-109">Örnek 2: boru kullanarak ExpressRoute devresi ile ilişkili devre</span><span class="sxs-lookup"><span data-stu-id="11732-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="11732-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11732-110">PARAMETERS</span></span>

### <span data-ttu-id="11732-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11732-111">-DefaultProfile</span></span>
<span data-ttu-id="11732-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="11732-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11732-113">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="11732-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="11732-114">Devre bağlantı yapılandırmasını içeren ExpressRoute devresi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="11732-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11732-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="11732-115">-Name</span></span>
<span data-ttu-id="11732-116">Alınacak devre bağlantısı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="11732-116">The name of the circuit connection configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11732-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11732-117">CommonParameters</span></span>
<span data-ttu-id="11732-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11732-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11732-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11732-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11732-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11732-120">INPUTS</span></span>

### <span data-ttu-id="11732-121">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="11732-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="11732-122">Parametreler: Expressroutedevresi (ByValue)</span><span class="sxs-lookup"><span data-stu-id="11732-122">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="11732-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11732-123">OUTPUTS</span></span>

### <span data-ttu-id="11732-124">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi bağlantısı</span><span class="sxs-lookup"><span data-stu-id="11732-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="11732-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11732-125">NOTES</span></span>

## <span data-ttu-id="11732-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11732-126">RELATED LINKS</span></span>

[<span data-ttu-id="11732-127">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="11732-127">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="11732-128">Add-Azurermexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="11732-128">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Add-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="11732-129">Remove-Azurermexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="11732-129">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="11732-130">Set-Azurermexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="11732-130">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="11732-131">New-Azurermexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="11732-131">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)
