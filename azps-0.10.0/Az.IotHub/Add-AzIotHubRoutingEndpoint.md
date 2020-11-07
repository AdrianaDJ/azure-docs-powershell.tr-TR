---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 9715e7ee505fce0b34039d74d35e53b7138d7160
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936705"
---
# <span data-ttu-id="1e2f2-101">Add-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e2f2-101">Add-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="1e2f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e2f2-102">SYNOPSIS</span></span>
<span data-ttu-id="1e2f2-103">IoT Hub 'ınıza uç nokta ekleme</span><span class="sxs-lookup"><span data-stu-id="1e2f2-103">Add an endpoint to your IoT Hub</span></span>

## <span data-ttu-id="1e2f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e2f2-104">SYNTAX</span></span>

### <span data-ttu-id="1e2f2-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1e2f2-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 -EndpointType <PSEndpointType> -EndpointResourceGroup <String> -EndpointSubscriptionId <String>
 -ConnectionString <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e2f2-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="1e2f2-106">InputObjectSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e2f2-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="1e2f2-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e2f2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e2f2-108">DESCRIPTION</span></span>
<span data-ttu-id="1e2f2-109">IoT Hub 'ınıza yeni uç nokta ekleyin.</span><span class="sxs-lookup"><span data-stu-id="1e2f2-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="1e2f2-110">Desteklenen uç noktalar hakkında bilgi edinmek için bkz. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="1e2f2-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="1e2f2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e2f2-111">EXAMPLES</span></span>

### <span data-ttu-id="1e2f2-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1e2f2-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="1e2f2-113">"Myiothub" IoT Hub 'ına EventHub türünün yeni "E2" uç noktasını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="1e2f2-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="1e2f2-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1e2f2-114">Example 2</span></span>
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

<span data-ttu-id="1e2f2-115">"Myiothub" IoT Hub 'ına AzureStorageContainer türünde yeni bir uç nokta "S1" ekleyin.</span><span class="sxs-lookup"><span data-stu-id="1e2f2-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="1e2f2-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e2f2-116">PARAMETERS</span></span>

### <span data-ttu-id="1e2f2-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="1e2f2-117">-ConnectionString</span></span>
<span data-ttu-id="1e2f2-118">Yönlendirme uç noktasının bağlantı dizesi</span><span class="sxs-lookup"><span data-stu-id="1e2f2-118">Connection string of the Routing Endpoint</span></span>

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

### <span data-ttu-id="1e2f2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e2f2-119">-DefaultProfile</span></span>
<span data-ttu-id="1e2f2-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1e2f2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e2f2-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1e2f2-121">-EndpointName</span></span>
<span data-ttu-id="1e2f2-122">Yönlendirme uç noktasının adı</span><span class="sxs-lookup"><span data-stu-id="1e2f2-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="1e2f2-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1e2f2-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="1e2f2-124">Uç nokta kaynağının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="1e2f2-124">Resource group of the Endpoint resource</span></span>

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

### <span data-ttu-id="1e2f2-125">-Endpointsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="1e2f2-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="1e2f2-126">Uç nokta kaynağının SubscriptionID 'ı</span><span class="sxs-lookup"><span data-stu-id="1e2f2-126">SubscriptionId of the Endpoint resource</span></span>

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

### <span data-ttu-id="1e2f2-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="1e2f2-127">-EndpointType</span></span>
<span data-ttu-id="1e2f2-128">Yönlendirme uç noktasının türü</span><span class="sxs-lookup"><span data-stu-id="1e2f2-128">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="1e2f2-129">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="1e2f2-129">-ContainerName</span></span>
<span data-ttu-id="1e2f2-130">Depolama kapsayıcısının adı</span><span class="sxs-lookup"><span data-stu-id="1e2f2-130">Name of the storage container</span></span>

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

### <span data-ttu-id="1e2f2-131">Kodlamalı</span><span class="sxs-lookup"><span data-stu-id="1e2f2-131">-Encoding</span></span>
<span data-ttu-id="1e2f2-132">Verilerinizi dolaştırmak istediğiniz biçimi seçin.</span><span class="sxs-lookup"><span data-stu-id="1e2f2-132">Select the format in which you want to route your data in.</span></span> <span data-ttu-id="1e2f2-133">JSON veya AVRO 'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1e2f2-133">You can select JSON or AVRO.</span></span> <span data-ttu-id="1e2f2-134">Varsayılan AVRO olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="1e2f2-134">The default is set to AVRO.</span></span>

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

### <span data-ttu-id="1e2f2-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e2f2-135">-InputObject</span></span>
<span data-ttu-id="1e2f2-136">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="1e2f2-136">IotHub Object</span></span>

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

### <span data-ttu-id="1e2f2-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="1e2f2-137">-Name</span></span>
<span data-ttu-id="1e2f2-138">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="1e2f2-138">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1e2f2-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e2f2-139">-ResourceGroupName</span></span>
<span data-ttu-id="1e2f2-140">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="1e2f2-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1e2f2-141">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1e2f2-141">-ResourceId</span></span>
<span data-ttu-id="1e2f2-142">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="1e2f2-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1e2f2-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="1e2f2-143">-Confirm</span></span>
<span data-ttu-id="1e2f2-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1e2f2-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e2f2-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e2f2-145">-WhatIf</span></span>
<span data-ttu-id="1e2f2-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1e2f2-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e2f2-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1e2f2-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e2f2-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e2f2-148">CommonParameters</span></span>
<span data-ttu-id="1e2f2-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e2f2-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e2f2-150">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e2f2-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e2f2-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e2f2-151">INPUTS</span></span>

### <span data-ttu-id="1e2f2-152">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="1e2f2-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1e2f2-153">System. String</span><span class="sxs-lookup"><span data-stu-id="1e2f2-153">System.String</span></span>

## <span data-ttu-id="1e2f2-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e2f2-154">OUTPUTS</span></span>

### <span data-ttu-id="1e2f2-155">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e2f2-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="1e2f2-156">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e2f2-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="1e2f2-157">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e2f2-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="1e2f2-158">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e2f2-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="1e2f2-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e2f2-159">NOTES</span></span>

## <span data-ttu-id="1e2f2-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e2f2-160">RELATED LINKS</span></span>
