---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
ms.openlocfilehash: fc108c633b70cc1eed32bcc0574ad25109a065fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097301"
---
# <span data-ttu-id="4b438-101">Get-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="4b438-101">Get-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="4b438-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b438-102">SYNOPSIS</span></span>
<span data-ttu-id="4b438-103">Belirli bir olay hub tüketici grubunun ayrıntılarını alır veya bir olay hub 'ındaki tüketici gruplarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="4b438-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

## <span data-ttu-id="4b438-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b438-104">SYNTAX</span></span>

```
Get-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b438-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b438-105">DESCRIPTION</span></span>
<span data-ttu-id="4b438-106">Get-AzEventHubConsumerGroup cmdlet 'i, belirtilen bir olay hub tüketici grubunun ayrıntılarını veya belirli bir olay hub 'ındaki tüketici gruplarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="4b438-106">The Get-AzEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="4b438-107">Tüketici grubunun adı sağlanmışsa, tek bir tüketici grubu ayrıntılarının ayrıntıları verilir.</span><span class="sxs-lookup"><span data-stu-id="4b438-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="4b438-108">Tüketici grubunun adı sağlanmadıysa, belirtilen olay hub 'ındaki tüketici gruplarının listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="4b438-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="4b438-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b438-109">EXAMPLES</span></span>

### <span data-ttu-id="4b438-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4b438-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="4b438-111">\` \` \` \` \` \` Myresourcegroupname kaynak grubuyla Adynamespacename ad alanında bulunan Olay Hub myeventhubname myconsumergroupname adlı \` Tüketici grubunu alır \` .</span><span class="sxs-lookup"><span data-stu-id="4b438-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="4b438-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4b438-112">Example 2</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="4b438-113">\` \` \` \` Myresourcegroupname kaynak grubuyla Mynamespacename ad alanında bulunan Olay Hub myeventhubname içindeki tüketici \` gruplarının bir listesini alır \` .</span><span class="sxs-lookup"><span data-stu-id="4b438-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="4b438-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b438-114">PARAMETERS</span></span>

### <span data-ttu-id="4b438-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b438-115">-DefaultProfile</span></span>
<span data-ttu-id="4b438-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b438-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b438-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="4b438-117">-EventHub</span></span>
<span data-ttu-id="4b438-118">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="4b438-118">EventHub Name</span></span>

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

### <span data-ttu-id="4b438-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="4b438-119">-MaxCount</span></span>
<span data-ttu-id="4b438-120">Döndürülecek ConsumerGroups sayısının üst sınırını belirleme.</span><span class="sxs-lookup"><span data-stu-id="4b438-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

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

### <span data-ttu-id="4b438-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="4b438-121">-Name</span></span>
<span data-ttu-id="4b438-122">ConsumerGroup adı</span><span class="sxs-lookup"><span data-stu-id="4b438-122">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="4b438-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4b438-123">-Namespace</span></span>
<span data-ttu-id="4b438-124">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="4b438-124">Namespace Name</span></span>

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

### <span data-ttu-id="4b438-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b438-125">-ResourceGroupName</span></span>
<span data-ttu-id="4b438-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4b438-126">Resource Group Name</span></span>

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

### <span data-ttu-id="4b438-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b438-127">CommonParameters</span></span>
<span data-ttu-id="4b438-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b438-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b438-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b438-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b438-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b438-130">INPUTS</span></span>

### <span data-ttu-id="4b438-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4b438-131">System.String</span></span>

## <span data-ttu-id="4b438-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b438-132">OUTPUTS</span></span>

### <span data-ttu-id="4b438-133">Microsoft. Azure. Commands. EventHub. modeller. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="4b438-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="4b438-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b438-134">NOTES</span></span>

## <span data-ttu-id="4b438-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b438-135">RELATED LINKS</span></span>
