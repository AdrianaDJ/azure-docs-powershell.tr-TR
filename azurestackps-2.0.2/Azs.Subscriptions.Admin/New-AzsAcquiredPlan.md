---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: 0db0f7ae4358e49ff62f94132701be1f4bd4d0b7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106822"
---
# <span data-ttu-id="51870-101">New-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="51870-101">New-AzsAcquiredPlan</span></span>

## <span data-ttu-id="51870-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51870-102">SYNOPSIS</span></span>


## <span data-ttu-id="51870-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51870-103">SYNTAX</span></span>

### <span data-ttu-id="51870-104">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="51870-104">CreateExpanded (Default)</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> [-PlanAcquisitionId <String>] [-SubscriptionId <String>]
 [-AcquisitionTime <DateTime>] [-ExternalReferenceId <String>] [-Id <String>] [-PlanId <String>]
 [-ProvisioningState <ProvisioningState>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="51870-105">Oluturmak</span><span class="sxs-lookup"><span data-stu-id="51870-105">Create</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> -AcquiredPlanDefinition <IPlanAcquisition>
 [-PlanAcquisitionId <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="51870-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="51870-106">DESCRIPTION</span></span>


## <span data-ttu-id="51870-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51870-107">EXAMPLES</span></span>

### <span data-ttu-id="51870-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="51870-108">Example 1</span></span>
```powershell
PS C:\> New-AzsAcquiredPlan -PlanAcquisitionId $([Guid]::NewGuid()) -PlanId "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan" -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

AcquisitionId       : 718c7f7c-4868-479a-98ce-5caaa8f158c1
AcquisitionTime     : 3/12/2020 11:16:08 PM
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/acquiredPlan
                      s/718c7f7c-4868-479a-98ce-5caaa8f158c1
PlanId              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/plans/testplan
ProvisioningState   : Succeeded
```

<span data-ttu-id="51870-109">Abonelik planı oluşturma.</span><span class="sxs-lookup"><span data-stu-id="51870-109">Create a subscription plan.</span></span>

## <span data-ttu-id="51870-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51870-110">PARAMETERS</span></span>

### <span data-ttu-id="51870-111">-AcquiredPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="51870-111">-AcquiredPlanDefinition</span></span>
<span data-ttu-id="51870-112">Oluşturmak için, ACQUIREDPLANDEFINITION özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="51870-112">To construct, see NOTES section for ACQUIREDPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="51870-113">-Tanışanı</span><span class="sxs-lookup"><span data-stu-id="51870-113">-AcquisitionTime</span></span>


```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="51870-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51870-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="51870-115">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="51870-115">-ExternalReferenceId</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="51870-116">-ID</span><span class="sxs-lookup"><span data-stu-id="51870-116">-Id</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="51870-117">-Planlama</span><span class="sxs-lookup"><span data-stu-id="51870-117">-PlanAcquisitionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="51870-118">-Plankimliği</span><span class="sxs-lookup"><span data-stu-id="51870-118">-PlanId</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="51870-119">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="51870-119">-ProvisioningState</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="51870-120">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="51870-120">-SubscriptionId</span></span>


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

### <span data-ttu-id="51870-121">-Targetsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="51870-121">-TargetSubscriptionId</span></span>


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

### <span data-ttu-id="51870-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="51870-122">-Confirm</span></span>
<span data-ttu-id="51870-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="51870-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51870-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51870-124">-WhatIf</span></span>
<span data-ttu-id="51870-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="51870-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51870-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="51870-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51870-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51870-127">CommonParameters</span></span>
<span data-ttu-id="51870-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51870-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51870-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="51870-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51870-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51870-130">INPUTS</span></span>

### <span data-ttu-id="51870-131">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ıplanalımı</span><span class="sxs-lookup"><span data-stu-id="51870-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

## <span data-ttu-id="51870-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51870-132">OUTPUTS</span></span>

### <span data-ttu-id="51870-133">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ıplanalımı</span><span class="sxs-lookup"><span data-stu-id="51870-133">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="51870-134">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="51870-134">ALIASES</span></span>

<span data-ttu-id="51870-135">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="51870-135">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="51870-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51870-136">NOTES</span></span>

<span data-ttu-id="51870-137">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="51870-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="51870-138">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="51870-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="51870-139">ACQUIREDPLANDEFINITION <IPlanAcquisition> :</span><span class="sxs-lookup"><span data-stu-id="51870-139">ACQUIREDPLANDEFINITION <IPlanAcquisition>:</span></span> 
  - <span data-ttu-id="51870-140">`[AcquisitionId <String>]`: Alım tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="51870-140">`[AcquisitionId <String>]`: Acquisition identifier.</span></span>
  - <span data-ttu-id="51870-141">`[AcquisitionTime <DateTime?>]`: Alım süresi.</span><span class="sxs-lookup"><span data-stu-id="51870-141">`[AcquisitionTime <DateTime?>]`: Acquisition time.</span></span>
  - <span data-ttu-id="51870-142">`[ExternalReferenceId <String>]`: Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="51870-142">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="51870-143">`[Id <String>]`: Kiracı aboneliği bağlamındaki tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="51870-143">`[Id <String>]`: Identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="51870-144">`[PlanId <String>]`: Kiracı aboneliği bağlamında plan tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="51870-144">`[PlanId <String>]`: Plan identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="51870-145">`[ProvisioningState <ProvisioningState?>]`: Sağlama durumu.</span><span class="sxs-lookup"><span data-stu-id="51870-145">`[ProvisioningState <ProvisioningState?>]`: State of the provisioning.</span></span>

## <span data-ttu-id="51870-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51870-146">RELATED LINKS</span></span>

