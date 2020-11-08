---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: f4aabb68fd1f508651406d7ccf7be91ff646d46c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279864"
---
# <span data-ttu-id="06bcb-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="06bcb-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="06bcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06bcb-102">SYNOPSIS</span></span>
<span data-ttu-id="06bcb-103">Expressroutedevresi özel eşiyle ilişkili bir ExpressRoute devre bağlantısı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="06bcb-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="06bcb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06bcb-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06bcb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="06bcb-105">DESCRIPTION</span></span>
<span data-ttu-id="06bcb-106">**Get-Azexpressroute, Connectionconfig** cmdlet 'ı ExpressRoute devresi Için özel eşiyle ilişkili bir devre bağlantısının yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="06bcb-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="06bcb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06bcb-107">EXAMPLES</span></span>

### <span data-ttu-id="06bcb-108">Örnek 1: ExpressRoute devresi için devre bağlantısı yapılandırmasını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="06bcb-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="06bcb-109">Örnek 2: boru kullanarak ExpressRoute devresi ile ilişkili devre</span><span class="sxs-lookup"><span data-stu-id="06bcb-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="06bcb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06bcb-110">PARAMETERS</span></span>

### <span data-ttu-id="06bcb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06bcb-111">-DefaultProfile</span></span>
<span data-ttu-id="06bcb-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="06bcb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06bcb-113">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="06bcb-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="06bcb-114">Devre bağlantı yapılandırmasını içeren ExpressRoute devresi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="06bcb-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

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

### <span data-ttu-id="06bcb-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="06bcb-115">-Name</span></span>
<span data-ttu-id="06bcb-116">Alınacak devre bağlantısı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="06bcb-116">The name of the circuit connection configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06bcb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06bcb-117">CommonParameters</span></span>
<span data-ttu-id="06bcb-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06bcb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06bcb-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="06bcb-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06bcb-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06bcb-120">INPUTS</span></span>

### <span data-ttu-id="06bcb-121">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="06bcb-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="06bcb-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06bcb-122">OUTPUTS</span></span>

### <span data-ttu-id="06bcb-123">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi bağlantısı</span><span class="sxs-lookup"><span data-stu-id="06bcb-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="06bcb-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06bcb-124">NOTES</span></span>

## <span data-ttu-id="06bcb-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06bcb-125">RELATED LINKS</span></span>

[<span data-ttu-id="06bcb-126">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="06bcb-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="06bcb-127">Add-Azexpressroute, Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="06bcb-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="06bcb-128">Remove-Azexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="06bcb-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="06bcb-129">Set-Azexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="06bcb-129">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="06bcb-130">Yeni-Azexpressroute, Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="06bcb-130">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)