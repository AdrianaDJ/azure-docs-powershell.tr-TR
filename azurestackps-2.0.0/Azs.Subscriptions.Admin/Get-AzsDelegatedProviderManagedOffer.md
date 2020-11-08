---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdelegatedprovidermanagedoffer
schema: 2.0.0
ms.openlocfilehash: 238fe2a9c3f0cf1d4fdefc5a09231066152cfe60
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94105136"
---
# <span data-ttu-id="73641-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="73641-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="73641-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73641-102">SYNOPSIS</span></span>
<span data-ttu-id="73641-103">Belirtilen temsilci sağlayıcı teklifini edinin.</span><span class="sxs-lookup"><span data-stu-id="73641-103">Get the specified delegated provider offer.</span></span>

## <span data-ttu-id="73641-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="73641-104">SYNTAX</span></span>

### <span data-ttu-id="73641-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="73641-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="73641-106">Al</span><span class="sxs-lookup"><span data-stu-id="73641-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId <String> -Name <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="73641-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="73641-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProviderManagedOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="73641-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="73641-108">DESCRIPTION</span></span>
<span data-ttu-id="73641-109">Belirtilen temsilci sağlayıcı teklifini edinin.</span><span class="sxs-lookup"><span data-stu-id="73641-109">Get the specified delegated provider offer.</span></span>

## <span data-ttu-id="73641-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="73641-110">EXAMPLES</span></span>

### <span data-ttu-id="73641-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="73641-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"

{{ Add output here }}
```

<span data-ttu-id="73641-112">Temsilci sağlayıcı tekliflerinin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="73641-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="73641-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="73641-113">PARAMETERS</span></span>

### <span data-ttu-id="73641-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73641-114">-DefaultProfile</span></span>
<span data-ttu-id="73641-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="73641-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73641-116">-Delegatevseçprovidersubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="73641-116">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="73641-117">Sağlayıcı aboneliği tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="73641-117">Delegated provider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: DelegatedProviderId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="73641-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73641-118">-InputObject</span></span>
<span data-ttu-id="73641-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="73641-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="73641-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="73641-120">-Name</span></span>
<span data-ttu-id="73641-121">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="73641-121">Name of an offer.</span></span>

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

### <span data-ttu-id="73641-122">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="73641-122">-SubscriptionId</span></span>
<span data-ttu-id="73641-123">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="73641-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="73641-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73641-124">CommonParameters</span></span>
<span data-ttu-id="73641-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="73641-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73641-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="73641-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73641-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="73641-127">INPUTS</span></span>

### <span data-ttu-id="73641-128">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. ısubscriptionsadminıdentity</span><span class="sxs-lookup"><span data-stu-id="73641-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="73641-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="73641-129">OUTPUTS</span></span>

### <span data-ttu-id="73641-130">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ıdelegatevseçproviderteklifini</span><span class="sxs-lookup"><span data-stu-id="73641-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IDelegatedProviderOffer</span></span>

<span data-ttu-id="73641-131">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="73641-131">ALIASES</span></span>

## <span data-ttu-id="73641-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="73641-132">NOTES</span></span>

<span data-ttu-id="73641-133">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="73641-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="73641-134">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="73641-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="73641-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="73641-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="73641-136">`[DelegatedProvider <String>]`: Delegatedpprovider tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="73641-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="73641-137">`[DelegatedProviderSubscriptionId <String>]`: Temsilci sağlayıcı abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="73641-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="73641-138">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="73641-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="73641-139">`[Location <String>]`: AzureStack konumu.</span><span class="sxs-lookup"><span data-stu-id="73641-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="73641-140">`[ManifestName <String>]`: Bildirim adı.</span><span class="sxs-lookup"><span data-stu-id="73641-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="73641-141">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="73641-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="73641-142">`[OfferDelegationName <String>]`: Teklif temsilcisinin adı.</span><span class="sxs-lookup"><span data-stu-id="73641-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="73641-143">`[OperationsStatusName <String>]`: İşlem durumu adı.</span><span class="sxs-lookup"><span data-stu-id="73641-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="73641-144">`[Plan <String>]`: Planın adı.</span><span class="sxs-lookup"><span data-stu-id="73641-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="73641-145">`[PlanAcquisitionId <String>]`: Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="73641-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="73641-146">`[Quota <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="73641-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="73641-147">`[ResourceGroupName <String>]`: Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="73641-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="73641-148">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="73641-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="73641-149">`[TargetSubscriptionId <String>]`: Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="73641-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="73641-150">`[Tenant <String>]`: Dizin kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="73641-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="73641-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="73641-151">RELATED LINKS</span></span>

