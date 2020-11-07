---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: e37c8fdded8fa5e141138903e502e2e1b0f1a0f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760604"
---
# <span data-ttu-id="2189e-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2189e-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="2189e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2189e-102">SYNOPSIS</span></span>
<span data-ttu-id="2189e-103">Azure 'dan bir Azure ExpressRoute devresi alır.</span><span class="sxs-lookup"><span data-stu-id="2189e-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="2189e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2189e-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2189e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2189e-105">DESCRIPTION</span></span>
<span data-ttu-id="2189e-106">**Get-Azexpressroutedevresi** cmdlet 'i aboneliğinizden bir ExpressRoute devresi nesnesini almak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2189e-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="2189e-107">Döndürülen devre nesnesi ExpressRoute devreleriyle çalışan diğer cmdlet 'ler için girdi olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2189e-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="2189e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2189e-108">EXAMPLES</span></span>

### <span data-ttu-id="2189e-109">Örnek 1: ExpressRoute devresini alma</span><span class="sxs-lookup"><span data-stu-id="2189e-109">Example 1: Get the ExpressRoute circuit</span></span>
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

<span data-ttu-id="2189e-110">"Testrg" adlı özel bir ExpressRoute devresini ve ResourceGroupName "test"</span><span class="sxs-lookup"><span data-stu-id="2189e-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="2189e-111">Örnek 2: filtreleme kullanarak ExpressRoute devrelerini listeleme</span><span class="sxs-lookup"><span data-stu-id="2189e-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
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

<span data-ttu-id="2189e-112">Adı "test" ile başlayan tüm ExpressRoute devrelerini edinin.</span><span class="sxs-lookup"><span data-stu-id="2189e-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="2189e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2189e-113">PARAMETERS</span></span>

### <span data-ttu-id="2189e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2189e-114">-DefaultProfile</span></span>
<span data-ttu-id="2189e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2189e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2189e-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="2189e-116">-Name</span></span>
<span data-ttu-id="2189e-117">ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="2189e-117">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="2189e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2189e-118">-ResourceGroupName</span></span>
<span data-ttu-id="2189e-119">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2189e-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="2189e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2189e-120">CommonParameters</span></span>
<span data-ttu-id="2189e-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2189e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2189e-122">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2189e-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2189e-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2189e-123">INPUTS</span></span>

### <span data-ttu-id="2189e-124">System. String</span><span class="sxs-lookup"><span data-stu-id="2189e-124">System.String</span></span>

## <span data-ttu-id="2189e-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2189e-125">OUTPUTS</span></span>

### <span data-ttu-id="2189e-126">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="2189e-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="2189e-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2189e-127">NOTES</span></span>

## <span data-ttu-id="2189e-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2189e-128">RELATED LINKS</span></span>

[<span data-ttu-id="2189e-129">Taşıma-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="2189e-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="2189e-130">Yeni-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="2189e-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="2189e-131">Remove-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="2189e-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="2189e-132">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="2189e-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
