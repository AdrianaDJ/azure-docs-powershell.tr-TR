---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsadminmanagedoffer
schema: 2.0.0
ms.openlocfilehash: 79cac7a530a9aedc1e53120b29eb2dd8cb73489b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94107092"
---
# <span data-ttu-id="78713-101">Get-AzsAdminManagedOffer</span><span class="sxs-lookup"><span data-stu-id="78713-101">Get-AzsAdminManagedOffer</span></span>

## <span data-ttu-id="78713-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78713-102">SYNOPSIS</span></span>
<span data-ttu-id="78713-103">Belirtilen teklifi edinin.</span><span class="sxs-lookup"><span data-stu-id="78713-103">Get the specified offer.</span></span>

## <span data-ttu-id="78713-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="78713-104">SYNTAX</span></span>

### <span data-ttu-id="78713-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="78713-105">List (Default)</span></span>
```
Get-AzsAdminManagedOffer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="78713-106">Al</span><span class="sxs-lookup"><span data-stu-id="78713-106">Get</span></span>
```
Get-AzsAdminManagedOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="78713-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="78713-107">GetViaIdentity</span></span>
```
Get-AzsAdminManagedOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="78713-108">List1</span><span class="sxs-lookup"><span data-stu-id="78713-108">List1</span></span>
```
Get-AzsAdminManagedOffer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="78713-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="78713-109">DESCRIPTION</span></span>
<span data-ttu-id="78713-110">Belirtilen teklifi edinin.</span><span class="sxs-lookup"><span data-stu-id="78713-110">Get the specified offer.</span></span>

## <span data-ttu-id="78713-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="78713-111">EXAMPLES</span></span>

### <span data-ttu-id="78713-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="78713-112">Example 1</span></span>
```powershell
PS C:\> Get-AzsAdminManagedOffer -Name "testoffer" -ResourceGroupName "testrg"

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

<span data-ttu-id="78713-113">Get by name and ResourceGroupName ile</span><span class="sxs-lookup"><span data-stu-id="78713-113">Get offer by Name and ResourceGroupName</span></span>

## <span data-ttu-id="78713-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="78713-114">PARAMETERS</span></span>

### <span data-ttu-id="78713-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78713-115">-DefaultProfile</span></span>
<span data-ttu-id="78713-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="78713-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78713-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78713-117">-InputObject</span></span>
<span data-ttu-id="78713-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="78713-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="78713-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="78713-119">-Name</span></span>
<span data-ttu-id="78713-120">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="78713-120">Name of an offer.</span></span>

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

### <span data-ttu-id="78713-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78713-121">-ResourceGroupName</span></span>
<span data-ttu-id="78713-122">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="78713-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="78713-123">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="78713-123">-SubscriptionId</span></span>
<span data-ttu-id="78713-124">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="78713-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="78713-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78713-125">CommonParameters</span></span>
<span data-ttu-id="78713-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="78713-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78713-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="78713-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78713-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="78713-128">INPUTS</span></span>

### <span data-ttu-id="78713-129">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. ısubscriptionsadminıdentity</span><span class="sxs-lookup"><span data-stu-id="78713-129">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="78713-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="78713-130">OUTPUTS</span></span>

### <span data-ttu-id="78713-131">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ıteklifini</span><span class="sxs-lookup"><span data-stu-id="78713-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="78713-132">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="78713-132">ALIASES</span></span>

<span data-ttu-id="78713-133">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="78713-133">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="78713-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="78713-134">NOTES</span></span>

<span data-ttu-id="78713-135">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="78713-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="78713-136">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="78713-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="78713-137">INPUTOBJECT <ISubscriptionsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="78713-137">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="78713-138">`[DelegatedProvider <String>]`: Delegatedpprovider tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="78713-138">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="78713-139">`[DelegatedProviderSubscriptionId <String>]`: Temsilci sağlayıcı abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="78713-139">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="78713-140">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="78713-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="78713-141">`[Location <String>]`: AzureStack konumu.</span><span class="sxs-lookup"><span data-stu-id="78713-141">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="78713-142">`[ManifestName <String>]`: Bildirim adı.</span><span class="sxs-lookup"><span data-stu-id="78713-142">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="78713-143">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="78713-143">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="78713-144">`[OfferDelegationName <String>]`: Teklif temsilcisinin adı.</span><span class="sxs-lookup"><span data-stu-id="78713-144">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="78713-145">`[OperationsStatusName <String>]`: İşlem durumu adı.</span><span class="sxs-lookup"><span data-stu-id="78713-145">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="78713-146">`[Plan <String>]`: Planın adı.</span><span class="sxs-lookup"><span data-stu-id="78713-146">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="78713-147">`[PlanAcquisitionId <String>]`: Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="78713-147">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="78713-148">`[Quota <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="78713-148">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="78713-149">`[ResourceGroupName <String>]`: Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="78713-149">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="78713-150">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="78713-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="78713-151">`[TargetSubscriptionId <String>]`: Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="78713-151">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="78713-152">`[Tenant <String>]`: Dizin kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="78713-152">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="78713-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="78713-153">RELATED LINKS</span></span>

