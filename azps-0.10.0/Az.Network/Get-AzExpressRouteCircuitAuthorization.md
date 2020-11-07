---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 3b51a16d6ff2de8292b1bbb66f7f5ab24cc17b93
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935548"
---
# <span data-ttu-id="f47b0-101">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="f47b0-101">Get-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="f47b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f47b0-102">SYNOPSIS</span></span>
<span data-ttu-id="f47b0-103">ExpressRoute devresi yetkilendirmeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="f47b0-103">Gets information about ExpressRoute circuit authorizations.</span></span>

## <span data-ttu-id="f47b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f47b0-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f47b0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f47b0-105">DESCRIPTION</span></span>
<span data-ttu-id="f47b0-106">**Get-Azexpressroutetorkuruthorter** cmdlet 'ı ExpressRoute devresine atanmış yetkilendirmeler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="f47b0-106">The **Get-AzExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="f47b0-107">ExpressRoute devreler şirket içi ağınızı, ortak Internet yerine bir bağlantı sağlayıcısı kullanarak Microsoft bulut 'a bağlayın.</span><span class="sxs-lookup"><span data-stu-id="f47b0-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="f47b0-108">ExpressRoute devresi sahibi her bir devrein en fazla 10 yetkilendirmesi oluşturabilir; Bu yetkilendirmeler, bir sanal ağ sahibi tarafından ağı devreye (sanal ağ başına bir yetkilendirme) bağlamak için kullanılabilecek bir yetkilendirme anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f47b0-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="f47b0-109">Yetkilendirme anahtarlarının yanı sıra yetkilendirme ile ilgili diğer bilgiler de, **Get-Azexpressroutetordi** 'i çalıştırarak herhangi bir zamanda görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="f47b0-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="f47b0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f47b0-110">EXAMPLES</span></span>

### <span data-ttu-id="f47b0-111">Örnek 1: tüm ExpressRoute yetkilendirmelerini alma</span><span class="sxs-lookup"><span data-stu-id="f47b0-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="f47b0-112">Bu komutlar ExpressRoute devresi ile ilişkilendirilmiş tüm ExpressRoute yetkilendirmeleri hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="f47b0-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="f47b0-113">İlk komut, Contosodevresi adlı bir devrenin nesne başvurusu oluşturmak için **Get-Azexpressroutedevresi** öğesini kullanır; Bu nesne başvurusu $Circuit değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="f47b0-113">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="f47b0-114">İkinci komut daha sonra, bu nesne başvurusunu ve **Get-Azexpressroutetorınuthorwıth**</span><span class="sxs-lookup"><span data-stu-id="f47b0-114">The second command then uses that object reference and the **Get-AzExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="f47b0-115">Örnek 2: Where-Object cmdlet 'ini kullanarak tüm ExpressRoute yetkilendirmelerini alma</span><span class="sxs-lookup"><span data-stu-id="f47b0-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="f47b0-116">Bu komutlar, örnek 1 ' de kullanılan komutlarda çeşitlemesini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="f47b0-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="f47b0-117">Bu durumda, bilgiler yalnızca kullanılabilir (yani sanal bir ağa atanmamış yetkilendirmeler için) için kullanılabilir olan yetkilendirmeler için döndürülür.</span><span class="sxs-lookup"><span data-stu-id="f47b0-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="f47b0-118">Bunu yapmak için, devre yetkilendirme bilgileri komut 2 ' de döndürülür ve **WHERE-Object** cmdlet 'ine gönderilir.</span><span class="sxs-lookup"><span data-stu-id="f47b0-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="f47b0-119">**Burada-Object** , yalnızca *authorizationusestatus* özelliğinin kullanılabilir olduğu yetkilendirmeler seçer.</span><span class="sxs-lookup"><span data-stu-id="f47b0-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="f47b0-120">Yalnızca kullanılamayan yetkilendirmeleri listelemek için, WHERE yan tümcesi için şu söz dizimini kullanın:</span><span class="sxs-lookup"><span data-stu-id="f47b0-120">To list only those authorizations that are not available, use this syntax for the Where clause:</span></span>

`{$_.AuthorizationUseStatus -ne "Available"}`

## <span data-ttu-id="f47b0-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f47b0-121">PARAMETERS</span></span>

### <span data-ttu-id="f47b0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f47b0-122">-DefaultProfile</span></span>
<span data-ttu-id="f47b0-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f47b0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f47b0-124">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="f47b0-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="f47b0-125">ExpressRoute devresi yetkilendirmesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f47b0-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="f47b0-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="f47b0-126">-Name</span></span>
<span data-ttu-id="f47b0-127">Bu cmdlet 'in aldığı ExpressRoute devresi yetkilendirmesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f47b0-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>

<span data-ttu-id="f47b0-128">-Name "Contosotorun"</span><span class="sxs-lookup"><span data-stu-id="f47b0-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="f47b0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f47b0-129">CommonParameters</span></span>
<span data-ttu-id="f47b0-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f47b0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f47b0-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f47b0-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f47b0-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f47b0-132">INPUTS</span></span>

### <span data-ttu-id="f47b0-133">Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="f47b0-133">PSExpressRouteCircuit</span></span>
<span data-ttu-id="f47b0-134">**Get-Azexpressroutetorduthor,** **Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi** nesnesinin ardışık olarak birleştirilmiş örneklerini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="f47b0-134">**Get-AzExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="f47b0-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f47b0-135">OUTPUTS</span></span>

### <span data-ttu-id="f47b0-136">Psexpressroutetorte</span><span class="sxs-lookup"><span data-stu-id="f47b0-136">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="f47b0-137">**Get-Azexpressroutetorduthorter** , **Microsoft. Azure. Commands. Network. model. Psexpressroutetorduthorter** nesnesinin örneklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="f47b0-137">**Get-AzExpressRouteCircuitAuthorization** returns instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="f47b0-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f47b0-138">NOTES</span></span>

## <span data-ttu-id="f47b0-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f47b0-139">RELATED LINKS</span></span>

[<span data-ttu-id="f47b0-140">Add-Azexpressroutetori Uthorter</span><span class="sxs-lookup"><span data-stu-id="f47b0-140">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="f47b0-141">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="f47b0-141">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="f47b0-142">Yeni-Azexpressroutetorter</span><span class="sxs-lookup"><span data-stu-id="f47b0-142">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="f47b0-143">Remove-Azexpressroutetori Uthorremove</span><span class="sxs-lookup"><span data-stu-id="f47b0-143">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)
