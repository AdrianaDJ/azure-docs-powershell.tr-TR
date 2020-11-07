---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: a9447c745ddf60c4a2adcb2a55c824b65d96efd8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764024"
---
# <span data-ttu-id="4912a-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="4912a-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="4912a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4912a-102">SYNOPSIS</span></span>
<span data-ttu-id="4912a-103">Belirtilen olay hub 'ı için yeni bir tüketici grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4912a-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4912a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4912a-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4912a-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4912a-105">EXAMPLES</span></span>

### <span data-ttu-id="4912a-106">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4912a-106">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="4912a-107">\` \` \` \` \` \` Myresourcegroupname kaynak grubuyla, mynamespacename ad alanı kapsamındaki Olay Hub myeventhubname ile tüketici \` \` grubu 'nu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4912a-107">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="4912a-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4912a-108">PARAMETERS</span></span>

### <span data-ttu-id="4912a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4912a-109">-DefaultProfile</span></span>
<span data-ttu-id="4912a-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4912a-110">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4912a-111">-EventHub</span><span class="sxs-lookup"><span data-stu-id="4912a-111">-EventHub</span></span>
<span data-ttu-id="4912a-112">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="4912a-112">EventHub Name</span></span>

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

### <span data-ttu-id="4912a-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="4912a-113">-Name</span></span>
<span data-ttu-id="4912a-114">ConsumerGroup adı</span><span class="sxs-lookup"><span data-stu-id="4912a-114">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4912a-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4912a-115">-Namespace</span></span>
<span data-ttu-id="4912a-116">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="4912a-116">Namespace Name</span></span>

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

### <span data-ttu-id="4912a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4912a-117">-ResourceGroupName</span></span>
<span data-ttu-id="4912a-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4912a-118">Resource Group Name</span></span>

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

### <span data-ttu-id="4912a-119">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="4912a-119">-UserMetadata</span></span>
<span data-ttu-id="4912a-120">ConsumerGroup için Kullanıcı meta verileri</span><span class="sxs-lookup"><span data-stu-id="4912a-120">User Metadata for ConsumerGroup</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4912a-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="4912a-121">-Confirm</span></span>
<span data-ttu-id="4912a-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4912a-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4912a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4912a-123">-WhatIf</span></span>
<span data-ttu-id="4912a-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4912a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4912a-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4912a-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4912a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4912a-126">CommonParameters</span></span>
<span data-ttu-id="4912a-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4912a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4912a-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4912a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4912a-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4912a-129">INPUTS</span></span>

### <span data-ttu-id="4912a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4912a-130">System.String</span></span>


## <span data-ttu-id="4912a-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4912a-131">OUTPUTS</span></span>

### <span data-ttu-id="4912a-132">Microsoft. Azure. Commands. EventHub. modeller. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="4912a-132">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>


## <span data-ttu-id="4912a-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4912a-133">NOTES</span></span>

## <span data-ttu-id="4912a-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4912a-134">RELATED LINKS</span></span>
