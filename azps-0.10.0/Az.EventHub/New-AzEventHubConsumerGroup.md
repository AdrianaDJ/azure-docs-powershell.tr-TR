---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: 2e9a3340e2e514d00c43328308f95bf35b38932c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935882"
---
# <span data-ttu-id="fa2cc-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="fa2cc-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="fa2cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa2cc-102">SYNOPSIS</span></span>
<span data-ttu-id="fa2cc-103">Belirtilen olay hub 'ı için yeni bir tüketici grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fa2cc-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="fa2cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa2cc-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa2cc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa2cc-105">DESCRIPTION</span></span>
<span data-ttu-id="fa2cc-106">Belirtilen olay hub 'ı için yeni bir tüketici grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fa2cc-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="fa2cc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa2cc-107">EXAMPLES</span></span>

### <span data-ttu-id="fa2cc-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fa2cc-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="fa2cc-109">\` \` \` \` \` \` Myresourcegroupname kaynak grubuyla, mynamespacename ad alanı kapsamındaki Olay Hub myeventhubname ile tüketici \` \` grubu 'nu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fa2cc-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="fa2cc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa2cc-110">PARAMETERS</span></span>

### <span data-ttu-id="fa2cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa2cc-111">-DefaultProfile</span></span>
<span data-ttu-id="fa2cc-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fa2cc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa2cc-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="fa2cc-113">-EventHub</span></span>
<span data-ttu-id="fa2cc-114">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="fa2cc-114">EventHub Name</span></span>

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

### <span data-ttu-id="fa2cc-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="fa2cc-115">-Name</span></span>
<span data-ttu-id="fa2cc-116">ConsumerGroup adı</span><span class="sxs-lookup"><span data-stu-id="fa2cc-116">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa2cc-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fa2cc-117">-Namespace</span></span>
<span data-ttu-id="fa2cc-118">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="fa2cc-118">Namespace Name</span></span>

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

### <span data-ttu-id="fa2cc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa2cc-119">-ResourceGroupName</span></span>
<span data-ttu-id="fa2cc-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="fa2cc-120">Resource Group Name</span></span>

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

### <span data-ttu-id="fa2cc-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="fa2cc-121">-UserMetadata</span></span>
<span data-ttu-id="fa2cc-122">ConsumerGroup için Kullanıcı meta verileri</span><span class="sxs-lookup"><span data-stu-id="fa2cc-122">User Metadata for ConsumerGroup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa2cc-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="fa2cc-123">-Confirm</span></span>
<span data-ttu-id="fa2cc-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fa2cc-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2cc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa2cc-125">-WhatIf</span></span>
<span data-ttu-id="fa2cc-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fa2cc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa2cc-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fa2cc-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2cc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa2cc-128">CommonParameters</span></span>
<span data-ttu-id="fa2cc-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa2cc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa2cc-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa2cc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa2cc-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa2cc-131">INPUTS</span></span>

### <span data-ttu-id="fa2cc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fa2cc-132">System.String</span></span>

## <span data-ttu-id="fa2cc-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa2cc-133">OUTPUTS</span></span>

### <span data-ttu-id="fa2cc-134">Microsoft. Azure. Commands. EventHub. modeller. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="fa2cc-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="fa2cc-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa2cc-135">NOTES</span></span>

## <span data-ttu-id="fa2cc-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa2cc-136">RELATED LINKS</span></span>
