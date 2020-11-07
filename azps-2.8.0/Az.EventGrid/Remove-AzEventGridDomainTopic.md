---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
ms.openlocfilehash: 04bed413aca213a558ab1e0afaf5e6badcf238c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751992"
---
# <span data-ttu-id="f5061-101">Remove-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="f5061-101">Remove-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="f5061-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5061-102">SYNOPSIS</span></span>
<span data-ttu-id="f5061-103">Bir Azure olay Kılavuzu etki alanı konusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f5061-103">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="f5061-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5061-104">SYNTAX</span></span>

### <span data-ttu-id="f5061-105">DomainTopicNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f5061-105">DomainTopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5061-106">Resourceıddomaintopicparameterset</span><span class="sxs-lookup"><span data-stu-id="f5061-106">ResourceIdDomainTopicParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5061-107">DomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5061-107">DomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-InputObject] <PSDomainTopic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5061-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5061-108">DESCRIPTION</span></span>
<span data-ttu-id="f5061-109">Bir Azure olay Kılavuzu etki alanı konusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f5061-109">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="f5061-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5061-110">EXAMPLES</span></span>

### <span data-ttu-id="f5061-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f5061-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1
```

<span data-ttu-id="f5061-112">\` \` \` \` Myresourcegroupname kaynak grubundaki konu1 etki alanı domain1 altındaki olay \` Kılavuzu etki alanı konu başlığını kaldırır \` .</span><span class="sxs-lookup"><span data-stu-id="f5061-112">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="f5061-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f5061-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/Topic1" | Remove-AzEventGridDomainTopic
```

<span data-ttu-id="f5061-114">\` \` \` \` Myresourcegroupname kaynak grubundaki konu1 etki alanı domain1 altındaki olay \` Kılavuzu etki alanı konu başlığını kaldırır \` .</span><span class="sxs-lookup"><span data-stu-id="f5061-114">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="f5061-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5061-115">PARAMETERS</span></span>

### <span data-ttu-id="f5061-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5061-116">-DefaultProfile</span></span>
<span data-ttu-id="f5061-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f5061-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5061-118">-EtkiAlanıAdı</span><span class="sxs-lookup"><span data-stu-id="f5061-118">-DomainName</span></span>
<span data-ttu-id="f5061-119">EventGrid etki alanı adı.</span><span class="sxs-lookup"><span data-stu-id="f5061-119">EventGrid domain name.</span></span>

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

### <span data-ttu-id="f5061-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5061-120">-InputObject</span></span>
<span data-ttu-id="f5061-121">EventGrid etki alanı konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f5061-121">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="f5061-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="f5061-122">-Name</span></span>
<span data-ttu-id="f5061-123">EventGrid etki alanı konu adı.</span><span class="sxs-lookup"><span data-stu-id="f5061-123">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="f5061-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f5061-124">-PassThru</span></span>
<span data-ttu-id="f5061-125">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="f5061-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f5061-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5061-126">-ResourceGroupName</span></span>
<span data-ttu-id="f5061-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f5061-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="f5061-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f5061-128">-ResourceId</span></span>
<span data-ttu-id="f5061-129">Olay Kılavuzu etki alanı konusunu temsil eden kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="f5061-129">Resource Identifier representing the Event Grid Domain Topic.</span></span>

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

### <span data-ttu-id="f5061-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="f5061-130">-Confirm</span></span>
<span data-ttu-id="f5061-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f5061-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5061-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5061-132">-WhatIf</span></span>
<span data-ttu-id="f5061-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f5061-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5061-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f5061-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5061-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5061-135">CommonParameters</span></span>
<span data-ttu-id="f5061-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5061-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5061-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5061-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5061-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5061-138">INPUTS</span></span>

### <span data-ttu-id="f5061-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f5061-139">System.String</span></span>

### <span data-ttu-id="f5061-140">Microsoft.Azure.Commands.EventGrid.Models.PSDOmainkonu başlığı</span><span class="sxs-lookup"><span data-stu-id="f5061-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="f5061-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5061-141">OUTPUTS</span></span>

### <span data-ttu-id="f5061-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5061-142">System.Boolean</span></span>

## <span data-ttu-id="f5061-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5061-143">NOTES</span></span>

## <span data-ttu-id="f5061-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5061-144">RELATED LINKS</span></span>
