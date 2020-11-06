---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/set-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
ms.openlocfilehash: 384c05e6424ab7b8d4fbb01a0c4822b73702c419
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590934"
---
# <span data-ttu-id="16ab2-101">Set-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="16ab2-101">Set-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="16ab2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16ab2-102">SYNOPSIS</span></span>
<span data-ttu-id="16ab2-103">Bir olay Kılavuzu konusunun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="16ab2-103">Sets the properties of an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16ab2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16ab2-104">SYNTAX</span></span>

### <span data-ttu-id="16ab2-105">TopicNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="16ab2-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16ab2-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="16ab2-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16ab2-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16ab2-107">TopicInputObjectParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16ab2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="16ab2-108">DESCRIPTION</span></span>
<span data-ttu-id="16ab2-109">Bir olay Kılavuzu konusunun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="16ab2-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="16ab2-110">Bu, bir olay Kılavuzu konusunun etiketlerinin yerini değiştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="16ab2-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="16ab2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16ab2-111">EXAMPLES</span></span>

### <span data-ttu-id="16ab2-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="16ab2-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="16ab2-113">\` \` \` \` Etiketleri belirtilen etiketlerle değiştirmek için myresourcegroupname kaynak grubundaki konu1 olay Kılavuzu konusunun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="16ab2-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="16ab2-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16ab2-114">PARAMETERS</span></span>

### <span data-ttu-id="16ab2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ab2-115">-DefaultProfile</span></span>
<span data-ttu-id="16ab2-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="16ab2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16ab2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16ab2-117">-InputObject</span></span>
<span data-ttu-id="16ab2-118">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="16ab2-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="16ab2-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="16ab2-119">-Name</span></span>
<span data-ttu-id="16ab2-120">EventGrid konu adı.</span><span class="sxs-lookup"><span data-stu-id="16ab2-120">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="16ab2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16ab2-121">-ResourceGroupName</span></span>
<span data-ttu-id="16ab2-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="16ab2-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="16ab2-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="16ab2-123">-ResourceId</span></span>
<span data-ttu-id="16ab2-124">EventGrid konu RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="16ab2-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="16ab2-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="16ab2-125">-Tag</span></span>
<span data-ttu-id="16ab2-126">Kaynak etiketini temsil eden hashtables 'lar.</span><span class="sxs-lookup"><span data-stu-id="16ab2-126">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="16ab2-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="16ab2-127">-Confirm</span></span>
<span data-ttu-id="16ab2-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="16ab2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16ab2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16ab2-129">-WhatIf</span></span>
<span data-ttu-id="16ab2-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="16ab2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16ab2-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="16ab2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16ab2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ab2-132">CommonParameters</span></span>
<span data-ttu-id="16ab2-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16ab2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ab2-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16ab2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ab2-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16ab2-135">INPUTS</span></span>

### <span data-ttu-id="16ab2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="16ab2-136">System.String</span></span>

### <span data-ttu-id="16ab2-137">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="16ab2-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="16ab2-138">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="16ab2-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="16ab2-139">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="16ab2-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="16ab2-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16ab2-140">OUTPUTS</span></span>

### <span data-ttu-id="16ab2-141">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="16ab2-141">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="16ab2-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16ab2-142">NOTES</span></span>

## <span data-ttu-id="16ab2-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16ab2-143">RELATED LINKS</span></span>
