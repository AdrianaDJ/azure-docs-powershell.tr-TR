---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoute.md
ms.openlocfilehash: 1b248225e86f4294603d3a07f1d8a1c7068e2851
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590238"
---
# <span data-ttu-id="c0e15-101">Add-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="c0e15-101">Add-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="c0e15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0e15-102">SYNOPSIS</span></span>
<span data-ttu-id="c0e15-103">IoT merkezinde yol oluşturma</span><span class="sxs-lookup"><span data-stu-id="c0e15-103">Create a route in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0e15-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0e15-104">SYNTAX</span></span>

### <span data-ttu-id="c0e15-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c0e15-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source] <PSRoutingSource> [-EndpointName] <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0e15-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="c0e15-106">InputObjectSet</span></span>
```
Add-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source] <PSRoutingSource>
 [-EndpointName] <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0e15-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="c0e15-107">ResourceIdSet</span></span>
```
Add-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source] <PSRoutingSource>
 [-EndpointName] <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0e15-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0e15-108">DESCRIPTION</span></span>
<span data-ttu-id="c0e15-109">Belirli bir veri kaynağı ve koşulu istenen uç noktaya göndermek için bir yol oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c0e15-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="c0e15-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0e15-110">EXAMPLES</span></span>

### <span data-ttu-id="c0e15-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c0e15-111">Example 1</span></span>
```
PS C:\> Add-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="c0e15-112">Yeni bir yol oluştur "R1".</span><span class="sxs-lookup"><span data-stu-id="c0e15-112">Create a new route "R1".</span></span>

## <span data-ttu-id="c0e15-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0e15-113">PARAMETERS</span></span>

### <span data-ttu-id="c0e15-114">-Koşul</span><span class="sxs-lookup"><span data-stu-id="c0e15-114">-Condition</span></span>
<span data-ttu-id="c0e15-115">Yönlendirme kuralını uygulamak için değerlendirilen koşul</span><span class="sxs-lookup"><span data-stu-id="c0e15-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="c0e15-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0e15-116">-DefaultProfile</span></span>
<span data-ttu-id="c0e15-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c0e15-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0e15-118">Özellikli</span><span class="sxs-lookup"><span data-stu-id="c0e15-118">-Enabled</span></span>
<span data-ttu-id="c0e15-119">Rotayı etkinleştir</span><span class="sxs-lookup"><span data-stu-id="c0e15-119">Enable route</span></span>

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

### <span data-ttu-id="c0e15-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c0e15-120">-EndpointName</span></span>
<span data-ttu-id="c0e15-121">Yönlendirme uç noktasının adı</span><span class="sxs-lookup"><span data-stu-id="c0e15-121">Name of the routing endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e15-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0e15-122">-InputObject</span></span>
<span data-ttu-id="c0e15-123">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="c0e15-123">IotHub Object</span></span>

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

### <span data-ttu-id="c0e15-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="c0e15-124">-Name</span></span>
<span data-ttu-id="c0e15-125">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="c0e15-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c0e15-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0e15-126">-ResourceGroupName</span></span>
<span data-ttu-id="c0e15-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="c0e15-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c0e15-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c0e15-128">-ResourceId</span></span>
<span data-ttu-id="c0e15-129">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="c0e15-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c0e15-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="c0e15-130">-RouteName</span></span>
<span data-ttu-id="c0e15-131">Rotanın adı</span><span class="sxs-lookup"><span data-stu-id="c0e15-131">Name of the Route</span></span>

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

### <span data-ttu-id="c0e15-132">-Kaynak</span><span class="sxs-lookup"><span data-stu-id="c0e15-132">-Source</span></span>
<span data-ttu-id="c0e15-133">Rotanın kaynağı</span><span class="sxs-lookup"><span data-stu-id="c0e15-133">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e15-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="c0e15-134">-Confirm</span></span>
<span data-ttu-id="c0e15-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c0e15-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0e15-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0e15-136">-WhatIf</span></span>
<span data-ttu-id="c0e15-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c0e15-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0e15-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c0e15-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0e15-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0e15-139">CommonParameters</span></span>
<span data-ttu-id="c0e15-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0e15-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0e15-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0e15-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0e15-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0e15-142">INPUTS</span></span>

### <span data-ttu-id="c0e15-143">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="c0e15-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="c0e15-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c0e15-144">System.String</span></span>

## <span data-ttu-id="c0e15-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0e15-145">OUTPUTS</span></span>

### <span data-ttu-id="c0e15-146">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="c0e15-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="c0e15-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0e15-147">NOTES</span></span>

## <span data-ttu-id="c0e15-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0e15-148">RELATED LINKS</span></span>
