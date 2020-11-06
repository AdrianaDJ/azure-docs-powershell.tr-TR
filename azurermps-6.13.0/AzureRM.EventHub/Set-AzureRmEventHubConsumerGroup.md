---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 52038de3d0bb8f07fdfe5abf0978e306a1959a94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590296"
---
# <span data-ttu-id="99a9c-101">Set-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="99a9c-101">Set-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="99a9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="99a9c-103">Belirtilen olay hub 'ı tüketici grubunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="99a9c-103">Updates the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99a9c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99a9c-104">SYNTAX</span></span>

```
Set-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99a9c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="99a9c-105">DESCRIPTION</span></span>
<span data-ttu-id="99a9c-106">Set-AzureRmEventHubConsumerGroup cmdlet 'i belirtilen olay hub 'ı tüketici grubuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="99a9c-106">The Set-AzureRmEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="99a9c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99a9c-107">EXAMPLES</span></span>

### <span data-ttu-id="99a9c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="99a9c-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="99a9c-109">Tüketici grubunun Kullanıcı meta verilerini \` myconsumergroupname \` "test" olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="99a9c-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="99a9c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99a9c-110">PARAMETERS</span></span>

### <span data-ttu-id="99a9c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99a9c-111">-DefaultProfile</span></span>
<span data-ttu-id="99a9c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="99a9c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99a9c-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="99a9c-113">-EventHub</span></span>
<span data-ttu-id="99a9c-114">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="99a9c-114">EventHub Name</span></span>

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

### <span data-ttu-id="99a9c-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="99a9c-115">-Name</span></span>
<span data-ttu-id="99a9c-116">ConsumerGroup adı</span><span class="sxs-lookup"><span data-stu-id="99a9c-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="99a9c-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="99a9c-117">-Namespace</span></span>
<span data-ttu-id="99a9c-118">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="99a9c-118">Namespace Name</span></span>

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

### <span data-ttu-id="99a9c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99a9c-119">-ResourceGroupName</span></span>
<span data-ttu-id="99a9c-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="99a9c-120">Resource Group Name</span></span>

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

### <span data-ttu-id="99a9c-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="99a9c-121">-UserMetadata</span></span>
<span data-ttu-id="99a9c-122">ConsumerGroup için Kullanıcı meta verileri</span><span class="sxs-lookup"><span data-stu-id="99a9c-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="99a9c-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="99a9c-123">-Confirm</span></span>
<span data-ttu-id="99a9c-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="99a9c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99a9c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99a9c-125">-WhatIf</span></span>
<span data-ttu-id="99a9c-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="99a9c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99a9c-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="99a9c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99a9c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99a9c-128">CommonParameters</span></span>
<span data-ttu-id="99a9c-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99a9c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99a9c-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99a9c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99a9c-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99a9c-131">INPUTS</span></span>

### <span data-ttu-id="99a9c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="99a9c-132">System.String</span></span>

## <span data-ttu-id="99a9c-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99a9c-133">OUTPUTS</span></span>

### <span data-ttu-id="99a9c-134">Microsoft. Azure. Commands. EventHub. modeller. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="99a9c-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="99a9c-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99a9c-135">NOTES</span></span>

## <span data-ttu-id="99a9c-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99a9c-136">RELATED LINKS</span></span>
