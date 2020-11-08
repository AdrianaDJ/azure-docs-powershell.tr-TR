---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d98366d9bd3fb42be39f68976e131ec644274431
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279643"
---
# <span data-ttu-id="a6d38-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="a6d38-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="a6d38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6d38-102">SYNOPSIS</span></span>
<span data-ttu-id="a6d38-103">Var olan ExpressRoute yapılandırma yetkilendirmesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a6d38-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="a6d38-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a6d38-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6d38-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a6d38-105">DESCRIPTION</span></span>
<span data-ttu-id="a6d38-106">**Remove-Azexpressroutetorvazuthoruthori**</span><span class="sxs-lookup"><span data-stu-id="a6d38-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="a6d38-107">ExpressRoute devreleri ortak Internet yerine bir bağlantı sağlayıcısı kullanarak şirket içi ağınızı Azure 'a bağlayın.</span><span class="sxs-lookup"><span data-stu-id="a6d38-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="a6d38-108">ExpressRoute devresi sahibi her bir devrein en fazla 10 yetkilendirmesi oluşturabilir; Bu yetkilendirmeler sanal ağ sahibi tarafından, ağı devreye bağlamak için kullanılabilecek bir yetkilendirme anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a6d38-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="a6d38-109">Sanal ağ başına yalnızca bir yetkilendirme olabilir.</span><span class="sxs-lookup"><span data-stu-id="a6d38-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="a6d38-110">Ancak, herhangi bir zamanda devre sahibi, sanal ağa atanmış yetkilendirmeyi kaldırmak için **Remove-Azexpressroutetor, uthorremove** kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="a6d38-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="a6d38-111">Bu durumda, ilgili sanal ağ artık Azure 'a bağlanmak için ExpressRoute devresini kullanamaz.</span><span class="sxs-lookup"><span data-stu-id="a6d38-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="a6d38-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a6d38-112">EXAMPLES</span></span>

### <span data-ttu-id="a6d38-113">Örnek 1: ExpressRoute devresi 'den devre yetkilendirmeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="a6d38-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="a6d38-114">Bu örnekte, ExpressRoute devresi bir devre yetkilendirmesi kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="a6d38-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="a6d38-115">İlk komut, Contosodevresi adlı bir ExpressRoute devresi 'e nesne başvurusu oluşturmak için **Get-Azexpressroutedevresini** kullanır ve sonucu $Circuit adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="a6d38-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="a6d38-116">İkinci komut devre yetkisini kaldırmak için devre</span><span class="sxs-lookup"><span data-stu-id="a6d38-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="a6d38-117">Üçüncü komut, $Circuit değişkeninde depolanan ExpressRoute devresini kaldırmayı onaylamak için Set-AzExpressRouteCircuit cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a6d38-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="a6d38-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a6d38-118">PARAMETERS</span></span>

### <span data-ttu-id="a6d38-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6d38-119">-DefaultProfile</span></span>
<span data-ttu-id="a6d38-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a6d38-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6d38-121">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a6d38-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="a6d38-122">Bu cmdlet 'in kaldırdığı Expressroutedevresi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6d38-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a6d38-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="a6d38-123">-Name</span></span>
<span data-ttu-id="a6d38-124">Bu cmdlet 'in kaldırdığı devre yetkilendirmesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6d38-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a6d38-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6d38-125">CommonParameters</span></span>
<span data-ttu-id="a6d38-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a6d38-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6d38-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6d38-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6d38-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a6d38-128">INPUTS</span></span>

### <span data-ttu-id="a6d38-129">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a6d38-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a6d38-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a6d38-130">OUTPUTS</span></span>

### <span data-ttu-id="a6d38-131">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a6d38-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a6d38-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a6d38-132">NOTES</span></span>

## <span data-ttu-id="a6d38-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a6d38-133">RELATED LINKS</span></span>

[<span data-ttu-id="a6d38-134">Add-Azexpressroutetori Uthorter</span><span class="sxs-lookup"><span data-stu-id="a6d38-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="a6d38-135">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a6d38-135">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a6d38-136">Get-Azexpressroutetorvazgetir</span><span class="sxs-lookup"><span data-stu-id="a6d38-136">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="a6d38-137">Yeni-Azexpressroutetorter</span><span class="sxs-lookup"><span data-stu-id="a6d38-137">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="a6d38-138">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a6d38-138">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
