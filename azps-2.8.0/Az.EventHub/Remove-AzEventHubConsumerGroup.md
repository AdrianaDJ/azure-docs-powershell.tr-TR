---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
ms.openlocfilehash: 8cbfe51ac9c4a415672bc96e18e61f5a82a454cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751948"
---
# <span data-ttu-id="e4bb8-101">Remove-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="e4bb8-101">Remove-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="e4bb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4bb8-102">SYNOPSIS</span></span>
<span data-ttu-id="e4bb8-103">Belirtilen olay hub 'ı tüketici grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="e4bb8-103">Deletes the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="e4bb8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4bb8-104">SYNTAX</span></span>

### <span data-ttu-id="e4bb8-105">ConsumergroupPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e4bb8-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4bb8-106">Consumergroupınputobjectset</span><span class="sxs-lookup"><span data-stu-id="e4bb8-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4bb8-107">Consumergroupresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e4bb8-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4bb8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4bb8-108">DESCRIPTION</span></span>
<span data-ttu-id="e4bb8-109">Remove-AzEventHubConsumerGroup cmdlet 'i, verilen olay hub 'ından belirtilen tüketici grubunu kaldırır ve siler.</span><span class="sxs-lookup"><span data-stu-id="e4bb8-109">The Remove-AzEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="e4bb8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4bb8-110">EXAMPLES</span></span>

### <span data-ttu-id="e4bb8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e4bb8-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="e4bb8-112">\`Myconsumergroupname adlı tüketici grubunu, \` kapsam dışı \` \` olarak \` mynamespacename \` ad alanına siler.</span><span class="sxs-lookup"><span data-stu-id="e4bb8-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="e4bb8-113">Örnek 2,1-InputObject-değişken kullanma</span><span class="sxs-lookup"><span data-stu-id="e4bb8-113">Example 2.1 - InputObject - Using Variable</span></span>
```
PS C:\> $inputobject = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="e4bb8-114">Örnek 2,2-InputObject-boru kullanarak</span><span class="sxs-lookup"><span data-stu-id="e4bb8-114">Example 2.2 - InputObject - Using Piping</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup <params> | Remove-AzEventHubConsumerGroup
```

### <span data-ttu-id="e4bb8-115">Örnek 3,1-değişken kullanan RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e4bb8-115">Example 3.1 - ResourceId Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="e4bb8-116">Örnek 3,2-dize kullanarak RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e4bb8-116">Example 3.2 - ResourceId Using string</span></span>
```
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="e4bb8-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4bb8-117">PARAMETERS</span></span>

### <span data-ttu-id="e4bb8-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="e4bb8-118">-AsJob</span></span>
<span data-ttu-id="e4bb8-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e4bb8-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4bb8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4bb8-120">-DefaultProfile</span></span>
<span data-ttu-id="e4bb8-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e4bb8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4bb8-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="e4bb8-122">-EventHub</span></span>
<span data-ttu-id="e4bb8-123">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="e4bb8-123">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4bb8-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4bb8-124">-InputObject</span></span>
<span data-ttu-id="e4bb8-125">ConsumerGroup nesnesi</span><span class="sxs-lookup"><span data-stu-id="e4bb8-125">ConsumerGroup Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes
Parameter Sets: ConsumergroupInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4bb8-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="e4bb8-126">-Name</span></span>
<span data-ttu-id="e4bb8-127">ConsumerGroup adı</span><span class="sxs-lookup"><span data-stu-id="e4bb8-127">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4bb8-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e4bb8-128">-Namespace</span></span>
<span data-ttu-id="e4bb8-129">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="e4bb8-129">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4bb8-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e4bb8-130">-PassThru</span></span>
<span data-ttu-id="e4bb8-131">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="e4bb8-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="e4bb8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4bb8-132">-ResourceGroupName</span></span>
<span data-ttu-id="e4bb8-133">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="e4bb8-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4bb8-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e4bb8-134">-ResourceId</span></span>
<span data-ttu-id="e4bb8-135">ConsumerGroup kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="e4bb8-135">ConsumerGroup Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4bb8-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="e4bb8-136">-Confirm</span></span>
<span data-ttu-id="e4bb8-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e4bb8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4bb8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4bb8-138">-WhatIf</span></span>
<span data-ttu-id="e4bb8-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e4bb8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4bb8-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e4bb8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4bb8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4bb8-141">CommonParameters</span></span>
<span data-ttu-id="e4bb8-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4bb8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4bb8-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4bb8-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4bb8-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4bb8-144">INPUTS</span></span>

### <span data-ttu-id="e4bb8-145">System. String</span><span class="sxs-lookup"><span data-stu-id="e4bb8-145">System.String</span></span>

### <span data-ttu-id="e4bb8-146">Microsoft. Azure. Commands. EventHub. modeller. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="e4bb8-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="e4bb8-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4bb8-147">OUTPUTS</span></span>

### <span data-ttu-id="e4bb8-148">System. void</span><span class="sxs-lookup"><span data-stu-id="e4bb8-148">System.Void</span></span>

## <span data-ttu-id="e4bb8-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4bb8-149">NOTES</span></span>

## <span data-ttu-id="e4bb8-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4bb8-150">RELATED LINKS</span></span>
