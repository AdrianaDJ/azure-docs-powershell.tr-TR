---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
ms.openlocfilehash: badbb8c392e053b1f8d994164183bd593843629e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590938"
---
# <span data-ttu-id="fea14-101">New-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="fea14-101">New-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="fea14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fea14-102">SYNOPSIS</span></span>
<span data-ttu-id="fea14-103">Azure olay Kılavuzu konusu için paylaşılan erişim anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fea14-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fea14-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fea14-104">SYNTAX</span></span>

### <span data-ttu-id="fea14-105">TopicNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fea14-105">TopicNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fea14-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fea14-106">TopicInputObjectParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fea14-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="fea14-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fea14-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fea14-108">DESCRIPTION</span></span>
<span data-ttu-id="fea14-109">Azure olay Kılavuzu konusu için paylaşılan erişim anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fea14-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="fea14-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fea14-110">EXAMPLES</span></span>

### <span data-ttu-id="fea14-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fea14-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="fea14-112">\' \` \` Myresourcegroupname kaynak grubundaki anahtar ' \ of olay Kılavuzu konu konu1 ile ilgili anahtarı yeniden oluşturun \` \` .</span><span class="sxs-lookup"><span data-stu-id="fea14-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="fea14-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="fea14-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzureRmEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="fea14-114">\' \` \` Myresourcegroupname kaynak grubundaki anahtar ' \ of olay Kılavuzu konu konu1 ile ilgili anahtarı yeniden oluşturun \` \` .</span><span class="sxs-lookup"><span data-stu-id="fea14-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="fea14-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fea14-115">PARAMETERS</span></span>

### <span data-ttu-id="fea14-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fea14-116">-DefaultProfile</span></span>
<span data-ttu-id="fea14-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fea14-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fea14-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fea14-118">-InputObject</span></span>
<span data-ttu-id="fea14-119">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fea14-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="fea14-120">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="fea14-120">-KeyName</span></span>
<span data-ttu-id="fea14-121">Yeniden oluşturulması gereken anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="fea14-121">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea14-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fea14-122">-ResourceGroupName</span></span>
<span data-ttu-id="fea14-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="fea14-123">Resource group name.</span></span>

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

### <span data-ttu-id="fea14-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fea14-124">-ResourceId</span></span>
<span data-ttu-id="fea14-125">Olay Kılavuzu konusunu temsil eden kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="fea14-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="fea14-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="fea14-126">-TopicName</span></span>
<span data-ttu-id="fea14-127">Konunun adı.</span><span class="sxs-lookup"><span data-stu-id="fea14-127">The name of the topic.</span></span>

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

### <span data-ttu-id="fea14-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="fea14-128">-Confirm</span></span>
<span data-ttu-id="fea14-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fea14-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fea14-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fea14-130">-WhatIf</span></span>
<span data-ttu-id="fea14-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fea14-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fea14-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fea14-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fea14-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea14-133">CommonParameters</span></span>
<span data-ttu-id="fea14-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fea14-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea14-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fea14-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea14-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fea14-136">INPUTS</span></span>

### <span data-ttu-id="fea14-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fea14-137">System.String</span></span>

### <span data-ttu-id="fea14-138">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="fea14-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="fea14-139">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fea14-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="fea14-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fea14-140">OUTPUTS</span></span>

### <span data-ttu-id="fea14-141">Microsoft. Azure. Management. EventGrid. modeller. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="fea14-141">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="fea14-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fea14-142">NOTES</span></span>

## <span data-ttu-id="fea14-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fea14-143">RELATED LINKS</span></span>
