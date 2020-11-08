---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 04c65bf74d6c32dcaf93d2183936f9c0980aae4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277776"
---
# <span data-ttu-id="a1899-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a1899-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="a1899-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1899-102">SYNOPSIS</span></span>
<span data-ttu-id="a1899-103">IoT Hub 'ındaki seçili uç noktalar için bir ileti zenginleştirme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1899-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="a1899-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1899-104">SYNTAX</span></span>

### <span data-ttu-id="a1899-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a1899-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1899-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="a1899-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1899-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="a1899-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1899-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1899-108">DESCRIPTION</span></span>
<span data-ttu-id="a1899-109">IoT Hub 'a kadar en çok 10 ileti zenginleştirme.</span><span class="sxs-lookup"><span data-stu-id="a1899-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="a1899-110">Bunlar, seçilen uç noktalara gönderilen iletilere uygulama özellikleri olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="a1899-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="a1899-111">Daha fazla bilgi için bkz. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="a1899-111">To know more, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="a1899-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1899-112">EXAMPLES</span></span>

### <span data-ttu-id="a1899-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a1899-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="a1899-114">"Yenianahtar" ve "YeniDeğer" değerlerini içeren yeni bir zenginleştirme ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a1899-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="a1899-115">Bu yeni zenginleştirme, "endpoint1" ve "endpoint2" uç noktalarına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="a1899-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="a1899-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1899-116">PARAMETERS</span></span>

### <span data-ttu-id="a1899-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1899-117">-DefaultProfile</span></span>
<span data-ttu-id="a1899-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a1899-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1899-119">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="a1899-119">-Endpoint</span></span>
<span data-ttu-id="a1899-120">Endın 'a uygulanacak uç nokta.</span><span class="sxs-lookup"><span data-stu-id="a1899-120">Endpoint(s) to apply enrichments to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1899-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1899-121">-InputObject</span></span>
<span data-ttu-id="a1899-122">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="a1899-122">IotHub object</span></span>

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

### <span data-ttu-id="a1899-123">-Tuşlu</span><span class="sxs-lookup"><span data-stu-id="a1899-123">-Key</span></span>
<span data-ttu-id="a1899-124">Zenginleştirme tuşu.</span><span class="sxs-lookup"><span data-stu-id="a1899-124">The enrichment's key.</span></span>

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

### <span data-ttu-id="a1899-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="a1899-125">-Name</span></span>
<span data-ttu-id="a1899-126">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="a1899-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a1899-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1899-127">-ResourceGroupName</span></span>
<span data-ttu-id="a1899-128">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="a1899-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a1899-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a1899-129">-ResourceId</span></span>
<span data-ttu-id="a1899-130">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="a1899-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a1899-131">-Değer</span><span class="sxs-lookup"><span data-stu-id="a1899-131">-Value</span></span>
<span data-ttu-id="a1899-132">Enrichment değeri.</span><span class="sxs-lookup"><span data-stu-id="a1899-132">The enrichment's value.</span></span>

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

### <span data-ttu-id="a1899-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="a1899-133">-Confirm</span></span>
<span data-ttu-id="a1899-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a1899-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1899-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1899-135">-WhatIf</span></span>
<span data-ttu-id="a1899-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a1899-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1899-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a1899-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1899-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1899-138">CommonParameters</span></span>
<span data-ttu-id="a1899-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1899-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1899-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1899-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1899-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1899-141">INPUTS</span></span>

### <span data-ttu-id="a1899-142">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="a1899-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a1899-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a1899-143">System.String</span></span>

## <span data-ttu-id="a1899-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1899-144">OUTPUTS</span></span>

### <span data-ttu-id="a1899-145">Microsoft. Azure. Commands. Management. IotHub. modeller. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="a1899-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="a1899-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1899-146">NOTES</span></span>

## <span data-ttu-id="a1899-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1899-147">RELATED LINKS</span></span>
