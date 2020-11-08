---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
ms.openlocfilehash: cb898921b7fdfddddc95fc88d49dade4654c7ad2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277439"
---
# <span data-ttu-id="06367-101">Set-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="06367-101">Set-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="06367-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06367-102">SYNOPSIS</span></span>
<span data-ttu-id="06367-103">Belirtilen olay hub 'ı tüketici grubunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="06367-103">Updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="06367-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06367-104">SYNTAX</span></span>

```
Set-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06367-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="06367-105">DESCRIPTION</span></span>
<span data-ttu-id="06367-106">Set-AzEventHubConsumerGroup cmdlet 'i belirtilen olay hub 'ı tüketici grubuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="06367-106">The Set-AzEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="06367-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06367-107">EXAMPLES</span></span>

### <span data-ttu-id="06367-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="06367-108">Example 1</span></span>
```
PS C:\> Set-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="06367-109">Tüketici grubunun Kullanıcı meta verilerini \` myconsumergroupname \` "test" olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="06367-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="06367-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06367-110">PARAMETERS</span></span>

### <span data-ttu-id="06367-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06367-111">-DefaultProfile</span></span>
<span data-ttu-id="06367-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="06367-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06367-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="06367-113">-EventHub</span></span>
<span data-ttu-id="06367-114">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="06367-114">EventHub Name</span></span>

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

### <span data-ttu-id="06367-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="06367-115">-Name</span></span>
<span data-ttu-id="06367-116">ConsumerGroup adı</span><span class="sxs-lookup"><span data-stu-id="06367-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="06367-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="06367-117">-Namespace</span></span>
<span data-ttu-id="06367-118">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="06367-118">Namespace Name</span></span>

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

### <span data-ttu-id="06367-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06367-119">-ResourceGroupName</span></span>
<span data-ttu-id="06367-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="06367-120">Resource Group Name</span></span>

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

### <span data-ttu-id="06367-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="06367-121">-UserMetadata</span></span>
<span data-ttu-id="06367-122">ConsumerGroup için Kullanıcı meta verileri</span><span class="sxs-lookup"><span data-stu-id="06367-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="06367-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="06367-123">-Confirm</span></span>
<span data-ttu-id="06367-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="06367-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06367-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06367-125">-WhatIf</span></span>
<span data-ttu-id="06367-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="06367-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06367-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="06367-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06367-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06367-128">CommonParameters</span></span>
<span data-ttu-id="06367-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06367-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06367-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06367-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06367-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06367-131">INPUTS</span></span>

### <span data-ttu-id="06367-132">System. String</span><span class="sxs-lookup"><span data-stu-id="06367-132">System.String</span></span>

## <span data-ttu-id="06367-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06367-133">OUTPUTS</span></span>

### <span data-ttu-id="06367-134">Microsoft. Azure. Commands. EventHub. modeller. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="06367-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="06367-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06367-135">NOTES</span></span>

## <span data-ttu-id="06367-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06367-136">RELATED LINKS</span></span>
