---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 1c1c865f37a6cb98fec0cc6b1403f9d9257a6d85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916491"
---
# <span data-ttu-id="3a9cf-101">Add-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a9cf-101">Add-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="3a9cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a9cf-102">SYNOPSIS</span></span>
<span data-ttu-id="3a9cf-103">IoT Hub 'ınıza uç nokta ekleme</span><span class="sxs-lookup"><span data-stu-id="3a9cf-103">Add an endpoint to your IoT Hub</span></span>

## <span data-ttu-id="3a9cf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a9cf-104">SYNTAX</span></span>

### <span data-ttu-id="3a9cf-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3a9cf-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 -EndpointType <PSEndpointType> -EndpointResourceGroup <String> -EndpointSubscriptionId <String>
 -ConnectionString <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a9cf-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="3a9cf-106">InputObjectSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a9cf-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="3a9cf-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a9cf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a9cf-108">DESCRIPTION</span></span>
<span data-ttu-id="3a9cf-109">IoT Hub 'ınıza yeni uç nokta ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="3a9cf-110">Desteklenen uç noktalar hakkında bilgi edinmek için bkz. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="3a9cf-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="3a9cf-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a9cf-111">EXAMPLES</span></span>

### <span data-ttu-id="3a9cf-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3a9cf-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="3a9cf-113">"Myiothub" IoT Hub 'ına EventHub türünün yeni "E2" uç noktasını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="3a9cf-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3a9cf-114">Example 2</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName S1 -EndpointType AzureStorageContainer -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'DefaultEndpointsProtocol=https;AccountName=mystorage1;AccountKey=*****;EndpointSuffix=core.windows.net' -ContainerName container -Encoding json

ResourceGroupName       : resourcegroup1
SubscriptionId          : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName            : S1
ContainerName           : container
ConnectionString        : DefaultEndpointsProtocol=https;EndpointSuffix=core.windows.net;AccountName=mystorage1;AccountKey=****
FileNameFormat          : {iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}
BatchFrequencyInSeconds : 300
MaxChunkSizeInBytes     : 314572800
Encoding                : json
```

<span data-ttu-id="3a9cf-115">"Myiothub" IoT Hub 'ına AzureStorageContainer türünde yeni bir uç nokta "S1" ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="3a9cf-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a9cf-116">PARAMETERS</span></span>

### <span data-ttu-id="3a9cf-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="3a9cf-117">-ConnectionString</span></span>
<span data-ttu-id="3a9cf-118">Yönlendirme uç noktasının bağlantı dizesi</span><span class="sxs-lookup"><span data-stu-id="3a9cf-118">Connection string of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9cf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a9cf-119">-DefaultProfile</span></span>
<span data-ttu-id="3a9cf-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a9cf-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3a9cf-121">-EndpointName</span></span>
<span data-ttu-id="3a9cf-122">Yönlendirme uç noktasının adı</span><span class="sxs-lookup"><span data-stu-id="3a9cf-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="3a9cf-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3a9cf-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="3a9cf-124">Son nokta kaynağının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="3a9cf-124">Resource group of the Endpoint resoure</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9cf-125">-Endpointsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="3a9cf-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="3a9cf-126">Uç nokta kaynağının SubscriptionID 'ı</span><span class="sxs-lookup"><span data-stu-id="3a9cf-126">SubscriptionId of the Endpoint resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9cf-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="3a9cf-127">-EndpointType</span></span>
<span data-ttu-id="3a9cf-128">Yönlendirme uç noktasının türü</span><span class="sxs-lookup"><span data-stu-id="3a9cf-128">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9cf-129">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="3a9cf-129">-ContainerName</span></span>
<span data-ttu-id="3a9cf-130">Depolama kapsayıcısının adı</span><span class="sxs-lookup"><span data-stu-id="3a9cf-130">Name of the storage container</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9cf-131">Kodlamalı</span><span class="sxs-lookup"><span data-stu-id="3a9cf-131">-Encoding</span></span>
<span data-ttu-id="3a9cf-132">Verilerinizi dolaştırmak istediğiniz biçimi seçin.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-132">Select the format in which you want to route your data in.</span></span> <span data-ttu-id="3a9cf-133">JSON veya AVRO 'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-133">You can select JSON or AVRO.</span></span> <span data-ttu-id="3a9cf-134">Varsayılan AVRO olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-134">The default is set to AVRO.</span></span>

```yaml
Type:System.String
Parameter Sets: (All)
Aliases:
Accepted values: JSON, AVRO

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9cf-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a9cf-135">-InputObject</span></span>
<span data-ttu-id="3a9cf-136">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="3a9cf-136">IotHub Object</span></span>

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

### <span data-ttu-id="3a9cf-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="3a9cf-137">-Name</span></span>
<span data-ttu-id="3a9cf-138">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="3a9cf-138">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3a9cf-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a9cf-139">-ResourceGroupName</span></span>
<span data-ttu-id="3a9cf-140">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="3a9cf-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3a9cf-141">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3a9cf-141">-ResourceId</span></span>
<span data-ttu-id="3a9cf-142">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="3a9cf-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3a9cf-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="3a9cf-143">-Confirm</span></span>
<span data-ttu-id="3a9cf-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a9cf-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a9cf-145">-WhatIf</span></span>
<span data-ttu-id="3a9cf-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a9cf-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a9cf-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a9cf-148">CommonParameters</span></span>
<span data-ttu-id="3a9cf-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a9cf-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a9cf-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a9cf-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a9cf-151">INPUTS</span></span>

### <span data-ttu-id="3a9cf-152">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="3a9cf-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3a9cf-153">System. String</span><span class="sxs-lookup"><span data-stu-id="3a9cf-153">System.String</span></span>

## <span data-ttu-id="3a9cf-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a9cf-154">OUTPUTS</span></span>

### <span data-ttu-id="3a9cf-155">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a9cf-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="3a9cf-156">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a9cf-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="3a9cf-157">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a9cf-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="3a9cf-158">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a9cf-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="3a9cf-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a9cf-159">NOTES</span></span>

## <span data-ttu-id="3a9cf-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a9cf-160">RELATED LINKS</span></span>
