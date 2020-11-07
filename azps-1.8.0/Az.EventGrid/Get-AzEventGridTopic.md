---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: 23004583a08dbcf5ef8785b62d0457b6b6ee0897
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760878"
---
# <span data-ttu-id="29dde-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="29dde-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="29dde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29dde-102">SYNOPSIS</span></span>
<span data-ttu-id="29dde-103">Bir olay Kılavuzu konusunun ayrıntılarını alır veya geçerli Azure aboneliğindeki tüm olay Kılavuzu konularının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="29dde-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="29dde-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="29dde-104">SYNTAX</span></span>

### <span data-ttu-id="29dde-105">ResourceGroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="29dde-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29dde-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="29dde-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29dde-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="29dde-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29dde-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="29dde-108">DESCRIPTION</span></span>
<span data-ttu-id="29dde-109">Get-AzEventGridTopic cmdlet 'i, belirli bir olay Kılavuzu konusunun ayrıntılarını veya geçerli Azure aboneliğindeki tüm olay Kılavuzu konularının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="29dde-109">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="29dde-110">Konu adı sağlanmışsa, tek bir olay Kılavuzu konusunun ayrıntıları verilir.</span><span class="sxs-lookup"><span data-stu-id="29dde-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="29dde-111">Konu adı sağlanmadıysa, konu listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="29dde-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="29dde-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="29dde-112">EXAMPLES</span></span>

### <span data-ttu-id="29dde-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="29dde-113">Example 1</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="29dde-114">\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunun ayrıntılarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="29dde-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="29dde-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="29dde-115">Example 2</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="29dde-116">\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunun ayrıntılarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="29dde-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="29dde-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="29dde-117">Example 3</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="29dde-118">Myresourcegroupname kaynak grubundaki tüm olay Kılavuzu konularını listeleyin \` \` .</span><span class="sxs-lookup"><span data-stu-id="29dde-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="29dde-119">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="29dde-119">Example 4</span></span>
```
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="29dde-120">Abonelikteki tüm olay Kılavuzu konularını listeleyin.</span><span class="sxs-lookup"><span data-stu-id="29dde-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="29dde-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="29dde-121">PARAMETERS</span></span>

### <span data-ttu-id="29dde-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29dde-122">-DefaultProfile</span></span>
<span data-ttu-id="29dde-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="29dde-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29dde-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="29dde-124">-Name</span></span>
<span data-ttu-id="29dde-125">EventGrid konu adı.</span><span class="sxs-lookup"><span data-stu-id="29dde-125">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="29dde-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29dde-126">-ResourceGroupName</span></span>
<span data-ttu-id="29dde-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="29dde-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="29dde-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="29dde-128">-ResourceId</span></span>
<span data-ttu-id="29dde-129">Olay Kılavuzu konusunu temsil eden kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="29dde-129">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="29dde-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29dde-130">CommonParameters</span></span>
<span data-ttu-id="29dde-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="29dde-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29dde-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29dde-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29dde-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="29dde-133">INPUTS</span></span>

### <span data-ttu-id="29dde-134">System. String</span><span class="sxs-lookup"><span data-stu-id="29dde-134">System.String</span></span>

## <span data-ttu-id="29dde-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="29dde-135">OUTPUTS</span></span>

### <span data-ttu-id="29dde-136">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="29dde-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="29dde-137">Microsoft. Azure. Commands. EventGrid. modeller. Pstopiclistınstance</span><span class="sxs-lookup"><span data-stu-id="29dde-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="29dde-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="29dde-138">NOTES</span></span>

## <span data-ttu-id="29dde-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="29dde-139">RELATED LINKS</span></span>
