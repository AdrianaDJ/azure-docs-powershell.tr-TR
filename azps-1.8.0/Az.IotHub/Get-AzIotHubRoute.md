---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: 1cc1bb46909260bd23cfa3f72e675251a011072d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916448"
---
# <span data-ttu-id="8de07-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="8de07-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="8de07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8de07-102">SYNOPSIS</span></span>
<span data-ttu-id="8de07-103">IoT merkezinde yol hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="8de07-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="8de07-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8de07-104">SYNTAX</span></span>

### <span data-ttu-id="8de07-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8de07-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8de07-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="8de07-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8de07-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="8de07-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8de07-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8de07-108">DESCRIPTION</span></span>
<span data-ttu-id="8de07-109">Yol hakkında bilgi edinin. Bir IoT Hub 'ından tüm yolları alabilir, bir uç nokta türüne yol veya belirli bir uç noktaya yol alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8de07-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="8de07-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8de07-110">EXAMPLES</span></span>

### <span data-ttu-id="8de07-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8de07-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="8de07-112">"Myiothub" IoT Hub 'ından tüm rotayı alın.</span><span class="sxs-lookup"><span data-stu-id="8de07-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="8de07-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="8de07-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="8de07-114">"Myiothub" IoT Hub 'ından yol bilgilerini alın.</span><span class="sxs-lookup"><span data-stu-id="8de07-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="8de07-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8de07-115">PARAMETERS</span></span>

### <span data-ttu-id="8de07-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8de07-116">-DefaultProfile</span></span>
<span data-ttu-id="8de07-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8de07-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8de07-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8de07-118">-InputObject</span></span>
<span data-ttu-id="8de07-119">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="8de07-119">IotHub Object</span></span>

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

### <span data-ttu-id="8de07-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="8de07-120">-Name</span></span>
<span data-ttu-id="8de07-121">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="8de07-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8de07-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8de07-122">-ResourceGroupName</span></span>
<span data-ttu-id="8de07-123">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="8de07-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8de07-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8de07-124">-ResourceId</span></span>
<span data-ttu-id="8de07-125">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="8de07-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8de07-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="8de07-126">-RouteName</span></span>
<span data-ttu-id="8de07-127">Rotanın adı</span><span class="sxs-lookup"><span data-stu-id="8de07-127">Name of the Route</span></span>

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

### <span data-ttu-id="8de07-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de07-128">CommonParameters</span></span>
<span data-ttu-id="8de07-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8de07-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de07-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8de07-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de07-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8de07-131">INPUTS</span></span>

### <span data-ttu-id="8de07-132">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="8de07-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8de07-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8de07-133">System.String</span></span>

## <span data-ttu-id="8de07-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8de07-134">OUTPUTS</span></span>

### <span data-ttu-id="8de07-135">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="8de07-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="8de07-136">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="8de07-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="8de07-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8de07-137">NOTES</span></span>

## <span data-ttu-id="8de07-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8de07-138">RELATED LINKS</span></span>