---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
ms.openlocfilehash: e71c479624cd77e25adbd4fbfdc609cfa89918b3
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93765215"
---
# <span data-ttu-id="5fbf8-101">Get-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="5fbf8-101">Get-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="5fbf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fbf8-102">SYNOPSIS</span></span>
<span data-ttu-id="5fbf8-103">Bir olay Kılavuzu konusunun ayrıntılarını alır veya geçerli Azure aboneliğindeki tüm olay Kılavuzu konularının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="5fbf8-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fbf8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5fbf8-104">SYNTAX</span></span>

### <span data-ttu-id="5fbf8-105">ResourceGroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5fbf8-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5fbf8-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fbf8-106">TopicNameParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fbf8-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fbf8-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5fbf8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5fbf8-108">DESCRIPTION</span></span>
<span data-ttu-id="5fbf8-109">Get-AzureRmEventGridTopic cmdlet 'i, belirli bir olay Kılavuzu konusunun ayrıntılarını veya geçerli Azure aboneliğindeki tüm olay Kılavuzu konularının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="5fbf8-109">The Get-AzureRmEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="5fbf8-110">Konu adı sağlanmışsa, tek bir olay Kılavuzu konusunun ayrıntıları verilir.</span><span class="sxs-lookup"><span data-stu-id="5fbf8-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="5fbf8-111">Konu adı sağlanmadıysa, konu listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="5fbf8-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="5fbf8-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5fbf8-112">EXAMPLES</span></span>

### <span data-ttu-id="5fbf8-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5fbf8-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="5fbf8-114">\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunun ayrıntılarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="5fbf8-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5fbf8-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5fbf8-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="5fbf8-116">\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunun ayrıntılarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="5fbf8-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5fbf8-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="5fbf8-117">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="5fbf8-118">Myresourcegroupname kaynak grubundaki tüm olay Kılavuzu konularını listeleyin \` \` .</span><span class="sxs-lookup"><span data-stu-id="5fbf8-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5fbf8-119">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="5fbf8-119">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridTopic
```

<span data-ttu-id="5fbf8-120">Abonelikteki tüm olay Kılavuzu konularını listeleyin.</span><span class="sxs-lookup"><span data-stu-id="5fbf8-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="5fbf8-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5fbf8-121">PARAMETERS</span></span>

### <span data-ttu-id="5fbf8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fbf8-122">-DefaultProfile</span></span>
<span data-ttu-id="5fbf8-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5fbf8-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5fbf8-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="5fbf8-124">-Name</span></span>
<span data-ttu-id="5fbf8-125">EventGrid konu adı.</span><span class="sxs-lookup"><span data-stu-id="5fbf8-125">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="5fbf8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fbf8-126">-ResourceGroupName</span></span>
<span data-ttu-id="5fbf8-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5fbf8-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="5fbf8-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5fbf8-128">-ResourceId</span></span>
<span data-ttu-id="5fbf8-129">Olay Kılavuzu konusunu temsil eden kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="5fbf8-129">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="5fbf8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fbf8-130">CommonParameters</span></span>
<span data-ttu-id="5fbf8-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5fbf8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fbf8-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fbf8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fbf8-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5fbf8-133">INPUTS</span></span>

### <span data-ttu-id="5fbf8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5fbf8-134">System.String</span></span>
<span data-ttu-id="5fbf8-135">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="5fbf8-135">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="5fbf8-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5fbf8-136">OUTPUTS</span></span>

### <span data-ttu-id="5fbf8-137">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="5fbf8-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="5fbf8-138">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. EventGrid. modeller. Pstopiclistınstance, Microsoft. Azure. Commands. EventGrid, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5fbf8-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5fbf8-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5fbf8-139">NOTES</span></span>

## <span data-ttu-id="5fbf8-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5fbf8-140">RELATED LINKS</span></span>

