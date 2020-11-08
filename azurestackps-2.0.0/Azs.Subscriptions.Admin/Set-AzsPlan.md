---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsplan
schema: 2.0.0
ms.openlocfilehash: 2e78b28705b625836d9020c5ddf1652f4bdc7a7d
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94105100"
---
# <span data-ttu-id="1455a-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="1455a-101">Set-AzsPlan</span></span>

## <span data-ttu-id="1455a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1455a-102">SYNOPSIS</span></span>
<span data-ttu-id="1455a-103">Planı oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="1455a-103">Create or update the plan.</span></span>

## <span data-ttu-id="1455a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1455a-104">SYNTAX</span></span>

### <span data-ttu-id="1455a-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1455a-105">UpdateExpanded (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Description <String>]
 [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>] [-PropertiesName <String>]
 [-QuotaIds <String[]>] [-SkuIds <String[]>] [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1455a-106">Güncelleştiremedi</span><span class="sxs-lookup"><span data-stu-id="1455a-106">Update</span></span>
```
Set-AzsPlan -PlanDefinition <IPlan> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1455a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1455a-107">DESCRIPTION</span></span>
<span data-ttu-id="1455a-108">Planı oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="1455a-108">Create or update the plan.</span></span>

## <span data-ttu-id="1455a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1455a-109">EXAMPLES</span></span>

### <span data-ttu-id="1455a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1455a-110">Example 1</span></span>
```powershell
PS C:\> $Plan = Get-AzsPlan | Select-Object -First 1
$Plan.Description = 'update plan'
$Plan | Set-AzsPlan

Description         : update plan
DisplayName         : DRPTestPlan5056-test-test-test
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/plans/DRPTestPlan5056
Location            : redmond
Name                : DRPTestPlan5056
PropertiesName      : DRPTestPlan5056
QuotaIds            : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Storage.Admin/locations/redmond/quotas/Default Quota, 
                      /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Compute.Admin/locations/redmond/quotas/Default Quota}
SkuIds              : 
SubscriptionCount   : 5
Tags                : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                : Microsoft.Subscriptions.Admin/plans
```

<span data-ttu-id="1455a-111">Belirtilen planı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="1455a-111">Updates the specified plan</span></span>

## <span data-ttu-id="1455a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1455a-112">PARAMETERS</span></span>

### <span data-ttu-id="1455a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1455a-113">-DefaultProfile</span></span>
<span data-ttu-id="1455a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1455a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1455a-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="1455a-115">-Description</span></span>
<span data-ttu-id="1455a-116">Planın açıklaması.</span><span class="sxs-lookup"><span data-stu-id="1455a-116">Description of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1455a-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1455a-117">-DisplayName</span></span>
<span data-ttu-id="1455a-118">Görünen ad.</span><span class="sxs-lookup"><span data-stu-id="1455a-118">Display name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1455a-119">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="1455a-119">-ExternalReferenceId</span></span>
<span data-ttu-id="1455a-120">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="1455a-120">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1455a-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="1455a-121">-Location</span></span>
<span data-ttu-id="1455a-122">Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="1455a-122">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1455a-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="1455a-123">-Name</span></span>
<span data-ttu-id="1455a-124">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="1455a-124">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1455a-125">-PlanDefinition</span><span class="sxs-lookup"><span data-stu-id="1455a-125">-PlanDefinition</span></span>
<span data-ttu-id="1455a-126">Bir plan, kiracıları sunan bir kotalar ve Özellikler paketini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="1455a-126">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="1455a-127">Bir kiracı bu planı temel bulut hizmetlerine erişimi yükseltme teklifi aracılığıyla alabilir.</span><span class="sxs-lookup"><span data-stu-id="1455a-127">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
<span data-ttu-id="1455a-128">Oluşturmak için, PLANTANıMı özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1455a-128">To construct, see NOTES section for PLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="1455a-129">-PropertiesName</span><span class="sxs-lookup"><span data-stu-id="1455a-129">-PropertiesName</span></span>
<span data-ttu-id="1455a-130">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="1455a-130">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1455a-131">-Quotaıds</span><span class="sxs-lookup"><span data-stu-id="1455a-131">-QuotaIds</span></span>
<span data-ttu-id="1455a-132">Planın altındaki kota tanımlayıcıları.</span><span class="sxs-lookup"><span data-stu-id="1455a-132">Quota identifiers under the plan.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1455a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1455a-133">-ResourceGroupName</span></span>
<span data-ttu-id="1455a-134">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="1455a-134">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1455a-135">-Skuid 'ler</span><span class="sxs-lookup"><span data-stu-id="1455a-135">-SkuIds</span></span>
<span data-ttu-id="1455a-136">SKU kimlikleri.</span><span class="sxs-lookup"><span data-stu-id="1455a-136">SKU identifiers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1455a-137">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="1455a-137">-SubscriptionCount</span></span>
<span data-ttu-id="1455a-138">Abonelik sayısı.</span><span class="sxs-lookup"><span data-stu-id="1455a-138">Subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1455a-139">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="1455a-139">-SubscriptionId</span></span>
<span data-ttu-id="1455a-140">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1455a-140">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1455a-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="1455a-141">-Confirm</span></span>
<span data-ttu-id="1455a-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1455a-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1455a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1455a-143">-WhatIf</span></span>
<span data-ttu-id="1455a-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1455a-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1455a-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1455a-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1455a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1455a-146">CommonParameters</span></span>
<span data-ttu-id="1455a-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1455a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1455a-148">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1455a-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1455a-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1455a-149">INPUTS</span></span>

### <span data-ttu-id="1455a-150">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="1455a-150">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

## <span data-ttu-id="1455a-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1455a-151">OUTPUTS</span></span>

### <span data-ttu-id="1455a-152">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="1455a-152">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

<span data-ttu-id="1455a-153">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="1455a-153">ALIASES</span></span>

## <span data-ttu-id="1455a-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1455a-154">NOTES</span></span>

<span data-ttu-id="1455a-155">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1455a-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1455a-156">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1455a-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1455a-157">PLANTANıMı <IPlan> : bir plan, kiracıları sunan bir kotalar ve Özellikler paketini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="1455a-157">PLANDEFINITION <IPlan>: A plan represents a package of quotas and capabilities that are offered tenants.</span></span> <span data-ttu-id="1455a-158">Bir kiracı bu planı temel bulut hizmetlerine erişimi yükseltme teklifi aracılığıyla alabilir.</span><span class="sxs-lookup"><span data-stu-id="1455a-158">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
  - <span data-ttu-id="1455a-159">`[Location <String>]`: Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="1455a-159">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="1455a-160">`[Description <String>]`: Planın açıklaması.</span><span class="sxs-lookup"><span data-stu-id="1455a-160">`[Description <String>]`: Description of the plan.</span></span>
  - <span data-ttu-id="1455a-161">`[DisplayName <String>]`: Görünen ad.</span><span class="sxs-lookup"><span data-stu-id="1455a-161">`[DisplayName <String>]`: Display name.</span></span>
  - <span data-ttu-id="1455a-162">`[ExternalReferenceId <String>]`: Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="1455a-162">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="1455a-163">`[PropertiesName <String>]`: Planın adı.</span><span class="sxs-lookup"><span data-stu-id="1455a-163">`[PropertiesName <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="1455a-164">`[QuotaIds <String[]>]`: Planın altındaki kota tanımlayıcıları.</span><span class="sxs-lookup"><span data-stu-id="1455a-164">`[QuotaIds <String[]>]`: Quota identifiers under the plan.</span></span>
  - <span data-ttu-id="1455a-165">`[SkuIds <String[]>]`: SKU tanımlayıcıları.</span><span class="sxs-lookup"><span data-stu-id="1455a-165">`[SkuIds <String[]>]`: SKU identifiers.</span></span>
  - <span data-ttu-id="1455a-166">`[SubscriptionCount <Int32?>]`: Abonelik sayısı.</span><span class="sxs-lookup"><span data-stu-id="1455a-166">`[SubscriptionCount <Int32?>]`: Subscription count.</span></span>

## <span data-ttu-id="1455a-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1455a-167">RELATED LINKS</span></span>

