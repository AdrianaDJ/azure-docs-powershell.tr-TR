---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
ms.openlocfilehash: 8c3aaad928545574c7da0adeae140a250056cd83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751768"
---
# <span data-ttu-id="31bc9-101">Add-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="31bc9-101">Add-AzIotHubRoute</span></span>

## <span data-ttu-id="31bc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="31bc9-103">IoT merkezinde yol oluşturma</span><span class="sxs-lookup"><span data-stu-id="31bc9-103">Create a route in IoT Hub</span></span>

## <span data-ttu-id="31bc9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31bc9-104">SYNTAX</span></span>

### <span data-ttu-id="31bc9-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="31bc9-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 -Source <PSRoutingSource> -EndpointName <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31bc9-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="31bc9-106">InputObjectSet</span></span>
```
Add-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> -Source <PSRoutingSource>
 -EndpointName <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31bc9-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="31bc9-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> -Source <PSRoutingSource> -EndpointName <String>
 [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31bc9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="31bc9-108">DESCRIPTION</span></span>
<span data-ttu-id="31bc9-109">Belirli bir veri kaynağı ve koşulu istenen uç noktaya göndermek için bir yol oluşturun.</span><span class="sxs-lookup"><span data-stu-id="31bc9-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="31bc9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31bc9-110">EXAMPLES</span></span>

### <span data-ttu-id="31bc9-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="31bc9-111">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="31bc9-112">Yeni bir yol oluştur "R1".</span><span class="sxs-lookup"><span data-stu-id="31bc9-112">Create a new route "R1".</span></span>

## <span data-ttu-id="31bc9-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31bc9-113">PARAMETERS</span></span>

### <span data-ttu-id="31bc9-114">-Koşul</span><span class="sxs-lookup"><span data-stu-id="31bc9-114">-Condition</span></span>
<span data-ttu-id="31bc9-115">Yönlendirme kuralını uygulamak için değerlendirilen koşul</span><span class="sxs-lookup"><span data-stu-id="31bc9-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="31bc9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31bc9-116">-DefaultProfile</span></span>
<span data-ttu-id="31bc9-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="31bc9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31bc9-118">Özellikli</span><span class="sxs-lookup"><span data-stu-id="31bc9-118">-Enabled</span></span>
<span data-ttu-id="31bc9-119">Rotayı etkinleştir</span><span class="sxs-lookup"><span data-stu-id="31bc9-119">Enable route</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31bc9-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="31bc9-120">-EndpointName</span></span>
<span data-ttu-id="31bc9-121">Yönlendirme uç noktasının adı</span><span class="sxs-lookup"><span data-stu-id="31bc9-121">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="31bc9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31bc9-122">-InputObject</span></span>
<span data-ttu-id="31bc9-123">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="31bc9-123">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31bc9-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="31bc9-124">-Name</span></span>
<span data-ttu-id="31bc9-125">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="31bc9-125">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31bc9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31bc9-126">-ResourceGroupName</span></span>
<span data-ttu-id="31bc9-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="31bc9-127">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31bc9-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="31bc9-128">-ResourceId</span></span>
<span data-ttu-id="31bc9-129">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="31bc9-129">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31bc9-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="31bc9-130">-RouteName</span></span>
<span data-ttu-id="31bc9-131">Rotanın adı</span><span class="sxs-lookup"><span data-stu-id="31bc9-131">Name of the Route</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31bc9-132">-Kaynak</span><span class="sxs-lookup"><span data-stu-id="31bc9-132">-Source</span></span>
<span data-ttu-id="31bc9-133">Rotanın kaynağı</span><span class="sxs-lookup"><span data-stu-id="31bc9-133">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31bc9-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="31bc9-134">-Confirm</span></span>
<span data-ttu-id="31bc9-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="31bc9-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31bc9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31bc9-136">-WhatIf</span></span>
<span data-ttu-id="31bc9-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="31bc9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31bc9-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="31bc9-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31bc9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31bc9-139">CommonParameters</span></span>
<span data-ttu-id="31bc9-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31bc9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31bc9-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31bc9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31bc9-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31bc9-142">INPUTS</span></span>

### <span data-ttu-id="31bc9-143">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="31bc9-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="31bc9-144">System. String</span><span class="sxs-lookup"><span data-stu-id="31bc9-144">System.String</span></span>

## <span data-ttu-id="31bc9-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31bc9-145">OUTPUTS</span></span>

### <span data-ttu-id="31bc9-146">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="31bc9-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="31bc9-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31bc9-147">NOTES</span></span>

## <span data-ttu-id="31bc9-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31bc9-148">RELATED LINKS</span></span>