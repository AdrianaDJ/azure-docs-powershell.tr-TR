---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9ff6532cb43d7ece7460651eb4493201de4734b1
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934740"
---
# <span data-ttu-id="07936-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="07936-101">Set-AzsPlan</span></span>

## <span data-ttu-id="07936-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07936-102">SYNOPSIS</span></span>
<span data-ttu-id="07936-103">Belirtilen planı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="07936-103">Updates the specified plan</span></span>

## <span data-ttu-id="07936-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07936-104">SYNTAX</span></span>

### <span data-ttu-id="07936-105">Güncelleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="07936-105">Update (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-QuotaIds <String[]>]
 [-SkuIds <String[]>] [-ExternalReferenceId <String>] [-Description <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07936-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="07936-106">InputObject</span></span>
```
Set-AzsPlan [-ResourceGroupName <String>] -InputObject <Plan> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07936-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="07936-107">ResourceId</span></span>
```
Set-AzsPlan -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07936-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="07936-108">DESCRIPTION</span></span>
<span data-ttu-id="07936-109">Belirtilen planı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="07936-109">Updates the specified plan</span></span>

## <span data-ttu-id="07936-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07936-110">EXAMPLES</span></span>

### <span data-ttu-id="07936-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="07936-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -Description "This plan is meant to be used by accounting only."
```

<span data-ttu-id="07936-112">Belirtilen planı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="07936-112">Updates the specified plan</span></span>

## <span data-ttu-id="07936-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07936-113">PARAMETERS</span></span>

### <span data-ttu-id="07936-114">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="07936-114">-Description</span></span>
<span data-ttu-id="07936-115">Planın açıklaması.</span><span class="sxs-lookup"><span data-stu-id="07936-115">Description of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07936-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="07936-116">-DisplayName</span></span>
<span data-ttu-id="07936-117">Görünen ad.</span><span class="sxs-lookup"><span data-stu-id="07936-117">Display name.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07936-118">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="07936-118">-ExternalReferenceId</span></span>
<span data-ttu-id="07936-119">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="07936-119">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07936-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07936-120">-InputObject</span></span>
<span data-ttu-id="07936-121">Microsoft. AzureStack. Management. abonelikler. admin. modeller. plan türünde giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="07936-121">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan.</span></span>

```yaml
Type: Plan
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07936-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="07936-122">-Location</span></span>
<span data-ttu-id="07936-123">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="07936-123">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07936-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="07936-124">-Name</span></span>
<span data-ttu-id="07936-125">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="07936-125">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07936-126">-Quotaıds</span><span class="sxs-lookup"><span data-stu-id="07936-126">-QuotaIds</span></span>
<span data-ttu-id="07936-127">Planın altındaki kota tanımlayıcıları.</span><span class="sxs-lookup"><span data-stu-id="07936-127">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07936-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07936-128">-ResourceGroupName</span></span>
<span data-ttu-id="07936-129">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="07936-129">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07936-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="07936-130">-ResourceId</span></span>
<span data-ttu-id="07936-131">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="07936-131">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07936-132">-Skuid 'ler</span><span class="sxs-lookup"><span data-stu-id="07936-132">-SkuIds</span></span>
<span data-ttu-id="07936-133">SKU kimlikleri.</span><span class="sxs-lookup"><span data-stu-id="07936-133">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07936-134">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="07936-134">-SubscriptionCount</span></span>
<span data-ttu-id="07936-135">Abonelik sayısı.</span><span class="sxs-lookup"><span data-stu-id="07936-135">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07936-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="07936-136">-Confirm</span></span>
<span data-ttu-id="07936-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="07936-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07936-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07936-138">-WhatIf</span></span>
<span data-ttu-id="07936-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="07936-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07936-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="07936-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07936-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07936-141">CommonParameters</span></span>
<span data-ttu-id="07936-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07936-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07936-143">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07936-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07936-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07936-144">INPUTS</span></span>

## <span data-ttu-id="07936-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07936-145">OUTPUTS</span></span>

### <span data-ttu-id="07936-146">Microsoft. AzureStack. Management. abonelikler. admin. modeller. plan</span><span class="sxs-lookup"><span data-stu-id="07936-146">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="07936-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07936-147">NOTES</span></span>

## <span data-ttu-id="07936-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07936-148">RELATED LINKS</span></span>

