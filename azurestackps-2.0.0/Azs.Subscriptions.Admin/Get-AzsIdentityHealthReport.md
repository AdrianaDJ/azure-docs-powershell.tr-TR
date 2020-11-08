---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsidentityhealthreport
schema: 2.0.0
ms.openlocfilehash: 995ddf191f870fee9d27438ebea6d29729ca4c9f
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94105133"
---
# <span data-ttu-id="cccc5-101">Get-AzsIdentityHealthReport</span><span class="sxs-lookup"><span data-stu-id="cccc5-101">Get-AzsIdentityHealthReport</span></span>

## <span data-ttu-id="cccc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cccc5-102">SYNOPSIS</span></span>
<span data-ttu-id="cccc5-103">Kimlik durumunu denetler</span><span class="sxs-lookup"><span data-stu-id="cccc5-103">Checks the identity health</span></span>

## <span data-ttu-id="cccc5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cccc5-104">SYNTAX</span></span>

### <span data-ttu-id="cccc5-105">Çek (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cccc5-105">Check (Default)</span></span>
```
Get-AzsIdentityHealthReport [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cccc5-106">Checkviaıdentity</span><span class="sxs-lookup"><span data-stu-id="cccc5-106">CheckViaIdentity</span></span>
```
Get-AzsIdentityHealthReport -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cccc5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cccc5-107">DESCRIPTION</span></span>
<span data-ttu-id="cccc5-108">Kimlik durumunu denetler</span><span class="sxs-lookup"><span data-stu-id="cccc5-108">Checks the identity health</span></span>

## <span data-ttu-id="cccc5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cccc5-109">EXAMPLES</span></span>

### <span data-ttu-id="cccc5-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cccc5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzsIdentityHealthReport

ReportEndTimeUtc      ReportStartTimeUtc    Status 
----------------      ------------------    ------ 
3/12/2020 11:41:08 PM 3/12/2020 11:40:50 PM Healthy
```

<span data-ttu-id="cccc5-111">Kimlik durumunun durumunu edinin.</span><span class="sxs-lookup"><span data-stu-id="cccc5-111">Get the status of the Identity Health.</span></span>

## <span data-ttu-id="cccc5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cccc5-112">PARAMETERS</span></span>

### <span data-ttu-id="cccc5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cccc5-113">-DefaultProfile</span></span>
<span data-ttu-id="cccc5-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cccc5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cccc5-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cccc5-115">-InputObject</span></span>
<span data-ttu-id="cccc5-116">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cccc5-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="cccc5-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="cccc5-117">-SubscriptionId</span></span>
<span data-ttu-id="cccc5-118">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cccc5-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cccc5-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="cccc5-119">-Confirm</span></span>
<span data-ttu-id="cccc5-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cccc5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cccc5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cccc5-121">-WhatIf</span></span>
<span data-ttu-id="cccc5-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cccc5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cccc5-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cccc5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cccc5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cccc5-124">CommonParameters</span></span>
<span data-ttu-id="cccc5-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cccc5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cccc5-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cccc5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cccc5-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cccc5-127">INPUTS</span></span>

### <span data-ttu-id="cccc5-128">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. ısubscriptionsadminıdentity</span><span class="sxs-lookup"><span data-stu-id="cccc5-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="cccc5-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cccc5-129">OUTPUTS</span></span>

### <span data-ttu-id="cccc5-130">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. ııdentityhealthcheckreportdefinition</span><span class="sxs-lookup"><span data-stu-id="cccc5-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IIdentityHealthCheckReportDefinition</span></span>

<span data-ttu-id="cccc5-131">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="cccc5-131">ALIASES</span></span>

## <span data-ttu-id="cccc5-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cccc5-132">NOTES</span></span>

<span data-ttu-id="cccc5-133">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="cccc5-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cccc5-134">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cccc5-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cccc5-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="cccc5-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cccc5-136">`[DelegatedProvider <String>]`: Delegatedpprovider tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="cccc5-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="cccc5-137">`[DelegatedProviderSubscriptionId <String>]`: Temsilci sağlayıcı abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="cccc5-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="cccc5-138">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="cccc5-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cccc5-139">`[Location <String>]`: AzureStack konumu.</span><span class="sxs-lookup"><span data-stu-id="cccc5-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="cccc5-140">`[ManifestName <String>]`: Bildirim adı.</span><span class="sxs-lookup"><span data-stu-id="cccc5-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="cccc5-141">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="cccc5-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="cccc5-142">`[OfferDelegationName <String>]`: Teklif temsilcisinin adı.</span><span class="sxs-lookup"><span data-stu-id="cccc5-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="cccc5-143">`[OperationsStatusName <String>]`: İşlem durumu adı.</span><span class="sxs-lookup"><span data-stu-id="cccc5-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="cccc5-144">`[Plan <String>]`: Planın adı.</span><span class="sxs-lookup"><span data-stu-id="cccc5-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="cccc5-145">`[PlanAcquisitionId <String>]`: Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="cccc5-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="cccc5-146">`[Quota <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="cccc5-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="cccc5-147">`[ResourceGroupName <String>]`: Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="cccc5-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="cccc5-148">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cccc5-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cccc5-149">`[TargetSubscriptionId <String>]`: Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cccc5-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="cccc5-150">`[Tenant <String>]`: Dizin kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="cccc5-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="cccc5-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cccc5-151">RELATED LINKS</span></span>

