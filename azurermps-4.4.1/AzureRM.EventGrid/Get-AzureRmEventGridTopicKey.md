---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 91e3acd227acd8a83dcd5ccb0beb2ed12d1cca99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764862"
---
# <span data-ttu-id="2aeb6-101">Get-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="2aeb6-101">Get-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="2aeb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2aeb6-102">SYNOPSIS</span></span>
<span data-ttu-id="2aeb6-103">Olay Kılavuzu konusunda etkinlikleri yayımlamak için kullanılan paylaşılan erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="2aeb6-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2aeb6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2aeb6-104">SYNTAX</span></span>

### <span data-ttu-id="2aeb6-105">TopicNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2aeb6-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2aeb6-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aeb6-106">TopicInputObjectParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2aeb6-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aeb6-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2aeb6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2aeb6-108">DESCRIPTION</span></span>
<span data-ttu-id="2aeb6-109">Olay Kılavuzu konusunda etkinlikleri yayımlamak için kullanılan paylaşılan erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="2aeb6-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="2aeb6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2aeb6-110">EXAMPLES</span></span>

### <span data-ttu-id="2aeb6-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2aeb6-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="2aeb6-112">\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunun paylaşılan erişim anahtarlarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="2aeb6-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2aeb6-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2aeb6-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzureRmEventGridTopicKey
```

<span data-ttu-id="2aeb6-114">\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunun paylaşılan erişim anahtarlarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="2aeb6-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="2aeb6-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2aeb6-115">PARAMETERS</span></span>

### <span data-ttu-id="2aeb6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2aeb6-116">-InputObject</span></span>
<span data-ttu-id="2aeb6-117">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2aeb6-117">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="2aeb6-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="2aeb6-118">-Name</span></span>
<span data-ttu-id="2aeb6-119">EventGrid konu adı.</span><span class="sxs-lookup"><span data-stu-id="2aeb6-119">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="2aeb6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aeb6-120">-ResourceGroupName</span></span>
<span data-ttu-id="2aeb6-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2aeb6-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="2aeb6-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2aeb6-122">-ResourceId</span></span>
<span data-ttu-id="2aeb6-123">Olay Kılavuzu konusunu temsil eden kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="2aeb6-123">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="2aeb6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aeb6-124">-DefaultProfile</span></span>
<span data-ttu-id="2aeb6-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2aeb6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2aeb6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aeb6-126">CommonParameters</span></span>
<span data-ttu-id="2aeb6-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2aeb6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aeb6-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aeb6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aeb6-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2aeb6-129">INPUTS</span></span>

### <span data-ttu-id="2aeb6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2aeb6-130">System.String</span></span>

## <span data-ttu-id="2aeb6-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2aeb6-131">OUTPUTS</span></span>

### <span data-ttu-id="2aeb6-132">Microsoft. Azure. Management. EventGrid. modeller. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="2aeb6-132">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="2aeb6-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2aeb6-133">NOTES</span></span>

## <span data-ttu-id="2aeb6-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2aeb6-134">RELATED LINKS</span></span>

