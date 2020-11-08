---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsplan
schema: 2.0.0
ms.openlocfilehash: 4aa59d41bc13d79e487465a6a0721ec19ed68bb8
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94105202"
---
# <span data-ttu-id="b5619-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="b5619-101">Get-AzsPlan</span></span>

## <span data-ttu-id="b5619-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5619-102">SYNOPSIS</span></span>
<span data-ttu-id="b5619-103">Belirtilen planı edinin.</span><span class="sxs-lookup"><span data-stu-id="b5619-103">Get the specified plan.</span></span>

## <span data-ttu-id="b5619-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5619-104">SYNTAX</span></span>

### <span data-ttu-id="b5619-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b5619-105">List (Default)</span></span>
```
Get-AzsPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b5619-106">Al</span><span class="sxs-lookup"><span data-stu-id="b5619-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b5619-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="b5619-107">GetViaIdentity</span></span>
```
Get-AzsPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b5619-108">List1</span><span class="sxs-lookup"><span data-stu-id="b5619-108">List1</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5619-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5619-109">DESCRIPTION</span></span>
<span data-ttu-id="b5619-110">Belirtilen planı edinin.</span><span class="sxs-lookup"><span data-stu-id="b5619-110">Get the specified plan.</span></span>

## <span data-ttu-id="b5619-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5619-111">EXAMPLES</span></span>

### <span data-ttu-id="b5619-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b5619-112">Example 1</span></span>
```powershell
PS C:\> Get-AzsPlan -Name "testplan" -ResourceGroupName "testrg"

Description         : testplan
DisplayName         : testplan
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan
Location            : redmond
Name                : testplan
PropertiesName      : testplan
QuotaIds            : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota}
SkuIds              : 
SubscriptionCount   : 1
Tags                : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                : Microsoft.Subscriptions.Admin/plans
```

<span data-ttu-id="b5619-113">Bu aboneliklerin altında bir</span><span class="sxs-lookup"><span data-stu-id="b5619-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="b5619-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5619-114">PARAMETERS</span></span>

### <span data-ttu-id="b5619-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5619-115">-DefaultProfile</span></span>
<span data-ttu-id="b5619-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5619-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5619-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5619-117">-InputObject</span></span>
<span data-ttu-id="b5619-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5619-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b5619-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b5619-119">-Name</span></span>
<span data-ttu-id="b5619-120">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="b5619-120">Name of the plan.</span></span>

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

### <span data-ttu-id="b5619-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5619-121">-ResourceGroupName</span></span>
<span data-ttu-id="b5619-122">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="b5619-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="b5619-123">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="b5619-123">-SubscriptionId</span></span>
<span data-ttu-id="b5619-124">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b5619-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b5619-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5619-125">CommonParameters</span></span>
<span data-ttu-id="b5619-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5619-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5619-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b5619-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5619-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5619-128">INPUTS</span></span>

### <span data-ttu-id="b5619-129">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. ısubscriptionsadminıdentity</span><span class="sxs-lookup"><span data-stu-id="b5619-129">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="b5619-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5619-130">OUTPUTS</span></span>

### <span data-ttu-id="b5619-131">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="b5619-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

<span data-ttu-id="b5619-132">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="b5619-132">ALIASES</span></span>

## <span data-ttu-id="b5619-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5619-133">NOTES</span></span>

<span data-ttu-id="b5619-134">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b5619-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b5619-135">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b5619-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b5619-136">INPUTOBJECT <ISubscriptionsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="b5619-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b5619-137">`[DelegatedProvider <String>]`: Delegatedpprovider tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="b5619-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="b5619-138">`[DelegatedProviderSubscriptionId <String>]`: Temsilci sağlayıcı abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="b5619-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="b5619-139">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="b5619-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b5619-140">`[Location <String>]`: AzureStack konumu.</span><span class="sxs-lookup"><span data-stu-id="b5619-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="b5619-141">`[ManifestName <String>]`: Bildirim adı.</span><span class="sxs-lookup"><span data-stu-id="b5619-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="b5619-142">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="b5619-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="b5619-143">`[OfferDelegationName <String>]`: Teklif temsilcisinin adı.</span><span class="sxs-lookup"><span data-stu-id="b5619-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="b5619-144">`[OperationsStatusName <String>]`: İşlem durumu adı.</span><span class="sxs-lookup"><span data-stu-id="b5619-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="b5619-145">`[Plan <String>]`: Planın adı.</span><span class="sxs-lookup"><span data-stu-id="b5619-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="b5619-146">`[PlanAcquisitionId <String>]`: Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="b5619-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="b5619-147">`[Quota <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="b5619-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="b5619-148">`[ResourceGroupName <String>]`: Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="b5619-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="b5619-149">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b5619-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b5619-150">`[TargetSubscriptionId <String>]`: Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b5619-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="b5619-151">`[Tenant <String>]`: Dizin kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="b5619-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="b5619-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5619-152">RELATED LINKS</span></span>

