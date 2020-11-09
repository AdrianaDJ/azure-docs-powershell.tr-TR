---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: a54bfdb26b7013e490ca36e4ae5608da228d9d70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319957"
---
# <span data-ttu-id="fbb61-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="fbb61-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="fbb61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbb61-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb61-103">IoT Hub 'da yol güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="fbb61-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="fbb61-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fbb61-104">SYNTAX</span></span>

### <span data-ttu-id="fbb61-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fbb61-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbb61-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="fbb61-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbb61-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="fbb61-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbb61-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fbb61-108">DESCRIPTION</span></span>
<span data-ttu-id="fbb61-109">Rotayı düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="fbb61-109">Edit a route.</span></span> <span data-ttu-id="fbb61-110">Veri kaynağı, uç nokta, yönlendirme sorgusu ve ayrıca rotayı etkinleştirme veya devre dışı bırakma gibi bir rotadaki tüm alanları güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbb61-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="fbb61-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fbb61-111">EXAMPLES</span></span>

### <span data-ttu-id="fbb61-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fbb61-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="fbb61-113">Yol bilgilerini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="fbb61-113">Updating the route information.</span></span>

### <span data-ttu-id="fbb61-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="fbb61-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="fbb61-115">Yol bilgilerini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="fbb61-115">Updating the route information.</span></span>

### <span data-ttu-id="fbb61-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="fbb61-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="fbb61-117">Yol bilgilerini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="fbb61-117">Updating the route information.</span></span>

## <span data-ttu-id="fbb61-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fbb61-118">PARAMETERS</span></span>

### <span data-ttu-id="fbb61-119">-Koşul</span><span class="sxs-lookup"><span data-stu-id="fbb61-119">-Condition</span></span>
<span data-ttu-id="fbb61-120">Yönlendirme kuralını uygulamak için değerlendirilen koşul</span><span class="sxs-lookup"><span data-stu-id="fbb61-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="fbb61-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb61-121">-DefaultProfile</span></span>
<span data-ttu-id="fbb61-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fbb61-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbb61-123">Özellikli</span><span class="sxs-lookup"><span data-stu-id="fbb61-123">-Enabled</span></span>
<span data-ttu-id="fbb61-124">Rotayı etkinleştir</span><span class="sxs-lookup"><span data-stu-id="fbb61-124">Enable route</span></span>

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

### <span data-ttu-id="fbb61-125">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fbb61-125">-EndpointName</span></span>
<span data-ttu-id="fbb61-126">Yönlendirme uç noktasının adı</span><span class="sxs-lookup"><span data-stu-id="fbb61-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="fbb61-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbb61-127">-InputObject</span></span>
<span data-ttu-id="fbb61-128">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="fbb61-128">IotHub Object</span></span>

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

### <span data-ttu-id="fbb61-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="fbb61-129">-Name</span></span>
<span data-ttu-id="fbb61-130">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="fbb61-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fbb61-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbb61-131">-ResourceGroupName</span></span>
<span data-ttu-id="fbb61-132">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="fbb61-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fbb61-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fbb61-133">-ResourceId</span></span>
<span data-ttu-id="fbb61-134">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="fbb61-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fbb61-135">-RouteName</span><span class="sxs-lookup"><span data-stu-id="fbb61-135">-RouteName</span></span>
<span data-ttu-id="fbb61-136">Rotanın adı</span><span class="sxs-lookup"><span data-stu-id="fbb61-136">Name of the Route</span></span>

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

### <span data-ttu-id="fbb61-137">-Kaynak</span><span class="sxs-lookup"><span data-stu-id="fbb61-137">-Source</span></span>
<span data-ttu-id="fbb61-138">Rotanın kaynağı</span><span class="sxs-lookup"><span data-stu-id="fbb61-138">Source of the route</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource]
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbb61-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="fbb61-139">-Confirm</span></span>
<span data-ttu-id="fbb61-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fbb61-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbb61-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbb61-141">-WhatIf</span></span>
<span data-ttu-id="fbb61-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fbb61-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbb61-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fbb61-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbb61-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb61-144">CommonParameters</span></span>
<span data-ttu-id="fbb61-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fbb61-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbb61-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbb61-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb61-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fbb61-147">INPUTS</span></span>

### <span data-ttu-id="fbb61-148">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="fbb61-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fbb61-149">System. String</span><span class="sxs-lookup"><span data-stu-id="fbb61-149">System.String</span></span>

## <span data-ttu-id="fbb61-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fbb61-150">OUTPUTS</span></span>

### <span data-ttu-id="fbb61-151">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="fbb61-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="fbb61-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fbb61-152">NOTES</span></span>

## <span data-ttu-id="fbb61-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fbb61-153">RELATED LINKS</span></span>
