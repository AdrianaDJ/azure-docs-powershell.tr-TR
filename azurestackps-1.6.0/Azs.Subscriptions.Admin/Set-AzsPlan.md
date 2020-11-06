---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f03365a81fc53af14e3fc9e686504ef3e4387c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571790"
---
# <span data-ttu-id="bafa8-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="bafa8-101">Set-AzsPlan</span></span>

## <span data-ttu-id="bafa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bafa8-102">SYNOPSIS</span></span>
<span data-ttu-id="bafa8-103">Belirtilen planı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="bafa8-103">Updates the specified plan</span></span>

## <span data-ttu-id="bafa8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bafa8-104">SYNTAX</span></span>

### <span data-ttu-id="bafa8-105">Güncelleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bafa8-105">Update (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-QuotaIds <String[]>]
 [-SkuIds <String[]>] [-ExternalReferenceId <String>] [-Description <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bafa8-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="bafa8-106">InputObject</span></span>
```
Set-AzsPlan [-ResourceGroupName <String>] -InputObject <Plan> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bafa8-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="bafa8-107">ResourceId</span></span>
```
Set-AzsPlan -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bafa8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bafa8-108">DESCRIPTION</span></span>
<span data-ttu-id="bafa8-109">Belirtilen planı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="bafa8-109">Updates the specified plan</span></span>

## <span data-ttu-id="bafa8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bafa8-110">EXAMPLES</span></span>

### <span data-ttu-id="bafa8-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bafa8-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -Description "This plan is meant to be used by accounting only."
```

<span data-ttu-id="bafa8-112">Belirtilen planı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="bafa8-112">Updates the specified plan</span></span>

## <span data-ttu-id="bafa8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bafa8-113">PARAMETERS</span></span>

### <span data-ttu-id="bafa8-114">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="bafa8-114">-Description</span></span>
<span data-ttu-id="bafa8-115">Planın açıklaması.</span><span class="sxs-lookup"><span data-stu-id="bafa8-115">Description of the plan.</span></span>

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

### <span data-ttu-id="bafa8-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bafa8-116">-DisplayName</span></span>
<span data-ttu-id="bafa8-117">Görünen ad.</span><span class="sxs-lookup"><span data-stu-id="bafa8-117">Display name.</span></span>

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

### <span data-ttu-id="bafa8-118">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="bafa8-118">-ExternalReferenceId</span></span>
<span data-ttu-id="bafa8-119">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="bafa8-119">External reference identifier.</span></span>

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

### <span data-ttu-id="bafa8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bafa8-120">-InputObject</span></span>
<span data-ttu-id="bafa8-121">Microsoft. AzureStack. Management. abonelikler. admin. modeller. plan türünde giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bafa8-121">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan.</span></span>

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

### <span data-ttu-id="bafa8-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="bafa8-122">-Location</span></span>
<span data-ttu-id="bafa8-123">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="bafa8-123">Location of the resource.</span></span>

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

### <span data-ttu-id="bafa8-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="bafa8-124">-Name</span></span>
<span data-ttu-id="bafa8-125">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="bafa8-125">Name of the plan.</span></span>

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

### <span data-ttu-id="bafa8-126">-Quotaıds</span><span class="sxs-lookup"><span data-stu-id="bafa8-126">-QuotaIds</span></span>
<span data-ttu-id="bafa8-127">Planın altındaki kota tanımlayıcıları.</span><span class="sxs-lookup"><span data-stu-id="bafa8-127">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="bafa8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bafa8-128">-ResourceGroupName</span></span>
<span data-ttu-id="bafa8-129">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="bafa8-129">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="bafa8-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bafa8-130">-ResourceId</span></span>
<span data-ttu-id="bafa8-131">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="bafa8-131">The resource id.</span></span>

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

### <span data-ttu-id="bafa8-132">-Skuid 'ler</span><span class="sxs-lookup"><span data-stu-id="bafa8-132">-SkuIds</span></span>
<span data-ttu-id="bafa8-133">SKU kimlikleri.</span><span class="sxs-lookup"><span data-stu-id="bafa8-133">SKU identifiers.</span></span>

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

### <span data-ttu-id="bafa8-134">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="bafa8-134">-SubscriptionCount</span></span>
<span data-ttu-id="bafa8-135">Abonelik sayısı.</span><span class="sxs-lookup"><span data-stu-id="bafa8-135">Subscription count.</span></span>

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

### <span data-ttu-id="bafa8-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="bafa8-136">-Confirm</span></span>
<span data-ttu-id="bafa8-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bafa8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bafa8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bafa8-138">-WhatIf</span></span>
<span data-ttu-id="bafa8-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bafa8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bafa8-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bafa8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bafa8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bafa8-141">CommonParameters</span></span>
<span data-ttu-id="bafa8-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bafa8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bafa8-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bafa8-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bafa8-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bafa8-144">INPUTS</span></span>

## <span data-ttu-id="bafa8-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bafa8-145">OUTPUTS</span></span>

### <span data-ttu-id="bafa8-146">Microsoft. AzureStack. Management. abonelikler. admin. modeller. plan</span><span class="sxs-lookup"><span data-stu-id="bafa8-146">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="bafa8-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bafa8-147">NOTES</span></span>

## <span data-ttu-id="bafa8-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bafa8-148">RELATED LINKS</span></span>

