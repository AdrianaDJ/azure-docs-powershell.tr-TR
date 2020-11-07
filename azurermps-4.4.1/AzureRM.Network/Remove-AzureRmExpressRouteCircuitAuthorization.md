---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: af8490ab242919d44b0b1b47c9cab92674e9df9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765150"
---
# <span data-ttu-id="0fd94-101">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="0fd94-101">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="0fd94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fd94-102">SYNOPSIS</span></span>
<span data-ttu-id="0fd94-103">Var olan ExpressRoute yapılandırma yetkilendirmesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0fd94-103">Removes an existing ExpressRoute configuration authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fd94-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0fd94-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fd94-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0fd94-105">DESCRIPTION</span></span>
<span data-ttu-id="0fd94-106">**Remove-Azurermexpressroutetormauthorter** cmdlet 'ı ExpressRoute devresine atanan bir yetkilendirmeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0fd94-106">The **Remove-AzureRmExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="0fd94-107">ExpressRoute devreleri ortak Internet yerine bir bağlantı sağlayıcısı kullanarak şirket içi ağınızı Azure 'a bağlayın.</span><span class="sxs-lookup"><span data-stu-id="0fd94-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="0fd94-108">ExpressRoute devresi sahibi her bir devrein en fazla 10 yetkilendirmesi oluşturabilir; Bu yetkilendirmeler sanal ağ sahibi tarafından, ağı devreye bağlamak için kullanılabilecek bir yetkilendirme anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0fd94-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="0fd94-109">Sanal ağ başına yalnızca bir yetkilendirme olabilir.</span><span class="sxs-lookup"><span data-stu-id="0fd94-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="0fd94-110">Ancak, herhangi bir zamanda, devre sahibi sanal ağa atanmış olan yetkilendirmeyi kaldırmak için **Remove-Azurermexpressroutedöngüye** at 'ı kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="0fd94-110">At any time, however, the circuit owner can use **Remove-AzureRmExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="0fd94-111">Bu durumda, ilgili sanal ağ artık Azure 'a bağlanmak için ExpressRoute devresini kullanamaz.</span><span class="sxs-lookup"><span data-stu-id="0fd94-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="0fd94-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0fd94-112">EXAMPLES</span></span>

### <span data-ttu-id="0fd94-113">Örnek 1: ExpressRoute devresi 'den devre yetkilendirmeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="0fd94-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="0fd94-114">Bu örnekte, ExpressRoute devresi bir devre yetkilendirmesi kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="0fd94-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="0fd94-115">İlk komut **Get-Azurermexpressroutedevresi** öğesini kullanarak, contosodevresi adlı bir ExpressRoute devresine nesne başvurusu oluşturabilir ve sonucu $Circuit adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="0fd94-115">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>

<span data-ttu-id="0fd94-116">İkinci komut devre yetkisini kaldırmak için devre</span><span class="sxs-lookup"><span data-stu-id="0fd94-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>

<span data-ttu-id="0fd94-117">Üçüncü komut, $Circuit değişkeninde depolanan ExpressRoute devresini kaldırmayı onaylamak için Set-AzureRmExpressRouteCircuit cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="0fd94-117">The third command uses the Set-AzureRmExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="0fd94-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0fd94-118">PARAMETERS</span></span>

### <span data-ttu-id="0fd94-119">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="0fd94-119">-ExpressRouteCircuit</span></span>
<span data-ttu-id="0fd94-120">Bu cmdlet 'in kaldırdığı Expressroutedevresi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0fd94-120">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fd94-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="0fd94-121">-Name</span></span>
<span data-ttu-id="0fd94-122">Bu cmdlet 'in kaldırdığı devre yetkilendirmesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0fd94-122">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0fd94-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fd94-123">-DefaultProfile</span></span>
<span data-ttu-id="0fd94-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0fd94-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fd94-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fd94-125">CommonParameters</span></span>
<span data-ttu-id="0fd94-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0fd94-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fd94-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fd94-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fd94-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0fd94-128">INPUTS</span></span>

### <span data-ttu-id="0fd94-129">Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="0fd94-129">PSExpressRouteCircuit</span></span>
<span data-ttu-id="0fd94-130">Bu cmdlet, **Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi** nesnesinin ardışık işlem örneklerini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="0fd94-130">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="0fd94-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0fd94-131">OUTPUTS</span></span>

### <span data-ttu-id="0fd94-132">Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="0fd94-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="0fd94-133">Bu cmdlet, **Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi** nesnesinin varolan örneklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0fd94-133">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="0fd94-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0fd94-134">NOTES</span></span>

## <span data-ttu-id="0fd94-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0fd94-135">RELATED LINKS</span></span>

[<span data-ttu-id="0fd94-136">Add-Azurermexpressroutetorisuthorter</span><span class="sxs-lookup"><span data-stu-id="0fd94-136">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="0fd94-137">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="0fd94-137">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="0fd94-138">Get-Azurermexpressrouteter</span><span class="sxs-lookup"><span data-stu-id="0fd94-138">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="0fd94-139">Yeni-azurermexpressroutepatlar</span><span class="sxs-lookup"><span data-stu-id="0fd94-139">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="0fd94-140">Set-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="0fd94-140">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)