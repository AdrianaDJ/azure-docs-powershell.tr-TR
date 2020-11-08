---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 01fa891933c8c3e3c0b4681a84d17b95ea06a6b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266915"
---
# <span data-ttu-id="3d584-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="3d584-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="3d584-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d584-102">SYNOPSIS</span></span>
<span data-ttu-id="3d584-103">Bir taşıma koleksiyonu oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3d584-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="3d584-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d584-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3d584-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d584-105">DESCRIPTION</span></span>
<span data-ttu-id="3d584-106">Bir taşıma koleksiyonu oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3d584-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="3d584-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d584-107">EXAMPLES</span></span>

### <span data-ttu-id="3d584-108">Örnek 1: yeni bir taşıma koleksiyonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3d584-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name PS-centralus-westcentralus-demoRM  -ResourceGroupName RG-MoveCollection-demoRM -SourceRegion centralus -TargetRegion westcentralus -Location eastus2

Location Name                               Type
-------- ----                               ----
eastus2  PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
```

<span data-ttu-id="3d584-109">Abonelik içinde yeni bir taşıma koleksiyonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3d584-109">Create a new Move collection within a subscription.</span></span>

## <span data-ttu-id="3d584-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d584-110">PARAMETERS</span></span>

### <span data-ttu-id="3d584-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d584-111">-DefaultProfile</span></span>
<span data-ttu-id="3d584-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3d584-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d584-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="3d584-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="3d584-114">Anapara kimliği alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3d584-114">Gets or sets the principal id.</span></span>

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

### <span data-ttu-id="3d584-115">-Identitytenantıd</span><span class="sxs-lookup"><span data-stu-id="3d584-115">-IdentityTenantId</span></span>
<span data-ttu-id="3d584-116">Kiracı kimliğini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3d584-116">Gets or sets the tenant id.</span></span>

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

### <span data-ttu-id="3d584-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="3d584-117">-IdentityType</span></span>
<span data-ttu-id="3d584-118">Bölge taşıma hizmeti için kullanılan kimliğin türü.</span><span class="sxs-lookup"><span data-stu-id="3d584-118">The type of identity used for the region move service.</span></span>

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

### <span data-ttu-id="3d584-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="3d584-119">-Location</span></span>
<span data-ttu-id="3d584-120">Kaynağın yaşadığı coğrafi konum.</span><span class="sxs-lookup"><span data-stu-id="3d584-120">The geo-location where the resource lives.</span></span>

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

### <span data-ttu-id="3d584-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="3d584-121">-Name</span></span>
<span data-ttu-id="3d584-122">Koleksiyon adını taşıma.</span><span class="sxs-lookup"><span data-stu-id="3d584-122">The Move Collection Name.</span></span>

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

### <span data-ttu-id="3d584-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d584-123">-ResourceGroupName</span></span>
<span data-ttu-id="3d584-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3d584-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="3d584-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="3d584-125">-SourceRegion</span></span>
<span data-ttu-id="3d584-126">Kaynak bölgeyi alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3d584-126">Gets or sets the source region.</span></span>

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

### <span data-ttu-id="3d584-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="3d584-127">-SubscriptionId</span></span>
<span data-ttu-id="3d584-128">Abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3d584-128">The Subscription ID.</span></span>

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

### <span data-ttu-id="3d584-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3d584-129">-Tag</span></span>
<span data-ttu-id="3d584-130">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="3d584-130">Resource tags.</span></span>

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

### <span data-ttu-id="3d584-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="3d584-131">-TargetRegion</span></span>
<span data-ttu-id="3d584-132">Hedef bölgeyi alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3d584-132">Gets or sets the target region.</span></span>

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

### <span data-ttu-id="3d584-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="3d584-133">-Confirm</span></span>
<span data-ttu-id="3d584-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3d584-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d584-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d584-135">-WhatIf</span></span>
<span data-ttu-id="3d584-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d584-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d584-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3d584-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d584-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d584-138">CommonParameters</span></span>
<span data-ttu-id="3d584-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d584-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d584-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3d584-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d584-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d584-141">INPUTS</span></span>

## <span data-ttu-id="3d584-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d584-142">OUTPUTS</span></span>

### <span data-ttu-id="3d584-143">Microsoft. Azure. PowerShell. cmdlet. Kaynaktaşıyıcısı. modeller. Api20191001Preview. ımovecollection</span><span class="sxs-lookup"><span data-stu-id="3d584-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="3d584-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d584-144">NOTES</span></span>

<span data-ttu-id="3d584-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="3d584-145">ALIASES</span></span>

## <span data-ttu-id="3d584-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d584-146">RELATED LINKS</span></span>

