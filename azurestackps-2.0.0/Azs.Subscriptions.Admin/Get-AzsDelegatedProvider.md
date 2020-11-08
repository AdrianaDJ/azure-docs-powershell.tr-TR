---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdelegatedprovider
schema: 2.0.0
ms.openlocfilehash: 2c6c87ce0b40fae228756d4a9dd452b49ce1aad2
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94105135"
---
# <span data-ttu-id="3a45a-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="3a45a-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="3a45a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a45a-102">SYNOPSIS</span></span>
<span data-ttu-id="3a45a-103">Belirtilen temsilci sağlayıcı edinin.</span><span class="sxs-lookup"><span data-stu-id="3a45a-103">Get the specified delegated provider.</span></span>

## <span data-ttu-id="3a45a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a45a-104">SYNTAX</span></span>

### <span data-ttu-id="3a45a-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3a45a-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3a45a-106">Al</span><span class="sxs-lookup"><span data-stu-id="3a45a-106">Get</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3a45a-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="3a45a-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProvider -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a45a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a45a-108">DESCRIPTION</span></span>
<span data-ttu-id="3a45a-109">Belirtilen temsilci sağlayıcı edinin.</span><span class="sxs-lookup"><span data-stu-id="3a45a-109">Get the specified delegated provider.</span></span>

## <span data-ttu-id="3a45a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a45a-110">EXAMPLES</span></span>

### <span data-ttu-id="3a45a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3a45a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProvider -DelegatedProviderId "ed3e275b-87d1-4e94-9962-b3700287bdbc" | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : cnur4866tenantresellersubscription843
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ed3e275b-87d1-4e94-9962-b3700287bdbc
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/cnur4866resellersubscrrg843/providers/Microsoft.Subscriptions.Admin/offers/cnur4866tenantsubsvcoffe
                                  r843
Owner                           : tenantadmin1@msazurestack.onmicrosoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ed3e275b-87d1-4e94-9962-b3700287bdbc
TenantId                        : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="3a45a-112">Belirli bir temsilci sağlayıcı edinin.</span><span class="sxs-lookup"><span data-stu-id="3a45a-112">Get a specific delegated provider.</span></span>

## <span data-ttu-id="3a45a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a45a-113">PARAMETERS</span></span>

### <span data-ttu-id="3a45a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a45a-114">-DefaultProfile</span></span>
<span data-ttu-id="3a45a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3a45a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a45a-116">-Delegatevseçproviderıd</span><span class="sxs-lookup"><span data-stu-id="3a45a-116">-DelegatedProviderId</span></span>
<span data-ttu-id="3a45a-117">Temsilci kimliği.</span><span class="sxs-lookup"><span data-stu-id="3a45a-117">DelegatedProvider identifier.</span></span>

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

### <span data-ttu-id="3a45a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a45a-118">-InputObject</span></span>
<span data-ttu-id="3a45a-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3a45a-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3a45a-120">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="3a45a-120">-SubscriptionId</span></span>
<span data-ttu-id="3a45a-121">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3a45a-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3a45a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a45a-122">CommonParameters</span></span>
<span data-ttu-id="3a45a-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a45a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a45a-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3a45a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a45a-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a45a-125">INPUTS</span></span>

### <span data-ttu-id="3a45a-126">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. ısubscriptionsadminıdentity</span><span class="sxs-lookup"><span data-stu-id="3a45a-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="3a45a-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a45a-127">OUTPUTS</span></span>

### <span data-ttu-id="3a45a-128">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ısubscriptiondefinition</span><span class="sxs-lookup"><span data-stu-id="3a45a-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="3a45a-129">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="3a45a-129">ALIASES</span></span>

## <span data-ttu-id="3a45a-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a45a-130">NOTES</span></span>

<span data-ttu-id="3a45a-131">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3a45a-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3a45a-132">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3a45a-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3a45a-133">INPUTOBJECT <ISubscriptionsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="3a45a-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3a45a-134">`[DelegatedProvider <String>]`: Delegatedpprovider tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="3a45a-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="3a45a-135">`[DelegatedProviderSubscriptionId <String>]`: Temsilci sağlayıcı abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="3a45a-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="3a45a-136">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="3a45a-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3a45a-137">`[Location <String>]`: AzureStack konumu.</span><span class="sxs-lookup"><span data-stu-id="3a45a-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="3a45a-138">`[ManifestName <String>]`: Bildirim adı.</span><span class="sxs-lookup"><span data-stu-id="3a45a-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="3a45a-139">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="3a45a-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="3a45a-140">`[OfferDelegationName <String>]`: Teklif temsilcisinin adı.</span><span class="sxs-lookup"><span data-stu-id="3a45a-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="3a45a-141">`[OperationsStatusName <String>]`: İşlem durumu adı.</span><span class="sxs-lookup"><span data-stu-id="3a45a-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="3a45a-142">`[Plan <String>]`: Planın adı.</span><span class="sxs-lookup"><span data-stu-id="3a45a-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="3a45a-143">`[PlanAcquisitionId <String>]`: Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="3a45a-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="3a45a-144">`[Quota <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="3a45a-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="3a45a-145">`[ResourceGroupName <String>]`: Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="3a45a-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="3a45a-146">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3a45a-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3a45a-147">`[TargetSubscriptionId <String>]`: Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3a45a-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="3a45a-148">`[Tenant <String>]`: Dizin kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="3a45a-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="3a45a-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a45a-149">RELATED LINKS</span></span>

