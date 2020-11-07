---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: 2e2abe03d0df4ccf662f99945c45e837669a1de9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751990"
---
# <span data-ttu-id="a7593-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a7593-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="a7593-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7593-102">SYNOPSIS</span></span>
<span data-ttu-id="a7593-103">Azure olay Kılavuzu olay aboneliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a7593-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="a7593-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7593-104">SYNTAX</span></span>

### <span data-ttu-id="a7593-105">ResourceGroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a7593-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7593-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7593-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7593-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7593-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7593-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7593-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7593-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7593-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7593-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7593-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7593-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7593-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7593-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7593-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7593-113">EtkiAlanıA</span><span class="sxs-lookup"><span data-stu-id="a7593-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7593-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7593-114">DESCRIPTION</span></span>
<span data-ttu-id="a7593-115">Azure olay Kılavuzu konusu, kaynak, Azure aboneliği veya kaynak grubu için bir Azure olay Kılavuzu olay aboneliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a7593-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="a7593-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7593-116">EXAMPLES</span></span>

### <span data-ttu-id="a7593-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a7593-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a7593-118">Olay aboneliği EventSubscription1, \` \` \` \` myresourcegroupname kaynak grubundaki bir Azure olay kılavuzu konusuna konu1 \` \` .</span><span class="sxs-lookup"><span data-stu-id="a7593-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a7593-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a7593-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a7593-120">Olay aboneliği \` EventSubscription1 \` myresourcegroupname kaynak grubuna kaldırır \` \` .</span><span class="sxs-lookup"><span data-stu-id="a7593-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a7593-121">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="a7593-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a7593-122">Olay aboneliği EventSubscription1 ' \` nu \` varsayılan Azure aboneliği 'ne kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a7593-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="a7593-123">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="a7593-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a7593-124">Olay aboneliği \` EventSubscription1 \` bir olay hub ad alanına kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a7593-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="a7593-125">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="a7593-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a7593-126">Olay aboneliği \` EventSubscription1 \` bir olay kılavuzu konusuna kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a7593-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="a7593-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7593-127">PARAMETERS</span></span>

### <span data-ttu-id="a7593-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7593-128">-DefaultProfile</span></span>
<span data-ttu-id="a7593-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a7593-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7593-130">-Domainınputobject</span><span class="sxs-lookup"><span data-stu-id="a7593-130">-DomainInputObject</span></span>
<span data-ttu-id="a7593-131">Olay Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="a7593-131">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7593-132">-EtkiAlanıAdı</span><span class="sxs-lookup"><span data-stu-id="a7593-132">-DomainName</span></span>
<span data-ttu-id="a7593-133">EventGrid etki alanı adı.</span><span class="sxs-lookup"><span data-stu-id="a7593-133">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7593-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="a7593-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="a7593-135">EventGrid etki alanı konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a7593-135">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7593-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="a7593-136">-DomainTopicName</span></span>
<span data-ttu-id="a7593-137">EventGrid etki alanı konu adı.</span><span class="sxs-lookup"><span data-stu-id="a7593-137">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7593-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a7593-138">-EventSubscriptionName</span></span>
<span data-ttu-id="a7593-139">Kaldırılması gereken olay aboneliğinin adı.</span><span class="sxs-lookup"><span data-stu-id="a7593-139">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet, DomainNameParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7593-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7593-140">-InputObject</span></span>
<span data-ttu-id="a7593-141">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a7593-141">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="a7593-142">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a7593-142">-PassThru</span></span>
<span data-ttu-id="a7593-143">Kaldırma işleminin durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="a7593-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="a7593-144">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a7593-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a7593-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7593-145">-ResourceGroupName</span></span>
<span data-ttu-id="a7593-146">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a7593-146">Resource Group Name.</span></span>

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
Parameter Sets: TopicNameParameterSet, DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7593-147">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a7593-147">-ResourceId</span></span>
<span data-ttu-id="a7593-148">Olay aboneliğinin kaldırılması gereken kaynağın tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="a7593-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="a7593-149">-TopicName</span><span class="sxs-lookup"><span data-stu-id="a7593-149">-TopicName</span></span>
<span data-ttu-id="a7593-150">Olay Kılavuzu konu adı.</span><span class="sxs-lookup"><span data-stu-id="a7593-150">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="a7593-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="a7593-151">-Confirm</span></span>
<span data-ttu-id="a7593-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a7593-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7593-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7593-153">-WhatIf</span></span>
<span data-ttu-id="a7593-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a7593-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7593-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a7593-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7593-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7593-156">CommonParameters</span></span>
<span data-ttu-id="a7593-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7593-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7593-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7593-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7593-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7593-159">INPUTS</span></span>

### <span data-ttu-id="a7593-160">System. String</span><span class="sxs-lookup"><span data-stu-id="a7593-160">System.String</span></span>

### <span data-ttu-id="a7593-161">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="a7593-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="a7593-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="a7593-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="a7593-163">Microsoft.Azure.Commands.EventGrid.Models.PSDOmainkonu başlığı</span><span class="sxs-lookup"><span data-stu-id="a7593-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="a7593-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7593-164">OUTPUTS</span></span>

### <span data-ttu-id="a7593-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a7593-165">System.Boolean</span></span>

## <span data-ttu-id="a7593-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7593-166">NOTES</span></span>

## <span data-ttu-id="a7593-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7593-167">RELATED LINKS</span></span>