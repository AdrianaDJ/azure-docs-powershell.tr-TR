---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
ms.openlocfilehash: 32af04aec91302304be3ed11c17d81d2e71cc772
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916752"
---
# <span data-ttu-id="55453-101">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="55453-101">New-AzFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="55453-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55453-102">SYNOPSIS</span></span>
<span data-ttu-id="55453-103">Ön kapı oluşturmak için PSBackendPool nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="55453-103">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="55453-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55453-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55453-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="55453-105">DESCRIPTION</span></span>
<span data-ttu-id="55453-106">Ön kapı oluşturmak için PSBackendPool nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="55453-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="55453-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55453-107">EXAMPLES</span></span>

### <span data-ttu-id="55453-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="55453-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendPoolObject -Name "backendpool1" -FrontDoorName $Name -ResourceGroupName $resourceGroupName -Backend $backend1 -He
althProbeSettingsName "healthProbeSetting1" -LoadBalancingSettingsName "loadBalancingSetting1"


Backends                : {Microsoft.Azure.Commands.FrontDoor.Models.PSBackend}
LoadBalancingSettingRef : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/LoadBalancingSettings/loadBalancingSetting1
HealthProbeSettingRef   : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/HealthProbeSettings/healthProbeSetting1
EnabledState            : Enabled
ResourceState           :
Id                      :
Name                    : backendpool1
Type                    :
```

<span data-ttu-id="55453-109">Ön kapı oluşturmak için PSBackendPool nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="55453-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="55453-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55453-110">PARAMETERS</span></span>

### <span data-ttu-id="55453-111">-Arka uç</span><span class="sxs-lookup"><span data-stu-id="55453-111">-Backend</span></span>
<span data-ttu-id="55453-112">Bu havuz için backends kümesi.</span><span class="sxs-lookup"><span data-stu-id="55453-112">The set of backends for this pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackend[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55453-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55453-113">-DefaultProfile</span></span>
<span data-ttu-id="55453-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55453-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55453-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="55453-115">-FrontDoorName</span></span>
<span data-ttu-id="55453-116">Bu yönlendirme kuralının ait olduğu ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="55453-116">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="55453-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="55453-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="55453-118">Bu arka uç havuzunun durum araştırma ayarlarının adı</span><span class="sxs-lookup"><span data-stu-id="55453-118">The name of the health probe settings for this backend pool</span></span>

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

### <span data-ttu-id="55453-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="55453-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="55453-120">Bu arka uç havuzu için Yük Dengeleme ayarlarının adı</span><span class="sxs-lookup"><span data-stu-id="55453-120">The name of the load balancing settings for this backend pool</span></span>

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

### <span data-ttu-id="55453-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="55453-121">-Name</span></span>
<span data-ttu-id="55453-122">BackendPool adı.</span><span class="sxs-lookup"><span data-stu-id="55453-122">BackendPool name.</span></span>

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

### <span data-ttu-id="55453-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55453-123">-ResourceGroupName</span></span>
<span data-ttu-id="55453-124">RoutingRule 'un içinde oluşturulduğu kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="55453-124">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="55453-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55453-125">CommonParameters</span></span>
<span data-ttu-id="55453-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55453-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55453-127">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="55453-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55453-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55453-128">INPUTS</span></span>

### <span data-ttu-id="55453-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="55453-129">None</span></span>

## <span data-ttu-id="55453-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55453-130">OUTPUTS</span></span>

### <span data-ttu-id="55453-131">Microsoft. Azure. Commands. Frontkapısı. modeller. PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="55453-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="55453-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55453-132">NOTES</span></span>

## <span data-ttu-id="55453-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55453-133">RELATED LINKS</span></span>

<span data-ttu-id="55453-134">[Yeni-azön kapı](./New-AzFrontDoor.md) 
 [Set-Azfrontkapısı](./Set-AzFrontDoor.md) 
 [New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="55453-134">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span></span>