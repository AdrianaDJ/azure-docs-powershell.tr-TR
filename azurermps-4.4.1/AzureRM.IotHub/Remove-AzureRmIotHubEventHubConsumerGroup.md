---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: b326f7228a60f7549fc6dcd227b9bad947f22add
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594265"
---
# <span data-ttu-id="5f13e-101">Remove-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5f13e-101">Remove-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="5f13e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f13e-102">SYNOPSIS</span></span>
<span data-ttu-id="5f13e-103">Bir eventhub consumergroup öğesini siler.</span><span class="sxs-lookup"><span data-stu-id="5f13e-103">Deletes an eventhub consumergroup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f13e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f13e-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f13e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f13e-105">DESCRIPTION</span></span>
<span data-ttu-id="5f13e-106">Bir eventhub consumergroup öğesini siler.</span><span class="sxs-lookup"><span data-stu-id="5f13e-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="5f13e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f13e-107">EXAMPLES</span></span>

### <span data-ttu-id="5f13e-108">Örnek 1 telemetri eventhub grubundan eventhub consumergroup öğesini kaldırın</span><span class="sxs-lookup"><span data-stu-id="5f13e-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="5f13e-109">Myconsumergroup adındaki IotHub adlı</span><span class="sxs-lookup"><span data-stu-id="5f13e-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="5f13e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f13e-110">PARAMETERS</span></span>

### <span data-ttu-id="5f13e-111">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="5f13e-111">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="5f13e-112">EventHub ConsumerGroup adı.</span><span class="sxs-lookup"><span data-stu-id="5f13e-112">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f13e-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="5f13e-113">-EventHubEndpointName</span></span>
<span data-ttu-id="5f13e-114">EventHub uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="5f13e-114">EventHub Endpoint Name.</span></span>
<span data-ttu-id="5f13e-115">Olası değer olayları, Operationsmenıtoringevents</span><span class="sxs-lookup"><span data-stu-id="5f13e-115">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f13e-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="5f13e-116">-Name</span></span>
<span data-ttu-id="5f13e-117">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="5f13e-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="5f13e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f13e-118">-ResourceGroupName</span></span>
<span data-ttu-id="5f13e-119">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="5f13e-119">Resource Group Name</span></span>

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

### <span data-ttu-id="5f13e-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="5f13e-120">-Confirm</span></span>
<span data-ttu-id="5f13e-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5f13e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f13e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f13e-122">-WhatIf</span></span>
<span data-ttu-id="5f13e-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5f13e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f13e-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5f13e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f13e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f13e-125">-DefaultProfile</span></span>
<span data-ttu-id="5f13e-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f13e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f13e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f13e-127">CommonParameters</span></span>
<span data-ttu-id="5f13e-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f13e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f13e-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f13e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f13e-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f13e-130">INPUTS</span></span>

### <span data-ttu-id="5f13e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5f13e-131">System.String</span></span>

## <span data-ttu-id="5f13e-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f13e-132">OUTPUTS</span></span>

### <span data-ttu-id="5f13e-133">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="5f13e-133">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="5f13e-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f13e-134">NOTES</span></span>

## <span data-ttu-id="5f13e-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f13e-135">RELATED LINKS</span></span>

