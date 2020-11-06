---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 445d20453b9f3d99e4ff5c72e118b287f0a83898
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593494"
---
# <span data-ttu-id="d4f59-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d4f59-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="d4f59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4f59-102">SYNOPSIS</span></span>
<span data-ttu-id="d4f59-103">Belirli bir olay hub tüketici grubunun ayrıntılarını alır veya bir olay hub 'ındaki tüketici gruplarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="d4f59-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4f59-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4f59-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4f59-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4f59-105">DESCRIPTION</span></span>
<span data-ttu-id="d4f59-106">Get-AzureRmEventHubConsumerGroup cmdlet 'i, belirtilen bir olay hub tüketici grubunun ayrıntılarını veya belirli bir olay hub 'ındaki tüketici gruplarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="d4f59-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="d4f59-107">Tüketici grubunun adı sağlanmışsa, tek bir tüketici grubu ayrıntılarının ayrıntıları verilir.</span><span class="sxs-lookup"><span data-stu-id="d4f59-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="d4f59-108">Tüketici grubunun adı sağlanmadıysa, belirtilen olay hub 'ındaki tüketici gruplarının listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="d4f59-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="d4f59-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4f59-109">EXAMPLES</span></span>

### <span data-ttu-id="d4f59-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d4f59-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="d4f59-111">\` \` \` \` \` \` Myresourcegroupname kaynak grubuyla Adynamespacename ad alanında bulunan Olay Hub myeventhubname myconsumergroupname adlı \` Tüketici grubunu alır \` .</span><span class="sxs-lookup"><span data-stu-id="d4f59-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d4f59-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d4f59-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="d4f59-113">\` \` \` \` Myresourcegroupname kaynak grubuyla Mynamespacename ad alanında bulunan Olay Hub myeventhubname içindeki tüketici \` gruplarının bir listesini alır \` .</span><span class="sxs-lookup"><span data-stu-id="d4f59-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d4f59-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4f59-114">PARAMETERS</span></span>

### <span data-ttu-id="d4f59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4f59-115">-DefaultProfile</span></span>
<span data-ttu-id="d4f59-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d4f59-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4f59-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="d4f59-117">-EventHub</span></span>
<span data-ttu-id="d4f59-118">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="d4f59-118">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f59-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d4f59-119">-Name</span></span>
<span data-ttu-id="d4f59-120">ConsumerGroup adı</span><span class="sxs-lookup"><span data-stu-id="d4f59-120">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f59-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d4f59-121">-Namespace</span></span>
<span data-ttu-id="d4f59-122">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="d4f59-122">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f59-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4f59-123">-ResourceGroupName</span></span>
<span data-ttu-id="d4f59-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d4f59-124">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f59-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4f59-125">CommonParameters</span></span>
<span data-ttu-id="d4f59-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4f59-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d4f59-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4f59-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4f59-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4f59-128">INPUTS</span></span>

### <span data-ttu-id="d4f59-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d4f59-129">System.String</span></span>


## <span data-ttu-id="d4f59-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4f59-130">OUTPUTS</span></span>

### <span data-ttu-id="d4f59-131">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. EventHub. modeller. PSConsumerGroupAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d4f59-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="d4f59-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4f59-132">NOTES</span></span>

## <span data-ttu-id="d4f59-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4f59-133">RELATED LINKS</span></span>
