---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: 80a4353497d0c7894a8c0ac4d95e57e56a6211a1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94107080"
---
# <span data-ttu-id="cf94c-101">Remove-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="cf94c-101">Remove-AzsAcquiredPlan</span></span>

## <span data-ttu-id="cf94c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf94c-102">SYNOPSIS</span></span>
<span data-ttu-id="cf94c-103">Alınan bir planı siler.</span><span class="sxs-lookup"><span data-stu-id="cf94c-103">Deletes an acquired plan.</span></span>

## <span data-ttu-id="cf94c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf94c-104">SYNTAX</span></span>

### <span data-ttu-id="cf94c-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cf94c-105">Delete (Default)</span></span>
```
Remove-AzsAcquiredPlan -PlanAcquisitionId <String> -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cf94c-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="cf94c-106">DeleteViaIdentity</span></span>
```
Remove-AzsAcquiredPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cf94c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf94c-107">DESCRIPTION</span></span>
<span data-ttu-id="cf94c-108">Alınan bir planı siler.</span><span class="sxs-lookup"><span data-stu-id="cf94c-108">Deletes an acquired plan.</span></span>

## <span data-ttu-id="cf94c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf94c-109">EXAMPLES</span></span>

### <span data-ttu-id="cf94c-110">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="cf94c-110">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsAcquiredPlan -PlanAcquisitionId "718c7f7c-4868-479a-98ce-5caaa8f158c2" -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

```

<span data-ttu-id="cf94c-111">Alınan bir planı silme.</span><span class="sxs-lookup"><span data-stu-id="cf94c-111">Delete an acquired plan.</span></span>

## <span data-ttu-id="cf94c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf94c-112">PARAMETERS</span></span>

### <span data-ttu-id="cf94c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf94c-113">-DefaultProfile</span></span>
<span data-ttu-id="cf94c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cf94c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf94c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf94c-115">-InputObject</span></span>
<span data-ttu-id="cf94c-116">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cf94c-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="cf94c-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cf94c-117">-PassThru</span></span>
<span data-ttu-id="cf94c-118">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="cf94c-118">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cf94c-119">-Planlama</span><span class="sxs-lookup"><span data-stu-id="cf94c-119">-PlanAcquisitionId</span></span>
<span data-ttu-id="cf94c-120">Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="cf94c-120">The plan acquisition Identifier</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cf94c-121">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="cf94c-121">-SubscriptionId</span></span>
<span data-ttu-id="cf94c-122">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cf94c-122">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cf94c-123">-Targetsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="cf94c-123">-TargetSubscriptionId</span></span>
<span data-ttu-id="cf94c-124">Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cf94c-124">The target subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cf94c-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="cf94c-125">-Confirm</span></span>
<span data-ttu-id="cf94c-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cf94c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf94c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf94c-127">-WhatIf</span></span>
<span data-ttu-id="cf94c-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf94c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf94c-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cf94c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf94c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf94c-130">CommonParameters</span></span>
<span data-ttu-id="cf94c-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf94c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf94c-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cf94c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf94c-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf94c-133">INPUTS</span></span>

### <span data-ttu-id="cf94c-134">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. ısubscriptionsadminıdentity</span><span class="sxs-lookup"><span data-stu-id="cf94c-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="cf94c-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf94c-135">OUTPUTS</span></span>

### <span data-ttu-id="cf94c-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf94c-136">System.Boolean</span></span>

<span data-ttu-id="cf94c-137">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="cf94c-137">ALIASES</span></span>

### <span data-ttu-id="cf94c-138">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="cf94c-138">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="cf94c-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf94c-139">NOTES</span></span>

<span data-ttu-id="cf94c-140">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="cf94c-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cf94c-141">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cf94c-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cf94c-142">INPUTOBJECT <ISubscriptionsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="cf94c-142">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cf94c-143">`[DelegatedProvider <String>]`: Delegatedpprovider tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="cf94c-143">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="cf94c-144">`[DelegatedProviderSubscriptionId <String>]`: Temsilci sağlayıcı abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="cf94c-144">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="cf94c-145">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="cf94c-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cf94c-146">`[Location <String>]`: AzureStack konumu.</span><span class="sxs-lookup"><span data-stu-id="cf94c-146">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="cf94c-147">`[ManifestName <String>]`: Bildirim adı.</span><span class="sxs-lookup"><span data-stu-id="cf94c-147">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="cf94c-148">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="cf94c-148">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="cf94c-149">`[OfferDelegationName <String>]`: Teklif temsilcisinin adı.</span><span class="sxs-lookup"><span data-stu-id="cf94c-149">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="cf94c-150">`[OperationsStatusName <String>]`: İşlem durumu adı.</span><span class="sxs-lookup"><span data-stu-id="cf94c-150">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="cf94c-151">`[Plan <String>]`: Planın adı.</span><span class="sxs-lookup"><span data-stu-id="cf94c-151">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="cf94c-152">`[PlanAcquisitionId <String>]`: Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="cf94c-152">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="cf94c-153">`[Quota <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="cf94c-153">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="cf94c-154">`[ResourceGroupName <String>]`: Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="cf94c-154">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="cf94c-155">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cf94c-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cf94c-156">`[TargetSubscriptionId <String>]`: Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cf94c-156">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="cf94c-157">`[Tenant <String>]`: Dizin kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="cf94c-157">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="cf94c-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf94c-158">RELATED LINKS</span></span>

