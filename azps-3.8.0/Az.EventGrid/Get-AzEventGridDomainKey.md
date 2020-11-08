---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: f4bc6e7b505f48fe335a5bbc19703032e9ecf06d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096189"
---
# <span data-ttu-id="bfabe-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="bfabe-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="bfabe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfabe-102">SYNOPSIS</span></span>
<span data-ttu-id="bfabe-103">Olay Kılavuzu etki alanında olayları yayımlamak için kullanılan paylaşılan erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="bfabe-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="bfabe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bfabe-104">SYNTAX</span></span>

### <span data-ttu-id="bfabe-105">DomainNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bfabe-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfabe-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfabe-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfabe-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfabe-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bfabe-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bfabe-108">DESCRIPTION</span></span>
<span data-ttu-id="bfabe-109">Olay Kılavuzu etki alanında olayları yayımlamak için kullanılan paylaşılan erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="bfabe-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="bfabe-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bfabe-110">EXAMPLES</span></span>

### <span data-ttu-id="bfabe-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bfabe-111">Example 1</span></span>

<span data-ttu-id="bfabe-112">\` \` Myresourcegroupname kaynak grubundaki olay Kılavuzu etki alanı domain1 paylaşılan erişim anahtarlarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="bfabe-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="bfabe-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="bfabe-113">Example 2</span></span>

<span data-ttu-id="bfabe-114">\` \` Myresourcegroupname kaynak grubundaki olay Kılavuzu etki alanı domain1 paylaşılan erişim anahtarlarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="bfabe-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="bfabe-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bfabe-115">PARAMETERS</span></span>

### <span data-ttu-id="bfabe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfabe-116">-DefaultProfile</span></span>
<span data-ttu-id="bfabe-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bfabe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfabe-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="bfabe-118">-DomainObject</span></span>
<span data-ttu-id="bfabe-119">Olay Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="bfabe-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="bfabe-120">-Domainresourceıd</span><span class="sxs-lookup"><span data-stu-id="bfabe-120">-DomainResourceId</span></span>
<span data-ttu-id="bfabe-121">Olay Kılavuzu etki alanını temsil eden kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="bfabe-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="bfabe-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="bfabe-122">-Name</span></span>
<span data-ttu-id="bfabe-123">EventGrid etki alanı adı.</span><span class="sxs-lookup"><span data-stu-id="bfabe-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfabe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfabe-124">-ResourceGroupName</span></span>
<span data-ttu-id="bfabe-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bfabe-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfabe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfabe-126">CommonParameters</span></span>
<span data-ttu-id="bfabe-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bfabe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfabe-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfabe-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfabe-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bfabe-129">INPUTS</span></span>

### <span data-ttu-id="bfabe-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bfabe-130">System.String</span></span>

### <span data-ttu-id="bfabe-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="bfabe-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="bfabe-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bfabe-132">OUTPUTS</span></span>

### <span data-ttu-id="bfabe-133">Microsoft. Azure. Management. EventGrid. modeller. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="bfabe-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="bfabe-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bfabe-134">NOTES</span></span>

## <span data-ttu-id="bfabe-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bfabe-135">RELATED LINKS</span></span>
