---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 9fa0a9d85dc9c7b1a6cc56c3c329b1810cceaa18
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103797"
---
# <span data-ttu-id="d9aae-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d9aae-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="d9aae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9aae-102">SYNOPSIS</span></span>
<span data-ttu-id="d9aae-103">Bir eventhub consumergroup öğesini siler.</span><span class="sxs-lookup"><span data-stu-id="d9aae-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="d9aae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9aae-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9aae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9aae-105">DESCRIPTION</span></span>
<span data-ttu-id="d9aae-106">Bir eventhub consumergroup öğesini siler.</span><span class="sxs-lookup"><span data-stu-id="d9aae-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="d9aae-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9aae-107">EXAMPLES</span></span>

### <span data-ttu-id="d9aae-108">Örnek 1 telemetri eventhub grubundan eventhub consumergroup öğesini kaldırın</span><span class="sxs-lookup"><span data-stu-id="d9aae-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="d9aae-109">Myconsumergroup adındaki IotHub adlı</span><span class="sxs-lookup"><span data-stu-id="d9aae-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="d9aae-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9aae-110">PARAMETERS</span></span>

### <span data-ttu-id="d9aae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9aae-111">-DefaultProfile</span></span>
<span data-ttu-id="d9aae-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d9aae-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9aae-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="d9aae-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="d9aae-114">EventHub ConsumerGroup adı.</span><span class="sxs-lookup"><span data-stu-id="d9aae-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9aae-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d9aae-115">-Name</span></span>
<span data-ttu-id="d9aae-116">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="d9aae-116">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9aae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9aae-117">-ResourceGroupName</span></span>
<span data-ttu-id="d9aae-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d9aae-118">Resource Group Name</span></span>

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

### <span data-ttu-id="d9aae-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="d9aae-119">-Confirm</span></span>
<span data-ttu-id="d9aae-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d9aae-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9aae-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9aae-121">-WhatIf</span></span>
<span data-ttu-id="d9aae-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d9aae-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9aae-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d9aae-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9aae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9aae-124">CommonParameters</span></span>
<span data-ttu-id="d9aae-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9aae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9aae-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9aae-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9aae-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9aae-127">INPUTS</span></span>

### <span data-ttu-id="d9aae-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d9aae-128">System.String</span></span>

## <span data-ttu-id="d9aae-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9aae-129">OUTPUTS</span></span>

### <span data-ttu-id="d9aae-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d9aae-130">System.String</span></span>

## <span data-ttu-id="d9aae-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9aae-131">NOTES</span></span>

## <span data-ttu-id="d9aae-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9aae-132">RELATED LINKS</span></span>
