---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 88d5e0baadaa625a2cd33a795b66d7484d496330
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274991"
---
# <span data-ttu-id="07de0-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="07de0-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="07de0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07de0-102">SYNOPSIS</span></span>
<span data-ttu-id="07de0-103">Azure olay Kılavuzu etki alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="07de0-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="07de0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07de0-104">SYNTAX</span></span>

### <span data-ttu-id="07de0-105">DomainNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="07de0-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07de0-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="07de0-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07de0-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07de0-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07de0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="07de0-108">DESCRIPTION</span></span>
<span data-ttu-id="07de0-109">Azure olay Kılavuzu etki alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="07de0-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="07de0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07de0-110">EXAMPLES</span></span>

### <span data-ttu-id="07de0-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="07de0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="07de0-112">\` \` Myresourcegroupname kaynak grubundaki olay Kılavuzu etki alanı domain1 \` \` .</span><span class="sxs-lookup"><span data-stu-id="07de0-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="07de0-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="07de0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="07de0-114">\` \` Myresourcegroupname kaynak grubundaki olay Kılavuzu etki alanı domain1 \` \` .</span><span class="sxs-lookup"><span data-stu-id="07de0-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="07de0-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07de0-115">PARAMETERS</span></span>

### <span data-ttu-id="07de0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07de0-116">-DefaultProfile</span></span>
<span data-ttu-id="07de0-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="07de0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07de0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07de0-118">-InputObject</span></span>
<span data-ttu-id="07de0-119">Olay Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="07de0-119">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: DomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07de0-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="07de0-120">-Name</span></span>
<span data-ttu-id="07de0-121">EventGrid etki alanı adı.</span><span class="sxs-lookup"><span data-stu-id="07de0-121">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07de0-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="07de0-122">-PassThru</span></span>
<span data-ttu-id="07de0-123">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="07de0-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="07de0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07de0-124">-ResourceGroupName</span></span>
<span data-ttu-id="07de0-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="07de0-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07de0-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="07de0-126">-ResourceId</span></span>
<span data-ttu-id="07de0-127">Olay Kılavuzu etki alanını temsil eden kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="07de0-127">Resource Identifier representing the Event Grid Domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07de0-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="07de0-128">-Confirm</span></span>
<span data-ttu-id="07de0-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="07de0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07de0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07de0-130">-WhatIf</span></span>
<span data-ttu-id="07de0-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="07de0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07de0-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="07de0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07de0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07de0-133">CommonParameters</span></span>
<span data-ttu-id="07de0-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07de0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07de0-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="07de0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07de0-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07de0-136">INPUTS</span></span>

### <span data-ttu-id="07de0-137">System. String</span><span class="sxs-lookup"><span data-stu-id="07de0-137">System.String</span></span>

### <span data-ttu-id="07de0-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="07de0-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="07de0-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07de0-139">OUTPUTS</span></span>

### <span data-ttu-id="07de0-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="07de0-140">System.Boolean</span></span>

## <span data-ttu-id="07de0-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07de0-141">NOTES</span></span>

## <span data-ttu-id="07de0-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07de0-142">RELATED LINKS</span></span>
