---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: c73a4c4bcc482b7e6e1281d0bc4ee6c29921b745
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94105144"
---
# <span data-ttu-id="07a73-101">Get-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="07a73-101">Get-AzsAcquiredPlan</span></span>

## <span data-ttu-id="07a73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07a73-102">SYNOPSIS</span></span>
<span data-ttu-id="07a73-103">Teklif kullanan bir abonelik tarafından alınan belirtilen planı alır.</span><span class="sxs-lookup"><span data-stu-id="07a73-103">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="07a73-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07a73-104">SYNTAX</span></span>

### <span data-ttu-id="07a73-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="07a73-105">List (Default)</span></span>
```
Get-AzsAcquiredPlan -TargetSubscriptionId <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="07a73-106">Al</span><span class="sxs-lookup"><span data-stu-id="07a73-106">Get</span></span>
```
Get-AzsAcquiredPlan -PlanAcquisitionId <String> -TargetSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="07a73-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="07a73-107">GetViaIdentity</span></span>
```
Get-AzsAcquiredPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="07a73-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="07a73-108">DESCRIPTION</span></span>
<span data-ttu-id="07a73-109">Teklif kullanan bir abonelik tarafından alınan belirtilen planı alır.</span><span class="sxs-lookup"><span data-stu-id="07a73-109">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="07a73-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07a73-110">EXAMPLES</span></span>

### <span data-ttu-id="07a73-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="07a73-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsAcquiredPlan -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

AcquisitionId       : 718c7f7c-4868-479a-98ce-5caaa8f158c1
AcquisitionTime     : 3/12/2020 11:16:08 PM
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/acquiredPlan
                      s/718c7f7c-4868-479a-98ce-5caaa8f158c1
PlanId              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/plans/testplan
ProvisioningState   : Succeeded
```

<span data-ttu-id="07a73-112">Aboneliğin erişimi olan tüm alınan planların koleksiyonunu edinin.</span><span class="sxs-lookup"><span data-stu-id="07a73-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="07a73-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07a73-113">PARAMETERS</span></span>

### <span data-ttu-id="07a73-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07a73-114">-DefaultProfile</span></span>
<span data-ttu-id="07a73-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="07a73-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07a73-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07a73-116">-InputObject</span></span>
<span data-ttu-id="07a73-117">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07a73-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="07a73-118">-Planlama</span><span class="sxs-lookup"><span data-stu-id="07a73-118">-PlanAcquisitionId</span></span>
<span data-ttu-id="07a73-119">Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="07a73-119">The plan acquisition Identifier</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="07a73-120">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="07a73-120">-SubscriptionId</span></span>
<span data-ttu-id="07a73-121">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="07a73-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="07a73-122">-Targetsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="07a73-122">-TargetSubscriptionId</span></span>
<span data-ttu-id="07a73-123">Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="07a73-123">The target subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="07a73-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07a73-124">CommonParameters</span></span>
<span data-ttu-id="07a73-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07a73-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07a73-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="07a73-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07a73-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07a73-127">INPUTS</span></span>

### <span data-ttu-id="07a73-128">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. ısubscriptionsadminıdentity</span><span class="sxs-lookup"><span data-stu-id="07a73-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="07a73-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07a73-129">OUTPUTS</span></span>

### <span data-ttu-id="07a73-130">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ıplanalımı</span><span class="sxs-lookup"><span data-stu-id="07a73-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="07a73-131">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="07a73-131">ALIASES</span></span>

<span data-ttu-id="07a73-132">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="07a73-132">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="07a73-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07a73-133">NOTES</span></span>

<span data-ttu-id="07a73-134">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="07a73-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="07a73-135">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="07a73-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="07a73-136">INPUTOBJECT <ISubscriptionsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="07a73-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="07a73-137">`[DelegatedProvider <String>]`: Delegatedpprovider tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="07a73-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="07a73-138">`[DelegatedProviderSubscriptionId <String>]`: Temsilci sağlayıcı abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="07a73-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="07a73-139">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="07a73-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="07a73-140">`[Location <String>]`: AzureStack konumu.</span><span class="sxs-lookup"><span data-stu-id="07a73-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="07a73-141">`[ManifestName <String>]`: Bildirim adı.</span><span class="sxs-lookup"><span data-stu-id="07a73-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="07a73-142">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="07a73-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="07a73-143">`[OfferDelegationName <String>]`: Teklif temsilcisinin adı.</span><span class="sxs-lookup"><span data-stu-id="07a73-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="07a73-144">`[OperationsStatusName <String>]`: İşlem durumu adı.</span><span class="sxs-lookup"><span data-stu-id="07a73-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="07a73-145">`[Plan <String>]`: Planın adı.</span><span class="sxs-lookup"><span data-stu-id="07a73-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="07a73-146">`[PlanAcquisitionId <String>]`: Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="07a73-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="07a73-147">`[Quota <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="07a73-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="07a73-148">`[ResourceGroupName <String>]`: Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="07a73-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="07a73-149">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="07a73-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="07a73-150">`[TargetSubscriptionId <String>]`: Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="07a73-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="07a73-151">`[Tenant <String>]`: Dizin kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="07a73-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="07a73-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07a73-152">RELATED LINKS</span></span>

