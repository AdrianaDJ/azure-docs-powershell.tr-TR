---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 442a88c7fe64fd8913e86ba0ee6be013f226061e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937758"
---
# <span data-ttu-id="fa74d-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="fa74d-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="fa74d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa74d-102">SYNOPSIS</span></span>
<span data-ttu-id="fa74d-103">Yeni bir Azure olay Kılavuzu etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fa74d-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="fa74d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa74d-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa74d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa74d-105">DESCRIPTION</span></span>
<span data-ttu-id="fa74d-106">Yeni bir Azure olay Kılavuzu etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fa74d-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="fa74d-107">Etki alanı oluşturulduktan sonra bir uygulama, konu uç noktasına etkinlik yayımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="fa74d-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="fa74d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa74d-108">EXAMPLES</span></span>

### <span data-ttu-id="fa74d-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fa74d-109">Example 1</span></span>

<span data-ttu-id="fa74d-110">\` \` \` \` Myresourcegroupname kaynak grubunda belirtilen coğrafi konum Westus2 domain1 \` bir olay Kılavuzu etki alanı oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="fa74d-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="fa74d-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="fa74d-111">Example 2</span></span>

<span data-ttu-id="fa74d-112">\` \` \` \` \` \` Belirtilen "Bölüm" ve "ortam" etiketli kaynak grubundaki belirtilen coğrafi konum westus2 domain1 bir olay Kılavuzu etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fa74d-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Department, Finance], [Environment, Test]}
```

## <span data-ttu-id="fa74d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa74d-113">PARAMETERS</span></span>

### <span data-ttu-id="fa74d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa74d-114">-DefaultProfile</span></span>
<span data-ttu-id="fa74d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fa74d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa74d-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="fa74d-116">-Location</span></span>
<span data-ttu-id="fa74d-117">Etki alanının konumu.</span><span class="sxs-lookup"><span data-stu-id="fa74d-117">The location of the domain.</span></span>

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

### <span data-ttu-id="fa74d-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="fa74d-118">-Name</span></span>
<span data-ttu-id="fa74d-119">EventGrid etki alanı adı.</span><span class="sxs-lookup"><span data-stu-id="fa74d-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa74d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa74d-120">-ResourceGroupName</span></span>
<span data-ttu-id="fa74d-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fa74d-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="fa74d-122">Etiketli</span><span class="sxs-lookup"><span data-stu-id="fa74d-122">-Tag</span></span>
<span data-ttu-id="fa74d-123">Kaynak etiketlerini temsil eden Hashtable.</span><span class="sxs-lookup"><span data-stu-id="fa74d-123">Hashtable which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa74d-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="fa74d-124">-Confirm</span></span>
<span data-ttu-id="fa74d-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fa74d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa74d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa74d-126">-WhatIf</span></span>
<span data-ttu-id="fa74d-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fa74d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa74d-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fa74d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa74d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa74d-129">CommonParameters</span></span>
<span data-ttu-id="fa74d-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa74d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa74d-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa74d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa74d-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa74d-132">INPUTS</span></span>

### <span data-ttu-id="fa74d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fa74d-133">System.String</span></span>

### <span data-ttu-id="fa74d-134">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fa74d-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fa74d-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa74d-135">OUTPUTS</span></span>

### <span data-ttu-id="fa74d-136">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="fa74d-136">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="fa74d-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa74d-137">NOTES</span></span>

## <span data-ttu-id="fa74d-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa74d-138">RELATED LINKS</span></span>
