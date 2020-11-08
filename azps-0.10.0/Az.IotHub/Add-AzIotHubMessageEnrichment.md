---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: caae747f7accd76db1424d14274416f0de97122d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936709"
---
# <span data-ttu-id="b4bd8-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b4bd8-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="b4bd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="b4bd8-103">IoT Hub 'ındaki seçili uç noktalar için bir ileti zenginleştirme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4bd8-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="b4bd8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4bd8-104">SYNTAX</span></span>

### <span data-ttu-id="b4bd8-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4bd8-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4bd8-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="b4bd8-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4bd8-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="b4bd8-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4bd8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4bd8-108">DESCRIPTION</span></span>
<span data-ttu-id="b4bd8-109">IoT Hub 'a kadar en çok 10 ileti zenginleştirme.</span><span class="sxs-lookup"><span data-stu-id="b4bd8-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="b4bd8-110">Bunlar, seçilen uç noktalara gönderilen iletilere uygulama özellikleri olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="b4bd8-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="b4bd8-111">Daha fazla bilgi için bkz. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="b4bd8-111">To know more, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="b4bd8-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4bd8-112">EXAMPLES</span></span>

### <span data-ttu-id="b4bd8-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b4bd8-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="b4bd8-114">"Yenianahtar" ve "YeniDeğer" değerlerini içeren yeni bir zenginleştirme ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b4bd8-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="b4bd8-115">Bu yeni zenginleştirme, "endpoint1" ve "endpoint2" uç noktalarına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="b4bd8-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="b4bd8-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4bd8-116">PARAMETERS</span></span>

### <span data-ttu-id="b4bd8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4bd8-117">-DefaultProfile</span></span>
<span data-ttu-id="b4bd8-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4bd8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4bd8-119">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="b4bd8-119">-Endpoint</span></span>
<span data-ttu-id="b4bd8-120">Endın 'a uygulanacak uç nokta.</span><span class="sxs-lookup"><span data-stu-id="b4bd8-120">Endpoint(s) to apply enrichments to.</span></span>

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

### <span data-ttu-id="b4bd8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4bd8-121">-InputObject</span></span>
<span data-ttu-id="b4bd8-122">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="b4bd8-122">IotHub object</span></span>

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

### <span data-ttu-id="b4bd8-123">-Tuşlu</span><span class="sxs-lookup"><span data-stu-id="b4bd8-123">-Key</span></span>
<span data-ttu-id="b4bd8-124">Zenginleştirme tuşu.</span><span class="sxs-lookup"><span data-stu-id="b4bd8-124">The enrichment's key.</span></span>

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

### <span data-ttu-id="b4bd8-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="b4bd8-125">-Name</span></span>
<span data-ttu-id="b4bd8-126">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="b4bd8-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b4bd8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4bd8-127">-ResourceGroupName</span></span>
<span data-ttu-id="b4bd8-128">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="b4bd8-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b4bd8-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b4bd8-129">-ResourceId</span></span>
<span data-ttu-id="b4bd8-130">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="b4bd8-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b4bd8-131">-Değer</span><span class="sxs-lookup"><span data-stu-id="b4bd8-131">-Value</span></span>
<span data-ttu-id="b4bd8-132">Enrichment değeri.</span><span class="sxs-lookup"><span data-stu-id="b4bd8-132">The enrichment's value.</span></span>

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

### <span data-ttu-id="b4bd8-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="b4bd8-133">-Confirm</span></span>
<span data-ttu-id="b4bd8-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b4bd8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4bd8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4bd8-135">-WhatIf</span></span>
<span data-ttu-id="b4bd8-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4bd8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4bd8-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b4bd8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4bd8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4bd8-138">CommonParameters</span></span>
<span data-ttu-id="b4bd8-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4bd8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4bd8-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4bd8-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4bd8-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4bd8-141">INPUTS</span></span>

### <span data-ttu-id="b4bd8-142">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="b4bd8-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b4bd8-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b4bd8-143">System.String</span></span>

## <span data-ttu-id="b4bd8-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4bd8-144">OUTPUTS</span></span>

### <span data-ttu-id="b4bd8-145">Microsoft. Azure. Commands. Management. IotHub. modeller. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="b4bd8-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="b4bd8-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4bd8-146">NOTES</span></span>

## <span data-ttu-id="b4bd8-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4bd8-147">RELATED LINKS</span></span>