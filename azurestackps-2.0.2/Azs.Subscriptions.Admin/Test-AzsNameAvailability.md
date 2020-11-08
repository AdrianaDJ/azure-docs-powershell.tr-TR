---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/test-azsnameavailability
schema: 2.0.0
ms.openlocfilehash: d92c2558375a180c96ff20260977bdb38908fa61
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94107144"
---
# <span data-ttu-id="20928-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="20928-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="20928-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20928-102">SYNOPSIS</span></span>
<span data-ttu-id="20928-103">Aboneliklerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="20928-103">Get the list of subscriptions.</span></span>

## <span data-ttu-id="20928-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="20928-104">SYNTAX</span></span>

### <span data-ttu-id="20928-105">Onay genişletme (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="20928-105">CheckExpanded (Default)</span></span>
```
Test-AzsNameAvailability [-SubscriptionId <String>] [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="20928-106">Denetleyebilir</span><span class="sxs-lookup"><span data-stu-id="20928-106">Check</span></span>
```
Test-AzsNameAvailability -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="20928-107">Checkviaıdentity</span><span class="sxs-lookup"><span data-stu-id="20928-107">CheckViaIdentity</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity>
 -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="20928-108">Checkviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="20928-108">CheckViaIdentityExpanded</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity> [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="20928-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="20928-109">DESCRIPTION</span></span>
<span data-ttu-id="20928-110">Aboneliklerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="20928-110">Get the list of subscriptions.</span></span>

## <span data-ttu-id="20928-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="20928-111">EXAMPLES</span></span>

### <span data-ttu-id="20928-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="20928-112">Example 1</span></span>
```powershell
PS C:\> Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name "testoffer" | fl *

Message       : A resource of type 'Microsoft.Subscriptions.Admin/offers' with name 'testoffer' already exists. Please select a different name.
NameAvailable : False
Reason        : AlreadyExists
```

<span data-ttu-id="20928-113">Belirtilen aboneliğin uygunluk adını ve adını döndürür</span><span class="sxs-lookup"><span data-stu-id="20928-113">Returns the availability of the specified subscription resource type and name</span></span>

## <span data-ttu-id="20928-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="20928-114">PARAMETERS</span></span>

### <span data-ttu-id="20928-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20928-115">-DefaultProfile</span></span>
<span data-ttu-id="20928-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="20928-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20928-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20928-117">-InputObject</span></span>
<span data-ttu-id="20928-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="20928-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: CheckViaIdentity, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="20928-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="20928-119">-Name</span></span>
<span data-ttu-id="20928-120">Doğrulanacak kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="20928-120">The resource name to verify.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="20928-121">-Namekullanılabilirlik tanım</span><span class="sxs-lookup"><span data-stu-id="20928-121">-NameAvailabilityDefinition</span></span>
<span data-ttu-id="20928-122">Ad kullanılabilirliğini denetleme eylem tanımı.</span><span class="sxs-lookup"><span data-stu-id="20928-122">The check name availability action definition.</span></span>
<span data-ttu-id="20928-123">Oluşturmak için, ad KULLANıLABILIRLIĞI için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="20928-123">To construct, see NOTES section for NAMEAVAILABILITYDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityDefinition
Parameter Sets: Check, CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="20928-124">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="20928-124">-ResourceType</span></span>
<span data-ttu-id="20928-125">Doğrulanacak kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="20928-125">The resource type to verify.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="20928-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="20928-126">-SubscriptionId</span></span>
<span data-ttu-id="20928-127">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="20928-127">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="20928-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="20928-128">-Confirm</span></span>
<span data-ttu-id="20928-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="20928-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20928-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20928-130">-WhatIf</span></span>
<span data-ttu-id="20928-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="20928-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20928-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="20928-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20928-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20928-133">CommonParameters</span></span>
<span data-ttu-id="20928-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="20928-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20928-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="20928-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20928-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="20928-136">INPUTS</span></span>

### <span data-ttu-id="20928-137">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ICheckNameAvailabilityDefinition</span><span class="sxs-lookup"><span data-stu-id="20928-137">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityDefinition</span></span>

### <span data-ttu-id="20928-138">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. ısubscriptionsadminıdentity</span><span class="sxs-lookup"><span data-stu-id="20928-138">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="20928-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="20928-139">OUTPUTS</span></span>

### <span data-ttu-id="20928-140">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ICheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="20928-140">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityResponse</span></span>

<span data-ttu-id="20928-141">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="20928-141">ALIASES</span></span>

## <span data-ttu-id="20928-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="20928-142">NOTES</span></span>

<span data-ttu-id="20928-143">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="20928-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="20928-144">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="20928-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="20928-145">INPUTOBJECT <ISubscriptionsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="20928-145">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="20928-146">`[DelegatedProvider <String>]`: Delegatedpprovider tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="20928-146">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="20928-147">`[DelegatedProviderSubscriptionId <String>]`: Temsilci sağlayıcı abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="20928-147">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="20928-148">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="20928-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="20928-149">`[Location <String>]`: AzureStack konumu.</span><span class="sxs-lookup"><span data-stu-id="20928-149">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="20928-150">`[ManifestName <String>]`: Bildirim adı.</span><span class="sxs-lookup"><span data-stu-id="20928-150">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="20928-151">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="20928-151">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="20928-152">`[OfferDelegationName <String>]`: Teklif temsilcisinin adı.</span><span class="sxs-lookup"><span data-stu-id="20928-152">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="20928-153">`[OperationsStatusName <String>]`: İşlem durumu adı.</span><span class="sxs-lookup"><span data-stu-id="20928-153">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="20928-154">`[Plan <String>]`: Planın adı.</span><span class="sxs-lookup"><span data-stu-id="20928-154">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="20928-155">`[PlanAcquisitionId <String>]`: Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="20928-155">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="20928-156">`[Quota <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="20928-156">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="20928-157">`[ResourceGroupName <String>]`: Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="20928-157">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="20928-158">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="20928-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="20928-159">`[TargetSubscriptionId <String>]`: Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="20928-159">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="20928-160">`[Tenant <String>]`: Dizin kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="20928-160">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="20928-161"><ICheckNameAvailabilityDefinition>Ad kullanılabilirliği: ad kullanılabilirliğini denetleme eylem tanımı.</span><span class="sxs-lookup"><span data-stu-id="20928-161">NAMEAVAILABILITYDEFINITION <ICheckNameAvailabilityDefinition>: The check name availability action definition.</span></span>
  - <span data-ttu-id="20928-162">`[Name <String>]`: Doğrulanacak kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="20928-162">`[Name <String>]`: The resource name to verify.</span></span>
  - <span data-ttu-id="20928-163">`[ResourceType <String>]`: Doğrulanacak kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="20928-163">`[ResourceType <String>]`: The resource type to verify.</span></span>

## <span data-ttu-id="20928-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="20928-164">RELATED LINKS</span></span>

