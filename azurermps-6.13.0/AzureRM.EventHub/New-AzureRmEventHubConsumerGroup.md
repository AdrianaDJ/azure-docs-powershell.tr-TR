---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 34a59f0530ed036397523e3810d68175e7ee2d3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587235"
---
# <span data-ttu-id="cab72-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="cab72-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="cab72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cab72-102">SYNOPSIS</span></span>
<span data-ttu-id="cab72-103">Belirtilen olay hub 'ı için yeni bir tüketici grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cab72-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cab72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cab72-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cab72-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cab72-105">DESCRIPTION</span></span>
<span data-ttu-id="cab72-106">Belirtilen olay hub 'ı için yeni bir tüketici grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cab72-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="cab72-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cab72-107">EXAMPLES</span></span>

### <span data-ttu-id="cab72-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cab72-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="cab72-109">\` \` \` \` \` \` Myresourcegroupname kaynak grubuyla, mynamespacename ad alanı kapsamındaki Olay Hub myeventhubname ile tüketici \` \` grubu 'nu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cab72-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="cab72-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cab72-110">PARAMETERS</span></span>

### <span data-ttu-id="cab72-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab72-111">-DefaultProfile</span></span>
<span data-ttu-id="cab72-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cab72-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cab72-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="cab72-113">-EventHub</span></span>
<span data-ttu-id="cab72-114">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="cab72-114">EventHub Name</span></span>

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

### <span data-ttu-id="cab72-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="cab72-115">-Name</span></span>
<span data-ttu-id="cab72-116">ConsumerGroup adı</span><span class="sxs-lookup"><span data-stu-id="cab72-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="cab72-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cab72-117">-Namespace</span></span>
<span data-ttu-id="cab72-118">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="cab72-118">Namespace Name</span></span>

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

### <span data-ttu-id="cab72-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cab72-119">-ResourceGroupName</span></span>
<span data-ttu-id="cab72-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="cab72-120">Resource Group Name</span></span>

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

### <span data-ttu-id="cab72-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="cab72-121">-UserMetadata</span></span>
<span data-ttu-id="cab72-122">ConsumerGroup için Kullanıcı meta verileri</span><span class="sxs-lookup"><span data-stu-id="cab72-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="cab72-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="cab72-123">-Confirm</span></span>
<span data-ttu-id="cab72-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cab72-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cab72-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cab72-125">-WhatIf</span></span>
<span data-ttu-id="cab72-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cab72-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cab72-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cab72-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cab72-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab72-128">CommonParameters</span></span>
<span data-ttu-id="cab72-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cab72-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab72-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cab72-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab72-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cab72-131">INPUTS</span></span>

### <span data-ttu-id="cab72-132">System. String</span><span class="sxs-lookup"><span data-stu-id="cab72-132">System.String</span></span>

## <span data-ttu-id="cab72-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cab72-133">OUTPUTS</span></span>

### <span data-ttu-id="cab72-134">Microsoft. Azure. Commands. EventHub. modeller. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="cab72-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="cab72-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cab72-135">NOTES</span></span>

## <span data-ttu-id="cab72-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cab72-136">RELATED LINKS</span></span>
