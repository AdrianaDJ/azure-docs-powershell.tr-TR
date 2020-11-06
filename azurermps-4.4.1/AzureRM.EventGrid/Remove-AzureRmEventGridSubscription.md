---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
ms.openlocfilehash: a15cb222108d79544d38ce730897e03fa61066ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594724"
---
# <span data-ttu-id="a9ee0-101">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a9ee0-101">Remove-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="a9ee0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9ee0-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ee0-103">Azure olay Kılavuzu olay aboneliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a9ee0-103">Removes an Azure Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9ee0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9ee0-104">SYNTAX</span></span>

### <span data-ttu-id="a9ee0-105">ResourceGroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a9ee0-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9ee0-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9ee0-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9ee0-107">Eventsubscriptionınputobjectset</span><span class="sxs-lookup"><span data-stu-id="a9ee0-107">EventSubscriptionInputObjectSet</span></span>
```
Remove-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9ee0-108">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9ee0-108">TopicNameParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9ee0-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9ee0-109">DESCRIPTION</span></span>
<span data-ttu-id="a9ee0-110">Azure olay Kılavuzu konusu, kaynak, Azure aboneliği veya kaynak grubu için bir Azure olay Kılavuzu olay aboneliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a9ee0-110">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="a9ee0-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9ee0-111">EXAMPLES</span></span>

### <span data-ttu-id="a9ee0-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a9ee0-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a9ee0-113">Olay aboneliği EventSubscription1, \` \` \` \` myresourcegroupname kaynak grubundaki bir Azure olay kılavuzu konusuna konu1 \` \` .</span><span class="sxs-lookup"><span data-stu-id="a9ee0-113">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a9ee0-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a9ee0-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a9ee0-115">Olay aboneliği \` EventSubscription1 \` myresourcegroupname kaynak grubuna kaldırır \` \` .</span><span class="sxs-lookup"><span data-stu-id="a9ee0-115">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a9ee0-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="a9ee0-116">Example 3</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a9ee0-117">Olay aboneliği EventSubscription1 ' \` nu \` varsayılan Azure aboneliği 'ne kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a9ee0-117">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="a9ee0-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="a9ee0-118">Example 4</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a9ee0-119">Olay aboneliği \` EventSubscription1 \` bir olay hub ad alanına kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a9ee0-119">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="a9ee0-120">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="a9ee0-120">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a9ee0-121">Olay aboneliği \` EventSubscription1 \` bir olay kılavuzu konusuna kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a9ee0-121">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="a9ee0-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9ee0-122">PARAMETERS</span></span>

### <span data-ttu-id="a9ee0-123">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a9ee0-123">-EventSubscriptionName</span></span>
<span data-ttu-id="a9ee0-124">Kaldırılması gereken olay aboneliğinin adı.</span><span class="sxs-lookup"><span data-stu-id="a9ee0-124">Name of the event subscription that needs to be removed.</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9ee0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9ee0-125">-InputObject</span></span>
<span data-ttu-id="a9ee0-126">EventGrid Olayaboneliği nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a9ee0-126">EventGrid EventSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9ee0-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a9ee0-127">-PassThru</span></span>
<span data-ttu-id="a9ee0-128">Kaldırma işleminin durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="a9ee0-128">Returns the status of the Remove operation.</span></span> <span data-ttu-id="a9ee0-129">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a9ee0-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a9ee0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9ee0-130">-ResourceGroupName</span></span>
<span data-ttu-id="a9ee0-131">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a9ee0-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="a9ee0-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a9ee0-132">-ResourceId</span></span>
<span data-ttu-id="a9ee0-133">Olay aboneliğinin kaldırılması gereken kaynağın tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="a9ee0-133">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="a9ee0-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="a9ee0-134">-TopicName</span></span>
<span data-ttu-id="a9ee0-135">Olay Kılavuzu konu adı.</span><span class="sxs-lookup"><span data-stu-id="a9ee0-135">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="a9ee0-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="a9ee0-136">-Confirm</span></span>
<span data-ttu-id="a9ee0-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a9ee0-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9ee0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9ee0-138">-WhatIf</span></span>
<span data-ttu-id="a9ee0-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9ee0-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9ee0-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a9ee0-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9ee0-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9ee0-141">-DefaultProfile</span></span>
<span data-ttu-id="a9ee0-142">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9ee0-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9ee0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ee0-143">CommonParameters</span></span>
<span data-ttu-id="a9ee0-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9ee0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ee0-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9ee0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ee0-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9ee0-146">INPUTS</span></span>

### <span data-ttu-id="a9ee0-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a9ee0-147">System.String</span></span>
<span data-ttu-id="a9ee0-148">Microsoft. Azure. Commands. EventGrid. modeller. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="a9ee0-148">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="a9ee0-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9ee0-149">OUTPUTS</span></span>

### <span data-ttu-id="a9ee0-150">System. Object</span><span class="sxs-lookup"><span data-stu-id="a9ee0-150">System.Object</span></span>

## <span data-ttu-id="a9ee0-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9ee0-151">NOTES</span></span>

## <span data-ttu-id="a9ee0-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9ee0-152">RELATED LINKS</span></span>

