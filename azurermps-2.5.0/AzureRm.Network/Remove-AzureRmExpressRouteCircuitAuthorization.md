---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: 144d70318463b7c5ffebfa6b7d942ec2a351fc24
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939088"
---
# <span data-ttu-id="e943f-101">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="e943f-101">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="e943f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e943f-102">SYNOPSIS</span></span>
<span data-ttu-id="e943f-103">Var olan ExpressRoute yapılandırma yetkilendirmesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e943f-103">Removes an existing ExpressRoute configuration authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e943f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e943f-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e943f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e943f-105">DESCRIPTION</span></span>
<span data-ttu-id="e943f-106">**Remove-Azurermexpressroutetormauthorter** cmdlet 'ı ExpressRoute devresine atanan bir yetkilendirmeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e943f-106">The **Remove-AzureRmExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="e943f-107">ExpressRoute devreleri ortak Internet yerine bir bağlantı sağlayıcısı kullanarak şirket içi ağınızı Azure 'a bağlayın.</span><span class="sxs-lookup"><span data-stu-id="e943f-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="e943f-108">ExpressRoute devresi sahibi her bir devrein en fazla 10 yetkilendirmesi oluşturabilir; Bu yetkilendirmeler sanal ağ sahibi tarafından, ağı devreye bağlamak için kullanılabilecek bir yetkilendirme anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e943f-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="e943f-109">Sanal ağ başına yalnızca bir yetkilendirme olabilir.</span><span class="sxs-lookup"><span data-stu-id="e943f-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="e943f-110">Ancak, herhangi bir zamanda, devre sahibi sanal ağa atanmış olan yetkilendirmeyi kaldırmak için **Remove-Azurermexpressroutedöngüye** at 'ı kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="e943f-110">At any time, however, the circuit owner can use **Remove-AzureRmExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="e943f-111">Bu durumda, ilgili sanal ağ artık Azure 'a bağlanmak için ExpressRoute devresini kullanamaz.</span><span class="sxs-lookup"><span data-stu-id="e943f-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="e943f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e943f-112">EXAMPLES</span></span>

### <span data-ttu-id="e943f-113">Örnek 1: ExpressRoute devresi 'den devre yetkilendirmeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="e943f-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="e943f-114">Bu örnekte, ExpressRoute devresi bir devre yetkilendirmesi kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="e943f-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="e943f-115">İlk komut **Get-Azurermexpressroutedevresi** öğesini kullanarak, contosodevresi adlı bir ExpressRoute devresine nesne başvurusu oluşturabilir ve sonucu $Circuit adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="e943f-115">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>

<span data-ttu-id="e943f-116">İkinci komut devre yetkisini kaldırmak için devre</span><span class="sxs-lookup"><span data-stu-id="e943f-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>

<span data-ttu-id="e943f-117">Üçüncü komut, $Circuit değişkeninde depolanan ExpressRoute devresini kaldırmayı onaylamak için Set-AzureRmExpressRouteCircuit cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e943f-117">The third command uses the Set-AzureRmExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="e943f-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e943f-118">PARAMETERS</span></span>

### <span data-ttu-id="e943f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e943f-119">-DefaultProfile</span></span>
<span data-ttu-id="e943f-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e943f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e943f-121">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="e943f-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="e943f-122">Bu cmdlet 'in kaldırdığı Expressroutedevresi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e943f-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e943f-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="e943f-123">-Name</span></span>
<span data-ttu-id="e943f-124">Bu cmdlet 'in kaldırdığı devre yetkilendirmesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e943f-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e943f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e943f-125">CommonParameters</span></span>
<span data-ttu-id="e943f-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e943f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e943f-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e943f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e943f-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e943f-128">INPUTS</span></span>

### <span data-ttu-id="e943f-129">Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="e943f-129">PSExpressRouteCircuit</span></span>
<span data-ttu-id="e943f-130">Bu cmdlet, **Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi** nesnesinin ardışık işlem örneklerini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="e943f-130">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="e943f-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e943f-131">OUTPUTS</span></span>

### <span data-ttu-id="e943f-132">Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="e943f-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="e943f-133">Bu cmdlet, **Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi** nesnesinin varolan örneklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e943f-133">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="e943f-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e943f-134">NOTES</span></span>

## <span data-ttu-id="e943f-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e943f-135">RELATED LINKS</span></span>

[<span data-ttu-id="e943f-136">Add-Azurermexpressroutetorisuthorter</span><span class="sxs-lookup"><span data-stu-id="e943f-136">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="e943f-137">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="e943f-137">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e943f-138">Get-Azurermexpressrouteter</span><span class="sxs-lookup"><span data-stu-id="e943f-138">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="e943f-139">Yeni-azurermexpressroutepatlar</span><span class="sxs-lookup"><span data-stu-id="e943f-139">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="e943f-140">Set-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="e943f-140">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
