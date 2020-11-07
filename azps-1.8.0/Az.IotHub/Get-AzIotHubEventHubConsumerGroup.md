---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 065c2e185be1a9cdc0f495b61104f659076b54b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916476"
---
# <span data-ttu-id="fea3e-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="fea3e-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="fea3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fea3e-102">SYNOPSIS</span></span>
<span data-ttu-id="fea3e-103">Tüm eventhub consumergroups 'ı alır.</span><span class="sxs-lookup"><span data-stu-id="fea3e-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="fea3e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fea3e-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fea3e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fea3e-105">DESCRIPTION</span></span>
<span data-ttu-id="fea3e-106">IotHub tarafından kullanılan farklı EventHubs için tüm eventhub consumergroups 'Leri alır.</span><span class="sxs-lookup"><span data-stu-id="fea3e-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="fea3e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fea3e-107">EXAMPLES</span></span>

### <span data-ttu-id="fea3e-108">Örnek 1 telemetri eventhub için tüm eventhub consumergroups gruplarını alır</span><span class="sxs-lookup"><span data-stu-id="fea3e-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="fea3e-109">İothub adındaki myiothub telemetri eventhub için tüm eventhub consumergroups gruplarını alır</span><span class="sxs-lookup"><span data-stu-id="fea3e-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

### <span data-ttu-id="fea3e-110">Örnek 2, operationsmonitoring eventhub için tüm eventhub consumergroups gruplarını alır</span><span class="sxs-lookup"><span data-stu-id="fea3e-110">Example 2 Gets all the eventhub consumergroups for the operationsmonitoring eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents"
```

<span data-ttu-id="fea3e-111">İothub adlı myiothub için Operationsmon ıtoringevents eventhub için tüm eventhub consumergroups 'leri alır</span><span class="sxs-lookup"><span data-stu-id="fea3e-111">Gets all the eventhub consumergroups for the operationsMonitoringEvents eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="fea3e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fea3e-112">PARAMETERS</span></span>

### <span data-ttu-id="fea3e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fea3e-113">-DefaultProfile</span></span>
<span data-ttu-id="fea3e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fea3e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fea3e-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="fea3e-115">-EventHubEndpointName</span></span>
<span data-ttu-id="fea3e-116">Olay Hub uç noktasının adı.</span><span class="sxs-lookup"><span data-stu-id="fea3e-116">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="fea3e-117">Olası değer olayları, Operationsmenıtoringevents</span><span class="sxs-lookup"><span data-stu-id="fea3e-117">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea3e-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="fea3e-118">-Name</span></span>
<span data-ttu-id="fea3e-119">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="fea3e-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="fea3e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fea3e-120">-ResourceGroupName</span></span>
<span data-ttu-id="fea3e-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="fea3e-121">Resource Group Name</span></span>

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

### <span data-ttu-id="fea3e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea3e-122">CommonParameters</span></span>
<span data-ttu-id="fea3e-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fea3e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea3e-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fea3e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea3e-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fea3e-125">INPUTS</span></span>

### <span data-ttu-id="fea3e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fea3e-126">System.String</span></span>

## <span data-ttu-id="fea3e-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fea3e-127">OUTPUTS</span></span>

### <span data-ttu-id="fea3e-128">Microsoft. Azure. Commands. Management. IotHub. modeller. Pyetthubconsumergroupınfo</span><span class="sxs-lookup"><span data-stu-id="fea3e-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="fea3e-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fea3e-129">NOTES</span></span>

## <span data-ttu-id="fea3e-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fea3e-130">RELATED LINKS</span></span>
