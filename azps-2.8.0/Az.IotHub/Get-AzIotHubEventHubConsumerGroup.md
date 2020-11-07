---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 3905111a0855eef6421a587bc7151b411106d13a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751760"
---
# <span data-ttu-id="b57f8-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b57f8-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="b57f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b57f8-102">SYNOPSIS</span></span>
<span data-ttu-id="b57f8-103">Tüm eventhub consumergroups 'ı alır.</span><span class="sxs-lookup"><span data-stu-id="b57f8-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="b57f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b57f8-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b57f8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b57f8-105">DESCRIPTION</span></span>
<span data-ttu-id="b57f8-106">IotHub tarafından kullanılan farklı EventHubs için tüm eventhub consumergroups 'Leri alır.</span><span class="sxs-lookup"><span data-stu-id="b57f8-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="b57f8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b57f8-107">EXAMPLES</span></span>

### <span data-ttu-id="b57f8-108">Örnek 1 telemetri eventhub için tüm eventhub consumergroups gruplarını alır</span><span class="sxs-lookup"><span data-stu-id="b57f8-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="b57f8-109">İothub adındaki myiothub telemetri eventhub için tüm eventhub consumergroups gruplarını alır</span><span class="sxs-lookup"><span data-stu-id="b57f8-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="b57f8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b57f8-110">PARAMETERS</span></span>

### <span data-ttu-id="b57f8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b57f8-111">-DefaultProfile</span></span>
<span data-ttu-id="b57f8-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b57f8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b57f8-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="b57f8-113">-EventHubEndpointName</span></span>
<span data-ttu-id="b57f8-114">Olay Hub uç noktasının adı.</span><span class="sxs-lookup"><span data-stu-id="b57f8-114">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="b57f8-115">Olası değer olayları, Operationsmenıtoringevents</span><span class="sxs-lookup"><span data-stu-id="b57f8-115">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="b57f8-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="b57f8-116">-Name</span></span>
<span data-ttu-id="b57f8-117">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="b57f8-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="b57f8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b57f8-118">-ResourceGroupName</span></span>
<span data-ttu-id="b57f8-119">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b57f8-119">Resource Group Name</span></span>

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

### <span data-ttu-id="b57f8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b57f8-120">CommonParameters</span></span>
<span data-ttu-id="b57f8-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b57f8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b57f8-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b57f8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b57f8-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b57f8-123">INPUTS</span></span>

### <span data-ttu-id="b57f8-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b57f8-124">System.String</span></span>

## <span data-ttu-id="b57f8-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b57f8-125">OUTPUTS</span></span>

### <span data-ttu-id="b57f8-126">Microsoft. Azure. Commands. Management. IotHub. modeller. Pyetthubconsumergroupınfo</span><span class="sxs-lookup"><span data-stu-id="b57f8-126">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="b57f8-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b57f8-127">NOTES</span></span>

## <span data-ttu-id="b57f8-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b57f8-128">RELATED LINKS</span></span>
