---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 192a20ee3d49bd79dff833a05ffd3ff98bcc30ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594082"
---
# <span data-ttu-id="fb503-101">Add-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="fb503-101">Add-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="fb503-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb503-102">SYNOPSIS</span></span>
<span data-ttu-id="fb503-103">Bir eventhub Tüketici grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb503-103">Creates an eventhub consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb503-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb503-104">SYNTAX</span></span>

```
Add-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb503-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb503-105">DESCRIPTION</span></span>
<span data-ttu-id="fb503-106">Belirtilen IotHub ile ilişkilendirilmiş Eventhub içinde tüketici grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb503-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="fb503-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb503-107">EXAMPLES</span></span>

### <span data-ttu-id="fb503-108">Örnek 1: telemetri eventhub 'a Tüketici grubu ekleme</span><span class="sxs-lookup"><span data-stu-id="fb503-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="fb503-109">"Myiothub" adındaki telemetri olayları için eventhub 'a "myconsumergroup" adlı yeni bir consumergroup ekler.</span><span class="sxs-lookup"><span data-stu-id="fb503-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

### <span data-ttu-id="fb503-110">Örnek 2: işlemlere izleme eventhub için tüketici grubu ekleme</span><span class="sxs-lookup"><span data-stu-id="fb503-110">Example 2: Add a consumer group to the operations monitoring eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="fb503-111">"Myiothub" adındaki iothub işlemleri izleme olayları için, "myconsumergroup" adlı yeni bir consumergroup öğesini ekler</span><span class="sxs-lookup"><span data-stu-id="fb503-111">Adds a new consumergroup named "myconsumergroup" to the eventhub for operations monitoring events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="fb503-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb503-112">PARAMETERS</span></span>

### <span data-ttu-id="fb503-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb503-113">-DefaultProfile</span></span>
<span data-ttu-id="fb503-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fb503-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb503-115">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="fb503-115">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="fb503-116">Eklemek istediğiniz EventHub ConsumerGroup 'un adı.</span><span class="sxs-lookup"><span data-stu-id="fb503-116">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb503-117">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="fb503-117">-EventHubEndpointName</span></span>
<span data-ttu-id="fb503-118">EventHub uç noktasının adı.</span><span class="sxs-lookup"><span data-stu-id="fb503-118">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="fb503-119">Olası değer olayları, Operationsmenıtoringevents</span><span class="sxs-lookup"><span data-stu-id="fb503-119">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb503-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="fb503-120">-Name</span></span>
<span data-ttu-id="fb503-121">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="fb503-121">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb503-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb503-122">-ResourceGroupName</span></span>
<span data-ttu-id="fb503-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fb503-123">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="fb503-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="fb503-124">-Confirm</span></span>
<span data-ttu-id="fb503-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fb503-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb503-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb503-126">-WhatIf</span></span>
<span data-ttu-id="fb503-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb503-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb503-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fb503-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb503-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb503-129">CommonParameters</span></span>
<span data-ttu-id="fb503-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb503-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb503-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb503-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb503-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb503-132">INPUTS</span></span>

### <span data-ttu-id="fb503-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fb503-133">System.String</span></span>

## <span data-ttu-id="fb503-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb503-134">OUTPUTS</span></span>

### <span data-ttu-id="fb503-135">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fb503-135">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="fb503-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb503-136">NOTES</span></span>

## <span data-ttu-id="fb503-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb503-137">RELATED LINKS</span></span>

