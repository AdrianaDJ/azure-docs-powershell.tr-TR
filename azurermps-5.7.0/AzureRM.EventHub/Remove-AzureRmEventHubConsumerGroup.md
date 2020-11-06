---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 5b88ce6edc92cb6483b8d6df95599fcea854f805
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590494"
---
# <span data-ttu-id="a81ac-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="a81ac-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="a81ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a81ac-102">SYNOPSIS</span></span>
<span data-ttu-id="a81ac-103">Belirtilen olay hub 'ı tüketici grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="a81ac-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a81ac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a81ac-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a81ac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a81ac-105">DESCRIPTION</span></span>
<span data-ttu-id="a81ac-106">Remove-AzureRmEventHubConsumerGroup cmdlet 'i, verilen olay hub 'ından belirtilen tüketici grubunu kaldırır ve siler.</span><span class="sxs-lookup"><span data-stu-id="a81ac-106">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="a81ac-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a81ac-107">EXAMPLES</span></span>

### <span data-ttu-id="a81ac-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a81ac-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="a81ac-109">\`Myconsumergroupname adlı tüketici grubunu, \` kapsam dışı \` \` olarak \` mynamespacename \` ad alanına siler.</span><span class="sxs-lookup"><span data-stu-id="a81ac-109">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

## <span data-ttu-id="a81ac-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a81ac-110">PARAMETERS</span></span>

### <span data-ttu-id="a81ac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a81ac-111">-DefaultProfile</span></span>
<span data-ttu-id="a81ac-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a81ac-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a81ac-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="a81ac-113">-EventHub</span></span>
<span data-ttu-id="a81ac-114">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="a81ac-114">EventHub Name</span></span>

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

### <span data-ttu-id="a81ac-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="a81ac-115">-Name</span></span>
<span data-ttu-id="a81ac-116">ConsumerGroup adı</span><span class="sxs-lookup"><span data-stu-id="a81ac-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="a81ac-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a81ac-117">-Namespace</span></span>
<span data-ttu-id="a81ac-118">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="a81ac-118">Namespace Name</span></span>

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

### <span data-ttu-id="a81ac-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a81ac-119">-ResourceGroupName</span></span>
<span data-ttu-id="a81ac-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a81ac-120">Resource Group Name</span></span>

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

### <span data-ttu-id="a81ac-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="a81ac-121">-Confirm</span></span>
<span data-ttu-id="a81ac-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a81ac-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a81ac-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a81ac-123">-WhatIf</span></span>
<span data-ttu-id="a81ac-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a81ac-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a81ac-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a81ac-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a81ac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a81ac-126">CommonParameters</span></span>
<span data-ttu-id="a81ac-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a81ac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a81ac-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a81ac-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a81ac-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a81ac-129">INPUTS</span></span>

### <span data-ttu-id="a81ac-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a81ac-130">System.String</span></span>


## <span data-ttu-id="a81ac-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a81ac-131">OUTPUTS</span></span>

### <span data-ttu-id="a81ac-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="a81ac-132">System.Object</span></span>

## <span data-ttu-id="a81ac-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a81ac-133">NOTES</span></span>

## <span data-ttu-id="a81ac-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a81ac-134">RELATED LINKS</span></span>
