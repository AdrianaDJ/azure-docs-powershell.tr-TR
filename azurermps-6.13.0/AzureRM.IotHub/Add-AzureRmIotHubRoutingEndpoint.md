---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: d251d3159111437cd06880a49069aee7aca6d80f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589527"
---
# <span data-ttu-id="a6056-101">Add-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6056-101">Add-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="a6056-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6056-102">SYNOPSIS</span></span>
<span data-ttu-id="a6056-103">IoT Hub 'ınıza uç nokta ekleme</span><span class="sxs-lookup"><span data-stu-id="a6056-103">Add an endpoint to your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6056-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a6056-104">SYNTAX</span></span>

### <span data-ttu-id="a6056-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a6056-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6056-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="a6056-106">InputObjectSet</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6056-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="a6056-107">ResourceIdSet</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6056-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a6056-108">DESCRIPTION</span></span>
<span data-ttu-id="a6056-109">IoT Hub 'ınıza yeni uç nokta ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a6056-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="a6056-110">Desteklenen uç noktalar hakkında bilgi edinmek için bkz. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="a6056-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="a6056-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a6056-111">EXAMPLES</span></span>

### <span data-ttu-id="a6056-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a6056-112">Example 1</span></span>
```
PS C:\> Add-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="a6056-113">"Myiothub" IoT Hub 'ına EventHub türünün yeni "E2" uç noktasını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a6056-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="a6056-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a6056-114">Example 2</span></span>
```
PS C:\> Add-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName S1 -EndpointType AzureStorageContainer -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'DefaultEndpointsProtocol=https;AccountName=mystorage1;AccountKey=*****;EndpointSuffix=core.windows.net' -ContainerName container

ResourceGroupName       : resourcegroup1
SubscriptionId          : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName            : S1
ContainerName           : container
ConnectionString        : DefaultEndpointsProtocol=https;EndpointSuffix=core.windows.net;AccountName=mystorage1;AccountKey=****
FileNameFormat          : {iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}
BatchFrequencyInSeconds : 300
MaxChunkSizeInBytes     : 314572800
Encoding                : avro
```

<span data-ttu-id="a6056-115">"Myiothub" IoT Hub 'ına AzureStorageContainer türünde yeni bir uç nokta "S1" ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a6056-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="a6056-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a6056-116">PARAMETERS</span></span>

### <span data-ttu-id="a6056-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="a6056-117">-ConnectionString</span></span>
<span data-ttu-id="a6056-118">Yönlendirme uç noktasının bağlantı dizesi</span><span class="sxs-lookup"><span data-stu-id="a6056-118">Connection string of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6056-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6056-119">-DefaultProfile</span></span>
<span data-ttu-id="a6056-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a6056-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6056-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a6056-121">-EndpointName</span></span>
<span data-ttu-id="a6056-122">Yönlendirme uç noktasının adı</span><span class="sxs-lookup"><span data-stu-id="a6056-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="a6056-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a6056-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="a6056-124">Son nokta kaynağının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="a6056-124">Resource group of the Endpoint resoure</span></span>

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

### <span data-ttu-id="a6056-125">-Endpointsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="a6056-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="a6056-126">Uç nokta kaynağının SubscriptionID 'ı</span><span class="sxs-lookup"><span data-stu-id="a6056-126">SubscriptionId of the Endpoint resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6056-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="a6056-127">-EndpointType</span></span>
<span data-ttu-id="a6056-128">Yönlendirme uç noktasının türü</span><span class="sxs-lookup"><span data-stu-id="a6056-128">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6056-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6056-129">-InputObject</span></span>
<span data-ttu-id="a6056-130">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="a6056-130">IotHub Object</span></span>

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

### <span data-ttu-id="a6056-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="a6056-131">-Name</span></span>
<span data-ttu-id="a6056-132">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="a6056-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a6056-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6056-133">-ResourceGroupName</span></span>
<span data-ttu-id="a6056-134">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="a6056-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a6056-135">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a6056-135">-ResourceId</span></span>
<span data-ttu-id="a6056-136">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="a6056-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a6056-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="a6056-137">-Confirm</span></span>
<span data-ttu-id="a6056-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a6056-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6056-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6056-139">-WhatIf</span></span>
<span data-ttu-id="a6056-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a6056-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6056-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a6056-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6056-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6056-142">CommonParameters</span></span>
<span data-ttu-id="a6056-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a6056-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6056-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6056-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6056-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a6056-145">INPUTS</span></span>

### <span data-ttu-id="a6056-146">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="a6056-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="a6056-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a6056-147">System.String</span></span>

## <span data-ttu-id="a6056-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a6056-148">OUTPUTS</span></span>

### <span data-ttu-id="a6056-149">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6056-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="a6056-150">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingServiceBusQueueEndpoint Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6056-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="a6056-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a6056-151">NOTES</span></span>

## <span data-ttu-id="a6056-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a6056-152">RELATED LINKS</span></span>
