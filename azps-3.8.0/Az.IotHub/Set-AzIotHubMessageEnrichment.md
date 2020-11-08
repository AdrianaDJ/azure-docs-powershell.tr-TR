---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 3420c4103f8e502b2d8ca208dd107ced629c0f3a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096878"
---
# <span data-ttu-id="66a3f-101">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="66a3f-101">Set-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="66a3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="66a3f-103">IoT merkeziniz içinde bir ileti zenginleştirme.</span><span class="sxs-lookup"><span data-stu-id="66a3f-103">Update a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="66a3f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66a3f-104">SYNTAX</span></span>

### <span data-ttu-id="66a3f-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="66a3f-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66a3f-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="66a3f-106">InputObjectSet</span></span>
```
Set-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66a3f-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="66a3f-107">ResourceIdSet</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> [-Value <String>] [-Endpoint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66a3f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="66a3f-108">DESCRIPTION</span></span>
<span data-ttu-id="66a3f-109">Azure IoT Hub 'ındaki ileti zenginleştirme hakkında ayrıntılı bir açıklama için bkz. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="66a3f-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="66a3f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66a3f-110">EXAMPLES</span></span>

### <span data-ttu-id="66a3f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="66a3f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "updatedValue"

Key         : newKey
Value       : updatedValue
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="66a3f-112">"Yenianahtar" anahtarının "updatedValue" şeklinde zenginleştirme değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="66a3f-112">Updates enrichment's value to "updatedValue" for the key "newKey".</span></span>
<span data-ttu-id="66a3f-113">Azure IoT Hub 'ındaki ileti zenginleştirme hakkında ayrıntılı bir açıklama için bkz. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="66a3f-113">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

### <span data-ttu-id="66a3f-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="66a3f-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Endpoint endpoint1,endpoint2,endpoint3

Key         : newKey
Value       : value1
Endpoint(s) : {endpoint1, endpoint2, endpoint3}
```

<span data-ttu-id="66a3f-115">"Yenianahtar" anahtarının "endpoint1, endpoint2, endpoint3" için zenginleştirme uç noktasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="66a3f-115">Updates enrichment's endpoint to "endpoint1, endpoint2, endpoint3" for the key "newKey".</span></span>
<span data-ttu-id="66a3f-116">Azure IoT Hub 'ındaki ileti zenginleştirme hakkında ayrıntılı bir açıklama için bkz. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="66a3f-116">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="66a3f-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66a3f-117">PARAMETERS</span></span>

### <span data-ttu-id="66a3f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a3f-118">-DefaultProfile</span></span>
<span data-ttu-id="66a3f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="66a3f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66a3f-120">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="66a3f-120">-Endpoint</span></span>
<span data-ttu-id="66a3f-121">Endın 'a uygulanacak uç nokta.</span><span class="sxs-lookup"><span data-stu-id="66a3f-121">Endpoint(s) to apply enrichments to.</span></span>

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

### <span data-ttu-id="66a3f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66a3f-122">-InputObject</span></span>
<span data-ttu-id="66a3f-123">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="66a3f-123">IotHub Object</span></span>

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

### <span data-ttu-id="66a3f-124">-Tuşlu</span><span class="sxs-lookup"><span data-stu-id="66a3f-124">-Key</span></span>
<span data-ttu-id="66a3f-125">Zenginleştirme tuşu.</span><span class="sxs-lookup"><span data-stu-id="66a3f-125">The enrichment's key.</span></span>

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

### <span data-ttu-id="66a3f-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="66a3f-126">-Name</span></span>
<span data-ttu-id="66a3f-127">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="66a3f-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="66a3f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66a3f-128">-ResourceGroupName</span></span>
<span data-ttu-id="66a3f-129">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="66a3f-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="66a3f-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="66a3f-130">-ResourceId</span></span>
<span data-ttu-id="66a3f-131">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="66a3f-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="66a3f-132">-Değer</span><span class="sxs-lookup"><span data-stu-id="66a3f-132">-Value</span></span>
<span data-ttu-id="66a3f-133">Enrichment değeri.</span><span class="sxs-lookup"><span data-stu-id="66a3f-133">The enrichment's value.</span></span>

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

### <span data-ttu-id="66a3f-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="66a3f-134">-Confirm</span></span>
<span data-ttu-id="66a3f-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="66a3f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66a3f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66a3f-136">-WhatIf</span></span>
<span data-ttu-id="66a3f-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="66a3f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66a3f-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="66a3f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66a3f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a3f-139">CommonParameters</span></span>
<span data-ttu-id="66a3f-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66a3f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a3f-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66a3f-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a3f-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66a3f-142">INPUTS</span></span>

### <span data-ttu-id="66a3f-143">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="66a3f-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="66a3f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="66a3f-144">System.String</span></span>

## <span data-ttu-id="66a3f-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66a3f-145">OUTPUTS</span></span>

### <span data-ttu-id="66a3f-146">Microsoft. Azure. Commands. Management. IotHub. modeller. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="66a3f-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="66a3f-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66a3f-147">NOTES</span></span>

## <span data-ttu-id="66a3f-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66a3f-148">RELATED LINKS</span></span>
