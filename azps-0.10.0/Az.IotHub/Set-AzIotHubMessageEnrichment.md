---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 4ecbbe9f37e4a2adf8d5ae5a06ef631d7a3b34cc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935812"
---
# <span data-ttu-id="f4ddd-101">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f4ddd-101">Set-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="f4ddd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ddd-103">IoT merkeziniz içinde bir ileti zenginleştirme.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-103">Update a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="f4ddd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4ddd-104">SYNTAX</span></span>

### <span data-ttu-id="f4ddd-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f4ddd-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4ddd-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="f4ddd-106">InputObjectSet</span></span>
```
Set-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4ddd-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="f4ddd-107">ResourceIdSet</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> [-Value <String>] [-Endpoint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4ddd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4ddd-108">DESCRIPTION</span></span>
<span data-ttu-id="f4ddd-109">Azure IoT Hub 'ındaki ileti zenginleştirme hakkında ayrıntılı bir açıklama için bkz. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="f4ddd-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="f4ddd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4ddd-110">EXAMPLES</span></span>

### <span data-ttu-id="f4ddd-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f4ddd-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "updatedValue"

Key         : newKey
Value       : updatedValue
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="f4ddd-112">"Yenianahtar" anahtarının "updatedValue" şeklinde zenginleştirme değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-112">Updates enrichment's value to "updatedValue" for the key "newKey".</span></span>
<span data-ttu-id="f4ddd-113">Azure IoT Hub 'ındaki ileti zenginleştirme hakkında ayrıntılı bir açıklama için bkz. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="f4ddd-113">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

### <span data-ttu-id="f4ddd-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f4ddd-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Endpoint endpoint1,endpoint2,endpoint3

Key         : newKey
Value       : value1
Endpoint(s) : {endpoint1, endpoint2, endpoint3}
```

<span data-ttu-id="f4ddd-115">"Yenianahtar" anahtarının "endpoint1, endpoint2, endpoint3" için zenginleştirme uç noktasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-115">Updates enrichment's endpoint to "endpoint1, endpoint2, endpoint3" for the key "newKey".</span></span>
<span data-ttu-id="f4ddd-116">Azure IoT Hub 'ındaki ileti zenginleştirme hakkında ayrıntılı bir açıklama için bkz. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="f4ddd-116">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="f4ddd-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4ddd-117">PARAMETERS</span></span>

### <span data-ttu-id="f4ddd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ddd-118">-DefaultProfile</span></span>
<span data-ttu-id="f4ddd-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4ddd-120">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="f4ddd-120">-Endpoint</span></span>
<span data-ttu-id="f4ddd-121">Endın 'a uygulanacak uç nokta.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-121">Endpoint(s) to apply enrichments to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ddd-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4ddd-122">-InputObject</span></span>
<span data-ttu-id="f4ddd-123">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="f4ddd-123">IotHub Object</span></span>

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

### <span data-ttu-id="f4ddd-124">-Tuşlu</span><span class="sxs-lookup"><span data-stu-id="f4ddd-124">-Key</span></span>
<span data-ttu-id="f4ddd-125">Zenginleştirme tuşu.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-125">The enrichment's key.</span></span>

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

### <span data-ttu-id="f4ddd-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="f4ddd-126">-Name</span></span>
<span data-ttu-id="f4ddd-127">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="f4ddd-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f4ddd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4ddd-128">-ResourceGroupName</span></span>
<span data-ttu-id="f4ddd-129">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="f4ddd-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f4ddd-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f4ddd-130">-ResourceId</span></span>
<span data-ttu-id="f4ddd-131">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="f4ddd-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f4ddd-132">-Değer</span><span class="sxs-lookup"><span data-stu-id="f4ddd-132">-Value</span></span>
<span data-ttu-id="f4ddd-133">Enrichment değeri.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-133">The enrichment's value.</span></span>

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

### <span data-ttu-id="f4ddd-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="f4ddd-134">-Confirm</span></span>
<span data-ttu-id="f4ddd-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4ddd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4ddd-136">-WhatIf</span></span>
<span data-ttu-id="f4ddd-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4ddd-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4ddd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ddd-139">CommonParameters</span></span>
<span data-ttu-id="f4ddd-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ddd-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4ddd-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ddd-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4ddd-142">INPUTS</span></span>

### <span data-ttu-id="f4ddd-143">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="f4ddd-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f4ddd-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f4ddd-144">System.String</span></span>

## <span data-ttu-id="f4ddd-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4ddd-145">OUTPUTS</span></span>

### <span data-ttu-id="f4ddd-146">Microsoft. Azure. Commands. Management. IotHub. modeller. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="f4ddd-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="f4ddd-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4ddd-147">NOTES</span></span>

## <span data-ttu-id="f4ddd-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4ddd-148">RELATED LINKS</span></span>
