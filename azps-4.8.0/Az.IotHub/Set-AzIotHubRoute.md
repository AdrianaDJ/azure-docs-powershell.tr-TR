---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: a54bfdb26b7013e490ca36e4ae5608da228d9d70
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274509"
---
# <span data-ttu-id="00675-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="00675-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="00675-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00675-102">SYNOPSIS</span></span>
<span data-ttu-id="00675-103">IoT Hub 'da yol güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="00675-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="00675-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00675-104">SYNTAX</span></span>

### <span data-ttu-id="00675-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="00675-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00675-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="00675-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00675-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="00675-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00675-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="00675-108">DESCRIPTION</span></span>
<span data-ttu-id="00675-109">Rotayı düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="00675-109">Edit a route.</span></span> <span data-ttu-id="00675-110">Veri kaynağı, uç nokta, yönlendirme sorgusu ve ayrıca rotayı etkinleştirme veya devre dışı bırakma gibi bir rotadaki tüm alanları güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="00675-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="00675-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00675-111">EXAMPLES</span></span>

### <span data-ttu-id="00675-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="00675-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="00675-113">Yol bilgilerini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="00675-113">Updating the route information.</span></span>

### <span data-ttu-id="00675-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="00675-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="00675-115">Yol bilgilerini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="00675-115">Updating the route information.</span></span>

### <span data-ttu-id="00675-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="00675-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="00675-117">Yol bilgilerini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="00675-117">Updating the route information.</span></span>

## <span data-ttu-id="00675-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00675-118">PARAMETERS</span></span>

### <span data-ttu-id="00675-119">-Koşul</span><span class="sxs-lookup"><span data-stu-id="00675-119">-Condition</span></span>
<span data-ttu-id="00675-120">Yönlendirme kuralını uygulamak için değerlendirilen koşul</span><span class="sxs-lookup"><span data-stu-id="00675-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="00675-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00675-121">-DefaultProfile</span></span>
<span data-ttu-id="00675-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="00675-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00675-123">Özellikli</span><span class="sxs-lookup"><span data-stu-id="00675-123">-Enabled</span></span>
<span data-ttu-id="00675-124">Rotayı etkinleştir</span><span class="sxs-lookup"><span data-stu-id="00675-124">Enable route</span></span>

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

### <span data-ttu-id="00675-125">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="00675-125">-EndpointName</span></span>
<span data-ttu-id="00675-126">Yönlendirme uç noktasının adı</span><span class="sxs-lookup"><span data-stu-id="00675-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="00675-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00675-127">-InputObject</span></span>
<span data-ttu-id="00675-128">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="00675-128">IotHub Object</span></span>

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

### <span data-ttu-id="00675-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="00675-129">-Name</span></span>
<span data-ttu-id="00675-130">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="00675-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="00675-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00675-131">-ResourceGroupName</span></span>
<span data-ttu-id="00675-132">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="00675-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="00675-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="00675-133">-ResourceId</span></span>
<span data-ttu-id="00675-134">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="00675-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="00675-135">-RouteName</span><span class="sxs-lookup"><span data-stu-id="00675-135">-RouteName</span></span>
<span data-ttu-id="00675-136">Rotanın adı</span><span class="sxs-lookup"><span data-stu-id="00675-136">Name of the Route</span></span>

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

### <span data-ttu-id="00675-137">-Kaynak</span><span class="sxs-lookup"><span data-stu-id="00675-137">-Source</span></span>
<span data-ttu-id="00675-138">Rotanın kaynağı</span><span class="sxs-lookup"><span data-stu-id="00675-138">Source of the route</span></span>

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

### <span data-ttu-id="00675-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="00675-139">-Confirm</span></span>
<span data-ttu-id="00675-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="00675-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00675-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00675-141">-WhatIf</span></span>
<span data-ttu-id="00675-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="00675-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00675-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="00675-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00675-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00675-144">CommonParameters</span></span>
<span data-ttu-id="00675-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00675-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00675-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00675-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00675-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00675-147">INPUTS</span></span>

### <span data-ttu-id="00675-148">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="00675-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="00675-149">System. String</span><span class="sxs-lookup"><span data-stu-id="00675-149">System.String</span></span>

## <span data-ttu-id="00675-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00675-150">OUTPUTS</span></span>

### <span data-ttu-id="00675-151">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="00675-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="00675-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00675-152">NOTES</span></span>

## <span data-ttu-id="00675-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00675-153">RELATED LINKS</span></span>
