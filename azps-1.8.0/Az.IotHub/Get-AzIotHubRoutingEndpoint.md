---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 8852139cfcedc5ff0ee42c234c44b1505042ef1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916447"
---
# <span data-ttu-id="cd6aa-101">Get-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd6aa-101">Get-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="cd6aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd6aa-102">SYNOPSIS</span></span>
<span data-ttu-id="cd6aa-103">IoT merkeziniz için tüm uç noktalar hakkında bilgi edinin</span><span class="sxs-lookup"><span data-stu-id="cd6aa-103">Get information on all the endpoints for your IoT Hub</span></span>

## <span data-ttu-id="cd6aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd6aa-104">SYNTAX</span></span>

### <span data-ttu-id="cd6aa-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cd6aa-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd6aa-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="cd6aa-106">InputObjectSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd6aa-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="cd6aa-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd6aa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd6aa-108">DESCRIPTION</span></span>
<span data-ttu-id="cd6aa-109">Uç nokta hakkında bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="cd6aa-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="cd6aa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd6aa-110">EXAMPLES</span></span>

### <span data-ttu-id="cd6aa-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cd6aa-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="cd6aa-112">"Myiothub" IoT Hub 'ından tüm uç noktaları alın.</span><span class="sxs-lookup"><span data-stu-id="cd6aa-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="cd6aa-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="cd6aa-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="cd6aa-114">"Myiothub" IoT Hub 'ından EventHub türündeki tüm uç noktaları edinin.</span><span class="sxs-lookup"><span data-stu-id="cd6aa-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="cd6aa-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="cd6aa-115">Example 3</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="cd6aa-116">"Myiothub" IoT Hub 'ından EventHub türündeki tüm uç noktaları edinin.</span><span class="sxs-lookup"><span data-stu-id="cd6aa-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="cd6aa-117">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="cd6aa-117">Example 4</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="cd6aa-118">"Myiothub" IoT Hub 'ından uç nokta bilgileri edinin.</span><span class="sxs-lookup"><span data-stu-id="cd6aa-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="cd6aa-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd6aa-119">PARAMETERS</span></span>

### <span data-ttu-id="cd6aa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd6aa-120">-DefaultProfile</span></span>
<span data-ttu-id="cd6aa-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cd6aa-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd6aa-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="cd6aa-122">-EndpointName</span></span>
<span data-ttu-id="cd6aa-123">Yönlendirme uç noktasının adı</span><span class="sxs-lookup"><span data-stu-id="cd6aa-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="cd6aa-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="cd6aa-124">-EndpointType</span></span>
<span data-ttu-id="cd6aa-125">Yönlendirme uç noktasının türü</span><span class="sxs-lookup"><span data-stu-id="cd6aa-125">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="cd6aa-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd6aa-126">-InputObject</span></span>
<span data-ttu-id="cd6aa-127">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="cd6aa-127">IotHub Object</span></span>

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

### <span data-ttu-id="cd6aa-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="cd6aa-128">-Name</span></span>
<span data-ttu-id="cd6aa-129">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="cd6aa-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="cd6aa-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd6aa-130">-ResourceGroupName</span></span>
<span data-ttu-id="cd6aa-131">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="cd6aa-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cd6aa-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cd6aa-132">-ResourceId</span></span>
<span data-ttu-id="cd6aa-133">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="cd6aa-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="cd6aa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd6aa-134">CommonParameters</span></span>
<span data-ttu-id="cd6aa-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd6aa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd6aa-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd6aa-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd6aa-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd6aa-137">INPUTS</span></span>

### <span data-ttu-id="cd6aa-138">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="cd6aa-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="cd6aa-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cd6aa-139">System.String</span></span>

## <span data-ttu-id="cd6aa-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd6aa-140">OUTPUTS</span></span>

### <span data-ttu-id="cd6aa-141">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd6aa-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="cd6aa-142">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingEventHubProperties, Microsoft. Azure. PowerShell. cmdlet. IotHub, Version = 1.0.0.0, kültür = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="cd6aa-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="cd6aa-143">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd6aa-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="cd6aa-144">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingServiceBusQueueEndpointProperties []</span><span class="sxs-lookup"><span data-stu-id="cd6aa-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span></span>

### <span data-ttu-id="cd6aa-145">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd6aa-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="cd6aa-146">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingServiceBusTopicEndpointProperties []</span><span class="sxs-lookup"><span data-stu-id="cd6aa-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span></span>

### <span data-ttu-id="cd6aa-147">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd6aa-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

### <span data-ttu-id="cd6aa-148">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingStorageContainerProperties []</span><span class="sxs-lookup"><span data-stu-id="cd6aa-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span></span>

### <span data-ttu-id="cd6aa-149">Microsoft. Azure. Commands. Management. IotHub. modeller. Psroutingcustomenvseçpoint []</span><span class="sxs-lookup"><span data-stu-id="cd6aa-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span></span>

## <span data-ttu-id="cd6aa-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd6aa-150">NOTES</span></span>

## <span data-ttu-id="cd6aa-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd6aa-151">RELATED LINKS</span></span>
