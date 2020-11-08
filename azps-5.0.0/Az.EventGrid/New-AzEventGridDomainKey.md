---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
ms.openlocfilehash: 6afb01ef46ba4f9c627f20a1c49ab58c2a79f252
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278708"
---
# <span data-ttu-id="bc5a5-101">New-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="bc5a5-101">New-AzEventGridDomainKey</span></span>

## <span data-ttu-id="bc5a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc5a5-102">SYNOPSIS</span></span>
<span data-ttu-id="bc5a5-103">Azure olay Kılavuzu etki alanının paylaşılan erişim anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bc5a5-103">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="bc5a5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc5a5-104">SYNTAX</span></span>

### <span data-ttu-id="bc5a5-105">DomainNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bc5a5-105">DomainNameParameterSet (Default)</span></span>
```
New-AzEventGridDomainKey [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc5a5-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc5a5-106">DomainInputObjectParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainInputObject] <PSDomain>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc5a5-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc5a5-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc5a5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc5a5-108">DESCRIPTION</span></span>
<span data-ttu-id="bc5a5-109">Azure olay Kılavuzu etki alanının paylaşılan erişim anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bc5a5-109">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="bc5a5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc5a5-110">EXAMPLES</span></span>

### <span data-ttu-id="bc5a5-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bc5a5-111">Example 1</span></span>

<span data-ttu-id="bc5a5-112">\' \` \` Myresourcegroupname kaynak grubundaki anahtar ' \ of olay Kılavuzu etki alanı domain1 ile ilgili anahtarı yeniden oluşturun \` \` .</span><span class="sxs-lookup"><span data-stu-id="bc5a5-112">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -DomainName Domain1 -Name key1

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="bc5a5-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="bc5a5-113">Example 2</span></span>

<span data-ttu-id="bc5a5-114">\' \` \` Myresourcegroupname kaynak grubundaki anahtar ' \ of olay Kılavuzu etki alanı domain1 ile ilgili anahtarı yeniden oluşturun \` \` .</span><span class="sxs-lookup"><span data-stu-id="bc5a5-114">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | New-AzEventGridTopicKey -KeyName "key1"

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="bc5a5-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="bc5a5-115">Example 3</span></span>

<span data-ttu-id="bc5a5-116">\' \` \` \` \` Tam kaynak kimliğini kullanarak myresourcegroupname kaynak grubundaki myresourcegroupname anahtar2 anahtarının</span><span class="sxs-lookup"><span data-stu-id="bc5a5-116">Regenerate the key corresponding to key \'key2'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using its full resource Id.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceId /subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1 -KeyName Key2

Key1                                         Key2
----                                         ----
<Old Value for Key1>                        <New Value for Key2>
```

## <span data-ttu-id="bc5a5-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc5a5-117">PARAMETERS</span></span>

### <span data-ttu-id="bc5a5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc5a5-118">-DefaultProfile</span></span>
<span data-ttu-id="bc5a5-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc5a5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc5a5-120">-Domainınputobject</span><span class="sxs-lookup"><span data-stu-id="bc5a5-120">-DomainInputObject</span></span>
<span data-ttu-id="bc5a5-121">Olay Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="bc5a5-121">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="bc5a5-122">-EtkiAlanıAdı</span><span class="sxs-lookup"><span data-stu-id="bc5a5-122">-DomainName</span></span>
<span data-ttu-id="bc5a5-123">EventGrid etki alanı adı.</span><span class="sxs-lookup"><span data-stu-id="bc5a5-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc5a5-124">-Domainresourceıd</span><span class="sxs-lookup"><span data-stu-id="bc5a5-124">-DomainResourceId</span></span>
<span data-ttu-id="bc5a5-125">Olay Kılavuzu etki alanını temsil eden kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="bc5a5-125">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="bc5a5-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="bc5a5-126">-Name</span></span>
<span data-ttu-id="bc5a5-127">Yeniden oluşturulması gereken anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="bc5a5-127">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc5a5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc5a5-128">-ResourceGroupName</span></span>
<span data-ttu-id="bc5a5-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bc5a5-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="bc5a5-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="bc5a5-130">-Confirm</span></span>
<span data-ttu-id="bc5a5-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bc5a5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc5a5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc5a5-132">-WhatIf</span></span>
<span data-ttu-id="bc5a5-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bc5a5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc5a5-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bc5a5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc5a5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc5a5-135">CommonParameters</span></span>
<span data-ttu-id="bc5a5-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc5a5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc5a5-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bc5a5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc5a5-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc5a5-138">INPUTS</span></span>

### <span data-ttu-id="bc5a5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bc5a5-139">System.String</span></span>

### <span data-ttu-id="bc5a5-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="bc5a5-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="bc5a5-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc5a5-141">OUTPUTS</span></span>

### <span data-ttu-id="bc5a5-142">Microsoft. Azure. Management. EventGrid. modeller. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="bc5a5-142">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="bc5a5-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc5a5-143">NOTES</span></span>

## <span data-ttu-id="bc5a5-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc5a5-144">RELATED LINKS</span></span>
