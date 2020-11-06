---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
ms.openlocfilehash: bb9cd92ff614a944c144f056d8d59aa1d4239b25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594725"
---
# <span data-ttu-id="a3a85-101">New-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="a3a85-101">New-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="a3a85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3a85-102">SYNOPSIS</span></span>
<span data-ttu-id="a3a85-103">Azure olay Kılavuzu konusu için paylaşılan erişim anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a3a85-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3a85-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3a85-104">SYNTAX</span></span>

### <span data-ttu-id="a3a85-105">TopicNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a3a85-105">TopicNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3a85-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3a85-106">TopicInputObjectParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3a85-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3a85-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3a85-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3a85-108">DESCRIPTION</span></span>
<span data-ttu-id="a3a85-109">Azure olay Kılavuzu konusu için paylaşılan erişim anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a3a85-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="a3a85-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3a85-110">EXAMPLES</span></span>

### <span data-ttu-id="a3a85-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a3a85-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="a3a85-112">\' \` \` Myresourcegroupname kaynak grubundaki anahtar ' \ of olay Kılavuzu konu konu1 ile ilgili anahtarı yeniden oluşturun \` \` .</span><span class="sxs-lookup"><span data-stu-id="a3a85-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a3a85-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a3a85-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzureRmEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="a3a85-114">\' \` \` Myresourcegroupname kaynak grubundaki anahtar ' \ of olay Kılavuzu konu konu1 ile ilgili anahtarı yeniden oluşturun \` \` .</span><span class="sxs-lookup"><span data-stu-id="a3a85-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="a3a85-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3a85-115">PARAMETERS</span></span>

### <span data-ttu-id="a3a85-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3a85-116">-InputObject</span></span>
<span data-ttu-id="a3a85-117">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a3a85-117">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="a3a85-118">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="a3a85-118">-KeyName</span></span>
<span data-ttu-id="a3a85-119">Yeniden oluşturulması gereken anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="a3a85-119">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="a3a85-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3a85-120">-ResourceGroupName</span></span>
<span data-ttu-id="a3a85-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a3a85-121">Resource group name.</span></span>

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

### <span data-ttu-id="a3a85-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a3a85-122">-ResourceId</span></span>
<span data-ttu-id="a3a85-123">Olay Kılavuzu konusunu temsil eden kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="a3a85-123">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="a3a85-124">-TopicName</span><span class="sxs-lookup"><span data-stu-id="a3a85-124">-TopicName</span></span>
<span data-ttu-id="a3a85-125">Konunun adı.</span><span class="sxs-lookup"><span data-stu-id="a3a85-125">The name of the topic.</span></span>

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

### <span data-ttu-id="a3a85-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="a3a85-126">-Confirm</span></span>
<span data-ttu-id="a3a85-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a3a85-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3a85-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3a85-128">-WhatIf</span></span>
<span data-ttu-id="a3a85-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a3a85-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3a85-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a3a85-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3a85-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3a85-131">-DefaultProfile</span></span>
<span data-ttu-id="a3a85-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3a85-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3a85-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3a85-133">CommonParameters</span></span>
<span data-ttu-id="a3a85-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3a85-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3a85-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3a85-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3a85-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3a85-136">INPUTS</span></span>

### <span data-ttu-id="a3a85-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a3a85-137">System.String</span></span>

## <span data-ttu-id="a3a85-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3a85-138">OUTPUTS</span></span>

### <span data-ttu-id="a3a85-139">Microsoft. Azure. Management. EventGrid. modeller. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="a3a85-139">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="a3a85-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3a85-140">NOTES</span></span>

## <span data-ttu-id="a3a85-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3a85-141">RELATED LINKS</span></span>

