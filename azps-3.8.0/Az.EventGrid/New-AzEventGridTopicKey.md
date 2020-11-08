---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: 8749f5ad542d55f167f866e436acf72aacf3bc14
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096909"
---
# <span data-ttu-id="d7401-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="d7401-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="d7401-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7401-102">SYNOPSIS</span></span>
<span data-ttu-id="d7401-103">Azure olay Kılavuzu konusu için paylaşılan erişim anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d7401-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="d7401-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7401-104">SYNTAX</span></span>

### <span data-ttu-id="d7401-105">TopicNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d7401-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7401-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7401-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7401-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7401-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7401-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7401-108">DESCRIPTION</span></span>
<span data-ttu-id="d7401-109">Azure olay Kılavuzu konusu için paylaşılan erişim anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d7401-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="d7401-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7401-110">EXAMPLES</span></span>

### <span data-ttu-id="d7401-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d7401-111">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="d7401-112">\' \` \` Myresourcegroupname kaynak grubundaki anahtar ' \ of olay Kılavuzu konu konu1 ile ilgili anahtarı yeniden oluşturun \` \` .</span><span class="sxs-lookup"><span data-stu-id="d7401-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d7401-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d7401-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="d7401-114">\' \` \` Myresourcegroupname kaynak grubundaki anahtar ' \ of olay Kılavuzu konu konu1 ile ilgili anahtarı yeniden oluşturun \` \` .</span><span class="sxs-lookup"><span data-stu-id="d7401-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d7401-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7401-115">PARAMETERS</span></span>

### <span data-ttu-id="d7401-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7401-116">-DefaultProfile</span></span>
<span data-ttu-id="d7401-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d7401-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7401-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7401-118">-InputObject</span></span>
<span data-ttu-id="d7401-119">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d7401-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="d7401-120">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="d7401-120">-KeyName</span></span>
<span data-ttu-id="d7401-121">Yeniden oluşturulması gereken anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="d7401-121">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="d7401-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7401-122">-ResourceGroupName</span></span>
<span data-ttu-id="d7401-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d7401-123">Resource group name.</span></span>

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

### <span data-ttu-id="d7401-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d7401-124">-ResourceId</span></span>
<span data-ttu-id="d7401-125">Olay Kılavuzu konusunu temsil eden kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="d7401-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="d7401-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="d7401-126">-TopicName</span></span>
<span data-ttu-id="d7401-127">Konunun adı.</span><span class="sxs-lookup"><span data-stu-id="d7401-127">The name of the topic.</span></span>

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

### <span data-ttu-id="d7401-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="d7401-128">-Confirm</span></span>
<span data-ttu-id="d7401-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d7401-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7401-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7401-130">-WhatIf</span></span>
<span data-ttu-id="d7401-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d7401-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7401-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d7401-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7401-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7401-133">CommonParameters</span></span>
<span data-ttu-id="d7401-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7401-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7401-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7401-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7401-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7401-136">INPUTS</span></span>

### <span data-ttu-id="d7401-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d7401-137">System.String</span></span>

### <span data-ttu-id="d7401-138">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="d7401-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="d7401-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7401-139">OUTPUTS</span></span>

### <span data-ttu-id="d7401-140">Microsoft. Azure. Management. EventGrid. modeller. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="d7401-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="d7401-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7401-141">NOTES</span></span>

## <span data-ttu-id="d7401-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7401-142">RELATED LINKS</span></span>
