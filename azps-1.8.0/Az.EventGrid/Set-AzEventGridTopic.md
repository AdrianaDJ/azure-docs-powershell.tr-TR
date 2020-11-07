---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: bcba056777cd9a5eef42799b170c2dad69c8bbf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760863"
---
# <span data-ttu-id="92ea8-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="92ea8-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="92ea8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="92ea8-103">Bir olay Kılavuzu konusunun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="92ea8-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="92ea8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="92ea8-104">SYNTAX</span></span>

### <span data-ttu-id="92ea8-105">TopicNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="92ea8-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92ea8-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="92ea8-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92ea8-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92ea8-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92ea8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="92ea8-108">DESCRIPTION</span></span>
<span data-ttu-id="92ea8-109">Bir olay Kılavuzu konusunun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="92ea8-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="92ea8-110">Bu, bir olay Kılavuzu konusunun etiketlerinin yerini değiştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="92ea8-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="92ea8-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="92ea8-111">EXAMPLES</span></span>

### <span data-ttu-id="92ea8-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="92ea8-112">Example 1</span></span>
```
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="92ea8-113">\` \` \` \` Etiketleri belirtilen etiketlerle değiştirmek için myresourcegroupname kaynak grubundaki konu1 olay Kılavuzu konusunun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="92ea8-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="92ea8-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="92ea8-114">PARAMETERS</span></span>

### <span data-ttu-id="92ea8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92ea8-115">-DefaultProfile</span></span>
<span data-ttu-id="92ea8-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="92ea8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92ea8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92ea8-117">-InputObject</span></span>
<span data-ttu-id="92ea8-118">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="92ea8-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="92ea8-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="92ea8-119">-Name</span></span>
<span data-ttu-id="92ea8-120">EventGrid konu adı.</span><span class="sxs-lookup"><span data-stu-id="92ea8-120">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="92ea8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92ea8-121">-ResourceGroupName</span></span>
<span data-ttu-id="92ea8-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="92ea8-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="92ea8-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="92ea8-123">-ResourceId</span></span>
<span data-ttu-id="92ea8-124">EventGrid konu RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="92ea8-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="92ea8-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="92ea8-125">-Tag</span></span>
<span data-ttu-id="92ea8-126">Kaynak etiketini temsil eden hashtables 'lar.</span><span class="sxs-lookup"><span data-stu-id="92ea8-126">Hashtables which represents resource Tag.</span></span>

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

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92ea8-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="92ea8-127">-Confirm</span></span>
<span data-ttu-id="92ea8-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="92ea8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92ea8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92ea8-129">-WhatIf</span></span>
<span data-ttu-id="92ea8-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="92ea8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92ea8-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="92ea8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92ea8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92ea8-132">CommonParameters</span></span>
<span data-ttu-id="92ea8-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="92ea8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92ea8-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92ea8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92ea8-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="92ea8-135">INPUTS</span></span>

### <span data-ttu-id="92ea8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="92ea8-136">System.String</span></span>

### <span data-ttu-id="92ea8-137">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="92ea8-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="92ea8-138">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="92ea8-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="92ea8-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="92ea8-139">OUTPUTS</span></span>

### <span data-ttu-id="92ea8-140">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="92ea8-140">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="92ea8-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="92ea8-141">NOTES</span></span>

## <span data-ttu-id="92ea8-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="92ea8-142">RELATED LINKS</span></span>