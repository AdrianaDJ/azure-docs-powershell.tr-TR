---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 03b9e64970be7f3d3876a3d04f26b11ac24dd8ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593538"
---
# <span data-ttu-id="bab13-101">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="bab13-101">Add-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="bab13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bab13-102">SYNOPSIS</span></span>
<span data-ttu-id="bab13-103">ExpressRoute devresi yetkilendirmesi ekler.</span><span class="sxs-lookup"><span data-stu-id="bab13-103">Adds an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bab13-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bab13-104">SYNTAX</span></span>

```
Add-AzureRmExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bab13-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bab13-105">DESCRIPTION</span></span>
<span data-ttu-id="bab13-106">**Add-Azurermexpressroutetor,** bir ExpressRoute devresini yetkilendirme ekler.</span><span class="sxs-lookup"><span data-stu-id="bab13-106">The **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="bab13-107">ExpressRoute devreler şirket içi ağınızı, ortak Internet yerine bir bağlantı sağlayıcısı kullanarak Microsoft bulut 'a bağlayın.</span><span class="sxs-lookup"><span data-stu-id="bab13-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="bab13-108">ExpressRoute devresi sahibi her bir devrein en fazla 10 yetkilendirmesi oluşturabilir; Bu yetkilendirmeler, bir sanal ağ sahibi tarafından ağı devreye (sanal ağ başına bir yetkilendirme) bağlamak için kullanılabilecek bir yetkilendirme anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bab13-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="bab13-109">**Add-Azurermexpressroutetorisuthorter** bir devreye yeni bir yetkilendirme ekler ve aynı zamanda ilgili yetkilendirme anahtarını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bab13-109">**Add-AzureRmExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="bab13-110">Bu tuşlar, Get-AzureRmExpressRouteCircuitAuthorization cmdlet 'i çalıştırarak ve gerektiğinde uygun ağ sahibine kopyalanabilir ve iletilebileceği zaman görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="bab13-110">These keys can be viewed at any time by running the Get-AzureRmExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>

<span data-ttu-id="bab13-111">**Add-Azurermexpressrouteter** 'i çalıştırdıktan sonra, anahtarı etkinleştirmek için Set-AzureRmExpressRouteCircuit cmdlet 'ini çağırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="bab13-111">Note that, after running **Add-AzureRmExpressRouteCircuitAuthorization** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="bab13-112">**Set-Azurermexpressroutedevresi** çağrımıyorsanız, yetkilendirme devreye eklenir ancak kullanım için etkinleştirilmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="bab13-112">If you do not call **Set-AzureRmExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="bab13-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bab13-113">EXAMPLES</span></span>

### <span data-ttu-id="bab13-114">Örnek 1: belirtilen ExpressRoute devresi için yetkilendirme ekleme</span><span class="sxs-lookup"><span data-stu-id="bab13-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="bab13-115">Bu örnekteki komutlar var olan ExpressRoute devresine yeni bir yetkilendirme ekler.</span><span class="sxs-lookup"><span data-stu-id="bab13-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="bab13-116">İlk komut, Contosodevresi adlı bir devrenin nesne başvurusunu oluşturmak için **Get-Azurermexpressroutedevresi** kullanır.</span><span class="sxs-lookup"><span data-stu-id="bab13-116">The first command uses **Get-AzureRmExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="bab13-117">Bu nesne başvurusu $Circuit adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="bab13-117">That object reference is stored in a variable named $Circuit.</span></span>

<span data-ttu-id="bab13-118">İkinci komutta, New Authorization (Contosoınuthorbir) ExpressRoute devresine eklemek için **Add-Azurermexpressroutetorisuthorter** cmdlet 'i kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bab13-118">In the second command, the **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="bab13-119">Bu komut yetkilendirmeyi ekler ancak bu yetkilendirmeyi etkilemez.</span><span class="sxs-lookup"><span data-stu-id="bab13-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="bab13-120">Yetkilendirmeyi etkinleştirmek, örnekteki son komutta gösterilen **set-Azurermexpressroutedevresi** gerektirir.</span><span class="sxs-lookup"><span data-stu-id="bab13-120">Activating an authorization requires the **Set-AzureRmExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="bab13-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bab13-121">PARAMETERS</span></span>

### <span data-ttu-id="bab13-122">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="bab13-122">-ExpressRouteCircuit</span></span>
<span data-ttu-id="bab13-123">Bu cmdlet 'in yetkilendirmeyi eklediği ExpressRoute devresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bab13-123">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="bab13-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="bab13-124">-Name</span></span>
<span data-ttu-id="bab13-125">Eklenecek devre yetkilendirmesi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bab13-125">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="bab13-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bab13-126">-DefaultProfile</span></span>
<span data-ttu-id="bab13-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bab13-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bab13-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bab13-128">CommonParameters</span></span>
<span data-ttu-id="bab13-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bab13-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bab13-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bab13-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bab13-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bab13-131">INPUTS</span></span>

### <span data-ttu-id="bab13-132">Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="bab13-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="bab13-133">**Add-Azurermexpressroutetorisuthorter** **Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi** nesnesinin ardışık olarak kullanılan örneklerini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="bab13-133">**Add-AzureRmExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="bab13-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bab13-134">OUTPUTS</span></span>

### <span data-ttu-id="bab13-135">Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="bab13-135">PSExpressRouteCircuit</span></span>
<span data-ttu-id="bab13-136">**Add-Azurermexpressroutepatlarmicrosoft** **. Azure. Commands. Network. model. Psexpressroutedevresi** nesnesinin örneklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bab13-136">**Add-AzureRmExpressRouteCircuitAuthorization** modifies instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="bab13-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bab13-137">NOTES</span></span>

## <span data-ttu-id="bab13-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bab13-138">RELATED LINKS</span></span>

[<span data-ttu-id="bab13-139">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="bab13-139">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="bab13-140">Get-Azurermexpressrouteter</span><span class="sxs-lookup"><span data-stu-id="bab13-140">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="bab13-141">Yeni-azurermexpressroutepatlar</span><span class="sxs-lookup"><span data-stu-id="bab13-141">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="bab13-142">Remove-Azurermexpressrouteter</span><span class="sxs-lookup"><span data-stu-id="bab13-142">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="bab13-143">Set-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="bab13-143">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
