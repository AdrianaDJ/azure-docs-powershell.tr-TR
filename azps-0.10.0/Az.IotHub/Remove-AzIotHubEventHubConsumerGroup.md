---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: e2b6bb4c58be90b205fc4a50ddab9c84c0d1ee20
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935825"
---
# <span data-ttu-id="24ef8-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="24ef8-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="24ef8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24ef8-102">SYNOPSIS</span></span>
<span data-ttu-id="24ef8-103">Bir eventhub consumergroup öğesini siler.</span><span class="sxs-lookup"><span data-stu-id="24ef8-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="24ef8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24ef8-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24ef8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="24ef8-105">DESCRIPTION</span></span>
<span data-ttu-id="24ef8-106">Bir eventhub consumergroup öğesini siler.</span><span class="sxs-lookup"><span data-stu-id="24ef8-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="24ef8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24ef8-107">EXAMPLES</span></span>

### <span data-ttu-id="24ef8-108">Örnek 1 telemetri eventhub grubundan eventhub consumergroup öğesini kaldırın</span><span class="sxs-lookup"><span data-stu-id="24ef8-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="24ef8-109">Myconsumergroup adındaki IotHub adlı</span><span class="sxs-lookup"><span data-stu-id="24ef8-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="24ef8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24ef8-110">PARAMETERS</span></span>

### <span data-ttu-id="24ef8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24ef8-111">-DefaultProfile</span></span>
<span data-ttu-id="24ef8-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="24ef8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24ef8-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="24ef8-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="24ef8-114">EventHub ConsumerGroup adı.</span><span class="sxs-lookup"><span data-stu-id="24ef8-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24ef8-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="24ef8-115">-Name</span></span>
<span data-ttu-id="24ef8-116">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="24ef8-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="24ef8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24ef8-117">-ResourceGroupName</span></span>
<span data-ttu-id="24ef8-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="24ef8-118">Resource Group Name</span></span>

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

### <span data-ttu-id="24ef8-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="24ef8-119">-Confirm</span></span>
<span data-ttu-id="24ef8-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="24ef8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24ef8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24ef8-121">-WhatIf</span></span>
<span data-ttu-id="24ef8-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="24ef8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24ef8-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="24ef8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24ef8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24ef8-124">CommonParameters</span></span>
<span data-ttu-id="24ef8-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24ef8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24ef8-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24ef8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24ef8-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24ef8-127">INPUTS</span></span>

### <span data-ttu-id="24ef8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="24ef8-128">System.String</span></span>

## <span data-ttu-id="24ef8-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24ef8-129">OUTPUTS</span></span>

### <span data-ttu-id="24ef8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="24ef8-130">System.String</span></span>

## <span data-ttu-id="24ef8-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24ef8-131">NOTES</span></span>

## <span data-ttu-id="24ef8-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24ef8-132">RELATED LINKS</span></span>