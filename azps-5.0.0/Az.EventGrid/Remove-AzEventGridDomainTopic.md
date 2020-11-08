---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
ms.openlocfilehash: 6f50f7e4224affb29584022ea8c61a4c0927a60d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275466"
---
# <span data-ttu-id="cdbc4-101">Remove-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="cdbc4-101">Remove-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="cdbc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdbc4-102">SYNOPSIS</span></span>
<span data-ttu-id="cdbc4-103">Bir Azure olay Kılavuzu etki alanı konusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cdbc4-103">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="cdbc4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cdbc4-104">SYNTAX</span></span>

### <span data-ttu-id="cdbc4-105">DomainTopicNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cdbc4-105">DomainTopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdbc4-106">Resourceıddomaintopicparameterset</span><span class="sxs-lookup"><span data-stu-id="cdbc4-106">ResourceIdDomainTopicParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdbc4-107">DomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdbc4-107">DomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-InputObject] <PSDomainTopic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdbc4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cdbc4-108">DESCRIPTION</span></span>
<span data-ttu-id="cdbc4-109">Bir Azure olay Kılavuzu etki alanı konusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cdbc4-109">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="cdbc4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cdbc4-110">EXAMPLES</span></span>

### <span data-ttu-id="cdbc4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cdbc4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1
```

<span data-ttu-id="cdbc4-112">\` \` \` \` Myresourcegroupname kaynak grubundaki konu1 etki alanı domain1 altındaki olay \` Kılavuzu etki alanı konu başlığını kaldırır \` .</span><span class="sxs-lookup"><span data-stu-id="cdbc4-112">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="cdbc4-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="cdbc4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/Topic1" | Remove-AzEventGridDomainTopic
```

<span data-ttu-id="cdbc4-114">\` \` \` \` Myresourcegroupname kaynak grubundaki konu1 etki alanı domain1 altındaki olay \` Kılavuzu etki alanı konu başlığını kaldırır \` .</span><span class="sxs-lookup"><span data-stu-id="cdbc4-114">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="cdbc4-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cdbc4-115">PARAMETERS</span></span>

### <span data-ttu-id="cdbc4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdbc4-116">-DefaultProfile</span></span>
<span data-ttu-id="cdbc4-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cdbc4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdbc4-118">-EtkiAlanıAdı</span><span class="sxs-lookup"><span data-stu-id="cdbc4-118">-DomainName</span></span>
<span data-ttu-id="cdbc4-119">EventGrid etki alanı adı.</span><span class="sxs-lookup"><span data-stu-id="cdbc4-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdbc4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdbc4-120">-InputObject</span></span>
<span data-ttu-id="cdbc4-121">EventGrid etki alanı konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="cdbc4-121">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: DomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdbc4-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="cdbc4-122">-Name</span></span>
<span data-ttu-id="cdbc4-123">EventGrid etki alanı konu adı.</span><span class="sxs-lookup"><span data-stu-id="cdbc4-123">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdbc4-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cdbc4-124">-PassThru</span></span>
<span data-ttu-id="cdbc4-125">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="cdbc4-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdbc4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdbc4-126">-ResourceGroupName</span></span>
<span data-ttu-id="cdbc4-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="cdbc4-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdbc4-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cdbc4-128">-ResourceId</span></span>
<span data-ttu-id="cdbc4-129">Olay Kılavuzu etki alanı konusunu temsil eden kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="cdbc4-129">Resource Identifier representing the Event Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdbc4-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="cdbc4-130">-Confirm</span></span>
<span data-ttu-id="cdbc4-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cdbc4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdbc4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdbc4-132">-WhatIf</span></span>
<span data-ttu-id="cdbc4-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cdbc4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdbc4-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cdbc4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdbc4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdbc4-135">CommonParameters</span></span>
<span data-ttu-id="cdbc4-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cdbc4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdbc4-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cdbc4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdbc4-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cdbc4-138">INPUTS</span></span>

### <span data-ttu-id="cdbc4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cdbc4-139">System.String</span></span>

### <span data-ttu-id="cdbc4-140">Microsoft.Azure.Commands.EventGrid.Models.PSDOmainkonu başlığı</span><span class="sxs-lookup"><span data-stu-id="cdbc4-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="cdbc4-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cdbc4-141">OUTPUTS</span></span>

### <span data-ttu-id="cdbc4-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cdbc4-142">System.Boolean</span></span>

## <span data-ttu-id="cdbc4-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cdbc4-143">NOTES</span></span>

## <span data-ttu-id="cdbc4-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cdbc4-144">RELATED LINKS</span></span>
