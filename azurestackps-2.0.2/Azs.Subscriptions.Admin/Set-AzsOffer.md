---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsoffer
schema: 2.0.0
ms.openlocfilehash: 82be26ae402278d8cdc24195fd62ed09b67bdc14
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106664"
---
# <span data-ttu-id="63e50-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="63e50-101">Set-AzsOffer</span></span>

## <span data-ttu-id="63e50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63e50-102">SYNOPSIS</span></span>
<span data-ttu-id="63e50-103">Teklifi oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="63e50-103">Create or update the offer.</span></span>

## <span data-ttu-id="63e50-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63e50-104">SYNTAX</span></span>

### <span data-ttu-id="63e50-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="63e50-105">UpdateExpanded (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AddonPlanDefinition <IAddonPlanDefinition[]>] [-BasePlanIds <String[]>] [-Description <String>]
 [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>]
 [-MaxSubscriptionsPerAccount <Int32>] [-PropertiesName <String>] [-State <AccessibilityState>]
 [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="63e50-106">Güncelleştiremedi</span><span class="sxs-lookup"><span data-stu-id="63e50-106">Update</span></span>
```
Set-AzsOffer -OfferDefinition <IOffer> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="63e50-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="63e50-107">DESCRIPTION</span></span>
<span data-ttu-id="63e50-108">Teklifi oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="63e50-108">Create or update the offer.</span></span>

## <span data-ttu-id="63e50-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63e50-109">EXAMPLES</span></span>

### <span data-ttu-id="63e50-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="63e50-110">Example 1</span></span>
```powershell
PS C:\> $Offer = Get-AzsAdminManagedOffer | Select-Object -First 1
$Offer.MaxSubscriptionsPerAccount = 18
$Offer | Set-AzsOffer

AddonPlans                 : {}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/plans/DRPTestPlan5056}
Description                : 
DisplayName                : DRPTestOffer5056
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Location                   : redmond
MaxSubscriptionsPerAccount : 18
Name                       : DRPTestOffer5056
PropertiesName             : DRPTestOffer5056
State                      : Private
SubscriptionCount          : 5
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="63e50-111">Teklifi güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="63e50-111">Update an offer.</span></span>

## <span data-ttu-id="63e50-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63e50-112">PARAMETERS</span></span>

### <span data-ttu-id="63e50-113">-Add</span><span class="sxs-lookup"><span data-stu-id="63e50-113">-AddonPlanDefinition</span></span>
<span data-ttu-id="63e50-114">Bir kiracının isteğe bağlı olarak teklifin bir parçası olarak edinebileceğiniz eklenti planlarına yönelik başvurular.</span><span class="sxs-lookup"><span data-stu-id="63e50-114">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
<span data-ttu-id="63e50-115">Oluşturmak için, Add, PLANTANıMı özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="63e50-115">To construct, see NOTES section for ADDONPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IAddonPlanDefinition[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="63e50-116">-Temelplankimlikleri</span><span class="sxs-lookup"><span data-stu-id="63e50-116">-BasePlanIds</span></span>
<span data-ttu-id="63e50-117">Kiracı teklife abone olduğunda kiracıya hemen sağlanan temel planların tanımlayıcıları.</span><span class="sxs-lookup"><span data-stu-id="63e50-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

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

### <span data-ttu-id="63e50-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e50-118">-DefaultProfile</span></span>
<span data-ttu-id="63e50-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="63e50-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63e50-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="63e50-120">-Description</span></span>
<span data-ttu-id="63e50-121">Teklifin açıklaması.</span><span class="sxs-lookup"><span data-stu-id="63e50-121">Description of offer.</span></span>

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

### <span data-ttu-id="63e50-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="63e50-122">-DisplayName</span></span>
<span data-ttu-id="63e50-123">Teklifin adını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="63e50-123">Display name of offer.</span></span>

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

### <span data-ttu-id="63e50-124">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="63e50-124">-ExternalReferenceId</span></span>
<span data-ttu-id="63e50-125">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="63e50-125">External reference identifier.</span></span>

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

### <span data-ttu-id="63e50-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="63e50-126">-Location</span></span>
<span data-ttu-id="63e50-127">Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="63e50-127">Location of the resource</span></span>

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

### <span data-ttu-id="63e50-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="63e50-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="63e50-129">Hesap başına maksimum abonelik.</span><span class="sxs-lookup"><span data-stu-id="63e50-129">Maximum subscriptions per account.</span></span>

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

### <span data-ttu-id="63e50-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="63e50-130">-Name</span></span>
<span data-ttu-id="63e50-131">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="63e50-131">Name of an offer.</span></span>

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

### <span data-ttu-id="63e50-132">-OfferDefinition</span><span class="sxs-lookup"><span data-stu-id="63e50-132">-OfferDefinition</span></span>
<span data-ttu-id="63e50-133">Aboneliğin oluşturulabildiği hizmet sunumunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="63e50-133">Represents an offering of services against which a subscription can be created.</span></span>
<span data-ttu-id="63e50-134">Oluşturmak için, OFFERDEFINITION özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="63e50-134">To construct, see NOTES section for OFFERDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="63e50-135">-PropertiesName</span><span class="sxs-lookup"><span data-stu-id="63e50-135">-PropertiesName</span></span>
<span data-ttu-id="63e50-136">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="63e50-136">Name of the Offer.</span></span>

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

### <span data-ttu-id="63e50-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63e50-137">-ResourceGroupName</span></span>
<span data-ttu-id="63e50-138">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="63e50-138">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="63e50-139">Durumlu</span><span class="sxs-lookup"><span data-stu-id="63e50-139">-State</span></span>
<span data-ttu-id="63e50-140">Erişilebilirlik durumunu sunma.</span><span class="sxs-lookup"><span data-stu-id="63e50-140">Offer accessibility state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.AccessibilityState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="63e50-141">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="63e50-141">-SubscriptionCount</span></span>
<span data-ttu-id="63e50-142">Geçerli abonelik sayısı.</span><span class="sxs-lookup"><span data-stu-id="63e50-142">Current subscription count.</span></span>

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

### <span data-ttu-id="63e50-143">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="63e50-143">-SubscriptionId</span></span>
<span data-ttu-id="63e50-144">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="63e50-144">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="63e50-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="63e50-145">-Confirm</span></span>
<span data-ttu-id="63e50-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="63e50-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63e50-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63e50-147">-WhatIf</span></span>
<span data-ttu-id="63e50-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="63e50-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63e50-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="63e50-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63e50-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e50-150">CommonParameters</span></span>
<span data-ttu-id="63e50-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63e50-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e50-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="63e50-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e50-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63e50-153">INPUTS</span></span>

### <span data-ttu-id="63e50-154">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ıteklifini</span><span class="sxs-lookup"><span data-stu-id="63e50-154">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

## <span data-ttu-id="63e50-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63e50-155">OUTPUTS</span></span>

### <span data-ttu-id="63e50-156">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ıteklifini</span><span class="sxs-lookup"><span data-stu-id="63e50-156">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="63e50-157">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="63e50-157">ALIASES</span></span>

## <span data-ttu-id="63e50-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63e50-158">NOTES</span></span>

<span data-ttu-id="63e50-159">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="63e50-159">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="63e50-160">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="63e50-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="63e50-161">ADDON PLANDEFINITION <ıaddon Plandefinition [] >: kiracının isteğe bağlı olarak teklifin bir parçası olarak edinebileceğiniz eklenti planlarına yönelik başvurular.</span><span class="sxs-lookup"><span data-stu-id="63e50-161">ADDONPLANDEFINITION <IAddonPlanDefinition[]>: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
  - <span data-ttu-id="63e50-162">`[MaxAcquisitionCount <Int32?>]`: Tek bir abonelikle edinildiği en fazla örnek sayısı.</span><span class="sxs-lookup"><span data-stu-id="63e50-162">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="63e50-163">Belirtilmemişse, kabul edilen değer 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="63e50-163">If not specified, the assumed value is 1.</span></span>
  - <span data-ttu-id="63e50-164">`[PlanId <String>]`: Plan tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="63e50-164">`[PlanId <String>]`: Plan identifier.</span></span>

<span data-ttu-id="63e50-165">OFFERDEFINITION <IOffer> : bir aboneliğin oluşturulabildiği hizmetlerin sunumunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="63e50-165">OFFERDEFINITION <IOffer>: Represents an offering of services against which a subscription can be created.</span></span>
  - <span data-ttu-id="63e50-166">`[Location <String>]`: Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="63e50-166">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="63e50-167">`[AddonPlans <IAddonPlanDefinition[]>]`: Kiracının isteğe bağlı olarak teklifin bir parçası olarak edinebileceğiniz eklenti planlarına yönelik başvurular.</span><span class="sxs-lookup"><span data-stu-id="63e50-167">`[AddonPlans <IAddonPlanDefinition[]>]`: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
    - <span data-ttu-id="63e50-168">`[MaxAcquisitionCount <Int32?>]`: Tek bir abonelikle edinildiği en fazla örnek sayısı.</span><span class="sxs-lookup"><span data-stu-id="63e50-168">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="63e50-169">Belirtilmemişse, kabul edilen değer 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="63e50-169">If not specified, the assumed value is 1.</span></span>
    - <span data-ttu-id="63e50-170">`[PlanId <String>]`: Plan tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="63e50-170">`[PlanId <String>]`: Plan identifier.</span></span>
  - <span data-ttu-id="63e50-171">`[BasePlanIds <String[]>]`: Kiracı teklife abone olduğunda kiracıya hemen uygun olan temel planların tanımlayıcıları.</span><span class="sxs-lookup"><span data-stu-id="63e50-171">`[BasePlanIds <String[]>]`: Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>
  - <span data-ttu-id="63e50-172">`[Description <String>]`: Teklifin açıklaması.</span><span class="sxs-lookup"><span data-stu-id="63e50-172">`[Description <String>]`: Description of offer.</span></span>
  - <span data-ttu-id="63e50-173">`[DisplayName <String>]`: Teklifin görünen adı.</span><span class="sxs-lookup"><span data-stu-id="63e50-173">`[DisplayName <String>]`: Display name of offer.</span></span>
  - <span data-ttu-id="63e50-174">`[ExternalReferenceId <String>]`: Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="63e50-174">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="63e50-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Hesap başına maksimum abonelik.</span><span class="sxs-lookup"><span data-stu-id="63e50-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Maximum subscriptions per account.</span></span>
  - <span data-ttu-id="63e50-176">`[PropertiesName <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="63e50-176">`[PropertiesName <String>]`: Name of the Offer.</span></span>
  - <span data-ttu-id="63e50-177">`[State <AccessibilityState?>]`: Erişilebilirlik durumu sunma.</span><span class="sxs-lookup"><span data-stu-id="63e50-177">`[State <AccessibilityState?>]`: Offer accessibility state.</span></span>
  - <span data-ttu-id="63e50-178">`[SubscriptionCount <Int32?>]`: Geçerli abonelik sayısı.</span><span class="sxs-lookup"><span data-stu-id="63e50-178">`[SubscriptionCount <Int32?>]`: Current subscription count.</span></span>

## <span data-ttu-id="63e50-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63e50-179">RELATED LINKS</span></span>

