---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: efe2a149d2ca02c075b2e0a1f73191e9e2b8859b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935643"
---
# <span data-ttu-id="41b84-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="41b84-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="41b84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41b84-102">SYNOPSIS</span></span>
<span data-ttu-id="41b84-103">ExpressRoute devresi yetkilendirmesi ekler.</span><span class="sxs-lookup"><span data-stu-id="41b84-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="41b84-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="41b84-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41b84-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="41b84-105">DESCRIPTION</span></span>
<span data-ttu-id="41b84-106">**Add-Azexpressroutetorvazuthor,** bir ExpressRoute devresini yetkilendirme ekler.</span><span class="sxs-lookup"><span data-stu-id="41b84-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="41b84-107">ExpressRoute devreler şirket içi ağınızı, ortak Internet yerine bir bağlantı sağlayıcısı kullanarak Microsoft bulut 'a bağlayın.</span><span class="sxs-lookup"><span data-stu-id="41b84-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="41b84-108">ExpressRoute devresi sahibi her bir devrein en fazla 10 yetkilendirmesi oluşturabilir; Bu yetkilendirmeler, bir sanal ağ sahibi tarafından ağı devreye (sanal ağ başına bir yetkilendirme) bağlamak için kullanılabilecek bir yetkilendirme anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="41b84-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="41b84-109">**Add-Azexpressroutetorti uthorter** bir devreye yeni bir yetkilendirme ekler ve aynı zamanda ilgili yetkilendirme anahtarını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="41b84-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="41b84-110">Bu tuşlar, Get-AzExpressRouteCircuitAuthorization cmdlet 'i çalıştırarak ve gerektiğinde uygun ağ sahibine kopyalanabilir ve iletilebileceği zaman görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="41b84-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>

<span data-ttu-id="41b84-111">**Add-Azexpressroutetortoruthorçalıştırılmı** çalıştırdıktan sonra, anahtarı etkinleştirmek için Set-AzExpressRouteCircuit cmdlet 'ini çağırmanız gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="41b84-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="41b84-112">**Set-Azexpressroutedevresi** çağrımıyorsanız, yetkilendirme devreye eklenir ancak kullanım için etkinleştirilmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="41b84-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="41b84-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="41b84-113">EXAMPLES</span></span>

### <span data-ttu-id="41b84-114">Örnek 1: belirtilen ExpressRoute devresi için yetkilendirme ekleme</span><span class="sxs-lookup"><span data-stu-id="41b84-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="41b84-115">Bu örnekteki komutlar var olan ExpressRoute devresine yeni bir yetkilendirme ekler.</span><span class="sxs-lookup"><span data-stu-id="41b84-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="41b84-116">İlk komut, Contosodevresi adlı bir devrenin nesne başvurusunu oluşturmak için **Get-Azexpressroutedevkomutunu** kullanır.</span><span class="sxs-lookup"><span data-stu-id="41b84-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="41b84-117">Bu nesne başvurusu $Circuit adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="41b84-117">That object reference is stored in a variable named $Circuit.</span></span>

<span data-ttu-id="41b84-118">İkinci komutta, New Authorization (Contosotoruthorbir kez) ExpressRoute devresi eklemek için **Add-Azexpressroutetorvazuthorme** cmdlet 'i kullanılır.</span><span class="sxs-lookup"><span data-stu-id="41b84-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="41b84-119">Bu komut yetkilendirmeyi ekler ancak bu yetkilendirmeyi etkilemez.</span><span class="sxs-lookup"><span data-stu-id="41b84-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="41b84-120">Yetkilendirmeyi etkinleştirmek, örnekteki son komutta gösterilen **set-Azexpressroutebir devresini** gerektirir.</span><span class="sxs-lookup"><span data-stu-id="41b84-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="41b84-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="41b84-121">PARAMETERS</span></span>

### <span data-ttu-id="41b84-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41b84-122">-DefaultProfile</span></span>
<span data-ttu-id="41b84-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="41b84-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41b84-124">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="41b84-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="41b84-125">Bu cmdlet 'in yetkilendirmeyi eklediği ExpressRoute devresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="41b84-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="41b84-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="41b84-126">-Name</span></span>
<span data-ttu-id="41b84-127">Eklenecek devre yetkilendirmesi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="41b84-127">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="41b84-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b84-128">CommonParameters</span></span>
<span data-ttu-id="41b84-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="41b84-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b84-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41b84-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b84-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="41b84-131">INPUTS</span></span>

### <span data-ttu-id="41b84-132">Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="41b84-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="41b84-133">**Add-Azexpressroutetorsunuthor,** **Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi** nesnesinin ardışık olarak birleştirilmiş örneklerini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="41b84-133">**Add-AzExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="41b84-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="41b84-134">OUTPUTS</span></span>

### <span data-ttu-id="41b84-135">Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="41b84-135">PSExpressRouteCircuit</span></span>
<span data-ttu-id="41b84-136">**Add-Azexpressroutetorstanuthor,** **Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi** nesnesinin örneklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="41b84-136">**Add-AzExpressRouteCircuitAuthorization** modifies instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="41b84-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="41b84-137">NOTES</span></span>

## <span data-ttu-id="41b84-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="41b84-138">RELATED LINKS</span></span>

[<span data-ttu-id="41b84-139">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="41b84-139">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="41b84-140">Get-Azexpressroutetorvazgetir</span><span class="sxs-lookup"><span data-stu-id="41b84-140">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="41b84-141">Yeni-Azexpressroutetorter</span><span class="sxs-lookup"><span data-stu-id="41b84-141">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="41b84-142">Remove-Azexpressroutetori Uthorremove</span><span class="sxs-lookup"><span data-stu-id="41b84-142">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="41b84-143">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="41b84-143">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
