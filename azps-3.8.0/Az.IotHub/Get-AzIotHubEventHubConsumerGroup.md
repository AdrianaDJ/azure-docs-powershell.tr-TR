---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: dc401fc74aff737b92cfe7164c19862678a3e1c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098467"
---
# <span data-ttu-id="492b6-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="492b6-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="492b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="492b6-102">SYNOPSIS</span></span>
<span data-ttu-id="492b6-103">Tüm eventhub consumergroups 'ı alır.</span><span class="sxs-lookup"><span data-stu-id="492b6-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="492b6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="492b6-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="492b6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="492b6-105">DESCRIPTION</span></span>
<span data-ttu-id="492b6-106">IotHub tarafından kullanılan farklı EventHubs için tüm eventhub consumergroups 'Leri alır.</span><span class="sxs-lookup"><span data-stu-id="492b6-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="492b6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="492b6-107">EXAMPLES</span></span>

### <span data-ttu-id="492b6-108">Örnek 1 telemetri eventhub için tüm eventhub consumergroups gruplarını alır</span><span class="sxs-lookup"><span data-stu-id="492b6-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="492b6-109">İothub adındaki myiothub telemetri eventhub için tüm eventhub consumergroups gruplarını alır</span><span class="sxs-lookup"><span data-stu-id="492b6-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="492b6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="492b6-110">PARAMETERS</span></span>

### <span data-ttu-id="492b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="492b6-111">-DefaultProfile</span></span>
<span data-ttu-id="492b6-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="492b6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="492b6-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="492b6-113">-Name</span></span>
<span data-ttu-id="492b6-114">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="492b6-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="492b6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="492b6-115">-ResourceGroupName</span></span>
<span data-ttu-id="492b6-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="492b6-116">Resource Group Name</span></span>

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

### <span data-ttu-id="492b6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="492b6-117">CommonParameters</span></span>
<span data-ttu-id="492b6-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="492b6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="492b6-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="492b6-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="492b6-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="492b6-120">INPUTS</span></span>

### <span data-ttu-id="492b6-121">System. String</span><span class="sxs-lookup"><span data-stu-id="492b6-121">System.String</span></span>

## <span data-ttu-id="492b6-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="492b6-122">OUTPUTS</span></span>

### <span data-ttu-id="492b6-123">Microsoft. Azure. Commands. Management. IotHub. modeller. Pyetthubconsumergroupınfo</span><span class="sxs-lookup"><span data-stu-id="492b6-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="492b6-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="492b6-124">NOTES</span></span>

## <span data-ttu-id="492b6-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="492b6-125">RELATED LINKS</span></span>
