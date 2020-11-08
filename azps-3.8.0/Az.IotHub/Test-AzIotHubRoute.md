---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: eb9d6a7b847c360861fd13bb285bc6f09bb70fbc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097369"
---
# <span data-ttu-id="73997-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="73997-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="73997-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73997-102">SYNOPSIS</span></span>
<span data-ttu-id="73997-103">IoT Hub 'daki test yolları</span><span class="sxs-lookup"><span data-stu-id="73997-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="73997-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="73997-104">SYNTAX</span></span>

### <span data-ttu-id="73997-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="73997-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73997-106">Inputobjecttestrouteset</span><span class="sxs-lookup"><span data-stu-id="73997-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73997-107">Inputobjecttestallrouteset</span><span class="sxs-lookup"><span data-stu-id="73997-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="73997-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="73997-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73997-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="73997-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="73997-110">Resourceıdtestrouteset</span><span class="sxs-lookup"><span data-stu-id="73997-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73997-111">Resourceıdtestallrouteset</span><span class="sxs-lookup"><span data-stu-id="73997-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73997-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="73997-112">DESCRIPTION</span></span>
<span data-ttu-id="73997-113">Belirli bir rotayı test edin.</span><span class="sxs-lookup"><span data-stu-id="73997-113">Test a specific route.</span></span>

## <span data-ttu-id="73997-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="73997-114">EXAMPLES</span></span>

### <span data-ttu-id="73997-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="73997-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="73997-116">Tüm rotayı "DeviceMessages" ile test edin.</span><span class="sxs-lookup"><span data-stu-id="73997-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="73997-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="73997-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="73997-118">Belirli bir rotayı test edin.</span><span class="sxs-lookup"><span data-stu-id="73997-118">Test a specific route.</span></span>

### <span data-ttu-id="73997-119">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="73997-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="73997-120">Belirli bir rotayı test etme ve hatanın nedenini gösterme.</span><span class="sxs-lookup"><span data-stu-id="73997-120">Test a specific route and showing the reason of failure.</span></span>

## <span data-ttu-id="73997-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="73997-121">PARAMETERS</span></span>

### <span data-ttu-id="73997-122">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="73997-122">-AppProperty</span></span>
<span data-ttu-id="73997-123">Yol iletisinin uygulama özellikleri</span><span class="sxs-lookup"><span data-stu-id="73997-123">App properties of the route message</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73997-124">-Gövde</span><span class="sxs-lookup"><span data-stu-id="73997-124">-Body</span></span>
<span data-ttu-id="73997-125">Yol iletisinin gövdesi</span><span class="sxs-lookup"><span data-stu-id="73997-125">Body of the route message</span></span>

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

### <span data-ttu-id="73997-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73997-126">-DefaultProfile</span></span>
<span data-ttu-id="73997-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="73997-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73997-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73997-128">-InputObject</span></span>
<span data-ttu-id="73997-129">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="73997-129">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectTestRouteSet, InputObjectTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73997-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="73997-130">-Name</span></span>
<span data-ttu-id="73997-131">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="73997-131">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73997-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73997-132">-ResourceGroupName</span></span>
<span data-ttu-id="73997-133">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="73997-133">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73997-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="73997-134">-ResourceId</span></span>
<span data-ttu-id="73997-135">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="73997-135">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdTestRouteSet, ResourceIdTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73997-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="73997-136">-RouteName</span></span>
<span data-ttu-id="73997-137">Rotanın adı</span><span class="sxs-lookup"><span data-stu-id="73997-137">Name of the Route</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73997-138">-ShowError</span><span class="sxs-lookup"><span data-stu-id="73997-138">-ShowError</span></span>
<span data-ttu-id="73997-139">Varsa, ayrıntılı hata göster</span><span class="sxs-lookup"><span data-stu-id="73997-139">Show detailed error, if exist</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73997-140">-Kaynak</span><span class="sxs-lookup"><span data-stu-id="73997-140">-Source</span></span>
<span data-ttu-id="73997-141">Rotanın kaynağı</span><span class="sxs-lookup"><span data-stu-id="73997-141">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: InputObjectTestAllRouteSet, TestAllRouteSet, ResourceIdTestAllRouteSet
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73997-142">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="73997-142">-SystemProperty</span></span>
<span data-ttu-id="73997-143">Yol iletisinin sistem özellikleri</span><span class="sxs-lookup"><span data-stu-id="73997-143">System properties of the route message</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73997-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73997-144">CommonParameters</span></span>
<span data-ttu-id="73997-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="73997-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73997-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73997-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73997-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="73997-147">INPUTS</span></span>

### <span data-ttu-id="73997-148">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="73997-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="73997-149">System. String</span><span class="sxs-lookup"><span data-stu-id="73997-149">System.String</span></span>

## <span data-ttu-id="73997-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="73997-150">OUTPUTS</span></span>

### <span data-ttu-id="73997-151">Microsoft. Azure. Commands. Management. IotHub. modeller. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="73997-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="73997-152">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="73997-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="73997-153">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="73997-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="73997-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="73997-154">NOTES</span></span>

## <span data-ttu-id="73997-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="73997-155">RELATED LINKS</span></span>
