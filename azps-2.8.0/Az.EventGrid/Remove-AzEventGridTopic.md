---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: 3cc0d587713bf287d9cc3bfa720d867e81370a8f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751988"
---
# <span data-ttu-id="5941b-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="5941b-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="5941b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5941b-102">SYNOPSIS</span></span>
<span data-ttu-id="5941b-103">Bir Azure olay Kılavuzu konusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5941b-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="5941b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5941b-104">SYNTAX</span></span>

### <span data-ttu-id="5941b-105">TopicNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5941b-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5941b-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="5941b-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5941b-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5941b-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5941b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5941b-108">DESCRIPTION</span></span>
<span data-ttu-id="5941b-109">Bir Azure olay Kılavuzu konusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5941b-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="5941b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5941b-110">EXAMPLES</span></span>

### <span data-ttu-id="5941b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5941b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="5941b-112">\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunu kaldırır \` \` .</span><span class="sxs-lookup"><span data-stu-id="5941b-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5941b-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5941b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="5941b-114">\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunu kaldırır \` \` .</span><span class="sxs-lookup"><span data-stu-id="5941b-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="5941b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5941b-115">PARAMETERS</span></span>

### <span data-ttu-id="5941b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5941b-116">-DefaultProfile</span></span>
<span data-ttu-id="5941b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5941b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5941b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5941b-118">-InputObject</span></span>
<span data-ttu-id="5941b-119">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5941b-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5941b-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="5941b-120">-Name</span></span>
<span data-ttu-id="5941b-121">EventGrid konu adı.</span><span class="sxs-lookup"><span data-stu-id="5941b-121">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5941b-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5941b-122">-PassThru</span></span>
<span data-ttu-id="5941b-123">Kaldırma işleminin durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="5941b-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="5941b-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="5941b-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5941b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5941b-125">-ResourceGroupName</span></span>
<span data-ttu-id="5941b-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5941b-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5941b-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5941b-127">-ResourceId</span></span>
<span data-ttu-id="5941b-128">EventGrid konu RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="5941b-128">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5941b-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="5941b-129">-Confirm</span></span>
<span data-ttu-id="5941b-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5941b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5941b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5941b-131">-WhatIf</span></span>
<span data-ttu-id="5941b-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5941b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5941b-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5941b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5941b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5941b-134">CommonParameters</span></span>
<span data-ttu-id="5941b-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5941b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5941b-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5941b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5941b-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5941b-137">INPUTS</span></span>

### <span data-ttu-id="5941b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5941b-138">System.String</span></span>

### <span data-ttu-id="5941b-139">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="5941b-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="5941b-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5941b-140">OUTPUTS</span></span>

### <span data-ttu-id="5941b-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5941b-141">System.Boolean</span></span>

## <span data-ttu-id="5941b-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5941b-142">NOTES</span></span>

## <span data-ttu-id="5941b-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5941b-143">RELATED LINKS</span></span>
