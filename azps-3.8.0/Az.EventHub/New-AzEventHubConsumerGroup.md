---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: ef03af9c452496d198aaaa073ee9fd967d851bb4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104100"
---
# <span data-ttu-id="318ba-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="318ba-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="318ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="318ba-102">SYNOPSIS</span></span>
<span data-ttu-id="318ba-103">Belirtilen olay hub 'ı için yeni bir tüketici grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="318ba-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="318ba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="318ba-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="318ba-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="318ba-105">DESCRIPTION</span></span>
<span data-ttu-id="318ba-106">Belirtilen olay hub 'ı için yeni bir tüketici grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="318ba-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="318ba-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="318ba-107">EXAMPLES</span></span>

### <span data-ttu-id="318ba-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="318ba-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="318ba-109">\` \` \` \` \` \` Myresourcegroupname kaynak grubuyla, mynamespacename ad alanı kapsamındaki Olay Hub myeventhubname ile tüketici \` \` grubu 'nu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="318ba-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="318ba-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="318ba-110">PARAMETERS</span></span>

### <span data-ttu-id="318ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="318ba-111">-DefaultProfile</span></span>
<span data-ttu-id="318ba-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="318ba-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="318ba-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="318ba-113">-EventHub</span></span>
<span data-ttu-id="318ba-114">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="318ba-114">EventHub Name</span></span>

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

### <span data-ttu-id="318ba-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="318ba-115">-Name</span></span>
<span data-ttu-id="318ba-116">ConsumerGroup adı</span><span class="sxs-lookup"><span data-stu-id="318ba-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="318ba-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="318ba-117">-Namespace</span></span>
<span data-ttu-id="318ba-118">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="318ba-118">Namespace Name</span></span>

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

### <span data-ttu-id="318ba-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="318ba-119">-ResourceGroupName</span></span>
<span data-ttu-id="318ba-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="318ba-120">Resource Group Name</span></span>

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

### <span data-ttu-id="318ba-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="318ba-121">-UserMetadata</span></span>
<span data-ttu-id="318ba-122">ConsumerGroup için Kullanıcı meta verileri</span><span class="sxs-lookup"><span data-stu-id="318ba-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="318ba-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="318ba-123">-Confirm</span></span>
<span data-ttu-id="318ba-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="318ba-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="318ba-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="318ba-125">-WhatIf</span></span>
<span data-ttu-id="318ba-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="318ba-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="318ba-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="318ba-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="318ba-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="318ba-128">CommonParameters</span></span>
<span data-ttu-id="318ba-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="318ba-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="318ba-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="318ba-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="318ba-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="318ba-131">INPUTS</span></span>

### <span data-ttu-id="318ba-132">System. String</span><span class="sxs-lookup"><span data-stu-id="318ba-132">System.String</span></span>

## <span data-ttu-id="318ba-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="318ba-133">OUTPUTS</span></span>

### <span data-ttu-id="318ba-134">Microsoft. Azure. Commands. EventHub. modeller. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="318ba-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="318ba-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="318ba-135">NOTES</span></span>

## <span data-ttu-id="318ba-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="318ba-136">RELATED LINKS</span></span>
