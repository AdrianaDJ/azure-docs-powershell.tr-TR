---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: 7997949db725d50dd656479852b10d12094b8da7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096855"
---
# <span data-ttu-id="e295a-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e295a-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="e295a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e295a-102">SYNOPSIS</span></span>
<span data-ttu-id="e295a-103">Azure 'dan bir Azure ExpressRoute devresi alır.</span><span class="sxs-lookup"><span data-stu-id="e295a-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="e295a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e295a-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e295a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e295a-105">DESCRIPTION</span></span>
<span data-ttu-id="e295a-106">**Get-Azexpressroutedevresi** cmdlet 'i aboneliğinizden bir ExpressRoute devresi nesnesini almak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e295a-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="e295a-107">Döndürülen devre nesnesi ExpressRoute devreleriyle çalışan diğer cmdlet 'ler için girdi olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e295a-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="e295a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e295a-108">EXAMPLES</span></span>

### <span data-ttu-id="e295a-109">Örnek 1: ExpressRoute devresini alma</span><span class="sxs-lookup"><span data-stu-id="e295a-109">Example 1: Get the ExpressRoute circuit</span></span>
```
Get-AzExpressRouteCircuit -ResourceGroupName testrg -Name test

Name                             : test
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="e295a-110">"Testrg" adlı özel bir ExpressRoute devresini ve ResourceGroupName "test"</span><span class="sxs-lookup"><span data-stu-id="e295a-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="e295a-111">Örnek 2: filtreleme kullanarak ExpressRoute devrelerini listeleme</span><span class="sxs-lookup"><span data-stu-id="e295a-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
```
Get-AzExpressRouteCircuit -Name test*

Name                             : test1
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test1
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :

Name                             : test2
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test2
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="e295a-112">Adı "test" ile başlayan tüm ExpressRoute devrelerini edinin.</span><span class="sxs-lookup"><span data-stu-id="e295a-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="e295a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e295a-113">PARAMETERS</span></span>

### <span data-ttu-id="e295a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e295a-114">-DefaultProfile</span></span>
<span data-ttu-id="e295a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e295a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e295a-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="e295a-116">-Name</span></span>
<span data-ttu-id="e295a-117">ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="e295a-117">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e295a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e295a-118">-ResourceGroupName</span></span>
<span data-ttu-id="e295a-119">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e295a-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e295a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e295a-120">CommonParameters</span></span>
<span data-ttu-id="e295a-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e295a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e295a-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e295a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e295a-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e295a-123">INPUTS</span></span>

### <span data-ttu-id="e295a-124">System. String</span><span class="sxs-lookup"><span data-stu-id="e295a-124">System.String</span></span>

## <span data-ttu-id="e295a-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e295a-125">OUTPUTS</span></span>

### <span data-ttu-id="e295a-126">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="e295a-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e295a-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e295a-127">NOTES</span></span>

## <span data-ttu-id="e295a-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e295a-128">RELATED LINKS</span></span>

[<span data-ttu-id="e295a-129">Taşıma-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="e295a-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="e295a-130">Yeni-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="e295a-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="e295a-131">Remove-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="e295a-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="e295a-132">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="e295a-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
