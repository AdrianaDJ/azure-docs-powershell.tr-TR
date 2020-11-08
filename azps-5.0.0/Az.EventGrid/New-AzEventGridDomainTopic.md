---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
ms.openlocfilehash: 2923f05bc954c0570c49886c3a036ef78848a1e7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278706"
---
# <span data-ttu-id="6fb62-101">New-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6fb62-101">New-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="6fb62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fb62-102">SYNOPSIS</span></span>
<span data-ttu-id="6fb62-103">Yeni bir Azure olay Kılavuzu etki alanı konusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6fb62-103">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="6fb62-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6fb62-104">SYNTAX</span></span>

```
New-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fb62-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6fb62-105">DESCRIPTION</span></span>
<span data-ttu-id="6fb62-106">Yeni bir Azure olay Kılavuzu etki alanı konusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6fb62-106">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="6fb62-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6fb62-107">EXAMPLES</span></span>

### <span data-ttu-id="6fb62-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6fb62-108">Example 1</span></span>

<span data-ttu-id="6fb62-109">\` \` \` \` Myresourcegroupname kaynak grubu altındaki etki alanı domain1 Konu1 \` bir olay Kılavuzu etki alanı konu başlığı oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="6fb62-109">Creates an Event Grid Domain Topic \`Topic1\` in Domain \`Domain1\` under resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : topic1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/topic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

## <span data-ttu-id="6fb62-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6fb62-110">PARAMETERS</span></span>

### <span data-ttu-id="6fb62-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fb62-111">-DefaultProfile</span></span>
<span data-ttu-id="6fb62-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6fb62-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fb62-113">-EtkiAlanıAdı</span><span class="sxs-lookup"><span data-stu-id="6fb62-113">-DomainName</span></span>
<span data-ttu-id="6fb62-114">EventGrid etki alanı adı.</span><span class="sxs-lookup"><span data-stu-id="6fb62-114">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fb62-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="6fb62-115">-Name</span></span>
<span data-ttu-id="6fb62-116">EventGrid etki alanı konu adı.</span><span class="sxs-lookup"><span data-stu-id="6fb62-116">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fb62-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fb62-117">-ResourceGroupName</span></span>
<span data-ttu-id="6fb62-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6fb62-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="6fb62-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="6fb62-119">-Confirm</span></span>
<span data-ttu-id="6fb62-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6fb62-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fb62-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fb62-121">-WhatIf</span></span>
<span data-ttu-id="6fb62-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6fb62-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fb62-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6fb62-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fb62-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fb62-124">CommonParameters</span></span>
<span data-ttu-id="6fb62-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6fb62-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fb62-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6fb62-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fb62-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6fb62-127">INPUTS</span></span>

### <span data-ttu-id="6fb62-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6fb62-128">System.String</span></span>

## <span data-ttu-id="6fb62-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6fb62-129">OUTPUTS</span></span>

### <span data-ttu-id="6fb62-130">Microsoft.Azure.Commands.EventGrid.Models.PSDOmainkonu başlığı</span><span class="sxs-lookup"><span data-stu-id="6fb62-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="6fb62-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6fb62-131">NOTES</span></span>

## <span data-ttu-id="6fb62-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6fb62-132">RELATED LINKS</span></span>
