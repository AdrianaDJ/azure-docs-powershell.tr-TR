---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 8bd28b3bbe043663a451b235abf46c3a42e235e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764662"
---
# <span data-ttu-id="4a32a-101">Get-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="4a32a-101">Get-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="4a32a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a32a-102">SYNOPSIS</span></span>
<span data-ttu-id="4a32a-103">Olay Kılavuzu konusunda etkinlikleri yayımlamak için kullanılan paylaşılan erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="4a32a-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a32a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a32a-104">SYNTAX</span></span>

### <span data-ttu-id="4a32a-105">TopicNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4a32a-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a32a-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a32a-106">TopicInputObjectParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a32a-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a32a-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a32a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a32a-108">DESCRIPTION</span></span>
<span data-ttu-id="4a32a-109">Olay Kılavuzu konusunda etkinlikleri yayımlamak için kullanılan paylaşılan erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="4a32a-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="4a32a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a32a-110">EXAMPLES</span></span>

### <span data-ttu-id="4a32a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4a32a-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="4a32a-112">\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunun paylaşılan erişim anahtarlarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="4a32a-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="4a32a-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4a32a-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzureRmEventGridTopicKey
```

<span data-ttu-id="4a32a-114">\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunun paylaşılan erişim anahtarlarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="4a32a-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="4a32a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a32a-115">PARAMETERS</span></span>

### <span data-ttu-id="4a32a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a32a-116">-DefaultProfile</span></span>
<span data-ttu-id="4a32a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4a32a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a32a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a32a-118">-InputObject</span></span>
<span data-ttu-id="4a32a-119">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4a32a-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="4a32a-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="4a32a-120">-Name</span></span>
<span data-ttu-id="4a32a-121">EventGrid konu adı.</span><span class="sxs-lookup"><span data-stu-id="4a32a-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="4a32a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a32a-122">-ResourceGroupName</span></span>
<span data-ttu-id="4a32a-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4a32a-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="4a32a-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4a32a-124">-ResourceId</span></span>
<span data-ttu-id="4a32a-125">Olay Kılavuzu konusunu temsil eden kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="4a32a-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="4a32a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a32a-126">CommonParameters</span></span>
<span data-ttu-id="4a32a-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a32a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a32a-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a32a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a32a-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a32a-129">INPUTS</span></span>

### <span data-ttu-id="4a32a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4a32a-130">System.String</span></span>

### <span data-ttu-id="4a32a-131">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="4a32a-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="4a32a-132">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4a32a-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4a32a-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a32a-133">OUTPUTS</span></span>

### <span data-ttu-id="4a32a-134">Microsoft. Azure. Management. EventGrid. modeller. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="4a32a-134">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="4a32a-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a32a-135">NOTES</span></span>

## <span data-ttu-id="4a32a-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a32a-136">RELATED LINKS</span></span>