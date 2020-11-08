---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/add-azsplantooffer
schema: 2.0.0
ms.openlocfilehash: 65691116ea8e73e8f03e8cc7dc97f38c61ecebdb
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106690"
---
# <span data-ttu-id="68f07-101">Add-AzsPlanToOffer</span><span class="sxs-lookup"><span data-stu-id="68f07-101">Add-AzsPlanToOffer</span></span>

## <span data-ttu-id="68f07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68f07-102">SYNOPSIS</span></span>
<span data-ttu-id="68f07-103">Bir planı teklife bağlar.</span><span class="sxs-lookup"><span data-stu-id="68f07-103">Links a plan to an offer.</span></span>

## <span data-ttu-id="68f07-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68f07-104">SYNTAX</span></span>

### <span data-ttu-id="68f07-105">Bağlantı genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="68f07-105">LinkExpanded (Default)</span></span>
```
Add-AzsPlanToOffer -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaxAcquisitionCount <Int32>] [-PlanLinkType <PlanLinkType>] [-PlanName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="68f07-106">Bağlantılandırabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="68f07-106">Link</span></span>
```
Add-AzsPlanToOffer -OfferName <String> -ResourceGroupName <String> -PlanLink <IPlanLinkDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="68f07-107">Linkviaıdentity</span><span class="sxs-lookup"><span data-stu-id="68f07-107">LinkViaIdentity</span></span>
```
Add-AzsPlanToOffer -InputObject <ISubscriptionsAdminIdentity> -PlanLink <IPlanLinkDefinition>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="68f07-108">Linkviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="68f07-108">LinkViaIdentityExpanded</span></span>
```
Add-AzsPlanToOffer -InputObject <ISubscriptionsAdminIdentity> [-MaxAcquisitionCount <Int32>]
 [-PlanLinkType <PlanLinkType>] [-PlanName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="68f07-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="68f07-109">DESCRIPTION</span></span>
<span data-ttu-id="68f07-110">Bir planı teklife bağlar.</span><span class="sxs-lookup"><span data-stu-id="68f07-110">Links a plan to an offer.</span></span>

## <span data-ttu-id="68f07-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68f07-111">EXAMPLES</span></span>

### <span data-ttu-id="68f07-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="68f07-112">Example 1</span></span>
```powershell
PS C:\> Add-AzsPlanToOffer -PlanName "addonplan" -PlanLinkType Addon -OfferName "testoffer" -ResourceGroupName "testrg" -MaxAcquisitionCount 18

AddonPlans                 : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/addonplan}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan}
Description                : 
DisplayName                : testoffer
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/testoffer
Location                   : redmond
MaxSubscriptionsPerAccount : 0
Name                       : testoffer
PropertiesName             : testoffer
State                      : Private
SubscriptionCount          : 0
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="68f07-113">Bir planı teklife bağlar.</span><span class="sxs-lookup"><span data-stu-id="68f07-113">Links a plan to an offer.</span></span>

## <span data-ttu-id="68f07-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68f07-114">PARAMETERS</span></span>

### <span data-ttu-id="68f07-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68f07-115">-DefaultProfile</span></span>
<span data-ttu-id="68f07-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="68f07-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68f07-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68f07-117">-InputObject</span></span>
<span data-ttu-id="68f07-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="68f07-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: LinkViaIdentity, LinkViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="68f07-119">-Maxtanışan</span><span class="sxs-lookup"><span data-stu-id="68f07-119">-MaxAcquisitionCount</span></span>
<span data-ttu-id="68f07-120">Abonelere göre en fazla Alım sayısı</span><span class="sxs-lookup"><span data-stu-id="68f07-120">The maximum acquisition count by subscribers</span></span>

```yaml
Type: System.Int32
Parameter Sets: LinkExpanded, LinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="68f07-121">-OfferName</span><span class="sxs-lookup"><span data-stu-id="68f07-121">-OfferName</span></span>
<span data-ttu-id="68f07-122">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="68f07-122">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Link, LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="68f07-123">-PlanLink</span><span class="sxs-lookup"><span data-stu-id="68f07-123">-PlanLink</span></span>
<span data-ttu-id="68f07-124">Tarifeleri bağlama ve bağlantılarını kaldırma tanımı.</span><span class="sxs-lookup"><span data-stu-id="68f07-124">Definition for linking and unlinking plans to offers.</span></span>
<span data-ttu-id="68f07-125">Oluşturmak için, PLANBAĞLANTı özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="68f07-125">To construct, see NOTES section for PLANLINK properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition
Parameter Sets: Link, LinkViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="68f07-126">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="68f07-126">-PlanLinkType</span></span>
<span data-ttu-id="68f07-127">Plan bağlantısının türü.</span><span class="sxs-lookup"><span data-stu-id="68f07-127">Type of the plan link.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.PlanLinkType
Parameter Sets: LinkExpanded, LinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="68f07-128">-PlanName</span><span class="sxs-lookup"><span data-stu-id="68f07-128">-PlanName</span></span>
<span data-ttu-id="68f07-129">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="68f07-129">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded, LinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="68f07-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68f07-130">-ResourceGroupName</span></span>
<span data-ttu-id="68f07-131">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="68f07-131">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Link, LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="68f07-132">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="68f07-132">-SubscriptionId</span></span>
<span data-ttu-id="68f07-133">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="68f07-133">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Link, LinkExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="68f07-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="68f07-134">-Confirm</span></span>
<span data-ttu-id="68f07-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="68f07-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68f07-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68f07-136">-WhatIf</span></span>
<span data-ttu-id="68f07-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="68f07-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68f07-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="68f07-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68f07-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68f07-139">CommonParameters</span></span>
<span data-ttu-id="68f07-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68f07-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68f07-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="68f07-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68f07-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68f07-142">INPUTS</span></span>

### <span data-ttu-id="68f07-143">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ıplanlinkdefinition</span><span class="sxs-lookup"><span data-stu-id="68f07-143">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition</span></span>

### <span data-ttu-id="68f07-144">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. ısubscriptionsadminıdentity</span><span class="sxs-lookup"><span data-stu-id="68f07-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="68f07-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68f07-145">OUTPUTS</span></span>

### <span data-ttu-id="68f07-146">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ıteklifini</span><span class="sxs-lookup"><span data-stu-id="68f07-146">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="68f07-147">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="68f07-147">ALIASES</span></span>

## <span data-ttu-id="68f07-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68f07-148">NOTES</span></span>

<span data-ttu-id="68f07-149">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="68f07-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="68f07-150">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="68f07-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="68f07-151">INPUTOBJECT <ISubscriptionsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="68f07-151">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="68f07-152">`[DelegatedProvider <String>]`: Delegatedpprovider tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="68f07-152">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="68f07-153">`[DelegatedProviderSubscriptionId <String>]`: Temsilci sağlayıcı abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="68f07-153">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="68f07-154">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="68f07-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="68f07-155">`[Location <String>]`: AzureStack konumu.</span><span class="sxs-lookup"><span data-stu-id="68f07-155">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="68f07-156">`[ManifestName <String>]`: Bildirim adı.</span><span class="sxs-lookup"><span data-stu-id="68f07-156">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="68f07-157">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="68f07-157">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="68f07-158">`[OfferDelegationName <String>]`: Teklif temsilcisinin adı.</span><span class="sxs-lookup"><span data-stu-id="68f07-158">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="68f07-159">`[OperationsStatusName <String>]`: İşlem durumu adı.</span><span class="sxs-lookup"><span data-stu-id="68f07-159">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="68f07-160">`[Plan <String>]`: Planın adı.</span><span class="sxs-lookup"><span data-stu-id="68f07-160">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="68f07-161">`[PlanAcquisitionId <String>]`: Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="68f07-161">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="68f07-162">`[Quota <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="68f07-162">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="68f07-163">`[ResourceGroupName <String>]`: Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="68f07-163">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="68f07-164">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="68f07-164">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="68f07-165">`[TargetSubscriptionId <String>]`: Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="68f07-165">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="68f07-166">`[Tenant <String>]`: Dizin kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="68f07-166">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="68f07-167">PLANLINK <IPlanLinkDefinition> : planlar için bağlama ve bağlantıları kaldırma tanımı.</span><span class="sxs-lookup"><span data-stu-id="68f07-167">PLANLINK <IPlanLinkDefinition>: Definition for linking and unlinking plans to offers.</span></span>
  - <span data-ttu-id="68f07-168">`[MaxAcquisitionCount <Int32?>]`: Abonelere göre en fazla Alım sayısı</span><span class="sxs-lookup"><span data-stu-id="68f07-168">`[MaxAcquisitionCount <Int32?>]`: The maximum acquisition count by subscribers</span></span>
  - <span data-ttu-id="68f07-169">`[PlanLinkType <PlanLinkType?>]`: Plan bağlantısının türü.</span><span class="sxs-lookup"><span data-stu-id="68f07-169">`[PlanLinkType <PlanLinkType?>]`: Type of the plan link.</span></span>
  - <span data-ttu-id="68f07-170">`[PlanName <String>]`: Planın adı.</span><span class="sxs-lookup"><span data-stu-id="68f07-170">`[PlanName <String>]`: Name of the plan.</span></span>

## <span data-ttu-id="68f07-171">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68f07-171">RELATED LINKS</span></span>

