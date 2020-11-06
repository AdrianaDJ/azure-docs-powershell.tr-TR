---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
ms.openlocfilehash: a20262e1414b8f747e638f22283aed26b5483896
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590940"
---
# <span data-ttu-id="cfa68-101">New-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="cfa68-101">New-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="cfa68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfa68-102">SYNOPSIS</span></span>
<span data-ttu-id="cfa68-103">Yeni bir Azure olay Kılavuzu konusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cfa68-103">Creates a new Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfa68-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cfa68-104">SYNTAX</span></span>

```
New-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfa68-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cfa68-105">DESCRIPTION</span></span>
<span data-ttu-id="cfa68-106">Yeni bir Azure olay Kılavuzu konusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cfa68-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="cfa68-107">Konu oluşturulduğunda, bir uygulama etkinlikleri konu noktasında yayımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="cfa68-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="cfa68-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cfa68-108">EXAMPLES</span></span>

### <span data-ttu-id="cfa68-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cfa68-109">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="cfa68-110">\` \` \` \` Myresourcegroupname kaynak grubunda belirtilen coğrafi konum Westus2 konu1 \` bir etkinlik Kılavuzu konusu oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="cfa68-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="cfa68-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="cfa68-111">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="cfa68-112">\` \` \` Belirtilen ( \` \` \` "Bölüm" ve "ortam" etiketli kaynak grubundaki belirtilen coğrafi konum westus2 konu1 bir etkinlik Kılavuzu konusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cfa68-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="cfa68-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cfa68-113">PARAMETERS</span></span>

### <span data-ttu-id="cfa68-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfa68-114">-DefaultProfile</span></span>
<span data-ttu-id="cfa68-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cfa68-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cfa68-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="cfa68-116">-Location</span></span>
<span data-ttu-id="cfa68-117">Konunun konumu</span><span class="sxs-lookup"><span data-stu-id="cfa68-117">The location of the topic</span></span>

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

### <span data-ttu-id="cfa68-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="cfa68-118">-Name</span></span>
<span data-ttu-id="cfa68-119">Konunun adı.</span><span class="sxs-lookup"><span data-stu-id="cfa68-119">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa68-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfa68-120">-ResourceGroupName</span></span>
<span data-ttu-id="cfa68-121">Konunun oluşturulması gereken kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="cfa68-121">The resource group in which the topic should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa68-122">Etiketli</span><span class="sxs-lookup"><span data-stu-id="cfa68-122">-Tag</span></span>
<span data-ttu-id="cfa68-123">Kaynak etiketlerini temsil eden hashtables 'lar.</span><span class="sxs-lookup"><span data-stu-id="cfa68-123">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa68-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="cfa68-124">-Confirm</span></span>
<span data-ttu-id="cfa68-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cfa68-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfa68-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfa68-126">-WhatIf</span></span>
<span data-ttu-id="cfa68-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cfa68-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfa68-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cfa68-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfa68-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfa68-129">CommonParameters</span></span>
<span data-ttu-id="cfa68-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cfa68-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfa68-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfa68-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfa68-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cfa68-132">INPUTS</span></span>

### <span data-ttu-id="cfa68-133">System. String</span><span class="sxs-lookup"><span data-stu-id="cfa68-133">System.String</span></span>

### <span data-ttu-id="cfa68-134">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cfa68-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cfa68-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cfa68-135">OUTPUTS</span></span>

### <span data-ttu-id="cfa68-136">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="cfa68-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="cfa68-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cfa68-137">NOTES</span></span>

## <span data-ttu-id="cfa68-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cfa68-138">RELATED LINKS</span></span>
