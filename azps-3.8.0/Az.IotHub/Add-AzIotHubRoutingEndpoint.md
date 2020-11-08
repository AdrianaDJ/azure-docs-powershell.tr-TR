---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 2af7a4518d551509089585877f74468510746dcd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095933"
---
# <span data-ttu-id="b63fe-101">Add-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="b63fe-101">Add-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="b63fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b63fe-102">SYNOPSIS</span></span>
<span data-ttu-id="b63fe-103">IoT Hub 'ınıza uç nokta ekleme</span><span class="sxs-lookup"><span data-stu-id="b63fe-103">Add an endpoint to your IoT Hub</span></span>

## <span data-ttu-id="b63fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b63fe-104">SYNTAX</span></span>

### <span data-ttu-id="b63fe-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b63fe-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 -EndpointType <PSEndpointType> -EndpointResourceGroup <String> -EndpointSubscriptionId <String>
 -ConnectionString <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b63fe-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="b63fe-106">InputObjectSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b63fe-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="b63fe-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b63fe-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b63fe-108">DESCRIPTION</span></span>
<span data-ttu-id="b63fe-109">IoT Hub 'ınıza yeni uç nokta ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b63fe-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="b63fe-110">Desteklenen uç noktalar hakkında bilgi edinmek için bkz. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="b63fe-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="b63fe-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b63fe-111">EXAMPLES</span></span>

### <span data-ttu-id="b63fe-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b63fe-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="b63fe-113">"Myiothub" IoT Hub 'ına EventHub türünün yeni "E2" uç noktasını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b63fe-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="b63fe-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b63fe-114">Example 2</span></span>
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

<span data-ttu-id="b63fe-115">"Myiothub" IoT Hub 'ına AzureStorageContainer türünde yeni bir uç nokta "S1" ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b63fe-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="b63fe-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b63fe-116">PARAMETERS</span></span>

### <span data-ttu-id="b63fe-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="b63fe-117">-ConnectionString</span></span>
<span data-ttu-id="b63fe-118">Yönlendirme uç noktasının bağlantı dizesi</span><span class="sxs-lookup"><span data-stu-id="b63fe-118">Connection string of the Routing Endpoint</span></span>

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

### <span data-ttu-id="b63fe-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b63fe-119">-DefaultProfile</span></span>
<span data-ttu-id="b63fe-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b63fe-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b63fe-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b63fe-121">-EndpointName</span></span>
<span data-ttu-id="b63fe-122">Yönlendirme uç noktasının adı</span><span class="sxs-lookup"><span data-stu-id="b63fe-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="b63fe-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b63fe-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="b63fe-124">Uç nokta kaynağının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="b63fe-124">Resource group of the Endpoint resource</span></span>

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

### <span data-ttu-id="b63fe-125">-Endpointsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="b63fe-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="b63fe-126">Uç nokta kaynağının SubscriptionID 'ı</span><span class="sxs-lookup"><span data-stu-id="b63fe-126">SubscriptionId of the Endpoint resource</span></span>

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

### <span data-ttu-id="b63fe-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="b63fe-127">-EndpointType</span></span>
<span data-ttu-id="b63fe-128">Yönlendirme uç noktasının türü</span><span class="sxs-lookup"><span data-stu-id="b63fe-128">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="b63fe-129">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="b63fe-129">-ContainerName</span></span>
<span data-ttu-id="b63fe-130">Depolama kapsayıcısının adı</span><span class="sxs-lookup"><span data-stu-id="b63fe-130">Name of the storage container</span></span>

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

### <span data-ttu-id="b63fe-131">Kodlamalı</span><span class="sxs-lookup"><span data-stu-id="b63fe-131">-Encoding</span></span>
<span data-ttu-id="b63fe-132">Verilerinizi dolaştırmak istediğiniz biçimi seçin.</span><span class="sxs-lookup"><span data-stu-id="b63fe-132">Select the format in which you want to route your data in.</span></span> <span data-ttu-id="b63fe-133">JSON veya AVRO 'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b63fe-133">You can select JSON or AVRO.</span></span> <span data-ttu-id="b63fe-134">Varsayılan AVRO olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="b63fe-134">The default is set to AVRO.</span></span>

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

### <span data-ttu-id="b63fe-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b63fe-135">-InputObject</span></span>
<span data-ttu-id="b63fe-136">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="b63fe-136">IotHub Object</span></span>

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

### <span data-ttu-id="b63fe-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="b63fe-137">-Name</span></span>
<span data-ttu-id="b63fe-138">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="b63fe-138">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b63fe-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b63fe-139">-ResourceGroupName</span></span>
<span data-ttu-id="b63fe-140">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="b63fe-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b63fe-141">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b63fe-141">-ResourceId</span></span>
<span data-ttu-id="b63fe-142">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="b63fe-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b63fe-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="b63fe-143">-Confirm</span></span>
<span data-ttu-id="b63fe-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b63fe-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b63fe-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b63fe-145">-WhatIf</span></span>
<span data-ttu-id="b63fe-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b63fe-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b63fe-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b63fe-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b63fe-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b63fe-148">CommonParameters</span></span>
<span data-ttu-id="b63fe-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b63fe-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b63fe-150">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b63fe-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b63fe-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b63fe-151">INPUTS</span></span>

### <span data-ttu-id="b63fe-152">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="b63fe-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b63fe-153">System. String</span><span class="sxs-lookup"><span data-stu-id="b63fe-153">System.String</span></span>

## <span data-ttu-id="b63fe-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b63fe-154">OUTPUTS</span></span>

### <span data-ttu-id="b63fe-155">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="b63fe-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="b63fe-156">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="b63fe-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="b63fe-157">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="b63fe-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="b63fe-158">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b63fe-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="b63fe-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b63fe-159">NOTES</span></span>

## <span data-ttu-id="b63fe-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b63fe-160">RELATED LINKS</span></span>