---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: 2aa49f01b16547987604a7ee978018596c7d9647
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764391"
---
# <span data-ttu-id="9c45a-101">Get-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="9c45a-101">Get-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="9c45a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c45a-102">SYNOPSIS</span></span>
<span data-ttu-id="9c45a-103">IoT merkeziniz için tüm uç noktalar hakkında bilgi edinin</span><span class="sxs-lookup"><span data-stu-id="9c45a-103">Get information on all the endpoints for your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c45a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c45a-104">SYNTAX</span></span>

### <span data-ttu-id="9c45a-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9c45a-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String>
 [-EndpointType <PSEndpointType>] [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c45a-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="9c45a-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c45a-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="9c45a-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c45a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c45a-108">DESCRIPTION</span></span>
<span data-ttu-id="9c45a-109">Uç nokta hakkında bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="9c45a-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="9c45a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c45a-110">EXAMPLES</span></span>

### <span data-ttu-id="9c45a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9c45a-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="9c45a-112">"Myiothub" IoT Hub 'ından tüm uç noktaları alın.</span><span class="sxs-lookup"><span data-stu-id="9c45a-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="9c45a-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9c45a-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="9c45a-114">"Myiothub" IoT Hub 'ından EventHub türündeki tüm uç noktaları edinin.</span><span class="sxs-lookup"><span data-stu-id="9c45a-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="9c45a-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="9c45a-115">Example 3</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="9c45a-116">"Myiothub" IoT Hub 'ından EventHub türündeki tüm uç noktaları edinin.</span><span class="sxs-lookup"><span data-stu-id="9c45a-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="9c45a-117">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="9c45a-117">Example 4</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="9c45a-118">"Myiothub" IoT Hub 'ından uç nokta bilgileri edinin.</span><span class="sxs-lookup"><span data-stu-id="9c45a-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="9c45a-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c45a-119">PARAMETERS</span></span>

### <span data-ttu-id="9c45a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c45a-120">-DefaultProfile</span></span>
<span data-ttu-id="9c45a-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9c45a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c45a-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="9c45a-122">-EndpointName</span></span>
<span data-ttu-id="9c45a-123">Yönlendirme uç noktasının adı</span><span class="sxs-lookup"><span data-stu-id="9c45a-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="9c45a-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="9c45a-124">-EndpointType</span></span>
<span data-ttu-id="9c45a-125">Yönlendirme uç noktasının türü</span><span class="sxs-lookup"><span data-stu-id="9c45a-125">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c45a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c45a-126">-InputObject</span></span>
<span data-ttu-id="9c45a-127">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="9c45a-127">IotHub Object</span></span>

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

### <span data-ttu-id="9c45a-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="9c45a-128">-Name</span></span>
<span data-ttu-id="9c45a-129">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="9c45a-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9c45a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c45a-130">-ResourceGroupName</span></span>
<span data-ttu-id="9c45a-131">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="9c45a-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9c45a-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9c45a-132">-ResourceId</span></span>
<span data-ttu-id="9c45a-133">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="9c45a-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9c45a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c45a-134">CommonParameters</span></span>
<span data-ttu-id="9c45a-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c45a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c45a-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c45a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c45a-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c45a-137">INPUTS</span></span>

### <span data-ttu-id="9c45a-138">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="9c45a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="9c45a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9c45a-139">System.String</span></span>

## <span data-ttu-id="9c45a-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c45a-140">OUTPUTS</span></span>

### <span data-ttu-id="9c45a-141">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="9c45a-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="9c45a-142">System. Koleksiyonlar. Generic. LIST `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List` 1 [[Microsoft. Azure. Commands. Management. IotHub. modeller. Psroutinghizmetibusqueueendpointproperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]] Microsoft... Commands. Management. `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List` Management. IotHub. modeller. PSRoutingStorageContainerProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]] System. Koleksiyonlar. Generic. List ' 1 [[Microsoft. Azure. Commands. Management. IotHub. modeller. Psroutingcustomenvseçpoint, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9c45a-142">System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9c45a-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c45a-143">NOTES</span></span>

## <span data-ttu-id="9c45a-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c45a-144">RELATED LINKS</span></span>
