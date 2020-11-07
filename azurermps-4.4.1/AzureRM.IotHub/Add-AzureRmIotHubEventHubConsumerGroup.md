---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 19a3098eff598c223014b65381e524d063f7d425
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763366"
---
# <span data-ttu-id="dc0d9-101">Add-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="dc0d9-101">Add-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="dc0d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc0d9-102">SYNOPSIS</span></span>
<span data-ttu-id="dc0d9-103">Bir eventhub Tüketici grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dc0d9-103">Creates an eventhub consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc0d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dc0d9-104">SYNTAX</span></span>

```
Add-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc0d9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dc0d9-105">DESCRIPTION</span></span>
<span data-ttu-id="dc0d9-106">Belirtilen IotHub ile ilişkilendirilmiş Eventhub içinde tüketici grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dc0d9-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="dc0d9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dc0d9-107">EXAMPLES</span></span>

### <span data-ttu-id="dc0d9-108">Örnek 1: telemetri eventhub 'a Tüketici grubu ekleme</span><span class="sxs-lookup"><span data-stu-id="dc0d9-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="dc0d9-109">"Myiothub" adındaki telemetri olayları için eventhub 'a "myconsumergroup" adlı yeni bir consumergroup ekler.</span><span class="sxs-lookup"><span data-stu-id="dc0d9-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

### <span data-ttu-id="dc0d9-110">Örnek 2: işlemlere izleme eventhub için tüketici grubu ekleme</span><span class="sxs-lookup"><span data-stu-id="dc0d9-110">Example 2: Add a consumer group to the operations monitoring eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="dc0d9-111">"Myiothub" adındaki iothub işlemleri izleme olayları için, "myconsumergroup" adlı yeni bir consumergroup öğesini ekler</span><span class="sxs-lookup"><span data-stu-id="dc0d9-111">Adds a new consumergroup named "myconsumergroup" to the eventhub for operations monitoring events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="dc0d9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dc0d9-112">PARAMETERS</span></span>

### <span data-ttu-id="dc0d9-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="dc0d9-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="dc0d9-114">Eklemek istediğiniz EventHub ConsumerGroup 'un adı.</span><span class="sxs-lookup"><span data-stu-id="dc0d9-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0d9-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="dc0d9-115">-EventHubEndpointName</span></span>
<span data-ttu-id="dc0d9-116">EventHub uç noktasının adı.</span><span class="sxs-lookup"><span data-stu-id="dc0d9-116">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="dc0d9-117">Olası değer olayları, Operationsmenıtoringevents</span><span class="sxs-lookup"><span data-stu-id="dc0d9-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="dc0d9-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="dc0d9-118">-Name</span></span>
<span data-ttu-id="dc0d9-119">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="dc0d9-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="dc0d9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc0d9-120">-ResourceGroupName</span></span>
<span data-ttu-id="dc0d9-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="dc0d9-121">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="dc0d9-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="dc0d9-122">-Confirm</span></span>
<span data-ttu-id="dc0d9-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dc0d9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc0d9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc0d9-124">-WhatIf</span></span>
<span data-ttu-id="dc0d9-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dc0d9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc0d9-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dc0d9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc0d9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc0d9-127">-DefaultProfile</span></span>
<span data-ttu-id="dc0d9-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dc0d9-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc0d9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc0d9-129">CommonParameters</span></span>
<span data-ttu-id="dc0d9-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dc0d9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc0d9-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc0d9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc0d9-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dc0d9-132">INPUTS</span></span>

### <span data-ttu-id="dc0d9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dc0d9-133">System.String</span></span>

## <span data-ttu-id="dc0d9-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dc0d9-134">OUTPUTS</span></span>

### <span data-ttu-id="dc0d9-135">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="dc0d9-135">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="dc0d9-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dc0d9-136">NOTES</span></span>

## <span data-ttu-id="dc0d9-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dc0d9-137">RELATED LINKS</span></span>

