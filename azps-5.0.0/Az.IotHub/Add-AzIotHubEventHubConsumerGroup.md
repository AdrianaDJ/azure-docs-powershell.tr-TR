---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 749bd1329537d165cb7c31850fd15ca23f38db2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277779"
---
# <span data-ttu-id="2467e-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="2467e-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="2467e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2467e-102">SYNOPSIS</span></span>
<span data-ttu-id="2467e-103">Bir eventhub Tüketici grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2467e-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="2467e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2467e-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2467e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2467e-105">DESCRIPTION</span></span>
<span data-ttu-id="2467e-106">Belirtilen IotHub ile ilişkilendirilmiş Eventhub içinde tüketici grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2467e-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="2467e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2467e-107">EXAMPLES</span></span>

### <span data-ttu-id="2467e-108">Örnek 1: telemetri eventhub 'a Tüketici grubu ekleme</span><span class="sxs-lookup"><span data-stu-id="2467e-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="2467e-109">"Myiothub" adındaki telemetri olayları için eventhub 'a "myconsumergroup" adlı yeni bir consumergroup ekler.</span><span class="sxs-lookup"><span data-stu-id="2467e-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="2467e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2467e-110">PARAMETERS</span></span>

### <span data-ttu-id="2467e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2467e-111">-DefaultProfile</span></span>
<span data-ttu-id="2467e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2467e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2467e-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="2467e-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="2467e-114">Eklemek istediğiniz EventHub ConsumerGroup 'un adı.</span><span class="sxs-lookup"><span data-stu-id="2467e-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="2467e-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="2467e-115">-Name</span></span>
<span data-ttu-id="2467e-116">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="2467e-116">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2467e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2467e-117">-ResourceGroupName</span></span>
<span data-ttu-id="2467e-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2467e-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="2467e-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="2467e-119">-Confirm</span></span>
<span data-ttu-id="2467e-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2467e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2467e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2467e-121">-WhatIf</span></span>
<span data-ttu-id="2467e-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2467e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2467e-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2467e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2467e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2467e-124">CommonParameters</span></span>
<span data-ttu-id="2467e-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2467e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2467e-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2467e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2467e-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2467e-127">INPUTS</span></span>

### <span data-ttu-id="2467e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2467e-128">System.String</span></span>

## <span data-ttu-id="2467e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2467e-129">OUTPUTS</span></span>

### <span data-ttu-id="2467e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2467e-130">System.String</span></span>

## <span data-ttu-id="2467e-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2467e-131">NOTES</span></span>

## <span data-ttu-id="2467e-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2467e-132">RELATED LINKS</span></span>
