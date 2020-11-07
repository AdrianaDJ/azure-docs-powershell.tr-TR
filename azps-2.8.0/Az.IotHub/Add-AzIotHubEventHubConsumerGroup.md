---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 938949ae1eada6d85bb6e01728f5be09655c3e06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751779"
---
# <span data-ttu-id="3bcad-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="3bcad-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="3bcad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bcad-102">SYNOPSIS</span></span>
<span data-ttu-id="3bcad-103">Bir eventhub Tüketici grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3bcad-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="3bcad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3bcad-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bcad-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3bcad-105">DESCRIPTION</span></span>
<span data-ttu-id="3bcad-106">Belirtilen IotHub ile ilişkilendirilmiş Eventhub içinde tüketici grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3bcad-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="3bcad-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3bcad-107">EXAMPLES</span></span>

### <span data-ttu-id="3bcad-108">Örnek 1: telemetri eventhub 'a Tüketici grubu ekleme</span><span class="sxs-lookup"><span data-stu-id="3bcad-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="3bcad-109">"Myiothub" adındaki telemetri olayları için eventhub 'a "myconsumergroup" adlı yeni bir consumergroup ekler.</span><span class="sxs-lookup"><span data-stu-id="3bcad-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="3bcad-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3bcad-110">PARAMETERS</span></span>

### <span data-ttu-id="3bcad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bcad-111">-DefaultProfile</span></span>
<span data-ttu-id="3bcad-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3bcad-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3bcad-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="3bcad-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="3bcad-114">Eklemek istediğiniz EventHub ConsumerGroup 'un adı.</span><span class="sxs-lookup"><span data-stu-id="3bcad-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="3bcad-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="3bcad-115">-EventHubEndpointName</span></span>
<span data-ttu-id="3bcad-116">EventHub uç noktasının adı.</span><span class="sxs-lookup"><span data-stu-id="3bcad-116">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="3bcad-117">Olası değer olayları, Operationsmenıtoringevents</span><span class="sxs-lookup"><span data-stu-id="3bcad-117">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bcad-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="3bcad-118">-Name</span></span>
<span data-ttu-id="3bcad-119">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="3bcad-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3bcad-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bcad-120">-ResourceGroupName</span></span>
<span data-ttu-id="3bcad-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3bcad-121">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="3bcad-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="3bcad-122">-Confirm</span></span>
<span data-ttu-id="3bcad-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3bcad-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bcad-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bcad-124">-WhatIf</span></span>
<span data-ttu-id="3bcad-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3bcad-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bcad-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3bcad-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bcad-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bcad-127">CommonParameters</span></span>
<span data-ttu-id="3bcad-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3bcad-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bcad-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bcad-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bcad-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3bcad-130">INPUTS</span></span>

### <span data-ttu-id="3bcad-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3bcad-131">System.String</span></span>

## <span data-ttu-id="3bcad-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3bcad-132">OUTPUTS</span></span>

### <span data-ttu-id="3bcad-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3bcad-133">System.String</span></span>

## <span data-ttu-id="3bcad-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3bcad-134">NOTES</span></span>

## <span data-ttu-id="3bcad-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3bcad-135">RELATED LINKS</span></span>
