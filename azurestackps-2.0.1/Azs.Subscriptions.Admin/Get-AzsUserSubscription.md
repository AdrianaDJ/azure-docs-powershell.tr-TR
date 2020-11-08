---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: a36406499be15c53e9bfabd8aa9abf56b2afa1c7
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94105339"
---
# <span data-ttu-id="652ca-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="652ca-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="652ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="652ca-102">SYNOPSIS</span></span>
<span data-ttu-id="652ca-103">Belirtilen aboneliği edinin.</span><span class="sxs-lookup"><span data-stu-id="652ca-103">Get a specified subscription.</span></span>

## <span data-ttu-id="652ca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="652ca-104">SYNTAX</span></span>

### <span data-ttu-id="652ca-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="652ca-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="652ca-106">Al</span><span class="sxs-lookup"><span data-stu-id="652ca-106">Get</span></span>
```
Get-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="652ca-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="652ca-107">GetViaIdentity</span></span>
```
Get-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="652ca-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="652ca-108">DESCRIPTION</span></span>
<span data-ttu-id="652ca-109">Belirtilen aboneliği edinin.</span><span class="sxs-lookup"><span data-stu-id="652ca-109">Get a specified subscription.</span></span>

## <span data-ttu-id="652ca-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="652ca-110">EXAMPLES</span></span>

### <span data-ttu-id="652ca-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="652ca-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsUserSubscription | Select-Object -First 1 | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : DRPTestffbffbe5-test-test-test-test-test-test
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ffbffbe5-8905-4f51-b2ed-4717049de782
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Owner                           : user@microsoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ffbffbe5-8905-4f51-b2ed-4717049de782
TenantId                        : 76440dfb-c97c-4fee-8f6c-dff8ddbe816f
```

<span data-ttu-id="652ca-112">Kullanıcı abonelikleri listesini işleç olarak alın.</span><span class="sxs-lookup"><span data-stu-id="652ca-112">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="652ca-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="652ca-113">PARAMETERS</span></span>

### <span data-ttu-id="652ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="652ca-114">-DefaultProfile</span></span>
<span data-ttu-id="652ca-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="652ca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="652ca-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="652ca-116">-Filter</span></span>
<span data-ttu-id="652ca-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="652ca-117">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="652ca-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="652ca-118">-InputObject</span></span>
<span data-ttu-id="652ca-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="652ca-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="652ca-120">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="652ca-120">-SubscriptionId</span></span>
<span data-ttu-id="652ca-121">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="652ca-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="652ca-122">-Targetsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="652ca-122">-TargetSubscriptionId</span></span>
<span data-ttu-id="652ca-123">Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="652ca-123">The target subscription ID.</span></span>

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

### <span data-ttu-id="652ca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="652ca-124">CommonParameters</span></span>
<span data-ttu-id="652ca-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="652ca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="652ca-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="652ca-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="652ca-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="652ca-127">INPUTS</span></span>

### <span data-ttu-id="652ca-128">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. ısubscriptionsadminıdentity</span><span class="sxs-lookup"><span data-stu-id="652ca-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="652ca-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="652ca-129">OUTPUTS</span></span>

### <span data-ttu-id="652ca-130">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ısubscriptiondefinition</span><span class="sxs-lookup"><span data-stu-id="652ca-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="652ca-131">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="652ca-131">ALIASES</span></span>

## <span data-ttu-id="652ca-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="652ca-132">NOTES</span></span>

<span data-ttu-id="652ca-133">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="652ca-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="652ca-134">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="652ca-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="652ca-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="652ca-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="652ca-136">`[DelegatedProvider <String>]`: Delegatedpprovider tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="652ca-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="652ca-137">`[DelegatedProviderSubscriptionId <String>]`: Temsilci sağlayıcı abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="652ca-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="652ca-138">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="652ca-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="652ca-139">`[Location <String>]`: AzureStack konumu.</span><span class="sxs-lookup"><span data-stu-id="652ca-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="652ca-140">`[ManifestName <String>]`: Bildirim adı.</span><span class="sxs-lookup"><span data-stu-id="652ca-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="652ca-141">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="652ca-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="652ca-142">`[OfferDelegationName <String>]`: Teklif temsilcisinin adı.</span><span class="sxs-lookup"><span data-stu-id="652ca-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="652ca-143">`[OperationsStatusName <String>]`: İşlem durumu adı.</span><span class="sxs-lookup"><span data-stu-id="652ca-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="652ca-144">`[Plan <String>]`: Planın adı.</span><span class="sxs-lookup"><span data-stu-id="652ca-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="652ca-145">`[PlanAcquisitionId <String>]`: Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="652ca-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="652ca-146">`[Quota <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="652ca-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="652ca-147">`[ResourceGroupName <String>]`: Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="652ca-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="652ca-148">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="652ca-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="652ca-149">`[TargetSubscriptionId <String>]`: Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="652ca-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="652ca-150">`[Tenant <String>]`: Dizin kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="652ca-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="652ca-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="652ca-151">RELATED LINKS</span></span>

