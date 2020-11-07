---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
ms.openlocfilehash: 7f10df478851679afeb73157252d954f756f0c4c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751974"
---
# <span data-ttu-id="65dde-101">Get-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="65dde-101">Get-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="65dde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65dde-102">SYNOPSIS</span></span>
<span data-ttu-id="65dde-103">Belirli bir olay hub tüketici grubunun ayrıntılarını alır veya bir olay hub 'ındaki tüketici gruplarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="65dde-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

## <span data-ttu-id="65dde-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65dde-104">SYNTAX</span></span>

```
Get-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65dde-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="65dde-105">DESCRIPTION</span></span>
<span data-ttu-id="65dde-106">Get-AzEventHubConsumerGroup cmdlet 'i, belirtilen bir olay hub tüketici grubunun ayrıntılarını veya belirli bir olay hub 'ındaki tüketici gruplarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="65dde-106">The Get-AzEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="65dde-107">Tüketici grubunun adı sağlanmışsa, tek bir tüketici grubu ayrıntılarının ayrıntıları verilir.</span><span class="sxs-lookup"><span data-stu-id="65dde-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="65dde-108">Tüketici grubunun adı sağlanmadıysa, belirtilen olay hub 'ındaki tüketici gruplarının listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="65dde-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="65dde-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65dde-109">EXAMPLES</span></span>

### <span data-ttu-id="65dde-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="65dde-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="65dde-111">\` \` \` \` \` \` Myresourcegroupname kaynak grubuyla Adynamespacename ad alanında bulunan Olay Hub myeventhubname myconsumergroupname adlı \` Tüketici grubunu alır \` .</span><span class="sxs-lookup"><span data-stu-id="65dde-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="65dde-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="65dde-112">Example 2</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="65dde-113">\` \` \` \` Myresourcegroupname kaynak grubuyla Mynamespacename ad alanında bulunan Olay Hub myeventhubname içindeki tüketici \` gruplarının bir listesini alır \` .</span><span class="sxs-lookup"><span data-stu-id="65dde-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="65dde-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65dde-114">PARAMETERS</span></span>

### <span data-ttu-id="65dde-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65dde-115">-DefaultProfile</span></span>
<span data-ttu-id="65dde-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="65dde-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65dde-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="65dde-117">-EventHub</span></span>
<span data-ttu-id="65dde-118">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="65dde-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65dde-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="65dde-119">-MaxCount</span></span>
<span data-ttu-id="65dde-120">Döndürülecek ConsumerGroups sayısının üst sınırını belirleme.</span><span class="sxs-lookup"><span data-stu-id="65dde-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65dde-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="65dde-121">-Name</span></span>
<span data-ttu-id="65dde-122">ConsumerGroup adı</span><span class="sxs-lookup"><span data-stu-id="65dde-122">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65dde-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="65dde-123">-Namespace</span></span>
<span data-ttu-id="65dde-124">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="65dde-124">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65dde-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65dde-125">-ResourceGroupName</span></span>
<span data-ttu-id="65dde-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="65dde-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65dde-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65dde-127">CommonParameters</span></span>
<span data-ttu-id="65dde-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65dde-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65dde-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65dde-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65dde-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65dde-130">INPUTS</span></span>

### <span data-ttu-id="65dde-131">System. String</span><span class="sxs-lookup"><span data-stu-id="65dde-131">System.String</span></span>

## <span data-ttu-id="65dde-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65dde-132">OUTPUTS</span></span>

### <span data-ttu-id="65dde-133">Microsoft. Azure. Commands. EventHub. modeller. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="65dde-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="65dde-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65dde-134">NOTES</span></span>

## <span data-ttu-id="65dde-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65dde-135">RELATED LINKS</span></span>
