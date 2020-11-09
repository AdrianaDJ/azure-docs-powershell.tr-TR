---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 01fa891933c8c3e3c0b4681a84d17b95ea06a6b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324319"
---
# <span data-ttu-id="01208-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="01208-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="01208-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01208-102">SYNOPSIS</span></span>
<span data-ttu-id="01208-103">Bir taşıma koleksiyonu oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="01208-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="01208-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01208-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="01208-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="01208-105">DESCRIPTION</span></span>
<span data-ttu-id="01208-106">Bir taşıma koleksiyonu oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="01208-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="01208-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01208-107">EXAMPLES</span></span>

### <span data-ttu-id="01208-108">Örnek 1: yeni bir taşıma koleksiyonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="01208-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name PS-centralus-westcentralus-demoRM  -ResourceGroupName RG-MoveCollection-demoRM -SourceRegion centralus -TargetRegion westcentralus -Location eastus2

Location Name                               Type
-------- ----                               ----
eastus2  PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
```

<span data-ttu-id="01208-109">Abonelik içinde yeni bir taşıma koleksiyonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="01208-109">Create a new Move collection within a subscription.</span></span>

## <span data-ttu-id="01208-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01208-110">PARAMETERS</span></span>

### <span data-ttu-id="01208-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01208-111">-DefaultProfile</span></span>
<span data-ttu-id="01208-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="01208-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01208-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="01208-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="01208-114">Anapara kimliği alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="01208-114">Gets or sets the principal id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01208-115">-Identitytenantıd</span><span class="sxs-lookup"><span data-stu-id="01208-115">-IdentityTenantId</span></span>
<span data-ttu-id="01208-116">Kiracı kimliğini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="01208-116">Gets or sets the tenant id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01208-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="01208-117">-IdentityType</span></span>
<span data-ttu-id="01208-118">Bölge taşıma hizmeti için kullanılan kimliğin türü.</span><span class="sxs-lookup"><span data-stu-id="01208-118">The type of identity used for the region move service.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.ResourceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01208-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="01208-119">-Location</span></span>
<span data-ttu-id="01208-120">Kaynağın yaşadığı coğrafi konum.</span><span class="sxs-lookup"><span data-stu-id="01208-120">The geo-location where the resource lives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01208-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="01208-121">-Name</span></span>
<span data-ttu-id="01208-122">Koleksiyon adını taşıma.</span><span class="sxs-lookup"><span data-stu-id="01208-122">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01208-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01208-123">-ResourceGroupName</span></span>
<span data-ttu-id="01208-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="01208-124">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01208-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="01208-125">-SourceRegion</span></span>
<span data-ttu-id="01208-126">Kaynak bölgeyi alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="01208-126">Gets or sets the source region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01208-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="01208-127">-SubscriptionId</span></span>
<span data-ttu-id="01208-128">Abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="01208-128">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01208-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="01208-129">-Tag</span></span>
<span data-ttu-id="01208-130">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="01208-130">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01208-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="01208-131">-TargetRegion</span></span>
<span data-ttu-id="01208-132">Hedef bölgeyi alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="01208-132">Gets or sets the target region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01208-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="01208-133">-Confirm</span></span>
<span data-ttu-id="01208-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="01208-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01208-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01208-135">-WhatIf</span></span>
<span data-ttu-id="01208-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="01208-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01208-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="01208-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01208-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01208-138">CommonParameters</span></span>
<span data-ttu-id="01208-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01208-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01208-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="01208-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01208-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01208-141">INPUTS</span></span>

## <span data-ttu-id="01208-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01208-142">OUTPUTS</span></span>

### <span data-ttu-id="01208-143">Microsoft. Azure. PowerShell. cmdlet. Kaynaktaşıyıcısı. modeller. Api20191001Preview. ımovecollection</span><span class="sxs-lookup"><span data-stu-id="01208-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="01208-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01208-144">NOTES</span></span>

<span data-ttu-id="01208-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="01208-145">ALIASES</span></span>

## <span data-ttu-id="01208-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01208-146">RELATED LINKS</span></span>

