---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 28b45f5368fb7a63450276c054654313d7e1c517
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104748"
---
# <span data-ttu-id="98118-101">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="98118-101">New-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="98118-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98118-102">SYNOPSIS</span></span>
<span data-ttu-id="98118-103">ExpressRoute devresi yetkilendirmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98118-103">Creates an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="98118-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98118-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98118-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="98118-105">DESCRIPTION</span></span>
<span data-ttu-id="98118-106">**New-Azexpressroutetorvazuthor,** bir ExpressRoute devresine eklenebilen bir devre yetkilendirmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98118-106">The **New-AzExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="98118-107">ExpressRoute devreler şirket içi ağınızı, ortak Internet yerine bir bağlantı sağlayıcısı kullanarak Microsoft bulut 'a bağlayın.</span><span class="sxs-lookup"><span data-stu-id="98118-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="98118-108">ExpressRoute devresi sahibi her bir devrein en fazla 10 yetkilendirmesi oluşturabilir; Bu yetkilendirmeler, bir ağı devreye bağlamak için sanal ağ sahibi tarafından kullanılabilen bir yetkilendirme anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98118-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="98118-109">Sanal ağ başına yalnızca bir yetkilendirme olabilir.</span><span class="sxs-lookup"><span data-stu-id="98118-109">There can only one authorization per virtual network.</span></span>
<span data-ttu-id="98118-110">ExpressRoute devresini oluşturduktan sonra, **Add-Azexpressroutetori**</span><span class="sxs-lookup"><span data-stu-id="98118-110">After you create an ExpressRoute circuit you can use **Add-AzExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="98118-111">Alternatif olarak, devrede aynı anda yeni bir devreye eklenebilen bir yetkilendirme oluşturmak için **Yeni-Azexpressroutetorda** 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="98118-111">Alternatively, you can use **New-AzExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="98118-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98118-112">EXAMPLES</span></span>

### <span data-ttu-id="98118-113">Örnek 1: yeni bir devre yetkilendirmesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="98118-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="98118-114">Bu komut, Contosotoruthoruthori adında yeni bir devre yetkilendirmesi oluşturur ve bu nesneyi $Authorization adlı bir değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="98118-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="98118-115">Nesneyi bir değişkene kaydetmek önemlidir: **New-Azexpressroutetorvazmauthorter** , bu yetkilendirmeyi bir devre</span><span class="sxs-lookup"><span data-stu-id="98118-115">Saving the object to a variable is important: although **New-AzExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="98118-116">Bunun yerine, yeni bir $Authorization ExpressRoute devresi oluştururken New-AzExpressRouteCircuit kullanılır.</span><span class="sxs-lookup"><span data-stu-id="98118-116">Instead, the variable $Authorization is used New-AzExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>
<span data-ttu-id="98118-117">Daha fazla bilgi için New-AzExpressRouteCircuit cmdlet belgelerine bakın.</span><span class="sxs-lookup"><span data-stu-id="98118-117">For more information, see the documentation for the New-AzExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="98118-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98118-118">PARAMETERS</span></span>

### <span data-ttu-id="98118-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98118-119">-DefaultProfile</span></span>
<span data-ttu-id="98118-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="98118-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98118-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="98118-121">-Name</span></span>
<span data-ttu-id="98118-122">Yeni ExpressRoute devresi yetkilendirmesi için benzersiz bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="98118-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="98118-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98118-123">CommonParameters</span></span>
<span data-ttu-id="98118-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98118-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98118-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98118-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98118-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98118-126">INPUTS</span></span>

### <span data-ttu-id="98118-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="98118-127">None</span></span>

## <span data-ttu-id="98118-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98118-128">OUTPUTS</span></span>

### <span data-ttu-id="98118-129">Microsoft. Azure. Commands. Network. model. Psexpressroutetorduthorter</span><span class="sxs-lookup"><span data-stu-id="98118-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="98118-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98118-130">NOTES</span></span>

## <span data-ttu-id="98118-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98118-131">RELATED LINKS</span></span>

[<span data-ttu-id="98118-132">Add-Azexpressroutetori Uthorter</span><span class="sxs-lookup"><span data-stu-id="98118-132">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="98118-133">Get-Azexpressroutetorvazgetir</span><span class="sxs-lookup"><span data-stu-id="98118-133">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="98118-134">Remove-Azexpressroutetori Uthorremove</span><span class="sxs-lookup"><span data-stu-id="98118-134">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

