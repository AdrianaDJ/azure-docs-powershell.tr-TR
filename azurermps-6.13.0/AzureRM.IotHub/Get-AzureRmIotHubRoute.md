---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoute.md
ms.openlocfilehash: 0711bd1d6290191c2d5311a7375e6f81c4ecd573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764387"
---
# <span data-ttu-id="d11d7-101">Get-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="d11d7-101">Get-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="d11d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d11d7-102">SYNOPSIS</span></span>
<span data-ttu-id="d11d7-103">IoT merkezinde yol hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="d11d7-103">Get information about the route in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d11d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d11d7-104">SYNTAX</span></span>

### <span data-ttu-id="d11d7-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d11d7-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d11d7-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="d11d7-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d11d7-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="d11d7-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d11d7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d11d7-108">DESCRIPTION</span></span>
<span data-ttu-id="d11d7-109">Yol hakkında bilgi edinin. Bir IoT Hub 'ından tüm yolları alabilir, bir uç nokta türüne yol veya belirli bir uç noktaya yol alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d11d7-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="d11d7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d11d7-110">EXAMPLES</span></span>

### <span data-ttu-id="d11d7-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d11d7-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="d11d7-112">"Myiothub" IoT Hub 'ından tüm rotayı alın.</span><span class="sxs-lookup"><span data-stu-id="d11d7-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="d11d7-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d11d7-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="d11d7-114">"Myiothub" IoT Hub 'ından yol bilgilerini alın.</span><span class="sxs-lookup"><span data-stu-id="d11d7-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="d11d7-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d11d7-115">PARAMETERS</span></span>

### <span data-ttu-id="d11d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d11d7-116">-DefaultProfile</span></span>
<span data-ttu-id="d11d7-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d11d7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d11d7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d11d7-118">-InputObject</span></span>
<span data-ttu-id="d11d7-119">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="d11d7-119">IotHub Object</span></span>

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

### <span data-ttu-id="d11d7-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="d11d7-120">-Name</span></span>
<span data-ttu-id="d11d7-121">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="d11d7-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d11d7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d11d7-122">-ResourceGroupName</span></span>
<span data-ttu-id="d11d7-123">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="d11d7-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d11d7-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d11d7-124">-ResourceId</span></span>
<span data-ttu-id="d11d7-125">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="d11d7-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d11d7-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="d11d7-126">-RouteName</span></span>
<span data-ttu-id="d11d7-127">Rotanın adı</span><span class="sxs-lookup"><span data-stu-id="d11d7-127">Name of the Route</span></span>

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

### <span data-ttu-id="d11d7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d11d7-128">CommonParameters</span></span>
<span data-ttu-id="d11d7-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d11d7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d11d7-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d11d7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d11d7-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d11d7-131">INPUTS</span></span>

### <span data-ttu-id="d11d7-132">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="d11d7-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="d11d7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d11d7-133">System.String</span></span>

## <span data-ttu-id="d11d7-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d11d7-134">OUTPUTS</span></span>

### <span data-ttu-id="d11d7-135">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="d11d7-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>
<span data-ttu-id="d11d7-136">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Management. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d11d7-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d11d7-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d11d7-137">NOTES</span></span>

## <span data-ttu-id="d11d7-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d11d7-138">RELATED LINKS</span></span>
