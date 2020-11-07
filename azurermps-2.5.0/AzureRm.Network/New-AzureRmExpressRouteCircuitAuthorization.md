---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: f0e66c1e601ab63eec6d2540edd3ba0235727e9a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939293"
---
# <span data-ttu-id="1037e-101">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="1037e-101">New-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="1037e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1037e-102">SYNOPSIS</span></span>
<span data-ttu-id="1037e-103">ExpressRoute devresi yetkilendirmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1037e-103">Creates an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1037e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1037e-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1037e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1037e-105">DESCRIPTION</span></span>
<span data-ttu-id="1037e-106">**Yeni-Azurermexpressroutetor,** bir ExpressRoute devresine eklenebilen bir devre yetkilendirmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1037e-106">The **New-AzureRmExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="1037e-107">ExpressRoute devreler şirket içi ağınızı, ortak Internet yerine bir bağlantı sağlayıcısı kullanarak Microsoft bulut 'a bağlayın.</span><span class="sxs-lookup"><span data-stu-id="1037e-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="1037e-108">ExpressRoute devresi sahibi her bir devrein en fazla 10 yetkilendirmesi oluşturabilir; Bu yetkilendirmeler, bir ağı devreye bağlamak için sanal ağ sahibi tarafından kullanılabilen bir yetkilendirme anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1037e-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="1037e-109">Sanal ağ başına yalnızca bir yetkilendirme olabilir.</span><span class="sxs-lookup"><span data-stu-id="1037e-109">There can only one authorization per virtual network.</span></span>

<span data-ttu-id="1037e-110">ExpressRoute devresini oluşturduktan sonra, bu devreye yetki eklemek için **Add-Azurermexpressroutetorisuthorter** 'ı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1037e-110">After you create an ExpressRoute circuit you can use **Add-AzureRmExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="1037e-111">Alternatif olarak, devrede aynı anda yeni bir devreye eklenebilen bir yetkilendirme oluşturmak için **Yeni-Azurermexpressroutetorleruthor'i** kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1037e-111">Alternatively, you can use **New-AzureRmExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="1037e-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1037e-112">EXAMPLES</span></span>

### <span data-ttu-id="1037e-113">Örnek 1: yeni bir devre yetkilendirmesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1037e-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="1037e-114">Bu komut, Contosotoruthoruthori adında yeni bir devre yetkilendirmesi oluşturur ve bu nesneyi $Authorization adlı bir değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="1037e-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="1037e-115">Nesneyi bir değişkene kaydetmek önemlidir: **Yeni-Azurermexpressroutetorruuthorter** , bir devre için bu yetkilendirmeyi bir devre yoluna ekleyemiyor.</span><span class="sxs-lookup"><span data-stu-id="1037e-115">Saving the object to a variable is important: although **New-AzureRmExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="1037e-116">Bunun yerine, yeni bir $Authorization ExpressRoute devresi oluştururken New-AzureRmExpressRouteCircuit kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1037e-116">Instead, the variable $Authorization is used New-AzureRmExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>

<span data-ttu-id="1037e-117">Daha fazla bilgi için New-AzureRmExpressRouteCircuit cmdlet belgelerine bakın.</span><span class="sxs-lookup"><span data-stu-id="1037e-117">For more information, see the documentation for the New-AzureRmExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="1037e-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1037e-118">PARAMETERS</span></span>

### <span data-ttu-id="1037e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1037e-119">-DefaultProfile</span></span>
<span data-ttu-id="1037e-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1037e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1037e-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="1037e-121">-Name</span></span>
<span data-ttu-id="1037e-122">Yeni ExpressRoute devresi yetkilendirmesi için benzersiz bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="1037e-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="1037e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1037e-123">CommonParameters</span></span>
<span data-ttu-id="1037e-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1037e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1037e-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1037e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1037e-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1037e-126">INPUTS</span></span>

### <span data-ttu-id="1037e-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1037e-127">None</span></span>
<span data-ttu-id="1037e-128">Bu cmdlet, ardışık düzen girişini kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="1037e-128">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="1037e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1037e-129">OUTPUTS</span></span>

### <span data-ttu-id="1037e-130">Psexpressroutetorte</span><span class="sxs-lookup"><span data-stu-id="1037e-130">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="1037e-131">Bu cmdlet, **Microsoft. Azure. Commands. Network. model. Psexpressroutetorsunuthorter** nesnesi örneklerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1037e-131">This cmdlet creates instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="1037e-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1037e-132">NOTES</span></span>

## <span data-ttu-id="1037e-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1037e-133">RELATED LINKS</span></span>

[<span data-ttu-id="1037e-134">Add-Azurermexpressroutetorisuthorter</span><span class="sxs-lookup"><span data-stu-id="1037e-134">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="1037e-135">Get-Azurermexpressrouteter</span><span class="sxs-lookup"><span data-stu-id="1037e-135">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="1037e-136">Remove-Azurermexpressrouteter</span><span class="sxs-lookup"><span data-stu-id="1037e-136">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

