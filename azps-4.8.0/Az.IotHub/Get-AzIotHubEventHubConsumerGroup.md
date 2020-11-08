---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: dc401fc74aff737b92cfe7164c19862678a3e1c6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110001"
---
# <span data-ttu-id="c3d28-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="c3d28-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="c3d28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3d28-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d28-103">Tüm eventhub consumergroups 'ı alır.</span><span class="sxs-lookup"><span data-stu-id="c3d28-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="c3d28-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3d28-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3d28-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3d28-105">DESCRIPTION</span></span>
<span data-ttu-id="c3d28-106">IotHub tarafından kullanılan farklı EventHubs için tüm eventhub consumergroups 'Leri alır.</span><span class="sxs-lookup"><span data-stu-id="c3d28-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="c3d28-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3d28-107">EXAMPLES</span></span>

### <span data-ttu-id="c3d28-108">Örnek 1 telemetri eventhub için tüm eventhub consumergroups gruplarını alır</span><span class="sxs-lookup"><span data-stu-id="c3d28-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="c3d28-109">İothub adındaki myiothub telemetri eventhub için tüm eventhub consumergroups gruplarını alır</span><span class="sxs-lookup"><span data-stu-id="c3d28-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="c3d28-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3d28-110">PARAMETERS</span></span>

### <span data-ttu-id="c3d28-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d28-111">-DefaultProfile</span></span>
<span data-ttu-id="c3d28-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c3d28-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3d28-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="c3d28-113">-Name</span></span>
<span data-ttu-id="c3d28-114">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="c3d28-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="c3d28-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3d28-115">-ResourceGroupName</span></span>
<span data-ttu-id="c3d28-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c3d28-116">Resource Group Name</span></span>

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

### <span data-ttu-id="c3d28-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d28-117">CommonParameters</span></span>
<span data-ttu-id="c3d28-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3d28-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d28-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3d28-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d28-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3d28-120">INPUTS</span></span>

### <span data-ttu-id="c3d28-121">System. String</span><span class="sxs-lookup"><span data-stu-id="c3d28-121">System.String</span></span>

## <span data-ttu-id="c3d28-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3d28-122">OUTPUTS</span></span>

### <span data-ttu-id="c3d28-123">Microsoft. Azure. Commands. Management. IotHub. modeller. Pyetthubconsumergroupınfo</span><span class="sxs-lookup"><span data-stu-id="c3d28-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="c3d28-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3d28-124">NOTES</span></span>

## <span data-ttu-id="c3d28-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3d28-125">RELATED LINKS</span></span>
