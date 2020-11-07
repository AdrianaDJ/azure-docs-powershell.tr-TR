---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: fd872830f82f1d75f0b3c5f60ba6b129d7edd6f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760866"
---
# <span data-ttu-id="7362c-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7362c-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="7362c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7362c-102">SYNOPSIS</span></span>
<span data-ttu-id="7362c-103">Azure olay Kılavuzu olay aboneliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7362c-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="7362c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7362c-104">SYNTAX</span></span>

### <span data-ttu-id="7362c-105">ResourceGroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7362c-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7362c-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7362c-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7362c-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7362c-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7362c-108">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7362c-108">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7362c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="7362c-109">DESCRIPTION</span></span>
<span data-ttu-id="7362c-110">Azure olay Kılavuzu konusu, kaynak, Azure aboneliği veya kaynak grubu için bir Azure olay Kılavuzu olay aboneliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7362c-110">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="7362c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7362c-111">EXAMPLES</span></span>

### <span data-ttu-id="7362c-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7362c-112">Example 1</span></span>
```
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7362c-113">Olay aboneliği EventSubscription1, \` \` \` \` myresourcegroupname kaynak grubundaki bir Azure olay kılavuzu konusuna konu1 \` \` .</span><span class="sxs-lookup"><span data-stu-id="7362c-113">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7362c-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7362c-114">Example 2</span></span>
```
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7362c-115">Olay aboneliği \` EventSubscription1 \` myresourcegroupname kaynak grubuna kaldırır \` \` .</span><span class="sxs-lookup"><span data-stu-id="7362c-115">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7362c-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="7362c-116">Example 3</span></span>
```
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7362c-117">Olay aboneliği EventSubscription1 ' \` nu \` varsayılan Azure aboneliği 'ne kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7362c-117">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="7362c-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="7362c-118">Example 4</span></span>
```
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7362c-119">Olay aboneliği \` EventSubscription1 \` bir olay hub ad alanına kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7362c-119">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="7362c-120">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="7362c-120">Example 5</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7362c-121">Olay aboneliği \` EventSubscription1 \` bir olay kılavuzu konusuna kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7362c-121">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="7362c-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7362c-122">PARAMETERS</span></span>

### <span data-ttu-id="7362c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7362c-123">-DefaultProfile</span></span>
<span data-ttu-id="7362c-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7362c-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7362c-125">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="7362c-125">-EventSubscriptionName</span></span>
<span data-ttu-id="7362c-126">Kaldırılması gereken olay aboneliğinin adı.</span><span class="sxs-lookup"><span data-stu-id="7362c-126">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7362c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7362c-127">-InputObject</span></span>
<span data-ttu-id="7362c-128">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7362c-128">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7362c-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7362c-129">-PassThru</span></span>
<span data-ttu-id="7362c-130">Kaldırma işleminin durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="7362c-130">Returns the status of the Remove operation.</span></span> <span data-ttu-id="7362c-131">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="7362c-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7362c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7362c-132">-ResourceGroupName</span></span>
<span data-ttu-id="7362c-133">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7362c-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7362c-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7362c-134">-ResourceId</span></span>
<span data-ttu-id="7362c-135">Olay aboneliğinin kaldırılması gereken kaynağın tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="7362c-135">Identifier of the resource whose event subscription needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7362c-136">-TopicName</span><span class="sxs-lookup"><span data-stu-id="7362c-136">-TopicName</span></span>
<span data-ttu-id="7362c-137">Olay Kılavuzu konu adı.</span><span class="sxs-lookup"><span data-stu-id="7362c-137">Event Grid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7362c-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="7362c-138">-Confirm</span></span>
<span data-ttu-id="7362c-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7362c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7362c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7362c-140">-WhatIf</span></span>
<span data-ttu-id="7362c-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7362c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7362c-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7362c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7362c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7362c-143">CommonParameters</span></span>
<span data-ttu-id="7362c-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7362c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7362c-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7362c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7362c-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7362c-146">INPUTS</span></span>

### <span data-ttu-id="7362c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="7362c-147">System.String</span></span>

### <span data-ttu-id="7362c-148">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="7362c-148">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="7362c-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7362c-149">OUTPUTS</span></span>

### <span data-ttu-id="7362c-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7362c-150">System.Boolean</span></span>

## <span data-ttu-id="7362c-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7362c-151">NOTES</span></span>

## <span data-ttu-id="7362c-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7362c-152">RELATED LINKS</span></span>
