---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9ff6532cb43d7ece7460651eb4493201de4734b1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934869"
---
# <span data-ttu-id="8e89f-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="8e89f-101">Set-AzsPlan</span></span>

## <span data-ttu-id="8e89f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e89f-102">SYNOPSIS</span></span>
<span data-ttu-id="8e89f-103">Belirtilen planı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="8e89f-103">Updates the specified plan</span></span>

## <span data-ttu-id="8e89f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e89f-104">SYNTAX</span></span>

### <span data-ttu-id="8e89f-105">Güncelleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8e89f-105">Update (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-QuotaIds <String[]>]
 [-SkuIds <String[]>] [-ExternalReferenceId <String>] [-Description <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e89f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8e89f-106">InputObject</span></span>
```
Set-AzsPlan [-ResourceGroupName <String>] -InputObject <Plan> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e89f-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="8e89f-107">ResourceId</span></span>
```
Set-AzsPlan -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e89f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e89f-108">DESCRIPTION</span></span>
<span data-ttu-id="8e89f-109">Belirtilen planı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="8e89f-109">Updates the specified plan</span></span>

## <span data-ttu-id="8e89f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e89f-110">EXAMPLES</span></span>

### <span data-ttu-id="8e89f-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8e89f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -Description "This plan is meant to be used by accounting only."
```

<span data-ttu-id="8e89f-112">Belirtilen planı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="8e89f-112">Updates the specified plan</span></span>

## <span data-ttu-id="8e89f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e89f-113">PARAMETERS</span></span>

### <span data-ttu-id="8e89f-114">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="8e89f-114">-Description</span></span>
<span data-ttu-id="8e89f-115">Planın açıklaması.</span><span class="sxs-lookup"><span data-stu-id="8e89f-115">Description of the plan.</span></span>

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

### <span data-ttu-id="8e89f-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8e89f-116">-DisplayName</span></span>
<span data-ttu-id="8e89f-117">Görünen ad.</span><span class="sxs-lookup"><span data-stu-id="8e89f-117">Display name.</span></span>

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

### <span data-ttu-id="8e89f-118">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="8e89f-118">-ExternalReferenceId</span></span>
<span data-ttu-id="8e89f-119">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="8e89f-119">External reference identifier.</span></span>

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

### <span data-ttu-id="8e89f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e89f-120">-InputObject</span></span>
<span data-ttu-id="8e89f-121">Microsoft. AzureStack. Management. abonelikler. admin. modeller. plan türünde giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8e89f-121">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan.</span></span>

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

### <span data-ttu-id="8e89f-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="8e89f-122">-Location</span></span>
<span data-ttu-id="8e89f-123">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="8e89f-123">Location of the resource.</span></span>

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

### <span data-ttu-id="8e89f-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="8e89f-124">-Name</span></span>
<span data-ttu-id="8e89f-125">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="8e89f-125">Name of the plan.</span></span>

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

### <span data-ttu-id="8e89f-126">-Quotaıds</span><span class="sxs-lookup"><span data-stu-id="8e89f-126">-QuotaIds</span></span>
<span data-ttu-id="8e89f-127">Planın altındaki kota tanımlayıcıları.</span><span class="sxs-lookup"><span data-stu-id="8e89f-127">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="8e89f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e89f-128">-ResourceGroupName</span></span>
<span data-ttu-id="8e89f-129">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="8e89f-129">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="8e89f-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8e89f-130">-ResourceId</span></span>
<span data-ttu-id="8e89f-131">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="8e89f-131">The resource id.</span></span>

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

### <span data-ttu-id="8e89f-132">-Skuid 'ler</span><span class="sxs-lookup"><span data-stu-id="8e89f-132">-SkuIds</span></span>
<span data-ttu-id="8e89f-133">SKU kimlikleri.</span><span class="sxs-lookup"><span data-stu-id="8e89f-133">SKU identifiers.</span></span>

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

### <span data-ttu-id="8e89f-134">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="8e89f-134">-SubscriptionCount</span></span>
<span data-ttu-id="8e89f-135">Abonelik sayısı.</span><span class="sxs-lookup"><span data-stu-id="8e89f-135">Subscription count.</span></span>

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

### <span data-ttu-id="8e89f-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="8e89f-136">-Confirm</span></span>
<span data-ttu-id="8e89f-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8e89f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e89f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e89f-138">-WhatIf</span></span>
<span data-ttu-id="8e89f-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e89f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e89f-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8e89f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e89f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e89f-141">CommonParameters</span></span>
<span data-ttu-id="8e89f-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e89f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e89f-143">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e89f-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e89f-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e89f-144">INPUTS</span></span>

## <span data-ttu-id="8e89f-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e89f-145">OUTPUTS</span></span>

### <span data-ttu-id="8e89f-146">Microsoft. AzureStack. Management. abonelikler. admin. modeller. plan</span><span class="sxs-lookup"><span data-stu-id="8e89f-146">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="8e89f-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e89f-147">NOTES</span></span>

## <span data-ttu-id="8e89f-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e89f-148">RELATED LINKS</span></span>

