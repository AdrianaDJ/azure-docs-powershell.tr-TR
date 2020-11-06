---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/remove-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
ms.openlocfilehash: d853d5d4659e41c9696ab87c3f9ab8b58c240044
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590935"
---
# <span data-ttu-id="eb326-101">Remove-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="eb326-101">Remove-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="eb326-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb326-102">SYNOPSIS</span></span>
<span data-ttu-id="eb326-103">Bir Azure olay Kılavuzu konusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="eb326-103">Removes an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb326-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eb326-104">SYNTAX</span></span>

### <span data-ttu-id="eb326-105">TopicNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eb326-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb326-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb326-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb326-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb326-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb326-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="eb326-108">DESCRIPTION</span></span>
<span data-ttu-id="eb326-109">Bir Azure olay Kılavuzu konusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="eb326-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="eb326-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eb326-110">EXAMPLES</span></span>

### <span data-ttu-id="eb326-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="eb326-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="eb326-112">\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunu kaldırır \` \` .</span><span class="sxs-lookup"><span data-stu-id="eb326-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="eb326-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="eb326-113">Example 2</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzureRmEventGridTopic
```

<span data-ttu-id="eb326-114">\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunu kaldırır \` \` .</span><span class="sxs-lookup"><span data-stu-id="eb326-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="eb326-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eb326-115">PARAMETERS</span></span>

### <span data-ttu-id="eb326-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb326-116">-DefaultProfile</span></span>
<span data-ttu-id="eb326-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="eb326-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb326-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb326-118">-InputObject</span></span>
<span data-ttu-id="eb326-119">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="eb326-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="eb326-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="eb326-120">-Name</span></span>
<span data-ttu-id="eb326-121">EventGrid konu adı.</span><span class="sxs-lookup"><span data-stu-id="eb326-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="eb326-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="eb326-122">-PassThru</span></span>
<span data-ttu-id="eb326-123">Kaldırma işleminin durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="eb326-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="eb326-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="eb326-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="eb326-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb326-125">-ResourceGroupName</span></span>
<span data-ttu-id="eb326-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="eb326-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="eb326-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="eb326-127">-ResourceId</span></span>
<span data-ttu-id="eb326-128">EventGrid konu RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="eb326-128">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="eb326-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="eb326-129">-Confirm</span></span>
<span data-ttu-id="eb326-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eb326-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb326-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb326-131">-WhatIf</span></span>
<span data-ttu-id="eb326-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eb326-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb326-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eb326-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb326-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb326-134">CommonParameters</span></span>
<span data-ttu-id="eb326-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eb326-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb326-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb326-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb326-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eb326-137">INPUTS</span></span>

### <span data-ttu-id="eb326-138">System. String</span><span class="sxs-lookup"><span data-stu-id="eb326-138">System.String</span></span>

### <span data-ttu-id="eb326-139">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="eb326-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="eb326-140">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="eb326-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="eb326-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eb326-141">OUTPUTS</span></span>

### <span data-ttu-id="eb326-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eb326-142">System.Boolean</span></span>

## <span data-ttu-id="eb326-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eb326-143">NOTES</span></span>

## <span data-ttu-id="eb326-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eb326-144">RELATED LINKS</span></span>
