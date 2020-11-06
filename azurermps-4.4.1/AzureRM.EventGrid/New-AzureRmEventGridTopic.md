---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
ms.openlocfilehash: fdd15de19f921781e89d7e24b57e1d82632e4735
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594726"
---
# <span data-ttu-id="d6b60-101">New-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="d6b60-101">New-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="d6b60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6b60-102">SYNOPSIS</span></span>
<span data-ttu-id="d6b60-103">Yeni bir Azure olay Kılavuzu konusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d6b60-103">Creates a new Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6b60-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d6b60-104">SYNTAX</span></span>

```
New-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6b60-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d6b60-105">DESCRIPTION</span></span>
<span data-ttu-id="d6b60-106">Yeni bir Azure olay Kılavuzu konusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d6b60-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="d6b60-107">Konu oluşturulduğunda, bir uygulama etkinlikleri konu noktasında yayımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="d6b60-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="d6b60-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d6b60-108">EXAMPLES</span></span>

### <span data-ttu-id="d6b60-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d6b60-109">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="d6b60-110">\` \` \` \` Myresourcegroupname kaynak grubunda belirtilen coğrafi konum Westus2 konu1 \` bir etkinlik Kılavuzu konusu oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="d6b60-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d6b60-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d6b60-111">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="d6b60-112">\` \` \` Belirtilen ( \` \` \` "Bölüm" ve "ortam" etiketli kaynak grubundaki belirtilen coğrafi konum westus2 konu1 bir etkinlik Kılavuzu konusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d6b60-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="d6b60-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d6b60-113">PARAMETERS</span></span>

### <span data-ttu-id="d6b60-114">-Konum</span><span class="sxs-lookup"><span data-stu-id="d6b60-114">-Location</span></span>
<span data-ttu-id="d6b60-115">Konunun konumu</span><span class="sxs-lookup"><span data-stu-id="d6b60-115">The location of the topic</span></span>

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

### <span data-ttu-id="d6b60-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="d6b60-116">-Name</span></span>
<span data-ttu-id="d6b60-117">Konunun adı.</span><span class="sxs-lookup"><span data-stu-id="d6b60-117">The name of the topic.</span></span>

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

### <span data-ttu-id="d6b60-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6b60-118">-ResourceGroupName</span></span>
<span data-ttu-id="d6b60-119">Konunun oluşturulması gereken kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="d6b60-119">The resource group in which the topic should be created.</span></span>

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

### <span data-ttu-id="d6b60-120">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d6b60-120">-Tag</span></span>
<span data-ttu-id="d6b60-121">Kaynak etiketlerini temsil eden hashtables 'lar.</span><span class="sxs-lookup"><span data-stu-id="d6b60-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="d6b60-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="d6b60-122">-Confirm</span></span>
<span data-ttu-id="d6b60-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d6b60-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6b60-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6b60-124">-WhatIf</span></span>
<span data-ttu-id="d6b60-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d6b60-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6b60-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d6b60-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6b60-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6b60-127">-DefaultProfile</span></span>
<span data-ttu-id="d6b60-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d6b60-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6b60-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6b60-129">CommonParameters</span></span>
<span data-ttu-id="d6b60-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d6b60-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6b60-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6b60-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6b60-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d6b60-132">INPUTS</span></span>

### <span data-ttu-id="d6b60-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d6b60-133">System.String</span></span>
<span data-ttu-id="d6b60-134">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d6b60-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d6b60-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d6b60-135">OUTPUTS</span></span>

### <span data-ttu-id="d6b60-136">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="d6b60-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="d6b60-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d6b60-137">NOTES</span></span>

## <span data-ttu-id="d6b60-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d6b60-138">RELATED LINKS</span></span>

