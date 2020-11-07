---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: f27533a36314ae2b31cd0055e8cc17027c95016a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751985"
---
# <span data-ttu-id="2be18-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="2be18-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="2be18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2be18-102">SYNOPSIS</span></span>
<span data-ttu-id="2be18-103">Bir olay Kılavuzu konusunun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2be18-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="2be18-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2be18-104">SYNTAX</span></span>

### <span data-ttu-id="2be18-105">TopicNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2be18-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2be18-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2be18-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2be18-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2be18-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2be18-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2be18-108">DESCRIPTION</span></span>
<span data-ttu-id="2be18-109">Bir olay Kılavuzu konusunun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2be18-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="2be18-110">Bu, bir olay Kılavuzu konusunun etiketlerinin yerini değiştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2be18-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="2be18-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2be18-111">EXAMPLES</span></span>

### <span data-ttu-id="2be18-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2be18-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="2be18-113">\` \` \` \` Etiketleri belirtilen etiketlerle değiştirmek için myresourcegroupname kaynak grubundaki konu1 olay Kılavuzu konusunun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2be18-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="2be18-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2be18-114">PARAMETERS</span></span>

### <span data-ttu-id="2be18-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2be18-115">-DefaultProfile</span></span>
<span data-ttu-id="2be18-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2be18-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2be18-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2be18-117">-InputObject</span></span>
<span data-ttu-id="2be18-118">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2be18-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="2be18-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="2be18-119">-Name</span></span>
<span data-ttu-id="2be18-120">EventGrid konu adı.</span><span class="sxs-lookup"><span data-stu-id="2be18-120">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="2be18-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2be18-121">-ResourceGroupName</span></span>
<span data-ttu-id="2be18-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2be18-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="2be18-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2be18-123">-ResourceId</span></span>
<span data-ttu-id="2be18-124">EventGrid konu RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="2be18-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="2be18-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2be18-125">-Tag</span></span>
<span data-ttu-id="2be18-126">Kaynak etiketini temsil eden hashtables 'lar.</span><span class="sxs-lookup"><span data-stu-id="2be18-126">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2be18-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="2be18-127">-Confirm</span></span>
<span data-ttu-id="2be18-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2be18-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2be18-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2be18-129">-WhatIf</span></span>
<span data-ttu-id="2be18-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2be18-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2be18-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2be18-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2be18-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2be18-132">CommonParameters</span></span>
<span data-ttu-id="2be18-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2be18-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2be18-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2be18-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2be18-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2be18-135">INPUTS</span></span>

### <span data-ttu-id="2be18-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2be18-136">System.String</span></span>

### <span data-ttu-id="2be18-137">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="2be18-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="2be18-138">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2be18-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2be18-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2be18-139">OUTPUTS</span></span>

### <span data-ttu-id="2be18-140">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="2be18-140">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="2be18-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2be18-141">NOTES</span></span>

## <span data-ttu-id="2be18-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2be18-142">RELATED LINKS</span></span>
