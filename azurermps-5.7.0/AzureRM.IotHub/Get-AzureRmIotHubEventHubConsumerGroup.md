---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 62704390e28f6f6a256b2202a61d1e400de7f7e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590463"
---
# <span data-ttu-id="f72df-101">Get-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="f72df-101">Get-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="f72df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f72df-102">SYNOPSIS</span></span>
<span data-ttu-id="f72df-103">Tüm eventhub consumergroups 'ı alır.</span><span class="sxs-lookup"><span data-stu-id="f72df-103">Gets all the eventhub consumergroups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f72df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f72df-104">SYNTAX</span></span>

```
Get-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f72df-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f72df-105">DESCRIPTION</span></span>
<span data-ttu-id="f72df-106">IotHub tarafından kullanılan farklı EventHubs için tüm eventhub consumergroups 'Leri alır.</span><span class="sxs-lookup"><span data-stu-id="f72df-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="f72df-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f72df-107">EXAMPLES</span></span>

### <span data-ttu-id="f72df-108">Örnek 1 telemetri eventhub için tüm eventhub consumergroups gruplarını alır</span><span class="sxs-lookup"><span data-stu-id="f72df-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="f72df-109">İothub adındaki myiothub telemetri eventhub için tüm eventhub consumergroups gruplarını alır</span><span class="sxs-lookup"><span data-stu-id="f72df-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

### <span data-ttu-id="f72df-110">Örnek 2, operationsmonitoring eventhub için tüm eventhub consumergroups gruplarını alır</span><span class="sxs-lookup"><span data-stu-id="f72df-110">Example 2 Gets all the eventhub consumergroups for the operationsmonitoring eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents"
```

<span data-ttu-id="f72df-111">İothub adlı myiothub için Operationsmon ıtoringevents eventhub için tüm eventhub consumergroups 'leri alır</span><span class="sxs-lookup"><span data-stu-id="f72df-111">Gets all the eventhub consumergroups for the operationsMonitoringEvents eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="f72df-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f72df-112">PARAMETERS</span></span>

### <span data-ttu-id="f72df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f72df-113">-DefaultProfile</span></span>
<span data-ttu-id="f72df-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f72df-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f72df-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="f72df-115">-EventHubEndpointName</span></span>
<span data-ttu-id="f72df-116">Olay Hub uç noktasının adı.</span><span class="sxs-lookup"><span data-stu-id="f72df-116">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="f72df-117">Olası değer olayları, Operationsmenıtoringevents</span><span class="sxs-lookup"><span data-stu-id="f72df-117">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f72df-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="f72df-118">-Name</span></span>
<span data-ttu-id="f72df-119">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="f72df-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="f72df-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f72df-120">-ResourceGroupName</span></span>
<span data-ttu-id="f72df-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="f72df-121">Resource Group Name</span></span>

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

### <span data-ttu-id="f72df-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f72df-122">CommonParameters</span></span>
<span data-ttu-id="f72df-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f72df-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f72df-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f72df-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f72df-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f72df-125">INPUTS</span></span>

### <span data-ttu-id="f72df-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f72df-126">System.String</span></span>

## <span data-ttu-id="f72df-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f72df-127">OUTPUTS</span></span>

### <span data-ttu-id="f72df-128">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f72df-128">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f72df-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f72df-129">NOTES</span></span>

## <span data-ttu-id="f72df-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f72df-130">RELATED LINKS</span></span>

