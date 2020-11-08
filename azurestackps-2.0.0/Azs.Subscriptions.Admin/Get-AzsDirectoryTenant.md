---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdirectorytenant
schema: 2.0.0
ms.openlocfilehash: f516562b6bc4a136c64a15fa1f128cd1bda502d9
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94105132"
---
# <span data-ttu-id="c2202-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="c2202-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="c2202-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2202-102">SYNOPSIS</span></span>
<span data-ttu-id="c2202-103">Bir dizin adını adıyla edinin.</span><span class="sxs-lookup"><span data-stu-id="c2202-103">Get a directory tenant by name.</span></span>

## <span data-ttu-id="c2202-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2202-104">SYNTAX</span></span>

### <span data-ttu-id="c2202-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c2202-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2202-106">Al</span><span class="sxs-lookup"><span data-stu-id="c2202-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c2202-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="c2202-107">GetViaIdentity</span></span>
```
Get-AzsDirectoryTenant -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2202-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2202-108">DESCRIPTION</span></span>
<span data-ttu-id="c2202-109">Bir dizin adını adıyla edinin.</span><span class="sxs-lookup"><span data-stu-id="c2202-109">Get a directory tenant by name.</span></span>

## <span data-ttu-id="c2202-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2202-110">EXAMPLES</span></span>

### <span data-ttu-id="c2202-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c2202-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDirectoryTenant -ResourceGroupName 'system.redmond'

Location Name                           Type                                          
-------- ----                           ----                                          
redmond  azurestack01.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
redmond  azurestack02.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
```

<span data-ttu-id="c2202-112">Geçerli aboneliğin ve verilen kaynak grubu adının altındaki tüm dizin kiracıları listeler.</span><span class="sxs-lookup"><span data-stu-id="c2202-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="c2202-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2202-113">PARAMETERS</span></span>

### <span data-ttu-id="c2202-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2202-114">-DefaultProfile</span></span>
<span data-ttu-id="c2202-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c2202-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2202-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2202-116">-InputObject</span></span>
<span data-ttu-id="c2202-117">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c2202-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c2202-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="c2202-118">-Name</span></span>
<span data-ttu-id="c2202-119">Dizin kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="c2202-119">Directory tenant name.</span></span>

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

### <span data-ttu-id="c2202-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2202-120">-ResourceGroupName</span></span>
<span data-ttu-id="c2202-121">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="c2202-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="c2202-122">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c2202-122">-SubscriptionId</span></span>
<span data-ttu-id="c2202-123">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c2202-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c2202-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2202-124">CommonParameters</span></span>
<span data-ttu-id="c2202-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2202-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2202-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c2202-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2202-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2202-127">INPUTS</span></span>

### <span data-ttu-id="c2202-128">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. ısubscriptionsadminıdentity</span><span class="sxs-lookup"><span data-stu-id="c2202-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="c2202-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2202-129">OUTPUTS</span></span>

### <span data-ttu-id="c2202-130">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ıdirectorytenant</span><span class="sxs-lookup"><span data-stu-id="c2202-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IDirectoryTenant</span></span>

<span data-ttu-id="c2202-131">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="c2202-131">ALIASES</span></span>

## <span data-ttu-id="c2202-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2202-132">NOTES</span></span>

<span data-ttu-id="c2202-133">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c2202-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c2202-134">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c2202-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c2202-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="c2202-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c2202-136">`[DelegatedProvider <String>]`: Delegatedpprovider tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="c2202-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="c2202-137">`[DelegatedProviderSubscriptionId <String>]`: Temsilci sağlayıcı abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="c2202-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="c2202-138">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="c2202-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c2202-139">`[Location <String>]`: AzureStack konumu.</span><span class="sxs-lookup"><span data-stu-id="c2202-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="c2202-140">`[ManifestName <String>]`: Bildirim adı.</span><span class="sxs-lookup"><span data-stu-id="c2202-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="c2202-141">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="c2202-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="c2202-142">`[OfferDelegationName <String>]`: Teklif temsilcisinin adı.</span><span class="sxs-lookup"><span data-stu-id="c2202-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="c2202-143">`[OperationsStatusName <String>]`: İşlem durumu adı.</span><span class="sxs-lookup"><span data-stu-id="c2202-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="c2202-144">`[Plan <String>]`: Planın adı.</span><span class="sxs-lookup"><span data-stu-id="c2202-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="c2202-145">`[PlanAcquisitionId <String>]`: Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="c2202-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="c2202-146">`[Quota <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="c2202-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="c2202-147">`[ResourceGroupName <String>]`: Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="c2202-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="c2202-148">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c2202-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c2202-149">`[TargetSubscriptionId <String>]`: Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c2202-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="c2202-150">`[Tenant <String>]`: Dizin kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="c2202-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="c2202-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c2202-151">RELATED LINKS</span></span>

