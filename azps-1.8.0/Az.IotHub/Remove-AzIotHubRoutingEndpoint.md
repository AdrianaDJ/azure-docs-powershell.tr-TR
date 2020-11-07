---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 1ff1ba2d8e3a4a7ce8a80c364ff8ccee3e91d8ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916408"
---
# <span data-ttu-id="025b3-101">Remove-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="025b3-101">Remove-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="025b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="025b3-102">SYNOPSIS</span></span>
<span data-ttu-id="025b3-103">IoT merkeziniz için uç noktayı silme</span><span class="sxs-lookup"><span data-stu-id="025b3-103">Delete an endpoint for your IoT Hub</span></span>

## <span data-ttu-id="025b3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="025b3-104">SYNTAX</span></span>

### <span data-ttu-id="025b3-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="025b3-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="025b3-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="025b3-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="025b3-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="025b3-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>] [-EndpointType <PSEndpointType>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="025b3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="025b3-108">DESCRIPTION</span></span>
<span data-ttu-id="025b3-109">Uç noktayı silme.</span><span class="sxs-lookup"><span data-stu-id="025b3-109">Delete an endpoint.</span></span> <span data-ttu-id="025b3-110">Bu uç noktayı kullanan yolların silinmesini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="025b3-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="025b3-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="025b3-111">EXAMPLES</span></span>

### <span data-ttu-id="025b3-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="025b3-112">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="025b3-113">"Myiothub" IoT Hub 'ından "E2" uç noktasını silin.</span><span class="sxs-lookup"><span data-stu-id="025b3-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="025b3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="025b3-114">PARAMETERS</span></span>

### <span data-ttu-id="025b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="025b3-115">-DefaultProfile</span></span>
<span data-ttu-id="025b3-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="025b3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="025b3-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="025b3-117">-EndpointName</span></span>
<span data-ttu-id="025b3-118">Yönlendirme uç noktasının adı</span><span class="sxs-lookup"><span data-stu-id="025b3-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="025b3-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="025b3-119">-EndpointType</span></span>
<span data-ttu-id="025b3-120">Yönlendirme uç noktasının türü</span><span class="sxs-lookup"><span data-stu-id="025b3-120">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="025b3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="025b3-121">-InputObject</span></span>
<span data-ttu-id="025b3-122">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="025b3-122">IotHub Object</span></span>

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

### <span data-ttu-id="025b3-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="025b3-123">-Name</span></span>
<span data-ttu-id="025b3-124">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="025b3-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="025b3-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="025b3-125">-PassThru</span></span>
<span data-ttu-id="025b3-126">Boole nesnesini döndürmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="025b3-126">Allows to return the boolean object.</span></span> <span data-ttu-id="025b3-127">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="025b3-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="025b3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="025b3-128">-ResourceGroupName</span></span>
<span data-ttu-id="025b3-129">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="025b3-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="025b3-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="025b3-130">-ResourceId</span></span>
<span data-ttu-id="025b3-131">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="025b3-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="025b3-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="025b3-132">-Confirm</span></span>
<span data-ttu-id="025b3-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="025b3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="025b3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="025b3-134">-WhatIf</span></span>
<span data-ttu-id="025b3-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="025b3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="025b3-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="025b3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="025b3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="025b3-137">CommonParameters</span></span>
<span data-ttu-id="025b3-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="025b3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="025b3-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="025b3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="025b3-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="025b3-140">INPUTS</span></span>

### <span data-ttu-id="025b3-141">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="025b3-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="025b3-142">System. String</span><span class="sxs-lookup"><span data-stu-id="025b3-142">System.String</span></span>

## <span data-ttu-id="025b3-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="025b3-143">OUTPUTS</span></span>

### <span data-ttu-id="025b3-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="025b3-144">System.Boolean</span></span>

## <span data-ttu-id="025b3-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="025b3-145">NOTES</span></span>

## <span data-ttu-id="025b3-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="025b3-146">RELATED LINKS</span></span>
