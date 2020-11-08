---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: 6e72a889264efa82af343a0aab019cc3e5580dc7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103822"
---
# <span data-ttu-id="e8952-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="e8952-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="e8952-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8952-102">SYNOPSIS</span></span>
<span data-ttu-id="e8952-103">IoT merkezinde yol hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="e8952-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="e8952-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8952-104">SYNTAX</span></span>

### <span data-ttu-id="e8952-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e8952-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8952-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="e8952-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8952-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="e8952-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8952-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8952-108">DESCRIPTION</span></span>
<span data-ttu-id="e8952-109">Yol hakkında bilgi edinin. Bir IoT Hub 'ından tüm yolları alabilir, bir uç nokta türüne yol veya belirli bir uç noktaya yol alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e8952-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="e8952-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8952-110">EXAMPLES</span></span>

### <span data-ttu-id="e8952-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e8952-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="e8952-112">"Myiothub" IoT Hub 'ından tüm rotayı alın.</span><span class="sxs-lookup"><span data-stu-id="e8952-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="e8952-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e8952-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="e8952-114">"Myiothub" IoT Hub 'ından yol bilgilerini alın.</span><span class="sxs-lookup"><span data-stu-id="e8952-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="e8952-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8952-115">PARAMETERS</span></span>

### <span data-ttu-id="e8952-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8952-116">-DefaultProfile</span></span>
<span data-ttu-id="e8952-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8952-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8952-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8952-118">-InputObject</span></span>
<span data-ttu-id="e8952-119">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="e8952-119">IotHub Object</span></span>

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

### <span data-ttu-id="e8952-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="e8952-120">-Name</span></span>
<span data-ttu-id="e8952-121">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="e8952-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e8952-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8952-122">-ResourceGroupName</span></span>
<span data-ttu-id="e8952-123">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="e8952-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e8952-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e8952-124">-ResourceId</span></span>
<span data-ttu-id="e8952-125">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="e8952-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e8952-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="e8952-126">-RouteName</span></span>
<span data-ttu-id="e8952-127">Rotanın adı</span><span class="sxs-lookup"><span data-stu-id="e8952-127">Name of the Route</span></span>

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

### <span data-ttu-id="e8952-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8952-128">CommonParameters</span></span>
<span data-ttu-id="e8952-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8952-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8952-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8952-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8952-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8952-131">INPUTS</span></span>

### <span data-ttu-id="e8952-132">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="e8952-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e8952-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e8952-133">System.String</span></span>

## <span data-ttu-id="e8952-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8952-134">OUTPUTS</span></span>

### <span data-ttu-id="e8952-135">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="e8952-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="e8952-136">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="e8952-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="e8952-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8952-137">NOTES</span></span>

## <span data-ttu-id="e8952-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8952-138">RELATED LINKS</span></span>
