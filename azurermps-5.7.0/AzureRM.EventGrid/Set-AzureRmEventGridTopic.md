---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/set-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
ms.openlocfilehash: c6a975ee5071ff3f31ae3daa0e6e9bf6ed9a42ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589800"
---
# <span data-ttu-id="87108-101">Set-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="87108-101">Set-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="87108-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87108-102">SYNOPSIS</span></span>
<span data-ttu-id="87108-103">Bir olay Kılavuzu konusunun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="87108-103">Sets the properties of an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87108-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87108-104">SYNTAX</span></span>

### <span data-ttu-id="87108-105">TopicNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="87108-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87108-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="87108-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87108-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87108-107">TopicInputObjectParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87108-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="87108-108">DESCRIPTION</span></span>
<span data-ttu-id="87108-109">Bir olay Kılavuzu konusunun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="87108-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="87108-110">Bu, bir olay Kılavuzu konusunun etiketlerinin yerini değiştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="87108-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="87108-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87108-111">EXAMPLES</span></span>

### <span data-ttu-id="87108-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="87108-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="87108-113">\` \` \` \` Etiketleri belirtilen etiketlerle değiştirmek için myresourcegroupname kaynak grubundaki konu1 olay Kılavuzu konusunun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="87108-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="87108-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87108-114">PARAMETERS</span></span>

### <span data-ttu-id="87108-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87108-115">-DefaultProfile</span></span>
<span data-ttu-id="87108-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="87108-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87108-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87108-117">-InputObject</span></span>
<span data-ttu-id="87108-118">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="87108-118">EventGrid Topic object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87108-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="87108-119">-Name</span></span>
<span data-ttu-id="87108-120">EventGrid konu adı.</span><span class="sxs-lookup"><span data-stu-id="87108-120">EventGrid Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87108-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87108-121">-ResourceGroupName</span></span>
<span data-ttu-id="87108-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="87108-122">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87108-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="87108-123">-ResourceId</span></span>
<span data-ttu-id="87108-124">EventGrid konu RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="87108-124">EventGrid Topic ResourceID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87108-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="87108-125">-Tag</span></span>
<span data-ttu-id="87108-126">Kaynak etiketini temsil eden hashtables 'lar.</span><span class="sxs-lookup"><span data-stu-id="87108-126">Hashtables which represents resource Tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87108-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="87108-127">-Confirm</span></span>
<span data-ttu-id="87108-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="87108-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87108-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87108-129">-WhatIf</span></span>
<span data-ttu-id="87108-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="87108-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87108-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="87108-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87108-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87108-132">CommonParameters</span></span>
<span data-ttu-id="87108-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87108-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87108-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87108-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87108-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87108-135">INPUTS</span></span>

### <span data-ttu-id="87108-136">System. String</span><span class="sxs-lookup"><span data-stu-id="87108-136">System.String</span></span>
<span data-ttu-id="87108-137">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="87108-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="87108-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87108-138">OUTPUTS</span></span>

### <span data-ttu-id="87108-139">Microsoft. Azure. Management. EventGrid. modeller. konu</span><span class="sxs-lookup"><span data-stu-id="87108-139">Microsoft.Azure.Management.EventGrid.Models.Topic</span></span>

## <span data-ttu-id="87108-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87108-140">NOTES</span></span>

## <span data-ttu-id="87108-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87108-141">RELATED LINKS</span></span>

