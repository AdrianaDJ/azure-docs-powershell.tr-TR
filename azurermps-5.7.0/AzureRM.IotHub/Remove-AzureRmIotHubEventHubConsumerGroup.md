---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 5f4324ab7a27b711d33042eede5c3b88d38c4511
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588915"
---
# <span data-ttu-id="9dd3b-101">Remove-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="9dd3b-101">Remove-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="9dd3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dd3b-102">SYNOPSIS</span></span>
<span data-ttu-id="9dd3b-103">Bir eventhub consumergroup öğesini siler.</span><span class="sxs-lookup"><span data-stu-id="9dd3b-103">Deletes an eventhub consumergroup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9dd3b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9dd3b-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dd3b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9dd3b-105">DESCRIPTION</span></span>
<span data-ttu-id="9dd3b-106">Bir eventhub consumergroup öğesini siler.</span><span class="sxs-lookup"><span data-stu-id="9dd3b-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="9dd3b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9dd3b-107">EXAMPLES</span></span>

### <span data-ttu-id="9dd3b-108">Örnek 1 telemetri eventhub grubundan eventhub consumergroup öğesini kaldırın</span><span class="sxs-lookup"><span data-stu-id="9dd3b-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="9dd3b-109">Myconsumergroup adındaki IotHub adlı</span><span class="sxs-lookup"><span data-stu-id="9dd3b-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="9dd3b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9dd3b-110">PARAMETERS</span></span>

### <span data-ttu-id="9dd3b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dd3b-111">-DefaultProfile</span></span>
<span data-ttu-id="9dd3b-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9dd3b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9dd3b-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="9dd3b-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="9dd3b-114">EventHub ConsumerGroup adı.</span><span class="sxs-lookup"><span data-stu-id="9dd3b-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dd3b-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="9dd3b-115">-EventHubEndpointName</span></span>
<span data-ttu-id="9dd3b-116">EventHub uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="9dd3b-116">EventHub Endpoint Name.</span></span>
<span data-ttu-id="9dd3b-117">Olası değer olayları, Operationsmenıtoringevents</span><span class="sxs-lookup"><span data-stu-id="9dd3b-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="9dd3b-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="9dd3b-118">-Name</span></span>
<span data-ttu-id="9dd3b-119">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="9dd3b-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="9dd3b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dd3b-120">-ResourceGroupName</span></span>
<span data-ttu-id="9dd3b-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="9dd3b-121">Resource Group Name</span></span>

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

### <span data-ttu-id="9dd3b-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="9dd3b-122">-Confirm</span></span>
<span data-ttu-id="9dd3b-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9dd3b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dd3b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dd3b-124">-WhatIf</span></span>
<span data-ttu-id="9dd3b-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9dd3b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dd3b-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9dd3b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dd3b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dd3b-127">CommonParameters</span></span>
<span data-ttu-id="9dd3b-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9dd3b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dd3b-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dd3b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dd3b-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9dd3b-130">INPUTS</span></span>

### <span data-ttu-id="9dd3b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9dd3b-131">System.String</span></span>

## <span data-ttu-id="9dd3b-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9dd3b-132">OUTPUTS</span></span>

### <span data-ttu-id="9dd3b-133">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9dd3b-133">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="9dd3b-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9dd3b-134">NOTES</span></span>

## <span data-ttu-id="9dd3b-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9dd3b-135">RELATED LINKS</span></span>

