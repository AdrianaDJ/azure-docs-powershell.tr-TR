---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: a956e0e99db44e5f92b4d9ec772158b262434c05
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937764"
---
# <span data-ttu-id="5d0ef-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="5d0ef-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="5d0ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d0ef-102">SYNOPSIS</span></span>
<span data-ttu-id="5d0ef-103">Olay Kılavuzu konusunda etkinlikleri yayımlamak için kullanılan paylaşılan erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="5d0ef-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="5d0ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5d0ef-104">SYNTAX</span></span>

### <span data-ttu-id="5d0ef-105">TopicNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5d0ef-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d0ef-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d0ef-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d0ef-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d0ef-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d0ef-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5d0ef-108">DESCRIPTION</span></span>
<span data-ttu-id="5d0ef-109">Olay Kılavuzu konusunda etkinlikleri yayımlamak için kullanılan paylaşılan erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="5d0ef-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="5d0ef-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5d0ef-110">EXAMPLES</span></span>

### <span data-ttu-id="5d0ef-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5d0ef-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="5d0ef-112">\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunun paylaşılan erişim anahtarlarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="5d0ef-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5d0ef-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5d0ef-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="5d0ef-114">\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunun paylaşılan erişim anahtarlarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="5d0ef-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="5d0ef-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5d0ef-115">PARAMETERS</span></span>

### <span data-ttu-id="5d0ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d0ef-116">-DefaultProfile</span></span>
<span data-ttu-id="5d0ef-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5d0ef-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d0ef-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d0ef-118">-InputObject</span></span>
<span data-ttu-id="5d0ef-119">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5d0ef-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="5d0ef-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="5d0ef-120">-Name</span></span>
<span data-ttu-id="5d0ef-121">EventGrid konu adı.</span><span class="sxs-lookup"><span data-stu-id="5d0ef-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="5d0ef-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d0ef-122">-ResourceGroupName</span></span>
<span data-ttu-id="5d0ef-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5d0ef-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="5d0ef-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5d0ef-124">-ResourceId</span></span>
<span data-ttu-id="5d0ef-125">Olay Kılavuzu konusunu temsil eden kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="5d0ef-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="5d0ef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d0ef-126">CommonParameters</span></span>
<span data-ttu-id="5d0ef-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5d0ef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d0ef-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d0ef-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d0ef-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5d0ef-129">INPUTS</span></span>

### <span data-ttu-id="5d0ef-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5d0ef-130">System.String</span></span>

### <span data-ttu-id="5d0ef-131">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="5d0ef-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="5d0ef-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5d0ef-132">OUTPUTS</span></span>

### <span data-ttu-id="5d0ef-133">Microsoft. Azure. Management. EventGrid. modeller. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="5d0ef-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="5d0ef-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5d0ef-134">NOTES</span></span>

## <span data-ttu-id="5d0ef-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5d0ef-135">RELATED LINKS</span></span>