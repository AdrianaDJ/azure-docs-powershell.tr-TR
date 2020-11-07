---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d97c6825a6681127e2275a7d3d171e6500daba5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760722"
---
# <span data-ttu-id="a9808-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="a9808-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="a9808-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9808-102">SYNOPSIS</span></span>
<span data-ttu-id="a9808-103">ExpressRoute devresi yetkilendirmesi ekler.</span><span class="sxs-lookup"><span data-stu-id="a9808-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="a9808-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9808-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9808-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9808-105">DESCRIPTION</span></span>
<span data-ttu-id="a9808-106">**Add-Azexpressroutetorvazuthor,** bir ExpressRoute devresini yetkilendirme ekler.</span><span class="sxs-lookup"><span data-stu-id="a9808-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="a9808-107">ExpressRoute devreler şirket içi ağınızı, ortak Internet yerine bir bağlantı sağlayıcısı kullanarak Microsoft bulut 'a bağlayın.</span><span class="sxs-lookup"><span data-stu-id="a9808-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="a9808-108">ExpressRoute devresi sahibi her bir devrein en fazla 10 yetkilendirmesi oluşturabilir; Bu yetkilendirmeler, bir sanal ağ sahibi tarafından ağı devreye (sanal ağ başına bir yetkilendirme) bağlamak için kullanılabilecek bir yetkilendirme anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9808-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="a9808-109">**Add-Azexpressroutetorti uthorter** bir devreye yeni bir yetkilendirme ekler ve aynı zamanda ilgili yetkilendirme anahtarını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9808-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="a9808-110">Bu tuşlar, Get-AzExpressRouteCircuitAuthorization cmdlet 'i çalıştırarak ve gerektiğinde uygun ağ sahibine kopyalanabilir ve iletilebileceği zaman görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="a9808-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>
<span data-ttu-id="a9808-111">**Add-Azexpressroutetortoruthorçalıştırılmı** çalıştırdıktan sonra, anahtarı etkinleştirmek için Set-AzExpressRouteCircuit cmdlet 'ini çağırmanız gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="a9808-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="a9808-112">**Set-Azexpressroutedevresi** çağrımıyorsanız, yetkilendirme devreye eklenir ancak kullanım için etkinleştirilmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="a9808-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="a9808-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9808-113">EXAMPLES</span></span>

### <span data-ttu-id="a9808-114">Örnek 1: belirtilen ExpressRoute devresi için yetkilendirme ekleme</span><span class="sxs-lookup"><span data-stu-id="a9808-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="a9808-115">Bu örnekteki komutlar var olan ExpressRoute devresine yeni bir yetkilendirme ekler.</span><span class="sxs-lookup"><span data-stu-id="a9808-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="a9808-116">İlk komut, Contosodevresi adlı bir devrenin nesne başvurusunu oluşturmak için **Get-Azexpressroutedevkomutunu** kullanır.</span><span class="sxs-lookup"><span data-stu-id="a9808-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="a9808-117">Bu nesne başvurusu $Circuit adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="a9808-117">That object reference is stored in a variable named $Circuit.</span></span>
<span data-ttu-id="a9808-118">İkinci komutta, New Authorization (Contosotoruthorbir kez) ExpressRoute devresi eklemek için **Add-Azexpressroutetorvazuthorme** cmdlet 'i kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a9808-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="a9808-119">Bu komut yetkilendirmeyi ekler ancak bu yetkilendirmeyi etkilemez.</span><span class="sxs-lookup"><span data-stu-id="a9808-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="a9808-120">Yetkilendirmeyi etkinleştirmek, örnekteki son komutta gösterilen **set-Azexpressroutebir devresini** gerektirir.</span><span class="sxs-lookup"><span data-stu-id="a9808-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="a9808-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9808-121">PARAMETERS</span></span>

### <span data-ttu-id="a9808-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9808-122">-DefaultProfile</span></span>
<span data-ttu-id="a9808-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9808-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9808-124">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a9808-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="a9808-125">Bu cmdlet 'in yetkilendirmeyi eklediği ExpressRoute devresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9808-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="a9808-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="a9808-126">-Name</span></span>
<span data-ttu-id="a9808-127">Eklenecek devre yetkilendirmesi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9808-127">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="a9808-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9808-128">CommonParameters</span></span>
<span data-ttu-id="a9808-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9808-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9808-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9808-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9808-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9808-131">INPUTS</span></span>

### <span data-ttu-id="a9808-132">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a9808-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a9808-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9808-133">OUTPUTS</span></span>

### <span data-ttu-id="a9808-134">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a9808-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a9808-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9808-135">NOTES</span></span>

## <span data-ttu-id="a9808-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9808-136">RELATED LINKS</span></span>

[<span data-ttu-id="a9808-137">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a9808-137">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a9808-138">Get-Azexpressroutetorvazgetir</span><span class="sxs-lookup"><span data-stu-id="a9808-138">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="a9808-139">Yeni-Azexpressroutetorter</span><span class="sxs-lookup"><span data-stu-id="a9808-139">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="a9808-140">Remove-Azexpressroutetori Uthorremove</span><span class="sxs-lookup"><span data-stu-id="a9808-140">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="a9808-141">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a9808-141">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
