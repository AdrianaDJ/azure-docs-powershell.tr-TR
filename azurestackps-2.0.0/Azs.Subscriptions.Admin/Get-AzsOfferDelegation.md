---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 995d7296ef1e5b6f846d5343fd072909a877b1ec
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94105119"
---
# <span data-ttu-id="59d1c-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="59d1c-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="59d1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59d1c-102">SYNOPSIS</span></span>
<span data-ttu-id="59d1c-103">Belirtilen teklif temsilcisini edinin.</span><span class="sxs-lookup"><span data-stu-id="59d1c-103">Get the specified offer delegation.</span></span>

## <span data-ttu-id="59d1c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59d1c-104">SYNTAX</span></span>

### <span data-ttu-id="59d1c-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="59d1c-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="59d1c-106">Al</span><span class="sxs-lookup"><span data-stu-id="59d1c-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="59d1c-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="59d1c-107">GetViaIdentity</span></span>
```
Get-AzsOfferDelegation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="59d1c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="59d1c-108">DESCRIPTION</span></span>
<span data-ttu-id="59d1c-109">Belirtilen teklif temsilcisini edinin.</span><span class="sxs-lookup"><span data-stu-id="59d1c-109">Get the specified offer delegation.</span></span>

## <span data-ttu-id="59d1c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59d1c-110">EXAMPLES</span></span>

### <span data-ttu-id="59d1c-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="59d1c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsOfferDelegation -OfferName "delegatedoffer" -ResourceGroupName "testrg"

Id             : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/delegatedoffer/offerDelegations/offerdelegation
Location       : redmond
Name           : delegatedoffer/offerdelegation
SubscriptionId : dbc27112-f67a-4690-ba12-730f71cbb018
Tags           : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type           : Microsoft.Subscriptions.Admin/offers/offerDelegations
```

<span data-ttu-id="59d1c-112">Temsilci seçilen tekliflerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="59d1c-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="59d1c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59d1c-113">PARAMETERS</span></span>

### <span data-ttu-id="59d1c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d1c-114">-DefaultProfile</span></span>
<span data-ttu-id="59d1c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="59d1c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59d1c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59d1c-116">-InputObject</span></span>
<span data-ttu-id="59d1c-117">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="59d1c-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="59d1c-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="59d1c-118">-Name</span></span>
<span data-ttu-id="59d1c-119">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="59d1c-119">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="59d1c-120">-OfferName</span><span class="sxs-lookup"><span data-stu-id="59d1c-120">-OfferName</span></span>
<span data-ttu-id="59d1c-121">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="59d1c-121">Name of an offer.</span></span>

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

### <span data-ttu-id="59d1c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59d1c-122">-ResourceGroupName</span></span>
<span data-ttu-id="59d1c-123">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="59d1c-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="59d1c-124">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="59d1c-124">-SubscriptionId</span></span>
<span data-ttu-id="59d1c-125">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="59d1c-125">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="59d1c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d1c-126">CommonParameters</span></span>
<span data-ttu-id="59d1c-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59d1c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d1c-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="59d1c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d1c-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59d1c-129">INPUTS</span></span>

### <span data-ttu-id="59d1c-130">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. ısubscriptionsadminıdentity</span><span class="sxs-lookup"><span data-stu-id="59d1c-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="59d1c-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59d1c-131">OUTPUTS</span></span>

### <span data-ttu-id="59d1c-132">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ıoffertemsilci</span><span class="sxs-lookup"><span data-stu-id="59d1c-132">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="59d1c-133">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="59d1c-133">ALIASES</span></span>

## <span data-ttu-id="59d1c-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59d1c-134">NOTES</span></span>

<span data-ttu-id="59d1c-135">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="59d1c-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="59d1c-136">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="59d1c-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="59d1c-137">INPUTOBJECT <ISubscriptionsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="59d1c-137">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="59d1c-138">`[DelegatedProvider <String>]`: Delegatedpprovider tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="59d1c-138">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="59d1c-139">`[DelegatedProviderSubscriptionId <String>]`: Temsilci sağlayıcı abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="59d1c-139">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="59d1c-140">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="59d1c-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="59d1c-141">`[Location <String>]`: AzureStack konumu.</span><span class="sxs-lookup"><span data-stu-id="59d1c-141">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="59d1c-142">`[ManifestName <String>]`: Bildirim adı.</span><span class="sxs-lookup"><span data-stu-id="59d1c-142">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="59d1c-143">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="59d1c-143">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="59d1c-144">`[OfferDelegationName <String>]`: Teklif temsilcisinin adı.</span><span class="sxs-lookup"><span data-stu-id="59d1c-144">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="59d1c-145">`[OperationsStatusName <String>]`: İşlem durumu adı.</span><span class="sxs-lookup"><span data-stu-id="59d1c-145">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="59d1c-146">`[Plan <String>]`: Planın adı.</span><span class="sxs-lookup"><span data-stu-id="59d1c-146">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="59d1c-147">`[PlanAcquisitionId <String>]`: Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="59d1c-147">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="59d1c-148">`[Quota <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="59d1c-148">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="59d1c-149">`[ResourceGroupName <String>]`: Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="59d1c-149">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="59d1c-150">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="59d1c-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="59d1c-151">`[TargetSubscriptionId <String>]`: Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="59d1c-151">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="59d1c-152">`[Tenant <String>]`: Dizin kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="59d1c-152">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="59d1c-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59d1c-153">RELATED LINKS</span></span>

