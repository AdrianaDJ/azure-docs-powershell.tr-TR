---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: 6caad4faec3dd292f902689757b82b90091afcde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594026"
---
# <span data-ttu-id="9cdac-101">Remove-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="9cdac-101">Remove-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="9cdac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cdac-102">SYNOPSIS</span></span>
<span data-ttu-id="9cdac-103">IoT merkeziniz için uç noktayı silme</span><span class="sxs-lookup"><span data-stu-id="9cdac-103">Delete an endpoint for your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cdac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9cdac-104">SYNTAX</span></span>

### <span data-ttu-id="9cdac-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9cdac-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9cdac-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="9cdac-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9cdac-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="9cdac-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9cdac-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9cdac-108">DESCRIPTION</span></span>
<span data-ttu-id="9cdac-109">Uç noktayı silme.</span><span class="sxs-lookup"><span data-stu-id="9cdac-109">Delete an endpoint.</span></span> <span data-ttu-id="9cdac-110">Bu uç noktayı kullanan yolların silinmesini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="9cdac-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="9cdac-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9cdac-111">EXAMPLES</span></span>

### <span data-ttu-id="9cdac-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9cdac-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="9cdac-113">"Myiothub" IoT Hub 'ından "E2" uç noktasını silin.</span><span class="sxs-lookup"><span data-stu-id="9cdac-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="9cdac-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9cdac-114">PARAMETERS</span></span>

### <span data-ttu-id="9cdac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cdac-115">-DefaultProfile</span></span>
<span data-ttu-id="9cdac-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9cdac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cdac-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="9cdac-117">-EndpointName</span></span>
<span data-ttu-id="9cdac-118">Yönlendirme uç noktasının adı</span><span class="sxs-lookup"><span data-stu-id="9cdac-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="9cdac-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="9cdac-119">-EndpointType</span></span>
<span data-ttu-id="9cdac-120">Yönlendirme uç noktasının türü</span><span class="sxs-lookup"><span data-stu-id="9cdac-120">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cdac-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cdac-121">-InputObject</span></span>
<span data-ttu-id="9cdac-122">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="9cdac-122">IotHub Object</span></span>

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

### <span data-ttu-id="9cdac-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="9cdac-123">-Name</span></span>
<span data-ttu-id="9cdac-124">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="9cdac-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9cdac-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9cdac-125">-PassThru</span></span>
<span data-ttu-id="9cdac-126">Boole nesnesini döndürmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="9cdac-126">Allows to return the boolean object.</span></span> <span data-ttu-id="9cdac-127">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="9cdac-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cdac-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cdac-128">-ResourceGroupName</span></span>
<span data-ttu-id="9cdac-129">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="9cdac-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9cdac-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9cdac-130">-ResourceId</span></span>
<span data-ttu-id="9cdac-131">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="9cdac-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9cdac-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="9cdac-132">-Confirm</span></span>
<span data-ttu-id="9cdac-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9cdac-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cdac-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cdac-134">-WhatIf</span></span>
<span data-ttu-id="9cdac-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9cdac-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cdac-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9cdac-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cdac-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cdac-137">CommonParameters</span></span>
<span data-ttu-id="9cdac-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9cdac-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cdac-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cdac-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cdac-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9cdac-140">INPUTS</span></span>

### <span data-ttu-id="9cdac-141">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="9cdac-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="9cdac-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9cdac-142">System.String</span></span>

## <span data-ttu-id="9cdac-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9cdac-143">OUTPUTS</span></span>

### <span data-ttu-id="9cdac-144">Microsoft. Azure. Commands. Management. IotHub. modeller. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="9cdac-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="9cdac-145">System. Koleksiyonlar. Generic. LIST `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List` 1 [[Microsoft. Azure. Commands. Management. IotHub. modeller. Psroutinghizmetibusqueueendpointproperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]] Microsoft... Commands. Management. `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List` Management. IotHub. modeller. PSRoutingStorageContainerProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]] System. Koleksiyonlar. Generic. List ' 1 [[Microsoft. Azure. Commands. Management. IotHub. modeller. Psroutingcustomenvseçpoint, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9cdac-145">System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9cdac-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9cdac-146">NOTES</span></span>

## <span data-ttu-id="9cdac-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9cdac-147">RELATED LINKS</span></span>
