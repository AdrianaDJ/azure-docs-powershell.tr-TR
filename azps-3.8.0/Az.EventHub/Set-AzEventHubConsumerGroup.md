---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
ms.openlocfilehash: cb898921b7fdfddddc95fc88d49dade4654c7ad2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937514"
---
# <span data-ttu-id="65ec4-101">Set-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="65ec4-101">Set-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="65ec4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65ec4-102">SYNOPSIS</span></span>
<span data-ttu-id="65ec4-103">Belirtilen olay hub 'ı tüketici grubunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="65ec4-103">Updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="65ec4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65ec4-104">SYNTAX</span></span>

```
Set-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65ec4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="65ec4-105">DESCRIPTION</span></span>
<span data-ttu-id="65ec4-106">Set-AzEventHubConsumerGroup cmdlet 'i belirtilen olay hub 'ı tüketici grubuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="65ec4-106">The Set-AzEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="65ec4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65ec4-107">EXAMPLES</span></span>

### <span data-ttu-id="65ec4-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="65ec4-108">Example 1</span></span>
```
PS C:\> Set-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="65ec4-109">Tüketici grubunun Kullanıcı meta verilerini \` myconsumergroupname \` "test" olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="65ec4-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="65ec4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65ec4-110">PARAMETERS</span></span>

### <span data-ttu-id="65ec4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65ec4-111">-DefaultProfile</span></span>
<span data-ttu-id="65ec4-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="65ec4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65ec4-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="65ec4-113">-EventHub</span></span>
<span data-ttu-id="65ec4-114">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="65ec4-114">EventHub Name</span></span>

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

### <span data-ttu-id="65ec4-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="65ec4-115">-Name</span></span>
<span data-ttu-id="65ec4-116">ConsumerGroup adı</span><span class="sxs-lookup"><span data-stu-id="65ec4-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="65ec4-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="65ec4-117">-Namespace</span></span>
<span data-ttu-id="65ec4-118">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="65ec4-118">Namespace Name</span></span>

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

### <span data-ttu-id="65ec4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65ec4-119">-ResourceGroupName</span></span>
<span data-ttu-id="65ec4-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="65ec4-120">Resource Group Name</span></span>

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

### <span data-ttu-id="65ec4-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="65ec4-121">-UserMetadata</span></span>
<span data-ttu-id="65ec4-122">ConsumerGroup için Kullanıcı meta verileri</span><span class="sxs-lookup"><span data-stu-id="65ec4-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="65ec4-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="65ec4-123">-Confirm</span></span>
<span data-ttu-id="65ec4-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="65ec4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65ec4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65ec4-125">-WhatIf</span></span>
<span data-ttu-id="65ec4-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="65ec4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65ec4-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="65ec4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65ec4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65ec4-128">CommonParameters</span></span>
<span data-ttu-id="65ec4-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65ec4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65ec4-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65ec4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65ec4-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65ec4-131">INPUTS</span></span>

### <span data-ttu-id="65ec4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="65ec4-132">System.String</span></span>

## <span data-ttu-id="65ec4-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65ec4-133">OUTPUTS</span></span>

### <span data-ttu-id="65ec4-134">Microsoft. Azure. Commands. EventHub. modeller. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="65ec4-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="65ec4-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65ec4-135">NOTES</span></span>

## <span data-ttu-id="65ec4-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65ec4-136">RELATED LINKS</span></span>
