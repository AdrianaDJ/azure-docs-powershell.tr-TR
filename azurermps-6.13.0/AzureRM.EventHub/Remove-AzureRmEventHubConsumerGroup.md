---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 2ef6227acf398b228d6ca5ffe4fad3d39ec75723
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590305"
---
# <span data-ttu-id="2ba24-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="2ba24-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="2ba24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ba24-102">SYNOPSIS</span></span>
<span data-ttu-id="2ba24-103">Belirtilen olay hub 'ı tüketici grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="2ba24-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ba24-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ba24-104">SYNTAX</span></span>

### <span data-ttu-id="2ba24-105">ConsumergroupPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2ba24-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ba24-106">Consumergroupınputobjectset</span><span class="sxs-lookup"><span data-stu-id="2ba24-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzureRmEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ba24-107">Consumergroupresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="2ba24-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ba24-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ba24-108">DESCRIPTION</span></span>
<span data-ttu-id="2ba24-109">Remove-AzureRmEventHubConsumerGroup cmdlet 'i, verilen olay hub 'ından belirtilen tüketici grubunu kaldırır ve siler.</span><span class="sxs-lookup"><span data-stu-id="2ba24-109">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="2ba24-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ba24-110">EXAMPLES</span></span>

### <span data-ttu-id="2ba24-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2ba24-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="2ba24-112">\`Myconsumergroupname adlı tüketici grubunu, \` kapsam dışı \` \` olarak \` mynamespacename \` ad alanına siler.</span><span class="sxs-lookup"><span data-stu-id="2ba24-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="2ba24-113">Örnek 2,1-InputObject-değişken kullanma</span><span class="sxs-lookup"><span data-stu-id="2ba24-113">Example 2.1 - InputObject - Using Variable</span></span>
```
PS C:\> $inputobject = Get-AzureRmEventHubConsumerGroup <params>
PS C:\> Remove-AzureRmEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="2ba24-114">Örnek 2,2-InputObject-boru kullanarak</span><span class="sxs-lookup"><span data-stu-id="2ba24-114">Example 2.2 - InputObject - Using Piping</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup <params> | Remove-AzureRmEventHubConsumerGroup
```

### <span data-ttu-id="2ba24-115">Örnek 3,1-</span><span class="sxs-lookup"><span data-stu-id="2ba24-115">Example 3.1 - ResourceId Using Vairable</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHubConsumerGroup <params>
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="2ba24-116">Örnek 3,2-dize kullanarak RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2ba24-116">Example 3.2 - ResourceId Using string</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="2ba24-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ba24-117">PARAMETERS</span></span>

### <span data-ttu-id="2ba24-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="2ba24-118">-AsJob</span></span>
<span data-ttu-id="2ba24-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2ba24-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ba24-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ba24-120">-DefaultProfile</span></span>
<span data-ttu-id="2ba24-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ba24-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ba24-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="2ba24-122">-EventHub</span></span>
<span data-ttu-id="2ba24-123">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="2ba24-123">EventHub Name</span></span>

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

### <span data-ttu-id="2ba24-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ba24-124">-InputObject</span></span>
<span data-ttu-id="2ba24-125">ConsumerGroup nesnesi</span><span class="sxs-lookup"><span data-stu-id="2ba24-125">ConsumerGroup Object</span></span>

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

### <span data-ttu-id="2ba24-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="2ba24-126">-Name</span></span>
<span data-ttu-id="2ba24-127">ConsumerGroup adı</span><span class="sxs-lookup"><span data-stu-id="2ba24-127">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="2ba24-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2ba24-128">-Namespace</span></span>
<span data-ttu-id="2ba24-129">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="2ba24-129">Namespace Name</span></span>

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

### <span data-ttu-id="2ba24-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2ba24-130">-PassThru</span></span>
<span data-ttu-id="2ba24-131">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="2ba24-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="2ba24-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ba24-132">-ResourceGroupName</span></span>
<span data-ttu-id="2ba24-133">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="2ba24-133">Resource Group Name</span></span>

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

### <span data-ttu-id="2ba24-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2ba24-134">-ResourceId</span></span>
<span data-ttu-id="2ba24-135">ConsumerGroup kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="2ba24-135">ConsumerGroup Resource Id</span></span>

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

### <span data-ttu-id="2ba24-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="2ba24-136">-Confirm</span></span>
<span data-ttu-id="2ba24-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2ba24-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ba24-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ba24-138">-WhatIf</span></span>
<span data-ttu-id="2ba24-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ba24-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ba24-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2ba24-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ba24-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ba24-141">CommonParameters</span></span>
<span data-ttu-id="2ba24-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ba24-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ba24-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ba24-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ba24-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ba24-144">INPUTS</span></span>

### <span data-ttu-id="2ba24-145">System. String</span><span class="sxs-lookup"><span data-stu-id="2ba24-145">System.String</span></span>

### <span data-ttu-id="2ba24-146">Microsoft. Azure. Commands. EventHub. modeller. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="2ba24-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>
<span data-ttu-id="2ba24-147">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2ba24-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2ba24-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ba24-148">OUTPUTS</span></span>

### <span data-ttu-id="2ba24-149">System. void</span><span class="sxs-lookup"><span data-stu-id="2ba24-149">System.Void</span></span>

## <span data-ttu-id="2ba24-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ba24-150">NOTES</span></span>

## <span data-ttu-id="2ba24-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ba24-151">RELATED LINKS</span></span>
