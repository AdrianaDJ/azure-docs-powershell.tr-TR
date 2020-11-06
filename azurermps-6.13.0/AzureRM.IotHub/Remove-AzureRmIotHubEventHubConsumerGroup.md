---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 59e7652d8ca3b2e26246ba4f8924f6a6b9d48f96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588114"
---
# <span data-ttu-id="01e75-101">Remove-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="01e75-101">Remove-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="01e75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01e75-102">SYNOPSIS</span></span>
<span data-ttu-id="01e75-103">Bir eventhub consumergroup öğesini siler.</span><span class="sxs-lookup"><span data-stu-id="01e75-103">Deletes an eventhub consumergroup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01e75-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01e75-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01e75-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="01e75-105">DESCRIPTION</span></span>
<span data-ttu-id="01e75-106">Bir eventhub consumergroup öğesini siler.</span><span class="sxs-lookup"><span data-stu-id="01e75-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="01e75-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01e75-107">EXAMPLES</span></span>

### <span data-ttu-id="01e75-108">Örnek 1 telemetri eventhub grubundan eventhub consumergroup öğesini kaldırın</span><span class="sxs-lookup"><span data-stu-id="01e75-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="01e75-109">Myconsumergroup adındaki IotHub adlı</span><span class="sxs-lookup"><span data-stu-id="01e75-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="01e75-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01e75-110">PARAMETERS</span></span>

### <span data-ttu-id="01e75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01e75-111">-DefaultProfile</span></span>
<span data-ttu-id="01e75-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="01e75-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01e75-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="01e75-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="01e75-114">EventHub ConsumerGroup adı.</span><span class="sxs-lookup"><span data-stu-id="01e75-114">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="01e75-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="01e75-115">-EventHubEndpointName</span></span>
<span data-ttu-id="01e75-116">EventHub uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="01e75-116">EventHub Endpoint Name.</span></span>
<span data-ttu-id="01e75-117">Olası değer olayları, Operationsmenıtoringevents</span><span class="sxs-lookup"><span data-stu-id="01e75-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="01e75-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="01e75-118">-Name</span></span>
<span data-ttu-id="01e75-119">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="01e75-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="01e75-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01e75-120">-ResourceGroupName</span></span>
<span data-ttu-id="01e75-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="01e75-121">Resource Group Name</span></span>

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

### <span data-ttu-id="01e75-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="01e75-122">-Confirm</span></span>
<span data-ttu-id="01e75-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="01e75-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01e75-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01e75-124">-WhatIf</span></span>
<span data-ttu-id="01e75-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="01e75-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01e75-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="01e75-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01e75-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01e75-127">CommonParameters</span></span>
<span data-ttu-id="01e75-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01e75-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01e75-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01e75-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01e75-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01e75-130">INPUTS</span></span>

### <span data-ttu-id="01e75-131">System. String</span><span class="sxs-lookup"><span data-stu-id="01e75-131">System.String</span></span>

## <span data-ttu-id="01e75-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01e75-132">OUTPUTS</span></span>

### <span data-ttu-id="01e75-133">System. String</span><span class="sxs-lookup"><span data-stu-id="01e75-133">System.String</span></span>

## <span data-ttu-id="01e75-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01e75-134">NOTES</span></span>

## <span data-ttu-id="01e75-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01e75-135">RELATED LINKS</span></span>
