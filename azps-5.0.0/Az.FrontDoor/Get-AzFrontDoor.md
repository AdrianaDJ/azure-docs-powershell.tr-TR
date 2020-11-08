---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: 8c378d7f0b1ac7a753f7f270fd3969eb881c7aec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279062"
---
# <span data-ttu-id="392d7-101">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="392d7-101">Get-AzFrontDoor</span></span>

## <span data-ttu-id="392d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="392d7-102">SYNOPSIS</span></span>
<span data-ttu-id="392d7-103">Ön kapı yük dengeleyicisi al</span><span class="sxs-lookup"><span data-stu-id="392d7-103">Get Front Door load balancer</span></span>

## <span data-ttu-id="392d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="392d7-104">SYNTAX</span></span>

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="392d7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="392d7-105">DESCRIPTION</span></span>
<span data-ttu-id="392d7-106">**Get-Azfrontkapı** cmdletGet, geçerli abonelikte sağlanan bilgilerle eşleşen tüm varolan ön kapıları alır.</span><span class="sxs-lookup"><span data-stu-id="392d7-106">The **Get-AzFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="392d7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="392d7-107">EXAMPLES</span></span>

### <span data-ttu-id="392d7-108">Örnek 1: geçerli abonelikteki tüm Frontkapılar alın.</span><span class="sxs-lookup"><span data-stu-id="392d7-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid1}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid2}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="392d7-109">Geçerli abonelikteki tüm Frontkapılar alın.</span><span class="sxs-lookup"><span data-stu-id="392d7-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="392d7-110">Örnek 2: geçerli abonelikteki "RG1" kaynak grubundaki tüm Frontkapılar alınamıyor.</span><span class="sxs-lookup"><span data-stu-id="392d7-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1"

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor2
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="392d7-111">Geçerli abonelikteki "RG1" kaynak grubundaki tüm Frontkapılar alın.</span><span class="sxs-lookup"><span data-stu-id="392d7-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="392d7-112">Örnek 3: geçerli abonelikte "frontDoor1" adlı "RG1" kaynak grubundaki Frontkapaklı 'ı edinin.</span><span class="sxs-lookup"><span data-stu-id="392d7-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="392d7-113">Geçerli abonelikte "frontDoor1" adlı kaynak grubundaki ön kapılara RG1.</span><span class="sxs-lookup"><span data-stu-id="392d7-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="392d7-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="392d7-114">PARAMETERS</span></span>

### <span data-ttu-id="392d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="392d7-115">-DefaultProfile</span></span>
<span data-ttu-id="392d7-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="392d7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="392d7-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="392d7-117">-Name</span></span>
<span data-ttu-id="392d7-118">Ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="392d7-118">Front Door name.</span></span>

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

### <span data-ttu-id="392d7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="392d7-119">-ResourceGroupName</span></span>
<span data-ttu-id="392d7-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="392d7-120">The resource group name.</span></span>

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

### <span data-ttu-id="392d7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="392d7-121">CommonParameters</span></span>
<span data-ttu-id="392d7-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="392d7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="392d7-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="392d7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="392d7-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="392d7-124">INPUTS</span></span>

### <span data-ttu-id="392d7-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="392d7-125">None</span></span>

## <span data-ttu-id="392d7-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="392d7-126">OUTPUTS</span></span>

### <span data-ttu-id="392d7-127">Microsoft. Azure. Commands. Frontkapısı. modeller. Psfrontkapısı</span><span class="sxs-lookup"><span data-stu-id="392d7-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="392d7-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="392d7-128">NOTES</span></span>

## <span data-ttu-id="392d7-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="392d7-129">RELATED LINKS</span></span>

<span data-ttu-id="392d7-130">[Yeni-azön kapı](./New-AzFrontDoor.md) 
 [Set-Azfrontkapısı](./Set-AzFrontDoor.md) 
 [Remove-Azfrontkapısı](./Remove-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="392d7-130">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span></span>
