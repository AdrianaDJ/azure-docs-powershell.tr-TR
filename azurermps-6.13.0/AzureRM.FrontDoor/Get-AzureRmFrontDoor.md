---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/get-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoor.md
ms.openlocfilehash: ca54e2cc86daca89a9872366dea32b375080c63d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762934"
---
# <span data-ttu-id="27340-101">Get-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="27340-101">Get-AzureRmFrontDoor</span></span>

## <span data-ttu-id="27340-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27340-102">SYNOPSIS</span></span>
<span data-ttu-id="27340-103">Ön kapı yük dengeleyicisi al</span><span class="sxs-lookup"><span data-stu-id="27340-103">Get Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27340-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27340-104">SYNTAX</span></span>

```
Get-AzureRmFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27340-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="27340-105">DESCRIPTION</span></span>
<span data-ttu-id="27340-106">**Get-Azurermfrontkapı** cmdletGet, geçerli abonelikte sağlanan bilgilerle eşleşen tüm varolan ön kapıları alır.</span><span class="sxs-lookup"><span data-stu-id="27340-106">The **Get-AzureRmFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="27340-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27340-107">EXAMPLES</span></span>

### <span data-ttu-id="27340-108">Örnek 1: geçerli abonelikteki tüm Frontkapılar alın.</span><span class="sxs-lookup"><span data-stu-id="27340-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor

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

<span data-ttu-id="27340-109">Geçerli abonelikteki tüm Frontkapılar alın.</span><span class="sxs-lookup"><span data-stu-id="27340-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="27340-110">Örnek 2: geçerli abonelikteki "RG1" kaynak grubundaki tüm Frontkapılar alınamıyor.</span><span class="sxs-lookup"><span data-stu-id="27340-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1"

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

<span data-ttu-id="27340-111">Geçerli abonelikteki "RG1" kaynak grubundaki tüm Frontkapılar alın.</span><span class="sxs-lookup"><span data-stu-id="27340-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="27340-112">Örnek 3: geçerli abonelikte "frontDoor1" adlı "RG1" kaynak grubundaki Frontkapaklı 'ı edinin.</span><span class="sxs-lookup"><span data-stu-id="27340-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

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

<span data-ttu-id="27340-113">Geçerli abonelikte "frontDoor1" adlı kaynak grubundaki ön kapılara RG1.</span><span class="sxs-lookup"><span data-stu-id="27340-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="27340-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27340-114">PARAMETERS</span></span>

### <span data-ttu-id="27340-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27340-115">-DefaultProfile</span></span>
<span data-ttu-id="27340-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="27340-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27340-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="27340-117">-Name</span></span>
<span data-ttu-id="27340-118">Ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="27340-118">Front Door name.</span></span>

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

### <span data-ttu-id="27340-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27340-119">-ResourceGroupName</span></span>
<span data-ttu-id="27340-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="27340-120">The resource group name.</span></span>

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

### <span data-ttu-id="27340-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27340-121">CommonParameters</span></span>
<span data-ttu-id="27340-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27340-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27340-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27340-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27340-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27340-124">INPUTS</span></span>

### <span data-ttu-id="27340-125">System. String</span><span class="sxs-lookup"><span data-stu-id="27340-125">System.String</span></span>

## <span data-ttu-id="27340-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27340-126">OUTPUTS</span></span>

### <span data-ttu-id="27340-127">Microsoft. Azure. Commands. Frontkapısı. modeller. Psfrontkapısı</span><span class="sxs-lookup"><span data-stu-id="27340-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="27340-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27340-128">NOTES</span></span>

## <span data-ttu-id="27340-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27340-129">RELATED LINKS</span></span>

<span data-ttu-id="27340-130">[Yeni-Azurermfrontkapısı](./New-AzureRmFrontDoor.md) 
 [Set-Azurermfrontkapısı](./Set-AzureRmFrontDoor.md) 
 [Remove-Azurermfrontkapısı](./Remove-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="27340-130">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)</span></span>
