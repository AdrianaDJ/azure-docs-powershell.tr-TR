---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: 3163ba513dea00a052f7042d7575f107421c0a6b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751997"
---
# <span data-ttu-id="0fc5b-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="0fc5b-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="0fc5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fc5b-102">SYNOPSIS</span></span>
<span data-ttu-id="0fc5b-103">Azure olay Kılavuzu konusu için paylaşılan erişim anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0fc5b-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="0fc5b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0fc5b-104">SYNTAX</span></span>

### <span data-ttu-id="0fc5b-105">TopicNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0fc5b-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fc5b-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fc5b-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fc5b-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fc5b-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fc5b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0fc5b-108">DESCRIPTION</span></span>
<span data-ttu-id="0fc5b-109">Azure olay Kılavuzu konusu için paylaşılan erişim anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0fc5b-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="0fc5b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0fc5b-110">EXAMPLES</span></span>

### <span data-ttu-id="0fc5b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0fc5b-111">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="0fc5b-112">\' \` \` Myresourcegroupname kaynak grubundaki anahtar ' \ of olay Kılavuzu konu konu1 ile ilgili anahtarı yeniden oluşturun \` \` .</span><span class="sxs-lookup"><span data-stu-id="0fc5b-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="0fc5b-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0fc5b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="0fc5b-114">\' \` \` Myresourcegroupname kaynak grubundaki anahtar ' \ of olay Kılavuzu konu konu1 ile ilgili anahtarı yeniden oluşturun \` \` .</span><span class="sxs-lookup"><span data-stu-id="0fc5b-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="0fc5b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0fc5b-115">PARAMETERS</span></span>

### <span data-ttu-id="0fc5b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fc5b-116">-DefaultProfile</span></span>
<span data-ttu-id="0fc5b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0fc5b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0fc5b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fc5b-118">-InputObject</span></span>
<span data-ttu-id="0fc5b-119">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0fc5b-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc5b-120">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="0fc5b-120">-KeyName</span></span>
<span data-ttu-id="0fc5b-121">Yeniden oluşturulması gereken anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="0fc5b-121">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="0fc5b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fc5b-122">-ResourceGroupName</span></span>
<span data-ttu-id="0fc5b-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0fc5b-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc5b-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0fc5b-124">-ResourceId</span></span>
<span data-ttu-id="0fc5b-125">Olay Kılavuzu konusunu temsil eden kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="0fc5b-125">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc5b-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="0fc5b-126">-TopicName</span></span>
<span data-ttu-id="0fc5b-127">Konunun adı.</span><span class="sxs-lookup"><span data-stu-id="0fc5b-127">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc5b-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="0fc5b-128">-Confirm</span></span>
<span data-ttu-id="0fc5b-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0fc5b-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc5b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fc5b-130">-WhatIf</span></span>
<span data-ttu-id="0fc5b-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0fc5b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fc5b-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0fc5b-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc5b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fc5b-133">CommonParameters</span></span>
<span data-ttu-id="0fc5b-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0fc5b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fc5b-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fc5b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fc5b-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0fc5b-136">INPUTS</span></span>

### <span data-ttu-id="0fc5b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0fc5b-137">System.String</span></span>

### <span data-ttu-id="0fc5b-138">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="0fc5b-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="0fc5b-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0fc5b-139">OUTPUTS</span></span>

### <span data-ttu-id="0fc5b-140">Microsoft. Azure. Management. EventGrid. modeller. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="0fc5b-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="0fc5b-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0fc5b-141">NOTES</span></span>

## <span data-ttu-id="0fc5b-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0fc5b-142">RELATED LINKS</span></span>