---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendPoolObject.md
ms.openlocfilehash: 13b28d236e1c6e758c4f7883285c55017ce5a727
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762932"
---
# <span data-ttu-id="60beb-101">New-AzureRmFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="60beb-101">New-AzureRmFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="60beb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60beb-102">SYNOPSIS</span></span>
<span data-ttu-id="60beb-103">Ön kapı oluşturmak için PSBackendPool nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="60beb-103">Create a PSBackendPool object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60beb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="60beb-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60beb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="60beb-105">DESCRIPTION</span></span>
<span data-ttu-id="60beb-106">Ön kapı oluşturmak için PSBackendPool nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="60beb-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="60beb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="60beb-107">EXAMPLES</span></span>

### <span data-ttu-id="60beb-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="60beb-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorBackendPoolObject -Name "backendpool1" -FrontDoorName $Name -ResourceGroupName $resourceGroupName -Backend $backend1 -He
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

<span data-ttu-id="60beb-109">Ön kapı oluşturmak için PSBackendPool nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="60beb-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="60beb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="60beb-110">PARAMETERS</span></span>

### <span data-ttu-id="60beb-111">-Arka uç</span><span class="sxs-lookup"><span data-stu-id="60beb-111">-Backend</span></span>
<span data-ttu-id="60beb-112">Bu havuz için backends kümesi.</span><span class="sxs-lookup"><span data-stu-id="60beb-112">The set of backends for this pool.</span></span>

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

### <span data-ttu-id="60beb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60beb-113">-DefaultProfile</span></span>
<span data-ttu-id="60beb-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="60beb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60beb-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="60beb-115">-FrontDoorName</span></span>
<span data-ttu-id="60beb-116">Bu yönlendirme kuralının ait olduğu ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="60beb-116">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="60beb-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="60beb-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="60beb-118">Bu arka uç havuzunun durum araştırma ayarlarının adı</span><span class="sxs-lookup"><span data-stu-id="60beb-118">The name of the health probe settings for this backend pool</span></span>

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

### <span data-ttu-id="60beb-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="60beb-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="60beb-120">Bu arka uç havuzu için Yük Dengeleme ayarlarının adı</span><span class="sxs-lookup"><span data-stu-id="60beb-120">The name of the load balancing settings for this backend pool</span></span>

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

### <span data-ttu-id="60beb-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="60beb-121">-Name</span></span>
<span data-ttu-id="60beb-122">BackendPool adı.</span><span class="sxs-lookup"><span data-stu-id="60beb-122">BackendPool name.</span></span>

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

### <span data-ttu-id="60beb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60beb-123">-ResourceGroupName</span></span>
<span data-ttu-id="60beb-124">RoutingRule 'un içinde oluşturulduğu kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="60beb-124">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="60beb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60beb-125">CommonParameters</span></span>
<span data-ttu-id="60beb-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="60beb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60beb-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60beb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60beb-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="60beb-128">INPUTS</span></span>

### <span data-ttu-id="60beb-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="60beb-129">None</span></span>

## <span data-ttu-id="60beb-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="60beb-130">OUTPUTS</span></span>

### <span data-ttu-id="60beb-131">Microsoft. Azure. Commands. Frontkapısı. modeller. PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="60beb-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="60beb-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="60beb-132">NOTES</span></span>

## <span data-ttu-id="60beb-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="60beb-133">RELATED LINKS</span></span>

<span data-ttu-id="60beb-134">[Yeni-Azurermfrontkapısı](./New-AzureRmFrontDoor.md) 
 [Set-Azurermfrontkapısı](./Set-AzureRmFrontDoor.md) 
 [New-AzureRmFrontDoorBackendObject](./New-AzureRmFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="60beb-134">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorBackendObject](./New-AzureRmFrontDoorBackendObject.md)</span></span>
