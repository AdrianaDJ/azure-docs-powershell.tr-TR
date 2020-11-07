---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 741a888287ba7fcb4a9b54c1281a6a27be5fbb0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764030"
---
# <span data-ttu-id="bf4a2-101">Get-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="bf4a2-101">Get-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="bf4a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf4a2-102">SYNOPSIS</span></span>
<span data-ttu-id="bf4a2-103">Olay Kılavuzu konusunda etkinlikleri yayımlamak için kullanılan paylaşılan erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="bf4a2-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf4a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf4a2-104">SYNTAX</span></span>

### <span data-ttu-id="bf4a2-105">TopicNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bf4a2-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf4a2-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf4a2-106">TopicInputObjectParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf4a2-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf4a2-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf4a2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf4a2-108">DESCRIPTION</span></span>
<span data-ttu-id="bf4a2-109">Olay Kılavuzu konusunda etkinlikleri yayımlamak için kullanılan paylaşılan erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="bf4a2-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="bf4a2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf4a2-110">EXAMPLES</span></span>

### <span data-ttu-id="bf4a2-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bf4a2-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="bf4a2-112">\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunun paylaşılan erişim anahtarlarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="bf4a2-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="bf4a2-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="bf4a2-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzureRmEventGridTopicKey
```

<span data-ttu-id="bf4a2-114">\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunun paylaşılan erişim anahtarlarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="bf4a2-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="bf4a2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf4a2-115">PARAMETERS</span></span>

### <span data-ttu-id="bf4a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf4a2-116">-DefaultProfile</span></span>
<span data-ttu-id="bf4a2-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bf4a2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf4a2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf4a2-118">-InputObject</span></span>
<span data-ttu-id="bf4a2-119">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bf4a2-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="bf4a2-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="bf4a2-120">-Name</span></span>
<span data-ttu-id="bf4a2-121">EventGrid konu adı.</span><span class="sxs-lookup"><span data-stu-id="bf4a2-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="bf4a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf4a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="bf4a2-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="bf4a2-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="bf4a2-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bf4a2-124">-ResourceId</span></span>
<span data-ttu-id="bf4a2-125">Olay Kılavuzu konusunu temsil eden kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="bf4a2-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="bf4a2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf4a2-126">CommonParameters</span></span>
<span data-ttu-id="bf4a2-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf4a2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf4a2-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf4a2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf4a2-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf4a2-129">INPUTS</span></span>

### <span data-ttu-id="bf4a2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bf4a2-130">System.String</span></span>

## <span data-ttu-id="bf4a2-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf4a2-131">OUTPUTS</span></span>

### <span data-ttu-id="bf4a2-132">Microsoft. Azure. Management. EventGrid. modeller. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="bf4a2-132">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="bf4a2-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf4a2-133">NOTES</span></span>

## <span data-ttu-id="bf4a2-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf4a2-134">RELATED LINKS</span></span>

