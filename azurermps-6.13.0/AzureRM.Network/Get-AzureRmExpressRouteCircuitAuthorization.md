---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 5b277ca35071c3639a3c7b341451cea78c024901
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594384"
---
# <span data-ttu-id="56e2c-101">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="56e2c-101">Get-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="56e2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56e2c-102">SYNOPSIS</span></span>
<span data-ttu-id="56e2c-103">ExpressRoute devresi yetkilendirmeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="56e2c-103">Gets information about ExpressRoute circuit authorizations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56e2c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56e2c-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56e2c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="56e2c-105">DESCRIPTION</span></span>
<span data-ttu-id="56e2c-106">**Get-Azurermexpressroutetormauthorter** cmdlet 'ı ExpressRoute devresini atanmış yetkilendirmeler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="56e2c-106">The **Get-AzureRmExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="56e2c-107">ExpressRoute devreler şirket içi ağınızı, ortak Internet yerine bir bağlantı sağlayıcısı kullanarak Microsoft bulut 'a bağlayın.</span><span class="sxs-lookup"><span data-stu-id="56e2c-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="56e2c-108">ExpressRoute devresi sahibi her bir devrein en fazla 10 yetkilendirmesi oluşturabilir; Bu yetkilendirmeler, bir sanal ağ sahibi tarafından ağı devreye (sanal ağ başına bir yetkilendirme) bağlamak için kullanılabilecek bir yetkilendirme anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="56e2c-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="56e2c-109">Yetkilendirme anahtarlarının yanı sıra yetkilendirme ile ilgili diğer bilgiler de, **Get-Azurermexpressroutepatınuthorçalıştırmaya** uygun olarak görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="56e2c-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzureRmExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="56e2c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56e2c-110">EXAMPLES</span></span>

### <span data-ttu-id="56e2c-111">Örnek 1: tüm ExpressRoute yetkilendirmelerini alma</span><span class="sxs-lookup"><span data-stu-id="56e2c-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="56e2c-112">Bu komutlar ExpressRoute devresi ile ilişkilendirilmiş tüm ExpressRoute yetkilendirmeleri hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="56e2c-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="56e2c-113">İlk komut, Contosodevresi adlı bir devrenin nesne başvurusu oluşturmak için **Get-Azurermexpressroutedevresi** cmdlet 'ini kullanır; Bu nesne başvurusu $Circuit değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="56e2c-113">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="56e2c-114">İkinci komut daha sonra bu nesne başvurusunu ve **Get-Azurermexpressroutedöngü** komutunu kullanarak, contosodevresi ile ilişkilendirilmiş yetkilendirmeler hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="56e2c-114">The second command then uses that object reference and the **Get-AzureRmExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="56e2c-115">Örnek 2: Where-Object cmdlet 'ini kullanarak tüm ExpressRoute yetkilendirmelerini alma</span><span class="sxs-lookup"><span data-stu-id="56e2c-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="56e2c-116">Bu komutlar, örnek 1 ' de kullanılan komutlarda çeşitlemesini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="56e2c-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="56e2c-117">Bu durumda, bilgiler yalnızca kullanılabilir (yani sanal bir ağa atanmamış yetkilendirmeler için) için kullanılabilir olan yetkilendirmeler için döndürülür.</span><span class="sxs-lookup"><span data-stu-id="56e2c-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="56e2c-118">Bunu yapmak için, devre yetkilendirme bilgileri komut 2 ' de döndürülür ve **WHERE-Object** cmdlet 'ine gönderilir.</span><span class="sxs-lookup"><span data-stu-id="56e2c-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="56e2c-119">**Burada-Object** , yalnızca *authorizationusestatus* özelliğinin kullanılabilir olduğu yetkilendirmeler seçer.</span><span class="sxs-lookup"><span data-stu-id="56e2c-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="56e2c-120">Yalnızca kullanılamayan yetkilendirmeleri listelemek için, WHERE yan tümcesi için şu söz dizimini kullanın: `{$_.AuthorizationUseStatus -ne "Available"}`</span><span class="sxs-lookup"><span data-stu-id="56e2c-120">To list only those authorizations that are not available, use this syntax for the Where clause: `{$_.AuthorizationUseStatus -ne "Available"}`</span></span>

## <span data-ttu-id="56e2c-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56e2c-121">PARAMETERS</span></span>

### <span data-ttu-id="56e2c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e2c-122">-DefaultProfile</span></span>
<span data-ttu-id="56e2c-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="56e2c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56e2c-124">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="56e2c-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="56e2c-125">ExpressRoute devresi yetkilendirmesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="56e2c-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="56e2c-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="56e2c-126">-Name</span></span>
<span data-ttu-id="56e2c-127">Bu cmdlet 'in aldığı ExpressRoute devresi yetkilendirmesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="56e2c-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>
<span data-ttu-id="56e2c-128">-Name "Contosotorun"</span><span class="sxs-lookup"><span data-stu-id="56e2c-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="56e2c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e2c-129">CommonParameters</span></span>
<span data-ttu-id="56e2c-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56e2c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e2c-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56e2c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e2c-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56e2c-132">INPUTS</span></span>

### <span data-ttu-id="56e2c-133">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="56e2c-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="56e2c-134">Parametreler: Expressroutedevresi (ByValue)</span><span class="sxs-lookup"><span data-stu-id="56e2c-134">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="56e2c-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56e2c-135">OUTPUTS</span></span>

### <span data-ttu-id="56e2c-136">Microsoft. Azure. Commands. Network. model. Psexpressroutetorduthorter</span><span class="sxs-lookup"><span data-stu-id="56e2c-136">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="56e2c-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56e2c-137">NOTES</span></span>

## <span data-ttu-id="56e2c-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56e2c-138">RELATED LINKS</span></span>

[<span data-ttu-id="56e2c-139">Add-Azurermexpressroutetorisuthorter</span><span class="sxs-lookup"><span data-stu-id="56e2c-139">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="56e2c-140">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="56e2c-140">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="56e2c-141">Yeni-azurermexpressroutepatlar</span><span class="sxs-lookup"><span data-stu-id="56e2c-141">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="56e2c-142">Remove-Azurermexpressrouteter</span><span class="sxs-lookup"><span data-stu-id="56e2c-142">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)
